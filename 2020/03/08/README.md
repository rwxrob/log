## Sunday, March 8, 2020, 8:15:29PM EDT [1583712929]

Alias -> Exported Function -> POSIX Shell Script -> Bash Shell Script ->
Compiled

## Sunday, March 8, 2020, 3:10:01PM EDT [1583694601]

Twitch wins again!. New friend on twitch just shared this ext-based
pastebin alternative <https://ix.io>. I am in fucking terminal heaven
over here. I simply cannot put a value on the number of amazing insights
I have had over the last month on Twitch.

I am so fucking blown away by how useful this is. You can create a
completely anonymous post from the command line by just sending a file
to the `ix` command after creating a simple `~/bin/ix` script like this:

```sh
#!/bin/sh argsorin "$*" | curl -F 'f:1=<-' ix.io
```

The `argsorin` is a useful script I made some time ago to intelligently
detect arguments and smoosh them together or read from stdin for here
doc syntax and stuff:

```sh
#!/bin/sh

argsorin () { buf="$*" if [ -n "$buf" ]; then echo -n "$buf" return fi
while IFS= read -r line; do buf=$buf$line done echo "$buf" }

echo $(argsorin $*)
```

Here's a simple example:


```
ix echo hello world http://ix.io/2dLp curl ix.io/2dLp echo hello
world
```

I usually write this stuff as functions so they can be cut and paste
easily if people want to just incorporate into their own code rather
than invoking a sub-process just for the command.

## Sunday, March 8, 2020, 2:40:42PM EDT [1583692842]

Need to take a look at <https://liveoverflow.com> which
[fox_maccloud](https://twitch.tv/fox_maccloud)  is recommending for
picking up memory buffer overflow vulns.

Also need to get a resources wiki-ish page ready to hold all these
references.

## Sunday, March 8, 2020, 1:18:05PM EDT [1583687885]

TIL you can add `-x` to `bash` to cause it to output the content of the
script as it is being executed. No more multiple `echo` statements.
Huzzah!

## Sunday, March 8, 2020, 1:13:46PM EDT [1583687626]

> Zsh, or Z shell, was first released by Paul Falstad back in 1990 *when
> he was still a student* at Princeton University.

See that continue to be a problem. People make things during college
that should never have existed and somehow people adopt them as
standards. The simple `vimtutor` (which is totally broken) is just one
such example.

## Sunday, March 8, 2020, 1:11:20PM EDT [1583687480]

There's something miraculous about purging the angst of hitting horrible
technology (that I cannot legally hack despite my initial impulse).
[Shameful Shitty Sites](/shameful-shitty-sites/) is one way to deal with
it. Who knows maybe it will pull up in an Internet search one day.

## Sunday, March 8, 2020, 12:12:02PM EDT [1583683922]

Still feeling the pain of that major burn setting up integration of Bash
command functions with applications that must call them from the
`exec()` system call (rendering them useless). I still feel they are far
more useful than aliases and should be used for anything that will be
called from the shell. In short, the best way to stay good is simply
think of them as shell extensions, period. Going too far and thinking of
them as commands will eventually trip you up (as it did me with TMUX
status).

The interesting question is then what language --- specifically which
shell version --- to write when creating actual command *scripts*. To me
the answer is pretty obvious: POSIX shell. These days the closet shell
to POSIX is `dash` without question. It is behind `/bin/sh` on all
Debian systems and is *wicked* fast. Since `dash` is already loaded into
memory (like `bash`) there is a good chance the interpreter loading time
is saved as well (which is *not* the case with Python or Perl).

So the moral of this sad tale is keep your functions as extensions of
your shell and write anything else as Dash scripts in `~/bin`. In doing
so we keep everyone happy because `/bin/sh` might be pretty much
anything on a given system and because your command scripts are all
POSIX there is never any fear of them not running on something.

Unfortunately this means that learning the shitty sub-process intensive
approaches are still required to maintain POSIX compliance. (Apparently
the world isn't ready for extreme efficiency like that.) If you *do*
want it, and don't particularly care about portability, just write it in
Bash and be happy, but not until you *need* a Bash-ism like good regular
expressions or avoiding a subproc monstrosity. After all POSIX was made
for a *completely* different world with different constraints. We don't
use many dynamically linked libraries now, for example. Everything seems
to be into static linking, and usually for good reason. POSIX isn't
dead, but it sure isn't required like it was anymore either.

As for me? Everything starts as a command function until I need it from
another program (`exec()` syscall). Then it gets ported to a `/bin/sh`
POSIX script. Then if I even have to make one subproc I change `/bin/sh`
to `/bin/bash` instead and live happily ever after. The end.

In most cases someone coming across `/bin/bash` who is using Ksh or Zsh
*should* just be able to change the name. But that's no longer my
problem.

## Sunday, March 8, 2020, 7:37:08AM EDT [1583667428]

While working on my TMUX status line and realizing that my exported bash
command functions were not usable using the `#(status)` syntax I did
some digging and found [this
information](https://stackoverflow.com/questions/35522187/how-to-export-a-function-from-tmux-conf).

This really had me challenging this new way of managing what I had
previously managed as a collection of stuff in `~/bin`. In fact, it has
caused me to seriously consider when to even use them.

Sometime in November I started to rewrite my Bash configuration scripts.
I noted the speed of exported command functions to be ridiculously
faster than invoking shell scripts instead. So being the freak I am when
it comes to efficiency I ported most of my utility commands into command
functions instead that are available to be run at any moment using the
`export -f myfunc` syntax, which is *not* available on anything else.

Not only are command functions much faster than actual command scripts,
they are far easier to maintain since they all go in some version of a
`bashrc` file which can be easily distributed.

I have just read all about "ShellShock" also ("Bashdoor") which happened
in 2014. I'm completely and totally blown away by the scope of that
vulnerability and how I have inadvertently fallen directly into a
horrible trap. I now have to help others avoid it and responsibly
describe how I have made a very understandable mistake to use command
functions *at all* (despite all the shit I say about zsh not supporting
them). There's actually a *very* good reason not to (or at least there
was). By adding on to the end of the exported environment variable
containing the command function hackers created the biggest shell
exploit in history. The fact that this bug went for so long without
being caught is unfathomable. Frankly it is a huge embarrassment for the
Bash team. Everything has been patched, but no wonder so many Linux
people have avoided them like the plague despite their utility. 

Does this means I will be converting to `zsh`? No way. But it does mean
that creating a `~/bin` directory (as I have done for more than two
decades) is *still* the best way to manage all your utilities.

The single best criterion as to whether something should be a Bash
command function or an actual command script is whether or not it will
every be used by anything but bash. So, for example, creating command
functions for stuff that is frequently paired with `!!` in vi is fine
since it always shells out to Bash, but any of those functions are to be
used from anything *but* Bash it might not be so useful.

This has me still horribly conflicted between the modularity and
convention of the `~/bin` approach versus the decidedly *only* Bash
approach of using command functions.


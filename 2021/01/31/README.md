## Sunday, January 31, 2021, 7:48:38PM EST <1612140518>

More I get into `kn` more I think that creating a Go version eventually
is going to be the way to go because I can include the `yq` code to
handle the YAML lookups without a dependency on the `yq` command itself.

## Sunday, January 31, 2021, 6:23:44PM EST <1612135424>

Decide to keep the `#!/usr/bin/perl` because it is standard on every
Linux and UNIX system for Perl. I could give a shit about Windows and
Mac paths that are someplace else. On Mac people just have to properly
`brew install gnu-core-utilities`. If people aren't willing to do that,
fuck 'em they can configure their own. I'm not willing to invoke another
wasteful indirections and subshell to lookup the local of `perl` every
fucking time a script runs that needs. In fact, it is absolutely stupid
to ever put `#!/usr/bin/env <anything>` into anything that is regularly
going to be run. Add the installer intelligence to do it right.

## Sunday, January 31, 2021, 6:17:10PM EST <1612135030>

All this Perl and automation is pulling me into cybersecurity again.
There are few industries where living on the terminal are as rewarding
and profitable.

Also, I realize now that Perl is coming back to me how much Bash felt
like pushing a rock up a steep hill even after I pretty much mastered
it. The stuff people hate about Perl makes it like butter to slice and
serve. So very calming. People will think that I'm crazy that coding and
reading Perl calms me down, but it just does. It's so fucking brilliant
for all the things that I most value: manipulating text.

## Sunday, January 31, 2021, 6:09:16PM EST <1612134556>

Intrigued if there is a chance of using PEGN to capture the `date -d`
grammar for modifying base date and time stamps. It would be relatively
easy to capture as a grammar and then generate. I'm thinking we need to
make that a priority for a helper Go package. The syntax is remarkable
flexible and powerful. It is sort of inline with efforts on the `dtime`
project that got me into PEG in the first place.

## Sunday, January 31, 2021, 6:07:24PM EST <1612134444>

Dance All Days (Wang Chung) just randomly played. All is well in the
world again.

## Sunday, January 31, 2021, 5:59:33PM EST <1612133973>

While reflecting on all this work with my family at dinner I realized
that perhaps the *biggest* interest group among knowledge workers across
the world is cybersecurity. No one makes use of a "black book" of
customized tweaks and notes than these types. I remember those who
trained me and the methods they had to manage all these little things in
a way they could recall later. And there is nothing better for this type
of need than command line interface to dump stdin and other script
output into. Combine that with drop-dead simple search ability, and then
even more, the ability to easily pass it over `keg` to others and you
have a tool that just doesn't exist that I would have *loved* to have
had when I started. After all, at the end of the day, this is all just
for me. If someone else benefits, that's even more amazing. But Imma do
it anyway just for my own needs.

## Sunday, January 31, 2021, 5:18:03PM EST <1612131483>

Another realization about doing this `kn` with a `kn.d` script directory
is that I can still leverage shell stuff like the very powerful `date
-d` arguments. The UNIX way really is the best way. Hell, I could have a
Python action as well if I wanted to do something that makes sense to do
in Python.

## Sunday, January 31, 2021, 4:08:13PM EST <1612127293>

Nice raid from [\@NahamSec](https://twitch.tv/NahamSec) who kindly forgave my lack of voice. 😄

## Sunday, January 31, 2021, 2:36:41PM EST <1612121801>

Oh my God, Perl tab completion is so much simpler than Bash:

```perl
if ($ENV{'COMP_LINE'}) {
  my $partial = $ARGV[1];
  my [\@actions](https://twitch.tv/actions) = map {s,^.*/,, and $_} glob "kn.d/*";
  map {/^$partial/ and say $_} [\@actions](https://twitch.tv/actions);
  exit 0;
}
```

I'm really kicking myself in the ass for ever leaving Perl for this kind
of stuff.

## Sunday, January 31, 2021, 1:59:01PM EST <1612119541>

Initial impression returning to perl is that it is actually far more
easy to comprehend --- and definitely safer --- than Bash. I've been
using `-T` and Bash has nothing like that. Plus there is no surprising
glob expansion, even though Bash `[[]]` is immune from those
vulnerabilities these days.

In other words, someone looking at the some complex use of associative
arrays or `coproc` or any number of new Bash features since 5.0 would be
equally just as confused and have to really spend time deciphering it
like they would require for the same code in Perl.

In other words, bubye Bash. For all these text-intensive shell scripts
Perl is rock solid.

It was nice exploring your possibilities, but ultimately you are no
where near as powerful --- or modern --- as Perl 5.30+ even if you are
both likely to be on any system I run across.

Perl has always been such a faithful companion. It's *never* let me
down. Not once.

When C was too heavy and Shell to insecure to handle the *entirety* of
backend processing for the entire fucking Web and the Common Gateway
Standard of the time:

Perl was there (even though it was never designed to be the Web's
savior).

When Java has a weird bug in the VM that prevented me from hitting Nike
store checkout system deadlines and no one believed me about it until
they flew in a guy from Sun to validate it who ended up concluding (and
I quote) "Huhn" when he saw it.

Perl was there.

When PHP dropped me on my ass with horrendous memory leaks and shitty
syntax requiring the fastest rewrite of the most lines of code I've ever
written on a deadline. 

Perl was there. 

When Python's startup time and absolute non-existent command-line
usability nagged me into leaving it for being so fucking butt ugly and
fat.

Perl was there.

When Ruby's speed and resource management continued to miss minimum
benchmarks.

Perl was there.

When the new Bash that has no knowledge of Unicode regular expressions
nor method of self-documenting scripts without incurring massive
performance penalties. 

Perl was there.

Here's the bald-face truth. The Perl developers are fucking rock stars
and always have been. They are more than 10x developers. And they
actually give a shit about a lot things the Python, Node, Ruby, and Rust
core teams could never even comprehend, let alone implement. (By the way,
it's no surprise that Go has been heavily influenced by Perl given
Plan9's inclusion and use of Perl extensive.)

It's good to be back. The rest of the world won't understand us. But we
don't have to care about them. We'll just get shit done faster than them
on every front and prove it. (Once I learn you again. I'm so, so sorry I
forgot you.)

## Sunday, January 31, 2021, 1:34:19PM EST <1612118059>

And another thing, Markdown was originally written in Perl.

## Sunday, January 31, 2021, 12:52:35PM EST <1612115555>

I'm actually a little excited to *re-learn* perl. It's absolutely crazy
that I wrote this extremely complicated, low-level
[`perlclasses`](https://github.com/rwxrob/perl-classes-pragma) pragma
and now I barely remember any of it. Looking through it is really
bringing it all back though. It's hard to believe I used to give
presentations on this stuff back in the day.

I am left wondering if, um, this will affect the focus of my imminent
job search. I'm starting to feel like SRE work is still deep in my
bones. I've always seemed to be able to straddle the fence of
development and operations. At this point the main priority is cleaning
up my GitHub repo and that involves porting a lot of this to Perl.
Nothing is significantly difficult.

Another advantage is how powerful having Perl back in my toolbox will be
when it comes to creating the cluster for automated bugbounty
monitoring, not to mention dealing quickly with stuff after getting in.
Perl has always been a preferred hacker language for that reason. Go
compliments it well because it is a single executable payload when the
time comes.

In fact, having a significant amount of Perl in my GitHub will actually
be a good filter for dumb ass potential employers who do not truly
understand when and where Perl is the unquestionable best pick. People
who dismiss Perl immediately out of hand and write shit like "a healthy
disdain for Perl" in their Job descriptions (including that completely
moronic company F-Security) can fuck right off. I don't give a shit. If
you don't understand it --- and especially if you make fun of it without
understanding it --- I want *nothing* to do with you. I'll fucking take
a janitorial job before I work for you.

And to all those people who call me "too emotional," well, you are the
first to understand me. If that makes you uncomfortable hiring or
working with me, you can fuck off as well.

## Sunday, January 31, 2021, 12:21:15PM EST <1612113675>

And, of course, Perl has its own license which is *not* GPLv3!!! Oh my
god, I love Bash, but that means I can keep my stuff free from that
shitty license.

Here's the greatest irony of all. This will make some people fucking
come unglued on my flip-flop. But I have always said the only reason to
learn Zsh was because it was not GPLv3 (which is why Mac uses it). The
simply fact is, that if I keep all my shell in Bourne/Dash/Ash (POSIX-y)
and all the other stuff in Perl that I've avoid GPLv3 completely. That's
something I simply cannot be ignored.

So here's what 2021's experiment will look like:

Language|Uses
|:-:|-
`sh`|Rudimentary Scripts (Bourne/POSIX/Dash/Ash)
`bash`|Interactive Shell (Only)
`perl`|Scripts Beyond Dash
`go`|Anything Compiled
`c`|Stuff That Requires It

And no fucking Python unless I'm writing automations or something, not
even for ML, there is plenty in Go for that now (that is actually
faster).

## Sunday, January 31, 2021, 12:04:50PM EST <1612112690>

I think I finally hit my limit with Bash. For the past year I've been
conducting a personal programming experiment. I decided to allow myself
to code Bash and use all the Bashisms I possibly could in an effort to
see if I could effectively replace Perl and Python with Bash and Go.

Well today I hit two *big* fucking blocks to productivity during this
experiment.

The first is support for `\p{Cc}` and other Unicode class regular
expression support. As usual, since Perl is literally the best language
on planet Earth for regular expressions --- having defined the modern
standard that is now included *in every other language* --- it is
naturally the first to invent and deploy support for full Unicode
classes. (Oh, and by the way, Perl supported Unicode *way* before Python
and didn't need a breaking change like Python3 to fix it.)

You simply cannot code in any other scripting language with that level
of regular expression and parsing support. Just think of `pack` all by
itself?!

Given the amount of language and knowledge manipulation that I do
regularly the primary criteria of the `kn` implementation language is
rock solid support for parsing and regular expressions. For that, Perl
is simply the best.

The second is small but oh so important: POD. I went to create an
efficient way to document my Actions for `kn` only to realize there is
simply no efficient way to do this in Bash. Go has it but they I have a
bunch of compilation steps for different target OSes, perhaps in the
long run, but not for throwing together stuff quickly. Perl POD comes
*after* the code (`__END__`) so the interpreter never gets bogged down
by parsing over it. This is a level of simple genius that most people
today just don't fucking appreciate. Python does *not* have this. It's
compiler is fucking brain dead, which is Guido is pushing so hard for a
new one in PEG. Again, Perl is king of *solid* script documentation.

I have to sit on this conclusion a bit, but these are *huge* discoveries
made in the fire of scientific personal research that I simply cannot
ignore. Perl is *literally* the best tool for *this* job, despite its
moronically uninformed unpopularity today. Given the amount of natural
language manipulation that I have been doing I have to consider the
possibility of prototyping `keg` and `kn` in Perl. 

I kind of like the prospect of building the next Internet Knowledge
Exchange Grid primarily on Perl to get started. Intelligent engineers
will make their considerations and discover why this is the right thing
to do.

## Sunday, January 31, 2021, 11:32:01AM EST <1612110721>

Struggling with the potential need for a convention for documenting
Actions. 

* Should I have the documentation be in a separate YAML file?
* Should embed it?
* Is YAML overkill?

People from the MAN page generation would say to keep is separate since
every execution of a Bash script is slowed by parsing the doc lines
unnecessarily (even though it is nanoseconds to do it).

This is where I *really* miss Perl where the convention was to put it in
the file after a certain point that the interpreter would always skip
and therefore didn't affect compilation. There's really no reason not to
use Perl for this actually, it's on everything by default as much as
Bash is. But people will really frown about it. Eventually Perl Actions
could be replaced with compiled Go code.

The thing about Perl is that it is absolutely the right pick to
prototype this stuff *mostly* because the `perl` executable is on
*everything* where a consistent version of Python is not. Besides,
Python start up times are fucking horrible and always have been. The
compiler is absolute shit.

But if I do this in Perl everyone will immediately write it off for all
the wrong fucking reasons. You know what *no* other scripting language has
right now? `\p{Cc}` Unicode notation. *Only* Perl supports that shit.
And yet assholes have the gall to suggest Perl is a "boomer" language.

I'm in a fucking bad mood as it is today, thinking about lesser
programmers throw shade at a language they know fucking nothing about
just pisses me off more. So Imma remind myself how to code in Perl
(after having set it down and coded nothing in it for over 15 years)
just to fucking piss them off.

## Sunday, January 31, 2021, 11:23:26AM EST <1612110206>

OMG I turned off the lights in my room and am coding like I used to all
the time and I cannot believe how much better it is than when I have
them on. Also my fucking fingernails are fucking with my typing. 

## Sunday, January 31, 2021, 11:15:41AM EST <1612109741>

I'm realizing that having the Action documentation for `kn` cannot be a
comment in a script if I'm going to keep the UNIX way of not caring what
languages the actions are written in. So it will have to be a command
that all of them support, probably `help`.

## Sunday, January 31, 2021, 10:44:41AM EST <1612107881>

Only chat streaming for me today. Last night knocked me out. Had to
cancel Beginner Boost. I need some recovery time. Ironic that coding
quietly is one of my best methods to do that.

And another thing, decided given the horrendously bad live chat API at
YouTube that I'll no longer be supporting live chat at all. There's
another *big* reason. After watching [this John Hammond
video](https://duck.com/lite?kd=-1&kp=-1&q=this+John+Hammond+SUDO+video) I
noticed something odd. He's chapters appeared on the side where live
chat normally would. Looks like when you incorporate live chat you give
up that ability. So I am just going to make sure that people know about
<https://chat.rwx.gg> and the options with Twitch and Discord. I know
that will be hard because it will still be two windows for some people,
but it is just not worth it to throw away chapter playlists and deal
with the stupid polling chat api for YouTube live chat. They won't be
able to keep that.

## Sunday, January 31, 2021, 1:06:42AM EST <1612073202>

I wish I could remember the name of the currency that is in control and
can just be printed more when the country controlling it wants to. It's
not "fiat."


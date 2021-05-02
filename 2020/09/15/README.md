## Tuesday, September 15, 2020, 5:45:55PM EDT <1600206355>

Once again I'm reminded of just how right I got the whole SkilStak thing
in the beginning by having a centralized multi-user server.

Today the main advantage I was reminded of was that beginners are not
required to learn *anything* but how to connect with `ssh` from their
computer --- no matter what operating system they have --- and then the
basics of bash shell navigation and `vi` editing. 

Most importantly it means no fucking around with Git and GitLab and
GitHub --- or even an email provider for that matter. Just pure terminal
mastery from day one.

I always shy away from mandating terminal skills for web development
only to return to the conclusion that they *are* required so might as
well learn them. Creating a web page and having it *immediately*
viewable without any extra steps is astoundingly effective for
engagement. This is what REPL.it and others claim but they bring a
shoddy web editor dependency that *always* fails. A minimal `ssh`
connection never does.

Backups are trivial to create of users' home directories.

SkilBots are easily deployed and maintained.

Login notices and ASCII art make it fun.

And Git and laptop Linux installation can always be added later. In
fact, I know feel it was a mistake to *start* beginners out with a Linux
laptop as a requirement. They certain learned a lot, but in the end they
have no memory of what they did to set up Linux on their workstations.
Until they care enough to want to do it over and over on old hardware
and the like --- and many may never achieve that level of interest
before leaving --- insisting *everyone* have a form of Linux installed
is simply too much overhead for what it provides *to beginners*.

I do wonder how I could leverage all of this for beginners who are not
in my private mentoring group, for example, those that I have helped
through beginner boosts. The best I can think of is to suggest they use
the PicoCTF stuff and make sure they work on levels while there. The
Carnegie Mellon admin team is top-notch and has a server supporting over
32,000 users.

The only down-side of suggesting PicoCTF server is the doxing of IP
numbers, but that would happen in any situation where a multi-user
system is involved.

The biggest difference this time around is that I refuse to create any
crutches --- including a `save` command of any kind. Anyone on the
system will have to learn `git` properly and all that goes with it.
Instead, I'll create SkilBots (eventually skilz.sh) to help them learn
it.

Another option also occurred to me for multi-user anonymity, I could
create a lightweight server with ssh tunnelling enabled so that the
machine with the users on it would never give up the IP of those
connecting. Hummm.

## Tuesday, September 15, 2020, 9:55:06AM EDT <1600178106>

It occurred to me while walking through a simulated parsing session in
order to check my PEGN for the AST JSON that it is perfectly possible to
create a tool that *visually* steps through the PEGN *and* the parsed
grammar in two windows showing the process of parsing for educational
and debugging purposes. It's not even that novel. Step-debugging is
already a thing for most languages but it impossible without at least
the possibility of creating an AST that can be traversed. 

There's just way to many cool things you can do once you have a solid
meta-language grammar. 

## Tuesday, September 15, 2020, 8:07:59AM EDT <1600171679>

Just discovered [magefiles](https://magefile.org/magefiles/), a Golang
makefiles alternative. Very intriguing. I'll have to get good with them.
I am particularly interested in seeing how they can be combined with
CI/CD to produce binaries (like `pegn`) automatically for all platforms.


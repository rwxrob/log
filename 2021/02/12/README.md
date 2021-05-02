## Friday, February 12, 2021, 8:55:19PM EST <1613181319>

After learning about the fiasco with the CapsLock key (which happened
way before the Apple foolishness with the ESC key) I've been sucked into
a vortex where I'm questioning every bit of reality I've observed over
the last several decades about knowledge workers, their tasks, skills,
and how to be both comfortable and productive.

Imma net out the facts:

* I haven't stepped foot in an office in over 22 years.
* I've always got my work done on hardware I owned.
* I've never used another's workstation for anything.
* Few times needed KVM in data center where very rare.
* Hyperterm (and ilk) are most common ways to "term" in to HW.
* COVID has permanently changed how we work in close quarters.

It seems like a perfect storm of things happened today. Nothing
particularly bad or troubling, my wife showed me a video about how COVID
has permanently changed office design and solidified the absolute
stupidity of open floor plans, concluding that working from home is the
perfect solution but that humans are 'social creatures' and will always
need to get together, but will *never* have access to one another's
keyboards and workstations ever again, which was always a bad idea ---
not just for the germs --- but the security of it all. In fact, *no one*
should *ever* use another person's computer for anything other than very
rudimentary web browsing. Key loggers are a very real thing.

I have regularly trotted out the example of a System Administrator (or
hacker) need quick access to whatever computer is available to them,
like you see in the movies, but the reality I'm faced to acknowledge is
that this is mostly fiction --- even when I trace every task I've ever
been assigned. Of all the work I've done I've probably only spent less
than 10 hours total working on a computer with a keyboard I could not
control or replace temporarily with my own.

This realization has huge implications for recommendations about the
primary tools of every knowledge worker:

### Pick What You Like

I love the Discord recruitment video that shows all the varied
keyboards. It really hits home this concept. The keyboard is the most
intimate tool a knowledge worker has. 

This means not only is learning Dvorak completely okay, but it could
even be preferred, which kinda sucks at this point because I *always*
wanted to learn it.

This also really changes several other core recommendations I have made
in the past

### Still Pick the Best Editor for Job

However, the same advice holds for Emacs v.s. Vi and Vim since even
though your keyboard and operating system will likely be your choice,
the systems you have to work on remotely probably won't be.

For example, `vi` is on everything as well as `nano`, not `emacs`.
That's just a plain fact. The movement toward individualism in the
workplace does not overrule the need to be productive on *any* system
you are asked to work with, it just means you will likely be remotely
connecting to it from your customized workstation.

In other words, if you are remotely logging into and editing files on
dozens of remote systems in a week might want `vi`, but not necessarily
depending on how you edit those files. Because you have the control of
how you connect and edit them. 

I've been reminded twice this week also that remotely logging into
systems to do *any* editing is not a thing people do in the Docker world
anymore. The workplace I grew up in with 30-100 systems assigned to me
required this ability (for which I created Virtual Server Administrator
to avoid it).

But while the System Administrator field and well as the term itself
are fading into history with the need to remotely edit files (which
would have required a change ticket anyway in most cases), the
cybersecurity field is ramping up with even more demand to be wicked
fast and undetectable on target systems of *any* type. 

One retro demand is to be able to edit remote files with at least one
editor that no one uses anymore. `ed` is the only editor
that will work after gaining a reverse proxy access since all you have
is a basic REPL, no terminal for even `vi` to use. Eventually, you can
upgrade your target system with a root kit, but being proficient right
away means using the best stuff that is already there. This is one of
the reasons people are pushing to remove `perl` from systems since it
provides so much power without loading any root kit at all.

### No Shaking Hands == No Touching Keyboards

Even if we completely and totally go back to "business as usual" with
cubicles and all, it will take a long time before people are okay with
basic handshaking, let alone letting even a close friend use their
keyboard on their workstation. It's a safe bet ain't no one touching
your keyboard but you, and that you are now motivated more than ever to
take your own keyboard with you on those rare times when you need to
work at someone else's workstation.

### Gamers' World

The gamers have taken over the world. Gamers fucking love their
keyboards. It is a part of their very body, the first thing you ever be
cyberneticly linked to them physically. Some live for the loudest noise
possible, while others (like me) would love to beat them to death with
that noisy thing. These preferences are only going to intensify and
become more and more mainstream, which means your human interface to the
computer now includes your keyboard. 

### Conclusions

**Still sticking with Vim.** While I'm still going to recommend and help
others learn Vim, I no longer think *any* Vimisms are off limits. 

**"Use what you want!"** That's my new mantra. I fucking tired of having
an opinion for anyone else on the best editor for what they need.
Problem is, most have no idea what they need.

**Control-C is still fucking stupid to use instead of ESC.** Because it
affects all your vim bindings even in things that having nothing to do
with Vim, like with `set -o vi`. Can you imagine what havok learning
Control-C has on someone doing that?

**Mapping CapsLock to ESC is brilliant and encouraged.** CapsLock needs
to die. No one uses it and it messes up beginners all the time in Vim.
Just map it for the workstation and be done with it. (Add this to `.bashrc`.)

```sh
setxkbmap -option ctrl:ctrl_modifier  # map capslock to control
```

**Learn Dvorak if you are young enough and special enough to not be
limited by anything but your keyboard layout.** I'm not.

In all I love the new level of autonomy everyone will likely gain from
all of this. But I'm also concerned some will think it applies to
everything and that customizing enterprise systems is okay without
approval. Only cybersecurity people with their own Arch rigs and shit
should be doing that, and they are already fucking with shit without
approval anyway --- and are thereby watched with that level of caution
to begin with. I imagine most will be just fine. But because I deal with
both my wires (and expectations) get crossed easily when talking about
it.

## Friday, February 12, 2021, 7:57:37PM EST <1613177857>

Having tremendous success helping beginners get started with terminal
web browsing using `w3m` which comes with drop-dead simple and intuitive
defaults. Eventually, some may decide to upgrade to a highly configured
Lynx session, but `w3m` is more than enough for most --- especially now
that I discovered that tab and shift-tab navigate the links (even though
that requires two hands and I prefer browsing entirely with one hand
while I drink coffee with my other, which can be configured in either
but is not the default).

Perhaps the most annoying thing about Lynx is all the cookie approvals
that are not accepted by default. That's enough to make any beginner
reach for w3m (and never leave it, for some). I don't begrudge that
decision by anyone.

My biggest gripe with `w3m` was always assuming too much about all the
table and image layouts that cluttered up reading the actual text, but
that has not been my experience with the defaults of late.

## Friday, February 12, 2021, 6:43:09PM EST <1613173389>

I've done it. I've deleted all my GitHub organization *except* PEGN and
AFKWorks. It feels wonderful I have all the stuff backed up here so I
can go through it as I need it without fear.

## Friday, February 12, 2021, 6:17:56PM EST <1613171876>

The more I think about how CapsLock has fucked up all our lives the
angrier I get at the morons who decided to change the default position
of ESC. The story infuriates me. How many times has CapsLock fucked up
entering a simple password for billions of people. And why? So a tiny
minority of people who actually have a need to type in all capital
letters can do their thing, shout.

In fact, the only assholes who use CapsLock these days are Trump
supporters, you know, the type of shithead you never want to communicate
with in the first place that thinks typing *anything* in all capital
letters is a good idea. The only *good* time is maybe to code Fortran or
write ENV VARIABLE names (but I just typed that without caps
lock).

There's something liberating and "FUCK YOU" about remapping Caps Lock on
my entire computer to ESC. In fact, I'm looking for keyboards that
enable the remapping permanently. My pinkies have never been happier and
every time I use it I'm quite sure some pig-headed, all-caps typing,
shit-fuck of a person feels a slight bit of pain for no rational reason.
(Hey, I can imagine it anyway.)

## Friday, February 12, 2021, 5:38:14PM EST <1613169494>

Blows me away that the installation instructions for `gh` have the user
use `curl -o` instead of `curl -O` to get the name from the URL. Just
goes to show there is a lot *everyone* has to learn and the learning
never stops.

## Friday, February 12, 2021, 5:12:05PM EST <1613167925>

After hearing that some people recommend using Control-C instead of ESC
for Vim I cannot believe how clueless otherwise really informed people
are. They have no idea that doing this not only encourages using
Control-C for mode changes in other contexts (which will usually
abruptly stop the program from working without saving anything) but they
also have no idea they are bypassing some of the most important Vim
events that Plugins use. But the worst thing of all is completely
destroying their ability to use `set -o vi` on their shell history.

Here's a recap of all the ways people deal with requirement for ESC in
Vi/m:

|::|::||
-|-
👍| CapsLock   | Original ESC position. Requires OS remapping. Universal.
👍| Alt-[hjkl] | Same as ESC Key. Easy to type. Supported everywhere.
👍| Control-[  | Same as ESC Key. Easy to type. Not supported in Europe.
👍| ESC Key    | Default but annoying and bad on pinkies.
👎| ff/jk/kj   | Requires remapping *every* Vim config. Vim specific.
👎| Control-C  | Builds really dangerous habits. Hack for Vi/m only.

I've come to conclude that remapping Caps Lock is objectively the best
solution. It has the added advantage of ensuring you never accidentally
hit it during a Vi/m session and *really* mess yourself up (you know you
have done it at least once, admit it).

Here's some [facts about why Caps Lock became king](https://simplyian.com/2015/01/08/The-real-reason-why-Caps-Lock-and-Escape-are-in-terrible-positions/).

Fuck you, Caps Lock. You always sucked anyway. Bubye. Take your useless
ass off of my keyboard. You are my ESC
once more. 

## Friday, February 12, 2021, 4:41:07PM EST <1613166067>

I cannot say how grateful I am for the `gh` command line tool provided
by GitHub. I would abandon GitLab just because of it.

After being notified that SkilStak no longer qualifies for "educational"
status (according to the new Microsoft owned GitHub) --- and ignoring
their suggestion I pay \$32/month just for the privilege of having what
I have kept for *over seven fucking years* I now have all my repos
locally with the following command:

```sh
for i in $(gh repos skilstak); do gh repo clone $i; done
```

This command cloned down all 144 repos from `skilstak` in under 20
minutes allowing me to sleep better knowing they won't suddenly
disappear because MS suddenly changed their mind about what
"educational" actually means (spoiler alert: it's only those paying into
the bullshit status quo system).

God, I cannot *wait* to be rid of both GitHub and GitLab dependencies.
Even though it is slightly more work and will result in some minor
personal monthly costs, I'm setting up *everything* on Gitea instances
for each domain (and will mirror the content to GitHub for visibility).
I'm so fucking done with bait-n-switch bullshit and the people who are
destroyed because of their whims. It's free, so it's hard to complain,
but the great lie they don't tell you is that you never really mattered
at all.


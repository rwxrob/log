## Monday, February 15, 2021, 8:09:44PM EST <1613437784>

Now that hosting my Git repos on my own domain seems more doable (and
palatable) than ever I'm drawn to rethink my domains again:

Domain|Description
|:-:|:-:|
skilstak.io|Keep as the mentoring portal.
skilstak.sh|Keep as the mentoring (TMUX) server.
skilz.dev|Instructional KEG node.
rwx.gg|Source and all things in need of cool short-domain.

## Monday, February 15, 2021, 5:33:51PM EST <1613428431>

How do you know you should never use a package because the author does
not give a shit enough about it to set a tagged version:

```
go: downloading github.com/nsf/termbox-go v0.0.0-20190121233118-02980233997d
```

When you get that in your output from `go get` anything.

## Monday, February 15, 2021, 5:13:59PM EST <1613427239>

It's not always possible, but when it is using IRC and chat for
text-based mentoring is so much more effective for certain things ---
mostly because there is something written that the person can go back
and read again if they didn't understand. Verbal instruction has to be
repeated a few times and then never has a written record unless it is
referring to something that was also written.

This phenomena is also why just-in-time curriculum and content
development is so effective because it literally captures the chat of
the session and puts it into a form that can be polished up and built
upon later for others to use as well. 

All things lead to `keg`.

## Monday, February 15, 2021, 4:36:00PM EST <1613424960>

So far so good with "monitored mentoring" while still live. I have
Discord open with a brother and sister working on their code and can
still report. Only problem is while on the same computer I have to mute
the whole thing. I'll fix that tonight with a secondary system just for
the mentoring. That will allow full simultaneous streaming with
mentoring breaks as well as eventually live mentoring for those who want
it. A few are really excited to be the guinea pigs with that. Both of
them have their own Twitch gaming streams already.

I'm feeling a bit torn about the mentoring of people who just want to
create games and that's all. I'm okay helping them out, but it is
completely against the momentum of everything else I'm doing. It's more
difficult because I have some that I mentor *in* hacking who, if I had
more of them, would be, um, better uses of my limited mentoring time.

I already feel like the writing is on the wall already. Unless it is at
least indirectly related to hacking it is likely it will fade out of my
mentoring and curriculum. It feels like the right thing to do given the
massive amount of learning people have to do to enter that industry
with a solid terminal mastery foundation (as opposed to the "I know
Burp Suite" crowd).

## Monday, February 15, 2021, 3:23:14PM EST <1613420594>

I am absolutely disgusted with how much I let myself buy into the Google
ecosystem. Been going through my stuff in my drive and blows me away how
fucking stupid I was. Nothing *really* insecure, just the documents and
stuff. 

Honestly, I about forgot about all that stuff because I have used
anything (but YouTube) that has anything to do with Google in over a
year. Working with my iPad I remembered it is synced to the cloud there,
because, ya know, mobile doesn't trust us with our own fucking data, we
have to have an "authorized" cloud provider to even use these devices. 

Seriously how the fuck did the entire world buy into this absolute shit? 

Apple polishes shit up rather nicely, that's how. I'm staring at one
beautiful piece of shit right now that I use for music.

I've never been more motivated to get off of all of it.

## Monday, February 15, 2021, 2:43:22PM EST <1613418202>

Seems rather ironic that at about this same time on this same day last
year I was touting the value of exportable functions in Bash. They are
definitely amazing and essential for *real* terminal mastery because
they can do things that no script (or alias) will ever be able to do.
But the lack of them being callable from a subshell (that isn't already
a Bash shell) is enough to tank their share-ability (if that is even a
word) with others. And these days I'm all about the sharing code.

## Monday, February 15, 2021, 2:27:31PM EST <1613417251>

Porting the `weather` alias to a script I noticed that Chubin's stuff is
really assuming you have a huge screen. Which leaves room to add stuff
of my own that is based on a much smaller screen default. Looks like I
*will* be renewing `know.sh` after all.

## Monday, February 15, 2021, 1:06:19PM EST <1613412379>

I've found that there is another disadvantage of using shell aliases for
anything. They are not available to subshells including Vim magic shell
integration. Yet another reason for really small shell scripts and/or
export Bash functions.

## Monday, February 15, 2021, 12:55:41PM EST <1613411741>

Fighting the temptation to jump right into JSON-schema when creating new
KEG node types. There are tools for that but they all suck and require a
graphic browser. Just a table for now.

## Monday, February 15, 2021, 12:50:22PM EST <1613411422>

All this is consistent with my desire to do something more Easter-egg-y
with skilstak.io and skilz.dev. Once again, a way to take on Try Hack Me
(which I fucking despise) and come up with an open competitor that is
supported by the community instead of some fucking fat-cat corporation
getting people to lie about their sponsorships as part of their
contractual obligation, while wearing a fucking Try Hack Me tee-shirt on
a Twitch live stream and never using anything else. Just the absolutely
shitty Linux "lessons" are worth the attack. Imma destroy Try Hack Me,
one day.

## Monday, February 15, 2021, 12:34:01PM EST <1613410441>

After deciding to do nothing but muted "CozyCoding" during the work day
I have realized several advantages from it:

* Zero preparation for the stream
* No regrets taking breaks
* I don't have to look good
* I'm not blinded by lights (can work in cave)
* I get shit done (even more because stream editors)
* Soothing ASMR audio with no music preference
* Only intelligent people are attracted to it
* It remains relatively suitable for work (audible, at least)

It turns out to be the kind of thing I would love to put on a screen
next to me and watch while I was working in another screen. Maybe I can
find others who are doing the same. It's even better if they use IRC
because I could pop over to chat in their stream anytime.

## Monday, February 15, 2021, 12:27:59PM EST <1613410079>

Just heard from @green_jenny about "orange hat hacking" and 
[Edward De Bono's Six Hacking
Hats](https://duck.com/lite?kd=-1&kp=-1&q=Edward+De+Bono's+Six+Hacking+Hats).

## Monday, February 15, 2021, 12:12:02PM EST <1613409122>

If you are a pedantic tech connoisseur who becomes an asshole when
dealing with shit you can channel that anger in positive ways that make
you less of an asshole, all of these focus your rage on *destroying*
that shit in positive ways:

1. Create better tech --- perhaps even open source it --- and then sell
   support services and give conferences on why yours is better and your
   competitor is absolute shit.

2. Directly attack the tech through pentesting and publicly shaming the
   shit out of it. After you are done with it no one will want to use it
   and they will know exactly *why* because you will have fucking proven
   it.

But you can actually do both at the same time. That's my intent. Keep my
coding skills senior while layering on additional redteam skills. I get
the sense that redteam is all about coding to own. (I'll have to keep
that phrase in my mind, "code to pwn").

I recently saw a Chuck episode where Casey meets his traitorous sensei
who gave him shit all his life for not finding "his calm center." I can
really relate. Chuck saves the day by *really* pissing off Casey at the
right time and he kicks his sensei's ass concluding, "I realized Casey
doesn't have a 'calm center', he has an angry center."

Sith Lord I am not. I believe in Yoga. I really do. I believe in being
positive. But it's the ongoing rage that never leaves me. Our world is
filled with so much shit I just makes me crazy with anger sometimes.

People have told me it will affect my job opportunities. Perhaps. But
there are jobs were directing that anger and passion into something good
can make a difference. God wouldn't have given us anger if it didn't
have a purpose. I understand that now. Call it righteous fucking
indignation if you want. I don't give a fuck.

I don't know where it comes from, probably from being fucked in the ass
by Mormons for 40 years. But maybe not. It certainly is not directed
toward any *person*. I actually love people. I really do. It is seeing
them be fucked over constantly that makes me literally shake sometimes.
But I can channel all that for good and keep the collateral damage to a
minimum. I know I can. And I will.

Luckily the careers where having tattoos (I don't), swearing, and being
an angry asshole are almost entirely in the cybersecurity trade.

OSCP here I come, again.

## Monday, February 15, 2021, 10:31:55AM EST <1613403115>

My new life goal is to fucking own a CTF using nothing but perl and curl
and show all these arrogant python scrids (most of whom can barely code
at all) what is absolutely impossible with truly contextual programming
that only perl brings to the table. No one will believe me until the
announcers covering it don't have a fucking clue what I'm doing. That
will be my revenge. Shit heads to bag on perl and use python for
cybersecurity have no *fucking* clue what they are talking about. Python
won *in the enterprise* because it forces readable code that take a long
time to write but is still horrible because of whitespace.

Here's the thing. I can *do* Python. Python is good for stuff that has
to be communicated in a report or some boring machine learning shit or
some kindergarten coding class. But it is absolutely *not* the best tool
for the job when the job is fastest hacking and payload creation
possible. Perl has always dominated at that and always will. The black
hats who never come up for air know this, but they don't make fucking
Twitch channels about it. Most of these scrids bagging on Perl on Twitch
(which is laughable all by itself) don't even know what IRC is.

I don't know what I even bother writing any of this. They won't believe
it until they see it. So imma show them, eventually. Gotta retrain my
perl contextual coding skills before I can really give a good
demonstration. 

1990s Rob is pissed as Hell at 2020s Rob right now. "I
fucking *told you* never to let your Perl skills get soft!"

## Monday, February 15, 2021, 9:50:57AM EST <1613400657>

Had a great conversation with my wife over coffee. She's laughing her
ass off because she absolutely has always known that hacking is in my
DNA, even my language skills and asshole-ness play into it. Being a
pedantic, "water-boiling" asshole is part of the job description, as is
being able to back it up. The more you can show a corporation how badly
they suck --- and communicate that effectively --- the more you prosper.

I was born to hack.

## Monday, February 15, 2021, 9:07:27AM EST <1613398047>

You know, I'm a hacker. I always have been. I don't know why I don't
just embrace that as a career. Thinking about what I was watching
on EsportsHacking and I was almost yelling at the screen about all the
better ways to do what everyone was doing.

I have the core skills and
the experience, I just fucking hate working with shitty tech, even to
own it. For example, I'd have to (re)learn PHP all over again.

Today I'm really feeling the pull of what I'm naturally good at. Sure
I can do all the other stuff. Sure I can be a software engineer, or an
SRE, or a DevOps dude. But when I think about NahamSec and other
CTFers success I'm reminded that the coding that makes these hackers
successful is *exactly* the coding I'm really good at and drawn
too, quick, dirty, effective, and powerful, which is why I *still* love
Perl so much. It blows the fuck out of Python for everything in
pentesting *except* the shit that scriddies use. 

Go could replace Burp suite with something so much better. Hell, I could
sell that shit after releasing as open source.

When asked about "note taking" --- something that comes up all the time
during conversations between hackers --- the methods they use are arcane
and silly compared to `kn`. They don't even know it exists. No wonder
NahamSec dropped by during my knowledge management streams. Dude knows
what's up, which is how he manages to *pay* \$7k/month just to keep his
k8s rig up at home doing all the scanning. Hell, that's easier than
setting up a Bitcoin mining operation for someone with a lot of coding
experience.

I'm realizing that one of the core differences I have from *most*
hackers is simply the ability to code good software. Most hardly know
how to code, and when they can, well, they look like kindergarteners to
*actual* software developers. I have the unique experience of doing both
systems operations and systems engineering and software development. I
just have to fucking use them both, and frankly, not even the modern
idea of "admins who code" (SREs) touches what is possible for a someone
with such skills in the redteam world. 

Why the fuck am I not going for this? Is it just my pristine arrogance
not to be exposed to shitty software? Probably. But let's face it.
Accepting a corporate gig of *any* kind means seeing that shit
*everywhere* so might as well take advantage of it and fucking own it
for greatest satisfaction rather than trying to sustain it until it
blows up in our fucking faces and everyone points the finger at me. Imma
be the blowing up that shit, not taking the fall.

All of this has caused me to really rethink my long term goals. After
all, if was hackers who created all the cool stuff we use every day on
the Internet. And it will be hackers who save the world from the
Idiocracy taking control of it right now. 

Kubernetes and such are still a core part of the entire thing. They all
overlap. So learning that shit ain't taking a back seat at all, right
after I redo the Web, I mean, finish the first iteration of KEG.

I really just want to be Gilfoyle. Is that asking too much?

## Monday, February 15, 2021, 8:59:55AM EST <1613397595>

Tough getting my Perl chops back after working in Bash for so long. Bash
is decidedly lame at doing things quickly and tersely, the very thing
Perl gets a bad rap for is the thing that makes it dominate so
completely as a shell scripting language. Again, why the fuck did I ever
leave it?

## Monday, February 15, 2021, 8:44:55AM EST <1613396695>

I'm wondering if I have been too harsh on the simple `#!/usr/bin/env
perl` in the past. I've always hated how insecure and unnecessarily slow
it is, but it is damn convenient and great for writing scripts that can
easily and quickly be executed and shared.

I suppose my biggest complaint is that people (once again) take a simple
convenience and deploy it into production without doing the minimal
effort to correct the shebang line in their installers. This is why I
hate it more than anything. I'm afraid that if I start doing it on
stream people will think they can (and should) do that in production.

After all, scripts should only be for hacking CTFs and utilities that
don't really matter. Everything else should be in a more substantial
language. And the `env` trick is in-line with the goals of that usage.
So I'm going to start using it again with that in mind. I can't prevent
people from doing stupid things either because they don't know better or
willingly choose to deploy that shit into production. Why should my
effectiveness and ability to share be affected by other people's
ignorance and/or carelessness?


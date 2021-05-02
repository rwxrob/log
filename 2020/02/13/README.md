## Thursday, February 13, 2020, 5:54:09PM EST [1581634449]

So Hexchat is definitely the IRC I'll be suggesting everyone learn
seeking their [PTP](https://skilstak.io/ptp) from me. It comes by
default on Mint and is the standard way to get help from the community
for anything related to Mint or Linux in general. As sexy as I
personally fine WeeChat and IRSSI to be they are simply not as
empowering. In fact, the only power they give you is to use an IRC
bouncer and participate in chats completely anonymously. There are
enough ways to do that using VPNs and Tor that allow the use of HexChat
that the GUI benefits of seeing when another channel has new information
strongly outweigh the benefits of being terminal only.

There, see, I'm not a terminal bigot. Right tool for the job. Being able
to set HexChat to always be on top and visually get all the data I need
so quickly would be really hard to match without a *lot* of WeeChat
customization. And even though WeeChat supports mouse interaction at
that point you have to seriously ask yourself why you aren't just using
HexChat in the first place.

So I guess I need to review my list of stuff from the PTP chart.

## Thursday, February 13, 2020, 5:29:58PM EST [1581632998]

I inadvertently turned on the JavaScript console while browsing just to
push over the rendered screen a bit (while streaming) and noticed Medium
sends messages to the console specifically for developers with a nice
bit of ASCII art. You know the obvious conclusion here, I will always
browse everything with my JavaScript console open from now on. Seems I
wasn't the first to hide Easter eggs there, and of course I wouldn't be.
It's a natural way for geeks to connect at a basic level.

## Thursday, February 13, 2020, 5:00:30PM EST [1581631230]

After jumping through all kinds of hoops for a GitHub action to pull
down and configure a full Python 3.7 instance just to run Vint, just to
lint the vimscript for the `vim-pandoc-syntax` plugin I'm *really*
triggered about how completely wasteful having a full action setup for
something as trivially simple as linting is. 

In fact, the entire value proposition of such a thing can only be
realized on projects where the different number of contributors is very
high and their experience varied. 

Call me old-fashioned, but what is the difference between an "Action"
and just running the damn linter from the command line before you even
save the fucking thing? 

I think I know the answer: to enable continuous testing and not have to
setup the testing every time. After all that the central promise from
the whole CI/CD thing. But I can't help thinking that like everything
DevOps these days, people are being stupid because they aren't
challenging the approach on *every* project and just doing it because
that is what everyone does --- or worse --- that is what will get them a
job or a new account.

The catastrophe that has become the massive cluster fuck of
micro-services today --- culminating in "mesh solutions" and the
(re)invention of (g)RPC --- is the natural result of all of this.
Sometimes I swear people forget to use their brains instead they read
the latest Gartner Group report or use whatever has the most GitHub
stars.

We talked about Deno and Ryan Dahl today and all of this is *exactly*
why I love that guy so much. He sees things practically and constantly
challenges everything including his own massively popular creations. We
need more of that, we need more Ryan Dahls.

## Thursday, February 13, 2020, 9:15:34AM EST [1581603334]

More conclusions:

### It's okay to have kids use VSCode.

Those who prefer it can still use it, but I'm going to make another very
clear map of what they *cannot* do until they learn `vim`.

### Need a fun three with fruit on it.

This way they can see what they get when they climb out onto a
particular branch. 

### Need to find or write some good mind mapping software.

So far I cannot find anything that has a decent outline conversion.
Inspiration was *so* good but they shut their doors in November 2019.
That was a pretty good run for them. I used them in 1996 a lot for all
my college work.

### GPLv3 all the things.

After reading a lot more about
[Tivoization](http://www.linfo.org/tivoization.html) I'm finding myself
siding pretty strongly with the FSF, which is a bit odd for me. In fact,
GPLv3 is the *only* thing that even attempts to take on the fight
against the movement toward devices just being extensions of services
that we don't actually own. If a company chooses to be that shitty I
want them to at least suffer from not having access to all the great
code that I (and the rest of free software developers) are making. 

They can put shitty Zsh substituted to avoid giving back their
improvements (as Apple did) but they will always suck for doing so. 

I have *no* problem with someone burning an encryption key onto a board
and making their device not work if someone tampers with it, so long as
they *provide the key to the end user* so they can do what they want
with it. Not only is that appropriate, it is the only fair solution and
covers *every* FUD inflammatory case (medical equipment, satellites, air
traffic control). 

In fact, the government is actually likely to *want* Tivoization in
order to assert dictatorial governance of the market and ensure they can
active and spy on citizens however they deem fit. This is just not okay
in *any* country. 

So Stallman (you controversial, industry-changing fuck) I'm with you on
this one. Linus can go fuck himself. Torvalds has always been completely
clueless when it comes to the *real* legal matters at hand. (Probably
had several governments and companies approach him.) 

I seriously doubt Torvalds has even read one court case brought which
the FSF has been constantly involved with to determine their course of
action. But that asshole has the gall to through shit and FUD at the FSF
suggesting they lied about what was in the license to entice people to
use it, instead of creating a new license. No wonder not a *single*
person in the audience raised their hand when he asked. No, Linus is
just old and clueless, brilliant, but clueless. 

Yes I think a new license would have been better, but there were so many
changes and clarifications to GPLv2 that it was the natural best place
to add the Tivoization clause as well. There was no sneaking around. 

In fact, after having been slightly on Torvalds side and then fully
reading the full arguments from the legal FSF team I think Linux is not
only uninformed, but, to use his words, "a fucking moron" on this topic
as are more of the "open source" people who just want to MIT license all
the things. I keep finding that people who *truly* dig into the issues
almost always land on the side of the FSF, but hardly none of the
developers I run across have even read *any* of the licenses involved
let alone understand them. This is how Facebook got away with their
React shit.


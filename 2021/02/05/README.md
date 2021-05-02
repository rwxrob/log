## Friday, February 5, 2021, 7:41:29PM EST <1612572089>

I've decided to go all in on one specific beginner to technologist path
with only minimal focus on web design at all. This means I will be
allowing those I mentor now who are only interested in creating games
and web development to just atrophy out and replace them with those on
my waiting list who are specifically interested in the main path I
offer.

This is a big departure from before where I had multiple paths, one
leading to front-end kinds of things and another leading to operations
kinds of things.

I'll be putting all of this organization into the Beginner Boosts.

## Friday, February 5, 2021, 5:21:00PM EST <1612563660>

Looks like the best balance of full-time job, mentoring, and live
streaming will be doing dedicated live streaming for about an hour at a
regular time in the morning (before the official work day) and on the
weekends for Beginner Boosts. I'm also going to start *during* the
mentoring sessions, just muted and from another computer.

I plan to never stream anything for work that isn't generic work for a
specific task that would easily pass any standard of ethics. I have no
problem surpassing such ethical requirements, besides all that work will
likely be on another computer entirely. 

This has caused me to realize that there are actually several types of
mentoring with different demands on my attention to ethically fulfill
the need for my paid services:

Cost|Public|Type
|:-:|:-:|:-:
1120|No|Paired
900|Yes|Paired
900|No|Monitored
720|Yes|Monitored
320|Yes|Directed

Here's a description of the types:

Type|Description
|:-:|-
Paired|100% dedicated attention and sharing a keyboard to work on challenges and planned projects simultaneously.
Monitored|Challenge-based instruction with corrections, interjections, and tips during session (while mentor works on other things as well).
Directed|Session strictly follows the Beginner Boost path and serves as recorded example of a person going through the sessions. Limited availability. Internet identity fully disclosed.

Having a dedicated computer for mentoring that pipes into my same
speakers is probably best. That way that screen is dedicated to the
person in the session and never at risk of being shared on the live
stream without complicated what I'm doing. 

The only time I ever need to share a keyboard is with TMUX on
skilstak.sh and that stuff is always something that can be shared over
the live stream as well, just muted because I'll be talking to the
person involved. Everyone in the live stream will see the person working
over TMUX and my assistant, but no one will know who the person is nor
hear anything we say to one another. People who aren't comfortable with
that can opt out for more money.

In fact, I can make an OBS setup or plugin that displays what is
happening on the screen so people are not confused.

One of the benefits of doing live mentoring is that the live stream
benefits as well, just in a different way. 

A positive side effects of doing paid live stream mentoring is that is
reduces the cost for those willing to make public anonymous mistakes
while motivating others to move into the mentoring realm. For those who
might be uncomfortable with the amount of muted stuff I'm doing they can
sign up and become a member.

## Friday, February 5, 2021, 10:23:30AM EST <1612538610>

It seems like putting a natural language layer that processes a raw
command-line into a generic, traditional function call with parameters
is the best approach and meets the needs to be able to create simple
actions without the extra thought as to how those actions will be
determined and called by the smart layer.

It also occurred to me that this separation applies to the work to
create an application. You have the person or team developing the
actions independently and without thought for how they will be
ultimately invoked from the command line. And you also have a person or
team dedicated to creating the language grammar that translates every
possible command line permutation into those actions. This has immediate
implications for creating fully functional interfaces in *any* foreign
language.

## Friday, February 5, 2021, 9:40:49AM EST <1612536049>

I am curious to know how long something remains in the Go caching
servers before (and if) it ages out.

TIL that `go mod vendor` and `go build -mod=vendor` will pull any
imported dependencies into the vendor folder so that they are
permanently a part of the source code rather than pulled even with the
saved checksums associated with stuff in `go.mod`.

## Friday, February 5, 2021, 8:10:57AM EST <1612530657>

Realized I cannot use case to distinguish context if I want an interface
that ultimately can be compatible with conversational UIs.


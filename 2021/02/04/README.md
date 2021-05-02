## Thursday, February 4, 2021, 6:34:58AM EST <1612438498>



## Thursday, February 4, 2021, 9:00:50PM EST <1612490450>

I'm absolutely losing my cool by how completely frustrating it is
watching our state of affairs right now. I just watched a dude on Twitch
fly around his expensive lab with gadgets everywhere with 1000s of
viewers and a very sustainable following. Then another guy, with
something like 80k subs on YouTube does his first Twitch stream and
decides he wants to do cybersecurity, 'cuz that sounds interesting. He
launches into Linux on TryHackMe, an absolutely horrible resource, and
when I suggest it is not the best first resource and that he try the one
from the Linux Foundation he takes that will a bit of trepidation.

It's a fucking up-hill, ongoing battle to counter all the bad
information out there. People will make their own decisions and I *want*
them to learn for themselves and be critical thinkers, but they don't
even know what fucking IRC is, or why TryHackMe is absolute shit and
when I point these things out I just come off as an asshole.

I take solace in the fact that there *are* clued in people like Nahamsec
who not only has been supportive and been fun to get to know in the
community, but chose to raid on Twitch a few times. I have to focus on
people like him to remind myself that it's not a systemic or generation
thing, it's a free will and apathy thing. There *are* fucking amazing
people out there, that would travel hours to have a beer with given the
chance, they are just a lot harder to find.

## Thursday, February 4, 2021, 7:17:19PM EST <1612484239>

Bumped up date time with timezone on screen to `brightwhite` in TMUX
config and realized the color format with words matches the color scheme
so that it perfectly matches whatever the terminal theme colors are,
another reason to stick with the Solarized approach rather than setting
specific values that don't play well with a particular theme change.

Going with the brighter white makes sense now that I leave
`[irc/freenode]` on the screen so it is immediately obvious what is
happening. It has helped save a lot of confusion, that and making sure
to but [chat.rwx.gg] into every title (which makes me glad to have a short
domain).

## Thursday, February 4, 2021, 6:18:54PM EST <1612480734>

Yeah, it's possible other people are lurking on my live streams
and picking up new idea for their more mainstream YouTube stuff. It's
flattering if it's happening.

As long as the momentum to replace the Web is moving on several levels
when people see what KEG can do they'll come around. None of the
alternatives --- including Gemini and Tim's --- have anything like the
semantic combination of Pandoc Markdown, YAML and JSON that I've been
working since [2014](https://github.com/essentials-web) and it now in
[KEG](https://github.com/afkworks). 

There isn't a moment to lose on this stuff. All of these fail to realize
that none of this has to do with the Web at all really, it is about
creating a *solution* to the unmet needs of millions of knowledge
workers, a need that manifests itself in both the bloated Web of today
and the search engines for it. No solution I have encountered so far
addresses this core need other than KEG.

The really great part is that I know what I have and I don't *really*
need to know that everyone else knows it. I can do my own thing and
astute, intelligent people will naturally gravitate to it because it is
simply superior, just like they did with Linux and Git. I just need to
demonstrate and document that superiority in plain working terms that
show people addressing the need and saying inside, "I want that!"

## Thursday, February 4, 2021, 2:54:52PM EST <1612468492>

Just had a major breakthrough that was the combination of many other
ideas over the last few years:

* Conversational UI Responders
* `cmdtab` Contextual Tab Completion
* `kn` Actions (Reserved, Builtin, Extensions)
* Common Gateway Interface
* `net/http` in Go

In short, I'll be creating what I am going to call the MimTab™ command
line interface.

The concept is simple: treat the entire command line as if it is a query
to be handled by one or more registered Handlers keyed to specific PEGN
or Regular Expression matches every time the user taps tab, essentially
turning every command line into a localized intelligent search fulfilled
by a single command line application (which can optional support other
commands as extensions).

This approach obliterates the ancient, dead, broken idea of a command
line with options and hashes and specific usage and ushers in further
the era of conversational user interfaces that anyone can use, not just
"terminal masters."

The obvious next step to all of this is to create Mim™ Shell (a
variation of a REPL) which is composed entirely of handlers and adds the
concept of temporary cache between command lines allowing the scripting
of 100% natural language.

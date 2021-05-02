## Wednesday, September 30, 2020, 8:56:29PM EDT <1601513789>

Just dropped in on a "learn to code rust" stream and the dude said,
"Just a little thing to keep your code that much cleaner" regarding the
dropping of semicolon and no `require` in functions. I laughed my ass
off but refrained from any comment. That is perhaps the single biggest
dumb-ass design decision made by the language's creators. The entire
language is a testament to kitchen-sink design. It's syntax is fucking
abysmal even if Rust has other redeeming qualities. Learning Rust *will*
make *everyone* a better programmer, but the level of pain just
swallowing that butt-ugly syntax all day is simply unbearable for me and
most who value minimalism and clarity.

## Wednesday, September 30, 2020, 7:42:05PM EDT <1601509325>

I'm at a crossroads with PEGN where I have to decide whether to support
binary packing or not. By allowing `Rune` types that are hex and octal
and even binary I've allowed for tokens that are purely binary data at
the lower level even resulting in the combining of different fields of
different types and lengths (sometimes called packing). As cool as that
is, it creates some unexpected difficulties when generating code to
represent those tokens and to parse and validate them. The bright side
is that when this is working it will be one of the easiest ways to deal
with packing and unpacking that I've encountered.

One *significant* requirement will be to change the parser to not depend
on `unicode.DecodeRune()` any further. Without knowing it at the time
I've hard-coded a fundamental bug that prevents all unpacking. 

But it gets more complicated than that. I can't even use the same rune
scanner technique at all. It fundamentally prevents parsing of single
bytes and bits. No matter what I'll have to stick with scanning single
bytes because you just can't get lower than that on the hardware, but
the parser will have to be able to inspect those bytes in different ways
consistent with the specified node parsers. The very design of nodes
depends on string values for terminals so `\x` would be required in the
current situation. 

What if we added numeric values as well? What if we added logic that
inferred something was out of the standard range for representation as a
string and simply turned it into a base 10 integer. The parser and code
generators would have a much easier time of it because they could switch
on type and just return a number that can be represented however. That
would allow node parsers to unpack sub-byte bits even.

This is a huge issue that I need to fully resolve before continuing.
I've already hit it by adding `ENDOFDATA` that is an `int32`/`rune` even
though it is way out of range for UNICODE code points. 

99% of users will stick with UNICODE, but it will be catering to those
users who always want to use PEGN to clearly represent complicated bit
fields that has the best chance of pushing PEGN into universal adoption.

## Wednesday, September 30, 2020, 5:08:49PM EDT <1601500129>

While those in mentoring sessions work on their projects and I watch
them push the pretty Gruvbox colorful cursor across my screen from a
shared TMUX session I can't help but feel a visceral call to keep up
what I'm doing at any cost. These people are progressing in ways that I
can literally see before my eyes. It's very addicting to experience.

Doris and I talked a lot about isolating and targeting our every effort
over the next year to propel us into our best lives going forward. It
was a nice break from bickering about how to best organize the move we
are doing. We are both very opinionated and headstrong. We never
"fought", per se, but stuff like this reminds me of all the times I just
choose the submissive path and let her do her thing. What is it with me
and strong women? \*sigh\*

Today I decided (perhaps temporarily) that in addition to whatever work
I take on being remote-only that it must also allow me to live-stream my
work at least 80% of the time. I'm so dedicated to helping others though
example --- and I so enjoy sharing my failures and successes with others
--- that I just see no alternative. After all, I don't *have* to get a
job. I will just accelerate getting a home so that Doris can have a
studio that will allow her to pursue more gallery showing opportunities
nd make her own impact on the world. It will also allow me to
*eventually* be stable enough to offer whatever help I can to my sons
who are growing beyond the control of their Mormon upbringing and
discovering their own paths (which zero intervention on my part, I might
add).

"What kind of company would *pay* you to live stream?"

It sounds odd, but there are some. Intel has a guy on Twitch, for
example, but the most likely scenario for me is to get a job working for
--- or be funded by --- any one of the open source foundations and
corporations that are out there --- chief among them GitLab, Netlify,
and the Linux Foundation.

GitLab keeps coming back into my mind. It is a company that prioritized
hyper-transparency at every level, that encourages thousands of
community contributed changes to their core product, that live streams
many (if not all) of their business meetings. I imagine after I prove my
worth (most probably by making several GitLab contributions) that
approaching them with the offer to simply continue working on what I am,
and pitching it to them in a way that demonstrates what I've managed to
accomplish heretofore, would produce a successful employment
opportunity with them. In fact, I can thing of *very* few other
companies that truly understand modern work as well as GitLab. So I
guess in the back of my mind I'll be asking, "What would GitLab do?"
more and more. Hopefully, I'll be able to prove my worth soon enough.
I'll dream of live-streaming eight hours of work for GitLab --- while
being paid for it --- and maintaining my great mentoring relationships.
I continue to get better at making every minute of this life count for
something.

## Wednesday, September 30, 2020, 4:11:33PM EDT <1601496693>

Just reading about FlatPack and I'm really impressed. It blows the
doors off of Canonical's Snap, which I still cannot believe people
actually use. I've never been happier that Mint is giving Ubuntu the
boot. Ubuntu is really starting to suck and make decisions that Apple
would approve. The disastrous horrid architecture Snap uses (polluting
the mount space) is a testament to the lack of experience on the Snap
team and at Canonical.

## Wednesday, September 30, 2020, 2:08:31PM EDT <1601489311>

On the stream <https://twitch.com/strager> had a great idea to
reverse lexicographically order `TokenIds` with a linter so that I don't
hit the `LF` before `LFAT` problem that I spent way too much time on.


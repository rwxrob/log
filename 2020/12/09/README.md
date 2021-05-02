## Wednesday, December 9, 2020, 6:16:17PM EST <1607555777>

One thing is for sure. Rob Pike seems like he has nothing to do with the
day-to-day direction and proposals to the Go language any longer. I
suspected there was a decline in his involvement beginning with 1.13 and
it seems to be confirmed. I have not seen him participate in any threads
from the Go core team.

With all the crap going on with the unnecessary and wasteful addition of
generics to the language in 2.0 I'm seriously thinking of orchestrating
a fork of the core language and ripping out all the `context`
dependencies that have polluted everything. Hell, I could even fix the
leaking `goroutine` situation if I really wanted to and had the time.

Obviously, I likely will not do that given the time constraints, but
damn, I really want to. The way the team has simply thumbed its nose at
the simple proposal for Go to follow it's own style guidelines
(changing `context.Context` to `context.C`) is just laughable. Most of
the thread says it is in agreement and out of no where one of the
contributors says, "I think this is a declined proposal based on the
above." It's like the dude can't fucking read.

This is *exactly* why Linus holds the kernel so close to his heart and
only let's extremely trusted people anywhere near it. Same with Brahm.
The Go team is currently running Go into the fucking wall and they don't
even see it.

I'll tell you who *is* seeing it though, the Rust community. While their
core team shares some of the same flaws, the overall way they deal with
proposals from *everyone* is far more democratic. That's probably why so
many parts of the language are `cargo` crates, because the best
submission wins instead of having to bow down to the core team.

I can't believe I'm saying this, but for the first time I'm starting to
see why some highly elite developers are just fucking done playing the
Go game. Google *does* have shadow control of Go. That much is becoming
more obvious every day. Google might not control it directly, but all
the people on the core team accepting and rejecting proposal all seem to
be employed by Google. I could have been seriously wrong about something
that is *very* important. Once upon a time I could be leery of *any*
language that has signifiant influence from *any* company. It's why I
was hesitant with C# and Java actually.

Bottom line: it is very likely that Google *does* control Go and any
peon like me doesn't have a prayer of getting a proposal even
considered. That's a big fucking problem, despite all the rest. If they
are not careful with 2.0 the rift might just give a large segment of the
Go community reason to leave to Rust, Typescript, new Typescript-esque
Python, or C.

I need to cool off a bit before I make any conclusions here. I'm just
pissed because something so obvious has created such a controversy,
mostly because it came from some random dude, and not a Google/Go team
member.

## Wednesday, December 9, 2020, 3:06:20PM EST <1607544380>

It was unusually difficult to discover the format for `protoc-gen-doc`
comments which turn out to be the same at Go, yet another suspicious
similarity between Go and Protobuf.

## Wednesday, December 9, 2020, 3:08:43AM EST <1607501323>

Looks like the word [crowdcoding](https://duck.com/lite?kd=-1&kp=-1&q=crowdcoding) already exists. It is definitely
what we are doing on the live stream.

## Wednesday, December 9, 2020, 2:23:34AM EST <1607498614>

I've actually never written a browser plugin and think it would be a fun
and useful addition to the "overengineered resume" project since
something will be needed to screen-scrape the LinkedIn data in a way
that has been authorized by the user and command-line alternatives are
more complicated when it comes to authorization.

Another option is to be able to "push" into LinkedIn rather than pull
out the data. Perhaps both. [\@the_kca](https://twitch.tv/the_kca) from Twitch recommended that.


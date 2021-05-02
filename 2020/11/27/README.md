## Friday, November 27, 2020, 10:08:46PM EST <1606532926>

Torn between doing this a quick way that I know will work because it is
just a little application that will only run currently as a command and
using a full `context` and `goroutine` idiom, which I really need to get
better at intuiting if I am going to get serious about a bunch of
communication work in Go because it is all about concurrency, API
requests, and handling the errant leaking `goroutines`. Context are
*specifically designed by Google* to address those issues and the
lack of elegance of `context.Context` (which was obviously not designed
by Rob Pike) is just one of the many things about contexts that I'll
have to overlook.

I also have to start using channels and concurrency even if it isn't the
natural first thing to pick because it is the *go to* thing in any
backend coding. Besides, which processor power the way it is now, it's
time to start approaching what seem to be simple menial tasks with a
*default* consideration for how they can be done concurrently (without
losing maintainability and simplicity too much).

## Friday, November 27, 2020, 9:37:51PM EST <1606531071>

Turns out that the super "clever" practice of embedding a GitHub Gist in
your blog (instead of just fucking typing in the code) makes the code
completely and totally unreadable by text-based browsers and blind
people. Yet another "yeah we royally fucked that up" moment from the
good people at GitHub. They are literally destroying the Web every day
with that shit.

Here's an example. Go look at this [shitty Medium blog](https://medium.com/codezillas/golang-leaky-goroutines-and-how-to-clean-them-30b505417028) (yet another
reason to *never* use that fucking horrendous service). The content is
relatively good, but the choice 1) to use Medium and 2) to embed a Gist
when you could have just backticked in the code makes it really lame and
distracts from the content.

## Friday, November 27, 2020, 9:15:21PM EST <1606529721>

I've been putting off using Golang contexts in anything significant. I
really hate them. But, they are used everywhere and I feel like firing
off a `ConnectAndLog()` goroutine seems to be a pretty obvious use case
for what people *say* they are good for. Imma try it out. Hopefully it
is lighter than passing a channel for coordination, which is what I'm
used to.

One reason I am considering them is that I believe they avoid the nasty
situation of starting a function as a goroutine that should have some
sort of error returned.

```go
func ConnectAndLog() error {...}
go ConnectAndLog() # blows up
```

Rather than returning the error, cancelling the
context is more effective and stable.

```go
func ConnectAndLog(ctx context) {...}
go ConnectAndLog() # fine now
```

I have to admit that if `context` is *the official* answer to the fact
that Go's already [unpopular garbage collection does *not*
cleanup](https://medium.com/codezillas/golang-leaky-goroutines-and-how-to-clean-them-30b505417028)
errant goroutines than I will openly confess Rust *might* have a solid
in on that front if it can make up its fucking mind how it wants to do
concurrency (they are on like their fourth iteration of official ways to
do it). I *really fucking hate* contexts.

## Friday, November 27, 2020, 7:49:08PM EST <1606524548>

So the design that is emerging for this `live` streaming helper utility
stuff is to just capture the websockets data to a rotated log file with
a `service` (sometimes called a `daemon`). That way the volume of
incoming chat and the speed won't affect memory of any app using it.
Then we just put a tail on it with something like `live tail` for those
who want to see the raw log. It also makes quick status commands like
`live views` faster to calculate because just have to reverse tail up
until we get the right status update and grab the data from those. This
also argues to keep the chat and event logs different, as Restream has
already designed them that way. The potential volume of chat could be
enormous for live streamers with lots of views, which reminds me, doing
it this way also ensures that the person running the stream can throttle
and filter the incoming messages as they desire, at least with regard to
what gets written to the screen. At some point integrating the `ban` and
`mod` commands for each supported service into `live` could be useful as
well.

Another thing logging also allows is the mocking up of utilities and
commands that can use the stream of log data to pretend it is incoming
live from the websocket.

This means I have to get the basic logging service working right away. I
already have the downloads working, so just have to pipe that to a file
and setup a concurrent log watcher to rotate when they get to a certain
size. I think watching the size is more important than anything else
otherwise it will be too hard to stitch everything back together again
when mining data from them.

I'm thinking I could also keep some running stats recorded as well and
just update them every time we rotate a log.

Oh, and then there is the possibility of importing all of it into a
database for searching later. I could build a web site that is updated
through static site generation with indexes on all keywords and allow
searching through the logs for stuff. That way we don't have to depend
on Discord for that.

Humm, I'm pausing to think if that would need a formal database or not.
I think if I made an SSG (like I will be using on Mim, The Knowledge
Network) with word indexes pointing to files that contain links to
specific posts in other static files that no database would even be
needed.

Let's face it. Databases are really old school these days. Other than a
quick, in memory thing like Redis for tracking sessions and Oauth2-like
stuff they are really useless and incur a *huge* technical debt
potential cost over time. As soon as you add a DB you can no longer
leverage CDN caching advantages. You are bound to one server without a
lot of complication, and as soon as you are bound to a server you have
all the other administrative problems that go with it.

Still, I could approach the whole thing in a K8S style. We'll see. Don't
want to get too crazy. It's just a way to search the logs after all and
grep (or equivalent) is fine for most of it.

## Friday, November 27, 2020, 7:25:01PM EST <1606523101>

Have to be really careful with OBS Studio lately. It keeps crashing but
keeps streaming. Something about the desktop GUI that stops working but
it is still found. You'll notice it when you try to run another OBS
because it thinks there is another one running, but only when you
attempt to stream and says the stream key is in use. The danger of this
is really obvious.

One way to be protected from such mishaps is the `live service` that I'm
creating that will stay connected to the websocket services and continue
to report on if something is still live or if there are still viewers. I
know that because when I open the web chat app from the `restream.io`
site it is there showing there is still something going on.

After the mishap with Discord live stream remaining on after OBS was off
that is yet another reason to centralize all these little things into a
single service running in the background that has your back with you
make a mistake.

It occurs to me that all of these little lessons in live streaming while
working are perhaps good for others as well so that more people can gain
a level of comfort sharing their daily coding work with others, thereby
helping and motivating them to contribute more themselves.

## Friday, November 27, 2020, 6:12:00PM EST <1606518720>

Forgot to add [Golang Swagger
implementation](https://duck.com/lite?kd=-1&kp=-1&q=Golang Swagger
implementation) to the list of core skills, and also Kafka.

## Friday, November 27, 2020, 3:11:46PM EST <1606507906>

I need to create a video and walkthrough of how to isolate bugs that are
not obvious without the use of any sort of error reporting that gives
you a line number. Using long comments and print statements any
developer can get to the root cause of a problem incredibly quickly even
if they cannot see what it is at several steps along the way. This
technique is not particularly obvious to beginners but is learned though
hard experience when nothing else will work. I've learned over the years
that even the best debugging, stepping IDE execution, and other code
analysis tools still are not as reliable as the good 'ol "comment and
print" method.

## Friday, November 27, 2020, 3:22:09AM EST <1606465329>

I have to remember that `slop` is the name of the X geometry helper
utility. It is essential when changing position for the `screenkey`
utility.

## Friday, November 27, 2020, 3:02:52AM EST <1606464172>

Oooo, more good resources for learning Kubernetes from one of the
original architects. <https://kube.academy/> 

I'm really torn because as much as I know stuff is important learning
and maintaining gRPC and re-learning IDL and all the other languages of
cloud platform application development is a *huge* amount. I suppose the
question for me is, will I remain interested in just maintaining and
helping people setup Kubernetes environments or is my true passion in
the systems integration programming and helping all the things
communicate with each other. I think I just answered my own question,
it's the second. I'm not even sure if I actually *like* k8s given a lot
of the dubious decisions in its architecture that I've *already*
encountered. No, I'm quite certain I want to keep with writing code, and
words, lots of words. I fucking love to communicate and that is not
something a lot of people into DevOps cloud development are into. I
fucking *love* writing technical docs. I know. I'm demented.

And, since I'm pontificating here again about my future and strengths.
I'm pretty damn good at helping other people learn things, so perhaps
that is the target career, to master all the things and them be the
executive consultant that my friend wanted to hire me to be (for
\$250k/year no less). Yes, I will *never* come away from the command
line and the coding, but there's something to be said for the amount of
change one can bring about by helping other organizations and
individuals master this shit. That's really my, um, calling? Oh, god.
Where's my coffee?

## Friday, November 27, 2020, 2:06:52AM EST <1606460812>

Doh! Turns out Restream has *two* websockets channels, one with a `chat`
subdomain and another with `streaming`. The first is the one I wanted,
the second the one I coded first. I'm glad I figured it out though
because I love that they are completely concurrent so that I can have
one goroutine updating status in the terminal view (incoming, outgoing,
views, etc.) while the other just focuses on drawing the incoming chat.

## Friday, November 27, 2020, 1:28:37AM EST <1606458517>

So looks like I have to do a round-trip for every "event" chat message
that comes in. The websocket API (that I got working finally) just tells
you a message happened, but not what's in it.


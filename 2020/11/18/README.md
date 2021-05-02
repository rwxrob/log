## Wednesday, November 18, 2020, 5:44:50PM EST <1605739490>

I love that `git config --global pull.ff only` is a thing now. I used to
always hate resolving the ugly merge conflicts that would sneak in.

## Wednesday, November 18, 2020, 4:29:45PM EST <1605734985>

Just taking a moment to enjoy the fact that I do have at least one
super-power: tech learning and research. I can find information in
seconds that takes others minutes just from the use of [Lynx, the text
terminal](). Beyond that because everything I do is in the terminal my
eyes (and brain) have become so accustomed to processing the input in a
consistent, noise-less way that I can read and scan the information in
fraction of the time if I had to look it up through graphics or books
and adapt to all the different graphical and writing styles.

It's not a secret that the best technologists in the world (based on
productivity and quality) are also the fastest researchers and learners
in the world. It's so sad that so few people ever understand this or
find the motivation to do what it takes to master this skills.

One more thing, when a period of intense learning focus is needed
putting some comfortable earplugs in is every bit as good as what I
imagine taking drugs would be.

## Wednesday, November 18, 2020, 4:16:31PM EST <1605734191>

Just would [this amazing Oauth2
walkthrough](https://fusionauth.io/blog/2020/10/22/securing-a-golang-app-with-oauth/).
It's definitely the best resource I have found on the entire Internet
for setting this stuff up in Golang as well as using at least one Oauth2
provider that is not specific to any give service.

The main take-away from reading through it initially is that almost none
of the server and redirect intercept stuff that I am doing is needed. As
I suspected, the semi-standard `oauth` package does all of that. 

What it *doesn't* do is manage all the different application configs in
your home directory in a manageable and safe way, nor does it provide
any kind of command line utility to help with shell script integration.
That's what I can focus on (and get done with this stuff a lot faster
from now on).

## Wednesday, November 18, 2020, 3:28:06PM EST <1605731286>

I feel kinda dumb for not noticing it earlier, but using the convenience
function `http.ListenAndServe()` *obviously* uses a single local server
for everything rather than one open to use with concurrent com channels,
duh. So I need to back and rip out the com system within my little
convenience `oauth` package if I'm going to use the simplified form.
Truth be told, I'm used to more complicated setups where there is more
than one possible server with its own goroutine/thread. I really don't
need the com channel now that I have put a `RWMutex` around the
`AppData` structs that are shared by every server instance that fires
off. It just means that I'll have to enforce some other type of
separation between the mock login server and the application client
server, even though they will be one and the same for testing.

Need to think about this one for a while because I can think of a
useful use case where a command line app or daemon would want to
maintain tokens for several Oauth2 APIs concurrently, for example, in
any sort of service bridge situation. I think the solution is to wrap
the entire app as a session with it's own unique HTTP server(s) for
redirection handling and mocking the service login authorization flow
There can be several apps on a single account with a given service. 

That just seems more *right* than throwing everything into the package
name space and limiting use of the package to non-concurrent parts of
any application. Doing so would make it impossible to refresh multiple
service application tokens at the same time during the same execution,
and since writing a daemon is a likely use of this package that kind of
thing will be common.

In other words, gotta back away a bit now and diagram some stuff to
manage the flow (as well as document it for others).

## Wednesday, November 18, 2020, 9:11:55AM EST <1605708715>

Okay, I have to rant about it. <https://developer.restream.io>, a site
entirely dedicated to documentation and communication *requires*
JavaScript to be enabled. I fucking *hate* that! The other day on stream
I was entertaining the possibility of working for them. No more. They
fucking SUCK if they don't understand how completely fucking brain dead
they are to put their *FUCKING DOCUMENTATION* behind a JavaScript wall,
just so *fucking* stupid.

There. I feel better.

## Wednesday, November 18, 2020, 7:29:47AM EST <1605702587>

Turns out to disable screen locking on PopOS!/Debian all I needed was to
install `dconf-editor` and then find the settings under
`org/gnome/desktop`. Working from home having to type that password in
all the time is rather annoying. 

## Wednesday, November 18, 2020, 5:48:36AM EST <1605696516>

Another thing I need is a way to mark locations such that they can be
exported to a YouTube video description so that I can automatically mark
locations in the YouTube video. I definitely need a way, post
processing, to update the YouTube title and description so that I can
just run a command and not have to even log into the thing.

## Wednesday, November 18, 2020, 5:38:16AM EST <1605695896>

I'm questioning the value of doing anything with the Restream chat
messages other than displaying them on the screen for me to respond to
and know about. In other words, I don't really need a chat bridge
between all my services that I'm streaming to if I am displaying them
all on the screen. Plus the lag between them all would make for a very
weird live stream. No, instead the best (and simplest) thing to do is
just to display everything that is coming in and respond to it as I see
it.

After all, the problem is that *I* can't see the stuff coming in from
others, not that they cannot see what I'm doing because even if I
respond in chat I'm typing it on the screen for them all to see. If they
want the most direct live exchange with me that needs to come through
the IRC in Twitch.

That keeps the ugly bot chat out of the feeds entirely even though that
means there isn't a searchable chat for people to go back and reference.
I will have that, but others won't. I suppose I can create a searchable
web site with all the chat logs at some point.

## Wednesday, November 18, 2020, 4:42:15AM EST <1605692535>

This is not going to make any sense, but when I voice stream it keeps me
up. For some reason speaking messes with my sleep schedule more than
anything else. In fact, now that I think about it, when I do a lot of
voice stuff I end up more randomly exhausted during the week than when I
don't. Just typing doesn't do that. If I just code with music I get
naturally tired. So weird.

I think what I'm saying is that I basically have two live streaming
modes:

* Code and music
* Code and voice

Here's another random observation: when I voice it annoys me to have
music on. It's like I'm talking over the music and it stresses me out,
sort of like being in a loud pub or coffee shop with a friend.

I find I get a lot more done also when I don't voice and I definitely
get side-tracked far less. Going down a rabbit hole in voice is *really*
hard to recover from, more emotional for some reason, more likely to end
in a rant that requires a full break to reset.

In fact, I'm so much more productive when I don't voice that I'm
inclined to do it far less, or at least when I do use voice I might as
well fully engage and go with video as well even if I'm recording a
podcast.

Occasionally, chat will be harder than talking through a problem, in
which case I'm just going to turn off the music (and external monitor
speakers so there isn't any feedback) and talk through the issue and
then switch back to music mode.

There's actually two more modes:

* Commentator
* Musician

Commentator mode is when I'm talking over something that has sound to make
commentary on it, usually a YouTube video of some kind. For this I have
to wear headphones and pipe the sound and mic into the same mix to I can
monitor the levels in real time. For this kind of thing you really do
need a sound board that allows for this.

Musician mode is also something that requires headphones to get the mix
right, especially when sing karaoke or something, and, of course, if a
guitar is involved.


## Saturday, March 7, 2020, 2:54:43PM EST [1583610883]

So looks like there is color emoji support in Alacritty in the latest
version by providing a font "fallback" for them (instead of the black
and white versions). Very helpful people on the IRC channel.

## Saturday, March 7, 2020, 1:34:04PM EST [1583606044]

Been reminded recently of the importance of learning a command-based
editor like `ed` (after recently talking about Rob Pike and his famous
"ed is the only editor you need" statement) is the *only* editor you
often can use when you don't have visual mode after hacking into a
system through a service that does not support a full TTY. I remember
doing that with Metasploitable some years ago for our Summer camp and
being like, "Hummm, so there actually is very real value in learning
`ed`." Now I'm trying to determine if `ex` (the successor to `ed`) is
just as good. I notice that it is now combined with the man page for
`vi` so not sure.

I want to create a simulation of a situation where `ed` is all you get
and how to do that. I think something as simple as a basic script tied
to `nc` should do the trick, sort of a local, hackable service just to
simulate lack of a full terminal environment.

In fact, a friend from the Twitch stream shared the fun fact that Joy
gave up on `vi` because there were so many different versions and just
used `ed` instead. `vi` didn't even start in visual mode by default. He
added that a couple months later after noticing that nobody was using it
as a line editor. Apparently there's a whole
[video](http://xahlee.info/comp/interview_with_bill_joy.html) and
[another](https://www.theregister.co.uk/Print/2003/09/11/bill_joys_greatest_gift/)
on the history of it all.

(God I love having a stream community.)

## Saturday, March 7, 2020, 1:29:18PM EST [1583605758]

Out of curiosity I actually looked up how `sed` suddenly had in-place
editing. Turns out it has been in the GNU version the whole time, which
is why I always used `perl -p -i -e` instead because I knew it would be
on *every* UNIX system, not just GNU stuff. But given the widespread use
of Linux now I suppose using `sed -i` is good to know.

It's not unlike things like `mkdir -p /some/long/path` which is
unsupported in any of the original POSIX `mkdir` versions (another thing
GNU added). I use it all the time now, but knowing when and how stuff
changed is something of an obsession.

## Saturday, March 7, 2020, 12:41:19PM EST [1583602879]

Gabe brought in his new Razer Blade 15" 2019 is reporting on it. I'm
completely convinced it's the go-to system for most pentesting and
forensics (not to mention best gaming laptop). He had problems initially
with suspension from screen closing (because he installed the default
Mint kernel on 19.3 ISO was too old) upgrading the kernel fixed it.

The chassis is the most solid I've encountered and I *love* the
keyboard, sturdy and chicklet-y. I *destroy* keyboards so that is a bare
requirement. Definitely my next purchase when ready to go mobile again
for everything. My (bork) XPS will have to do for now.

Gabe says make sure to get it from Amazon since price and warranty is
better. He bought the four year coverage including accidents.

## Saturday, March 7, 2020, 12:26:40PM EST [1583602000]

GitLab *sucks* when viewed with Lynx. Need to open a ticket.

## Saturday, March 7, 2020, 12:23:12PM EST [1583601792]

TIL that screen now has splitting panes. The question came from a
long-time screen user about why he should consider TMUX. A bunch of
things came to mind, but these are best summarized
[here](https://superuser.com/a/279167). The author left off the
customization of vim bindings for navigation between panes and resizing
them, which I could not live without.

I did find it extremely validating that the `screen` default bindings
for splitting us the same exact keys I have set in my
[tmux.conf](https://gitlab.com/rwxrob/config/-/blob/master/tmux.conf)
file (rather than the bork defaults).

## Saturday, March 7, 2020, 11:13:57AM EST [1583597637]

Back on standard Xterm colors. There is something about it that is
beyond "retro" feel. The colors are very solid. The contrasts are
amazing on any device at any size and dimensions. And people see what
they will likely see when they pull up a terminal for the first time on
Raspberry Pi or whatever. Plus asquiiquarium looks as expected.

## Saturday, March 7, 2020, 10:28:07AM EST [1583594887]

Last night someone showed us a video about a seriously mentally ill
genius who created their own compiler and operating system and
everything that goes with it including some really crazy graphics. At
first it was intriguing but by the end I was sad and pissed for having
seen it. I know the person mentioning it wanted to explore the
possibility of making an OS and was pointing out the extreme
intelligence involved, but the video seemed to linger and dwell on this
person's descent into madness for no other purpose than to
sensationalize the drama. I suppose capturing the story is one thing,
but showing all the videos of his worst moments crossed the line. I
didn't need that. It triggered my disgust with people who laugh or just
overly sensationalize any mental illness. I think I might of hurt some
feelings without meaning to but it's not okay. Mr. Robot deals with that
topic so perfectly.

## Saturday, March 7, 2020, 1:04:02AM EST [1583561042]

So today's OTW had a lot of SSL port stuff in it that was nice to see
because last time I did anything with port connections and enumerations
was in the 90s (other than for fun here). The combination of `openssl`
and `s_client` is absolutely amazing. It takes all the hassle out of the
SSL/TLS complexity when connecting to ports allowing connections to SSL
enabled ports without having to negotiate all the cert shit. Here's one
to remember:


``` openssh s_client -ign_eof -connect <host>:<port>

```

It is the same as plain old `nc` of old. It waits around to see what you
type in and otherwise passes the whatever you paste in. The `-ign_eof`
holds the connection open for interactive sessions. Looks like you need
this and cannot just pipe to stdin as you can with `nc` but I'll
research that more later.


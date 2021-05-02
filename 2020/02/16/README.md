## Sunday, February 16, 2020, 2:56:14PM EST [1581882974]

Next time I do a video about Git hosting it has to include a lot more
than just GitHub vs GitLab, namely the following:

* [Gitea](https://gitea.io)
* [cgit](https://git.zx2c4.com/cgit)
* [SourceHut](https://sr.ht)

There are other options is the point if you don't want to play the big
"Facebook for developers" (GitHub) game.

Now that I've had a little more time to think about it, I'm *really*
convinced that hosting repos all over the place is just not my thing. I
cannot see a compelling reason for it anymore, the *only* significant
reason was for visibility and to make it easier for those who already
have a GitHub account but anyone unwilling (or unable) to use GitLab is
probably not someone you want to see a PR from anyway. People who do not
understand the substantial advantages of GitLab's foundational CI/CD
integration (and all their other advantages) either out of ignorance or
simply an inability to understand are not worth having on a project team
until they *do* understand why. The end. The sounds harsh, but I've been
too wishy-washy on this topic and it has seriously cost me a lot of time
and energy.

I think that using *what you want* after putting in an enormous amount
of energy to understand why your selection is objectively the best for
your situation should be rewarded, not punished. After all, that's
*exactly* how Linux came into existence.

## Sunday, February 16, 2020, 2:49:06PM EST [1581882546]

I did realize that there is still a compelling reason to maintain an
active GitHub account: to manage forks and submit issues using that
service. If I seriously fork something I can move it to GitLab (like the
latest `vim-pandoc-syntax-simply` fork of mine).

I am going to keep more of everything under my personal account (instead
creating one of the very easy to create free groups on GitLab). I'll
save a group for when I actually have other people working on the
project with me an want to vary the organization of repos and
permissions. For example, the `readme.world` group will remain and I can
put `rw` and any server infrastructure in there. S²OIL will remain as
well as a place for utilities and documentation about lessons-learned
from the initiative and community that can accept submissions and
participation from a much larger group than just me and the community
here. And, of course, SKILSTAK will remain a group there as well.

God I'll be glad with all this migration and cleanup is finished. I
suppose this means my priority in that regard is finishing the basic
`repo` tool for dealing with the repos on both systems, something the
`hub` tool can never offer.

## Sunday, February 16, 2020, 2:08:35PM EST [1581880115]

Just ran into [another
project](https://gitlab.com/tslocum/cview/-/blob/master/FORK.md) ---
with a core library --- that has [migrated to
GitLab](https://gitlab.com/tslocum/cview/-/commit/5f880bc2c7e62eab34ea46946b8ae2d2e9b1f6a4).
I *keep* running into these. Usually it is really informed technologists
and teams that are doing it.

The `cview` team is remarkable. They seriously know their stuff and they
have decided that to use the `gitlab.com/tslocum/cview` package that you
will forever have to be dependent on GitLab, *not* GitHub. This flies in
the face of the \#1 reason to keep stuff on GitHub: availability and
community size.

I'm feeling *horribly* conflicted at the moment. After my evaluation
earlier in the year about why everything public needs to be on GitHub
because that is where the contributors and recruiters are I'm seeing
solid evidence that this is changing, slowly, but definitely changing.

The conclusion I'm arriving at is that there are far fewer people on
GitLab, but those who *are* on GitLab are by and large *far* more
informed and intelligent about their decisions regard source management
and even aesthetics. In short, they are more discerning and would rather
face not being found than be on GitHub.

So which type of community do I want to make myself a part of?

You already know that answer. GitLab beats GitHub on every single point
that matters. The only thing I have not yet tested is their GraphQL API.
I'm going to sit on this decision for a week or so and talk it out with
other amazing technologists on stream and in person, but I have a
feeling I will be saying goodbye to the closed-source, cluster-fuck that
is GitHub. I already feel less dirty for porting things over *to* GitHub
in the first place.

I mean, if you depend on being found in GitHub or playing with all the
script kiddies there that don't even understand why GitLab is so
ridiculously superior then you have bigger problems. It's not like my
having bought Macs at one point because I thought it would help attract
more students. It certainly did, but the ones it attracted sucked. Had I
stayed Linux my student base would have remained more like what I have
today. 

In other words, I've all but decided to abandon GitHub entirely, once
and for all and to put a placeholder there that says, find me on GitLab.
The End.

Ya know, every time I allow myself to be influenced by a *perceived*
perception management concern it is always the wrong decision. Picking
the superior ideas and technologies and using them *no matter what
others thing* is the only way to live.

As for my people here? Well, imma let them decide for themselves. I'll
tell them what I'm doing and I'll leave it at that.

As for me, I'll be keeping my stuff all under a new group named `rwxrob`
and making a very distinct line between personal stuff and stuff for
SkilStak. The `ssoil` stuff will remain it's own entity.

## Sunday, February 16, 2020, 1:59:34PM EST [1581879574]

I've confirmed the problem with sound levels being out of sync. My
lights on this board were not even hitting the orange at all. And when I
bump up the channel volumes to put them in the orange on the board they
go in the red on OBS Studio. Which means that OBS Studio is bork and
off, which is consistent with what Rairden was complaining about
earlier. He'll like learning he was right again. ;)

This means the *only* reason to watch OBS is to be able to quickly hide
something with passwords, which means I have one less thing that needs
to be on the main screen. Huzzah!

## Sunday, February 16, 2020, 1:52:20PM EST [1581879140]

It has to be said. Streamers who are putting they chat into their main
video feed and who are *not* able to textually respond seem to be doing
it the hard way. I know that Twitch is designed for streamers to be able
to vocally respond to text chat on stream and that might help, but
having HexChat on the screen set to "Always On Top" is much more
efficient for the kind of live-coding streaming I'm doing because not
only can I see the messages coming it, but I can respond to them
immediately without even switching to show anything in the web browser.
In fact, the only reason I even need the web browser *at all* is to edit
the stream settings to change what people see when notifications go out.
And I'm also learning that you have to stop the stream anyway for that
to really take hold properly, if even for a short moment.I'm getting
much better at quickly starting and stopping the stream so I don't lose
the connection with everyone, which also helps to split the videos on
demand (VODs).

## Sunday, February 16, 2020, 1:37:15PM EST [1581878235]

Reminded that my Twitch agent/bot needs to be able to regex search the
titles from YouTube and list the URL for the video so I can pull it up
instantly without cutting and pasting from YouTube. A sort of query
language just for content of the different videos in the
<https://rwxrob.live> collection. Come to think of it, as soon as they
are all paired with their written content on <https://skilstak.io> I
could just pull up those and make the bot use the `rw search` command to
find hits. That would integrate the whole damn thing! Woot!

## Sunday, February 16, 2020, 1:15:53PM EST [1581876953]

Arggg, the sound meter in OBS Studio lies. I know it isn't probably the
most scientific measure, but listening to music coming from the coffee
music streams is at the right sound level and without changing any
volumes I cannot hear myself on the news stream this morning. 

Actually I don't think it is OBS Studio that is the problem. This board
is way to underpowered to send an amplified signal to my device. Upping
the main output volume would very likely fix this problem but the board
is way to underpowered to do it. Hopefully the new board, that should
work entirely through USB can handle all this much better because the
return signal will be digital and not depend on board amplification.
This crappy board requires an analog setup.

It is possible that it's not the board at all, that the digital signal
coming in as a mic source cannot be maxed further. For now that just
means recording at ranges that hit regularly in the red on OBS. We'll
see what that does with distortion though.

## Sunday, February 16, 2020, 12:14:45PM EST [1581873285]

I got to thinking about how much information a person gives up about
themselves to Google when they setup repeating, regular search reports
that come as email. I imagine whatever heuristics they have for that
stuff ranks such search terms with much higher priority further creating
an "echo chamber" effect not only on all Google activity, but all the
activity of anyone in your home (on the same IP) who goes to *any* web
page that uses Google Analytics. It's pretty damn 1984 with the goal
controlling your buying habits, not world domination... oh wait, that
*is* world domination.

Of course that got me to thinking (in the shower) about possible
solutions. The obvious solution is for people to create and control
their own web crawlers. This is an idea that would have been dismissed
immediately in previous iterations of the Internet and WorldWideWeb but
is very acceptable today given current bandwidth and computer resources.
"What if everybody did it?". Well, that's something we can't know fully.
It is certainly orders of magnitude better for humanity than if
*everyone* traded in crytpo-currencies, which would destroy our current
world power grid.

There are several web crawlers out there that have come across my radar
(none of which I can remember right now). One of the most interesting
ones used Go concurrency to search the entire open web in 24 hours (was
the claim).

None of the crawlers (that I know of) cover deep-web, dark web, and
README knowledge network, nor do they mine data from Newsgroups,
specific tweets, and other crawlable knowledge sources. Yet these
alternative sources are *invaluable* in all decision making and
knowledge of current events. The Go-Nuts mailing list comes to mind. The
opinions and information expressed there *never* hit the mainstream
social media of Twitter, Reddit, etc. Yet *that* information is 10 times
more valuable than anything from social media.

So there is a very clear value proposition to creating a way for people
to customize their own Internet keyword crawlers. A lot of the
technology would overlap with crawlers/scanners that I already want to
make to improve bug bounty hunting. Hell, the hacker community certainly
doesn't have any problem scanning the whole Internet all the time.
Shodan.io regularly scans *every* device. Which is what I would
envision. There is a *lot* more information to be had from the entire
Internet than there is just the Web. In fact, the amount of useful data
on the Web is diminishing as more and more people keep their information
in their own communities and countries.

I wonder what [Aaron](https://youtu.be/gpvcc9C8SbM) would make of all
this? I wish he were here to lead us. There's no doubt in my mind now
that he was killed by the American government, which has said it would
kill Snowden if they ever got a hold of him as well. God I hope I don't
suddenly show up in the news with a suspicious death like Aaron. But I'm
no where near the threat he was. Aaron almost single-handedly defeat
legislation in congress through passionate, non-violent activism.

I certainly don't have time to write such a tool right now, but after I
finish `rw` and `readme.world` I definitely will. 

I wonder what we could name it, perhaps something to honor the memory of
Aaron. Perhaps `hil` from his middle name Hillel. Now for a domain, the
inexhaustible form of hope for projects I'll *eventually* get to for the
low, low price of \$7 a year.

Humm, what if I used `know.sh`. Yeah, that might work. I'm not inclined
to put a pretty GUI front end on it anyway, and with `cview` being a
thing now that people could `ssh` into I would be directly rewarding
people for searching for information in the safest, most private, most
cost-effective way, through text. Yeah, I can see Aaron smiling about
that idea. Sure he felt everyone should have access to data and I'm not
saying they can't, just that I want to build the entire infrastructure
based on no GUI first and *then* layer an appropriate GUI on it after
that.

In fact, maybe the main command needs to be `know` with a bunch of
subcommands. Yeah, I really like that idea. Aaron will *know* it is for
him. I like it to because it has all kinds of tag-line possibilities,
like "in the know" and "did you know" and "be a know-it-all". 

I really wish I had a army of developers to help make stuff like this
into a reality. I suppose I'm doing the right things to find them,
through streaming and finally putting myself out there on YouTube. So
far the talent and minds that is attracted to my stream are rather
significant.

## Sunday, February 16, 2020, 11:04:09AM EST [1581869049]

With Pandoc 2.9.2's release it is really clear that the project is
moving toward a data-centric design and architecture. This is
phenomenally cool. It is consistent with the reason I left Hugo (forming
Hugonot and FADB and contributed to the TOML project) as well as the
main idea behind my [Hugo
tutorial](https://github.com/rwxrob/hugo-tutorial-link-data-to-type)
that helps create data-centric, data-driven Hugo sites.


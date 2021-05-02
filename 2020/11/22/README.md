## Sunday, November 22, 2020, 10:45:13AM EST <1606059913>

Now that the hard part of the `auth` tool is finished, the rest is just
clean up, like "closing" in the medical world. If I was a surgeon like
my buddy Mike from High School is now I would be handing off the rest to
a junior, but I don't mind. I need to get good and fast at it. It is
what keeps me from publishing so many things. I get the challenging hard
stuff done and then fade off and the end. Then, metaphorically, my
patient dies and never leaves the table. At least I just own that
about myself and try to work on it. 

The good news is that what results will be something I can use forever
to make coding anything with an Oauth2 authentication a breeze,
including simple shell scripts. I'm particularly proud of just being
able to use `curl` and still get all the automatically refreshing
ability that `config.Client()` gives. All the token refreshing happens
behind the scenes, but without writing in a heavier language like Go.
This is crucial to coding and testing Oauth2 clients as well as servers
and I imagine I will be using it a lot.

Stuff like `auth` is not sexy; it's not some sort of fancy game
development; it's not hacking (although I can think of tons of ways this
will make hacking easier by enabling quick shell scripts that would have
been hampered by the Oauth2 stuff before). No, `auth` is one of those
super boring things that *everyone* needs and no one wants to make, like
`curl` (and `libcurl`) that is used literally by everyone who uses the
Internet today. 

Can you name the person who created `curl`? Are they famous? They
fucking should be. Our entire world would not be as it is today without
this person's quiet contribution. *These* are the contributions I seek
to make, those that are appreciated by people like me who actually give
a damn about the engineers who are building our civilizations instead
of the "warriors" (to quote B'Elanna Torres) who get all the "glory".

People like me are hard to find. That's not arrogance. We are
*literally* hard to find because we usually have our noses in something
that isn't being broadcast to the world. We like attention but
don't usually seek it. That's for people like the decidedly
non-engineer types like Steve fucking Jobs to do while the Woz's build.
We need the Jobs' (unfortunately), but I'm a Woz, or at least I want to
be. [\@qmacro99](https://twitch.tv/qmacro99) from Twitch reminded us that [Dennis Ritchie](https://duck.com/lite?kd=-1&kp=-1&q=Dennis Ritchie) (you
should fucking know who he is) died not just seven days after Jobs but
his passing was "eclipsed" because of it. Who had the greater
contribution to the world? The person who said on camera, "I've been
shameless in stealing good ideas" or the person that co-created C in
order to create the Unix operating system that Jobs stole (among many
other things)?

But things are changing though and even the `libcurl` guy is now live
streaming. So are a lot more engineering professionals who are far more
talented than I. The world *is* changing for the better because of
streaming and at least we have that, even though a few troll-monkeys
will inevitably throw shit because they just can't do it.  Being
reminded how mediocre you are really hurts. They have to do *something*.
The good people of the Internet will stick around and learn something. I
know I did, just last night from [Simon
Frey](https://twitter.com/eu_frey) who only has 121 followers on Twitter
but has produced some of the most important content I have *ever* read
on the Internet. Nothing Earth-shattering, just not found anywhere else.
Because he took the time to capture and share it with or without fame.
That's what we need more of today.

So, I guess I'm just taking a moment to realize what matters most, and
enjoying the silent comradery with amazing engineers, all of us
"building civilization" together in our own quiet workshops, taking an
occasional glance at the Trump/Kim Kardashian madness of the popular
world, and then quietly smiling and turning back to our work like Mr.
Horologist adjusting his glasses as he looks back at his watches.

There, I feel better.

## Sunday, November 22, 2020, 2:38:33AM EST <1606030713>

I really need to take a full look at `context` again. I really never
liked them but they *are everywhere* these days.

## Sunday, November 22, 2020, 2:26:19AM EST <1606029979>

Now that everything works for the `Authorize` flow --- integrated web
browser authorization and redirect and all --- it's time to look at how
all of this could be running to manage several services at the same
time, like in a chat bridge which is a very likely use case. I did hit a
blocking condition due to mutex conflicts near the end during testing,
so need to look closer.

One approach would be to just use mutexes on either the `Config`
collection of `App` structs, or on the `App` struct itself. The easiest
way to do this is to create accessor and mutator methods for all the
struct fields and even hide them behind the defined interface. Hiding
them incurs a lot more coding overhead, however, because now we can't
just marshal and unmarshal the JSON the same way.

We also have the entire issue of running just one HTTP server or more.
Just one makes best use of resource, but then we need to essentially
build a Redis table in memory to keep track of all the sessions and make
sure they get aged out over time. Any access, read or write to that
table must be surrounded by some sort of concurrency check or a channel
and an internal protocol.

Honestly, for something of this size I think the shared-memory model
works best. I know the saying, "don't share memory to communicate,
communicate to share memory" but it's an over complication in this
approach, I think. 

All I really have to do is lock the Sessions table for every write and
read using a `RWMutex`. In fact, if I do that I don't need to incur any
of the other overhead.

The embedded `oauth2` stuff doesn't have accessors so that would get
really hairy really fast. No, I need to think like a C programmer about
this.

## Sunday, November 22, 2020, 2:00:06AM EST <1606028406>

I just have to write about what this dumb ass had to say on my YouTube
channel because it just makes me laugh so much and is *so* indicative of
the broken thinking and attitudes plaguing our world:

> [YouTube: Jason Perry] How to completely tank a twitch channel: go from teaching linux command-line and JavaScriqt to Go and Oath. Too bad you could care less...

*[That is verbatim from the chat log.]*

I have run into this attitude a few times now. People feign they are
joking but some are seriously pissed that suddenly I *dared* to not give
them a fucking free education with nothing in return only to have most
of them effective silently drop out leaving me talking to the howling
empty wind, like one of my "cozy" live streams lately.

Here's the thing. I can risk teaching a bunch of random people who I
have no idea what they will do with the skills, or I can share my skills
with those I mentor after an application interview to be sure they are
the kind of people a fucking want to work with. And I'll be damned if
I'm going to give out that knowledge for free with the climate we are in
right now. Too many fucking Sith Lord / Trump Supporters out there and
I'm in this war for the right side.

So no, I'm not going to hand over this knowledge to just anyone anymore,
at least not my best skills. Those will go to my employer and those I
*know* will put them to good use. Like my beloved friend who just landed
his *first* job for \$100,000 after being with me for about three years.
I'll take that shit over some whiny anonymous YouTuber any day.

I'm still doing things for everyone, just not the things they *thing* I
should. It's like that skit with the guy complaining about the airline
flight and the other dude turns to him and says, "You're flying at 3000
feet in a metal tube, have some gratitude for Christ's sake."

The software I'm working on right now will have wide-reaching benefit to
thousands of people. Keeping a few hundred Twitch subscribers happy is a
pittance by comparison. 

So know, anonymous fuck-tard, take what you get and *maybe* if you had a
little patience and intelligence you could actually learn something by
watching the 10 hours of streaming I do every *fucking* day.

There. Better.

And you gave away a lot by dissing Go like that. Just proves you're
nothing but a troll and script kiddy. Imma focus on the *real* hackers.

And as much as I just needed to rant that out, I do realize there are a
ton of people who appreciate what I'm doing. Like everything in life
right now, it's more important to focus on them, always. In fact, having
a troll or two is a good sign. It means people are finding the stream
still even though I just code on it these days. That's all I care about.
The elite will see it for what it is and learn. The rest will enjoy
their mediocre lives.

## Sunday, November 22, 2020, 12:29:10AM EST <1606022950>

If I get burned one more time by forgetting to put a `*` in front of the
type for a receiver Imma scream, or something. It is one of the hardest
bugs to track when you don't know what you are looking for because
instead of altering the struct being pointed to, you are altering a copy
of it that dies when it goes out of scope. Typical pointer problems.
Thankfully they aren't too bad in Go.


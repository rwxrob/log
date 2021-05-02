## Monday, November 16, 2020, 6:11:01PM EST <1605568261>

Feeling a real need to rebalance my time and get on some sort of
schedule again. The election and move really blew everything away.
Here's my daily time budget Imma gonna try:

Hours|Activity
-|-
8|Sleep
5|Mentor (Work)
6|Code (Work)
1|Eat
1|Yoga
1|Walk/Run
2|Relaxing
24|TOTAL

I'll do really long walks/runs on Saturday and Sunday until I'm back
down to Patagonia size. I'll keep up my guitar and singing skills on
those days as well. Sundays I'll do all my household cleaning and
chores. (Sabbath? What's a Sabbath? 😈 )

But here's the hard part. Where to plan all of this during the day:

Hour|Activity
-|-
6:30a|Up / Coffee / Live Coding / Project
7|*Eat (light)* / Live Coding / Project
8|Live Coding / Project
9|Live Coding / Project
10| *Eat* / Live Coding / Project
11| Outside / Run / Walk
12p|Yoga
1|*Eat* / Relax / Coffee|
2|Live Coding / Project
3|Live Coding / Project
4|*Snack* / Private Mentoring|
5|Private Mentoring
6|*Eat (heavy)* / Private Mentoring
7|Private Mentoring
8|Private Mentoring
9|Walk Dog|
10|*Eat (light)* / Relax|
11|Sleep|

While I am mentoring often I'll have down time while monitoring the
coding that they are doing. That's good time to tidy up, check in with
social media, and keep the administrative part of mentoring working.

The struggle I have is that when I get coding on a project (or frankly
into anything) I have a hard time focusing on anything else. I'm very
obsessive about stuff.

## Monday, November 16, 2020, 4:47:37PM EST <1605563257>

I'm struggling with balancing the work on PEGN and the other stuff to
push along my mastery of the core backend tech I mentioned in the
previous post. 

PEGN is something I've always dreamed of, but is only
secondarily relevant to the employable skills of a *Senior Backend
Software Engineer* which is why you don't run into a lot of people
online who are doing it. No one gets *paid* to work on something like
PEGN unless they are in academia or have already established a language
and gained their financial independence doing it (like Guido). 

While I *am* financially independent, the need to get health insurance
for me and my family, while living through the biggest and deadliest
pandemic of my lifetime, seems like a priority, to say the least. Hence
my immediate focus on stuff people will be most likely to pay me for,
and the reduction in screwing around shit I've been known to do on
stream. I've recovered from my Twitter obsession through the election
and no longer have time to follow it as closely as before. Also I need
to start run/shuffling again to reduce my stress.

I know everything will work out in the end. Somehow I just know that.

## Monday, November 16, 2020, 4:14:38PM EST <1605561278>

The more I've been futzing around with Oauth2, HTTP, and such I'm
reminded how substantial the field of knowledge has become in *just* the
backend API and Authentication space. Even though everyone throws around
the *Full Stack Engineer* title a lot no one ever *really* retains a
readied mastery of *all* the skills required for that. No, the reality
is that rational hiring managers and project leaders understand that ---
while a good technologist can reskill quickly as needed to fill in gaps
that happen on the team --- *most* teams will be composed of specialists
who *also* have broad general ability. In other words, it's still a good
idea to find some skill and tech for which you will be the obvious pick
for SME even within a team of "Full Stack" engineers.

"Oh he's our Oauth guru."

"She's definitely the GraphQL pro here."

"They've really shown their the master of SSL and TLS."

You get the point.

Why does this matter? Because as soon as possible you (and I) need to
identify *very specifically* what tech and skill we will master beyond
any other such that people talk about you (me) that way when working on
a team.

Any one of these components of any large-scale web service requires so
much depth that working *just* in that technology all day every day
would be required to keep up with most of it in a way that provides real
context and insight that only comes from repeated exposure.

What is *my* pick?

That's a tough thing to answer for someone with more than 25 years of
broad-ranging and highly specialized career experience. At any number
of points over the years I was *the* specialist for a given thing from
creating data stores with terabytes of data, to writing my own network
protocols, to doing low-level core dump analysis. Arg. This is something
hard to decide.

I'm most drawn to GraphQL, REST API development combined with gRPC. I
want to be the how-stuff-communicates guru of any team I join. I've
always been obsessed with what I call "clean seams" so that everything
can work seamlessly together.

I hate Oauth2, but there is no escaping it. Implementing clean services
that use Oauth2 is an absolute priority for anyone calling themselves a
*Senior Backend Software Engineer*.

So here are the technologies that, let's say, I would have to know
*better* than anyone else on my team to be viewed as the team Backend
and services integration SME:

* HTTP
* SSL/TLS
* GraphQL
* REST
* gRPC
* Oauth2
* JSON Web Tokens
* `net/http`
* `html/template`
* `text/template`
* `curl`
* `netcat`

I need to have every line of every specification or information about
these technologies and tools committed to memory so well my fingers
just know what to do.

The good news is that I already know all of that stuff enough to get a
pretty good job creating and managing it, but I really need to take it
up a notch and target several projects in those areas to further
demonstrate to myself and others that I'm *the* senior specialist in
those areas, areas that I do not have a high demand to master in my
personal or professional life at the moment because once I get something
working it no longer needs my attention.

Incidently, were I to become a pentester instead --- or even just a guy
collecting bug bounties --- those are the same core skills I would
require.

It's also interesting that there isn't that much educational content on
these areas out there so live streaming this stuff could help a lot of
people. The frontend materials are covered pretty heavily, not so much
with the backend stuff. I also believe that is why getting a job with
exceptional mastery *specifically in those backend areas* will make me
(and anyone else) stand out when going for *most* developer jobs. It's
safe to say that most developer jobs today are in the SaaS space. Hence
their overall popularity and scarcity.

And yes, doing all this stuff in Go as my primary language will put me
even further ahead of all the Ruby and Node people who are now
scrambling to learn what I predicted would take over the server-side in
2014 when I made the switch to Go as my primary language. So glad I did.

## Monday, November 16, 2020, 3:39:17PM EST <1605559157>

This entire paragraph (1.3.1 Authorization Code) from the Oauth RFC is
just not relevant when one has to overcome the fact that an API
provider has decided to *assume* that everything using the API is a web
application:

> Before directing the resource owner back to the client with the
> authorization code, the authorization server authenticates the
> resource owner and obtains authorization.  Because the resource owner
> only authenticates with the authorization server, the resource owner's
> credentials are never shared with the client.

I'm pretty fucking tired of API providers *assuming* that everything is
a fucking web app. There are *lots* of other applications that need this
that aren't. Since I live on the terminal I'm justifiably pissed off. In
order to use *any* of these bullshit APIs I have to create my own
"application" and register it with the service. But worse, I have to
talk every user of any terminal application that I create through the
entire process because the fucking API provided requires it. Arguably,
it isn't that bad, and is getting better now that I'll have a library
for it. But still, not everything is a fucking web app.

## Monday, November 16, 2020, 3:34:03PM EST <1605558843>

All that Python programming has me forgetting that Go does not have the
`foo.Get("key")` method, which is probably a good thing because of how
slow all that unnecessary indirection is. Still, I always forget.

## Monday, November 16, 2020, 3:23:38PM EST <1605558218>

I'm torn between using the simplest HTTP server for the job with just
`http.ListenAndServe()` and creating a `Server` instance. There is no
way to explicitly close the default easy server setup, but there is
nothing wrong with starting up a server for the live of the process
because I can always reuse it by passing in new app contexts. This is
not a full production server after all, it's just a quick-n-dirty local
server to handle local redirects and mocks for testing stuff.

## Monday, November 16, 2020, 3:07:04PM EST <1605557224>

It occurred to me that I might not want to lock down the server to
`http://localhost:8080` --- especially since I might want to use the
`mock` path on interfaces other than the local one. So I'm just going to
allow it to be passed and push off that decision to the caller.

## Monday, November 16, 2020, 2:32:20PM EST <1605555140>

I always forget that to make a channel in Go effective you need to
create it and send it to the function that is going to need it, or do
you. I think it is possible to just return it, but that involves firing
off yet another goroutine within the function to allow the channel to be
returned. Passing in a unbuffered channel and then just blocking on it
with a simple loop makes for easier code to understand even if it puts
the work of creating the channel on the caller and not the function
itself.

## Monday, November 16, 2020, 2:20:49PM EST <1605554449>

Oooo, there's a shiny new Golang [blog post](https://blog.golang.org/)
about gRPC that I *definitely* need to check out. Truth of the matter is
that I really need to get freshened up on all the concurrency and
messaging stuff. I really don't use it all that much in daily life so I
need to create projects that use it. I already have a pretty good handle
on `text/template` and `net/http` but I need to have those mastered the
most of any secondary packages in all of Go. Add
[`google.golang.org/grpc`](https://pkg.go.dev/google.golang.org/grpc) to
the list. It has quickly become the standard communication method for
all things cloud-ish including both `k8s` and `k3s`.

## Monday, November 16, 2020, 1:22:24PM EST <1605550944>

Trying something different with the `net/http` package this time. I'm
going to embed the `http.Server` and implement a `Handler` for the
entire thing rather than depending on the built in
`http.DefaultServeMux`. Usually, it's easier to just use the built in,
but this server is pretty straight-forward so having everything together
might be better. In fact, for a bunch of stuff I don't even need to
determine the route at all since what is wanted can be derived from the
incoming data.

## Monday, November 16, 2020, 1:06:16PM EST <1605549976>

Today I need to focus on the main flow for authorization. I have it
completely tested, but need to clean it up and make it reusable. It
consists of firing off a local HTTP server to handle the redirects and
process the data only available from them. Thankfully Go is a breeze to
work with when it comes to concurrency and firing up HTTP servers.

## Monday, November 16, 2020, 3:32:55AM EST <1605515575>

I sent this [long
tweet](https://twitter.com/rwxrob/status/1328252857221525508) to Leah
Remini (who ironically has the same first name as my vile ex-wife's "new
name" that she'll go to Mormon hell for revealing). Her Scientology
series has one episode dedicated to Jehovah's Witnesses and I have to
say it got to me. Ellen G. White was a peer of Joseph Smith and you can
see so many similarities between the cults. Thankfully, for Mormons,
they believe in "modern revelation" meaning that they can adapt and
change as time goes on --- and have significantly --- rather than being
permanently bound by some interpretation of a book that means people let
their children die to be with Jehovah rather than live with a blood
transfusion. They made an obvious point I had not thought of. Once you
double-down on shit like that you are *stuck* because you cannot
suddenly say that letting children die was wrong that whole time. Many
similar things exist in the Mormon church, but to a lesser degree.
Polygamy is *still* the law of Mormons. They just don't "practice" it
while on Earth. And don't forget the [Mountain Meadows Massacre](https://duck.com/lite?kd=-1&kp=-1&q=Mountain Meadows Massacre) when
good Mormon men were commanded by their "Elders" to hack men, women, and
children to death with machetes.


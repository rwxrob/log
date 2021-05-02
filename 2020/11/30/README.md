## Monday, November 30, 2020, 5:10:15PM EST <1606774215>

Read this [interesting write-up on [immutable data structures in
Go](https://levelup.gitconnected.com/persistent-data-structures-for-gophers-persistent-stack-70aa012d3bfa).
It's really a unintentional testament to why premature optimization for
the compiler and garbage collection is fundamentally evil and should be
avoided at all costs until you *really* need it and have someone
proficient with the profiler to do it *after* you've already prototyped
your application.

## Monday, November 30, 2020, 3:11:07PM EST <1606767067>

I've concluded that the best to combine my career learning and fun
projects is to turn this `live` project, an assistant for live
streaming into a full-blown microservices app with bots in containers,
notifiers in their own containers and a centralized interface that
supports commands from the command, a terminal user interface in
`cview`, and an HTTP interface using websockets.

## Monday, November 30, 2020, 9:52:00AM EST <1606747920>

Jackpot! The [Certified Kubernetes Application Developer
(CKAD)](https://www.cncf.io/certification/ckad/) as a completely free
[open source curriculum](https://github.com/cncf/curriculum). This is
*exactly* what I need. It focuses on the specific things to be
trustworthy as a Go CKAD, perhaps the most in demand --- and lucrative
--- occupation for any Go developer in the world right now, not to
mention a lot of fun. 

Getting this certification is my number one priority above everything
else. Nothing I do will be related to anything *but* increasing my
ability to pass this exam. Thankfully all the work I've been doing on
the `live` project directly relates to most of this. After reading all
about gRPC and Protocol Buffers it's clear that even though I *could*
implement all the logical components of it within the same executable,
that it will be a much better learning project if I make each major
component into a container using the appropriate protocols. The `live`
project will definitely be over-engineered for the basic need, but I
will accomplish my goal of modularity while also working toward CKAD
certification.

## Monday, November 30, 2020, 9:31:48AM EST <1606746708>

Learning all about [Protocol Buffers](https://restream.io/channel) from
Google today and so far been really impressed. It also really makes me
feel amazing about what I managed to do with PEGN AST JSON compact form,
which is the smallest possible JSON. Protocol Buffers discard any
reference to the values in order to make them the absolute fastest way
to communicate over a network wire in a flexibly structured way.

I mean just read this, it's as if they literally picked my brain on the
PEGN AST JSON long and short form:

> A schema for a particular use of protocol buffers associates data
> types with field names, using integers to identify each field. (The
> protocol buffer data contains only the numbers, not the field names,
> providing some bandwidth/storage savings compared with systems that
> include the field names in the data.)

It sounds really arrogant, but I could totally work for Google if
I *really* wanted to. I just *really* don't want to.

## Monday, November 30, 2020, 5:21:41AM EST <1606731701>

Looks like it clearly is better to send a link to the YouTube live
stream instead of using Periscope *at all* which is *horrendous* quality
in comparison. The only effective difference is that followers on
twitter cannot see the number of views and also have to click to make
the video play.

So, I'm dropping streaming to Twitter, which has the added bonus of
allowing people to participate in chat immediately and sub if they like.
After all, if I ever wanted to monetize YouTube would be the place to
send people.

Also, I need to detect when people make comments on a Twitter post of a
live YouTube video or retweet it so that I can get the notification in
real time.

That reminds me that I also have to integrate comments on the YouTube
live stream videos so that they show up in the chat log pane.

## Monday, November 30, 2020, 5:08:27AM EST <1606730907>

Did some calculations of what if we used Digital Ocean for my own
restreaming of RTMP in conjunction with chat from bots logged into the
services to reduce all lag.

* 1800/hour/stream @ 4000Kbps
* 540GB per stream per month
* DigitalOcean @ 0.10/GB
* \$54/stream/month @ DO
* 10 hours a day for 30 days


## Wednesday, February 26, 2020, 6:07:11PM EST [1582758431]

Looks like InfluxDB is moving to rust for their version 2. Their Flux
parser clearly has a version implemented in Rust. I have one person
interviewing for their internship he happens to be obsessed with Rust.

InfluxDB is a major player in the IoT time-series database line up, and
it is in the absolute sweet spot for Rust. Alacritty is as well and is
so fucking amazing people cannot ignore that most of the advantage of
that terminal is simply because it was written in Rust.
[GoDot](https://github.com/GodotNativeTools/godot-rust) game engine is
in Rust and another studio has announced it will only code further games
in Rust (can't find the name though right now).

I gotta say, I've been watching Rust for a few years now and 2019 it
really came onto the scene hard. Then this last week Rust chatter is
*really* off the chart. Even big Go people saying essentially, "Well
duh, that is obviously an application that would be better done in
Rust." Ryan Dahl went with Go for Deno for almost a year before picking
up Rust. Brian Cantrill says Rust isn't the pick for a full operating
system but just might be the single best language for all the other
stuff. Even Fuscia (the brain-dead project from Google to replace
Android with C++ and Dart) even very publicly stated its support for
Rust and "banned" Go for any development on the operating system because
of Go's bigger runtime and such.

Combine that with the minor fail that is Go 1.14 and the waning
governance of the Go project (having lost a core founder as well) and I
think something significant is happening in that space. There's
certainly no cause for alarm, but the systems programming space is
shaping up to be Go or Rust.

What do I care?

Because I need to make sure those focusing on the back-end of things,
the systems people really get a solid handle on both Rust and C. In
fact, Rust is *far* more important in that space than Python ever will
be. Python will hold the machine learning and a lot of the cybersecurity
stuff for a while, but will eventually give way to Go, which has better
concurrency that is easier to implement, which is what both machine
learning and cybersecurity really need at the core.

## Wednesday, February 26, 2020, 3:22:52PM EST [1582748572]

Arvo Bold is the font I'm using for the heading title in the schedule
scene for OBS.

## Wednesday, February 26, 2020, 9:54:36AM EST [1582728876]

After reading the following on GitLab's page about their GraphQL API I
did some research (pulling up bad memories) and concluded it's probably
still okay to use GraphQL even though it comes from that massive turd of
a company (Facebook):

> Although there were some patenting and licensing concerns with
> GraphQL, these have been resolved to our satisfaction by the
> relicensing of the reference implementations under MIT, and the use of
> the OWF license for the GraphQL specification.

## Wednesday, February 26, 2020, 9:31:30AM EST [1582727490]

Looks like you can use *personal access tokens* as "OAuth-compliant"
headers as well according to
[GitLab](https://docs.gitlab.com/ee/api/#personal-access-tokens). This
is good information because we see them all the time documented
differently but knowing the two are equivalent is useful:

```bash

curl --header "Private-Token: <your_access_token>"
https://gitlab.example.com/api/v4/projects

```

Or more commonly:

```bash

curl --header "Authorization: Bearer <your_access_token>"
https://gitlab.example.com/api/v4/projects

```


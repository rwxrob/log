## Thursday, November 19, 2020, 5:57:05PM EST <1605826625>

Another way that I can contribute in ways that benefit corporations as
well as the world is to get them *off* of AWS/Azure/GCP dependency. It's
a point of professional pride for me to support those who can to "roll
their own" systems and architectures. There's nothing wrong with people
who use cloud providers. I certainly do. But it is a better personal
contribution to the world if the positions I take are helping companies
and organizations of all kinds to drop their dependency on the
monopolies as much as possible, or at least to make it more of an
indirect dependency (Kubernetes is opensource, but influenced by Google,
but so is Go).

Another benefit of such opportunities is that I don't have to learn or
deal with AWS and any of its crappy dashboards, of those of other cloud
providers, by the way. I can focus uniquely on getting cloud
applications written and deploying them to internal Kubernetes clouds.
That's my target core expertise, which is nice because it is *entirely*
in line with exactly what I built for IBM.

## Thursday, November 19, 2020, 5:24:03PM EST <1605824643>

*Cloud Software Platform Developer* is the title I recently heard for a
position that perfectly describes the skills I seek to do on a daily
basis for any kind of full-time employer. Here's the job description:

* Go, gRPC, REST for cloud-native applications
* Management of data center physical infrastructure (servers/arrays/switches)
* Virtualization and containerization with Docker, K8S, Istio
* Excellent analytical and problem-solving skills
* Innovative thinker who can lead architecture and development
* Passion for learning, programming, automation, and analytics
* Agile development (Scrum, Kanban)
* Test automation (unit, integration, system) 
• Outstanding verbal and written communication skills
* Team player who with demonstrated ability to collaborate across teams and organization

I love that they don't even mention the essentials like Linux. They are
just assumed.

As the recruiters contact me with different positions and I have been
searching for different ones on my own it is clear that the industry
doesn't know what to call all the new positions that are emerging in the
"backend" space that aren't the backend of anything. 

Notice the following are *not* included:

* GraphQL
* Oauth2
* NodeJS
* AWS/Azure/GCP

The reason these important technologies are not present is because what
you are coding usually doesn't have a front-end to talk to. This is the
shit I *live* to code. It's what I did for IBM *en masse* and look
forward to doing for someone else.

A particularly important distinction is between "Senior Backend Software
Engineer" and the stuff dealing with "Cloud Software Platform
Development". I've heard some call it "deep end" but that has a lot of
meanings to different people.

## Thursday, November 19, 2020, 12:53:58PM EST <1605808438>

I have noticed that I write better code when live streaming in *music
and code* mode (without voice). Because I can't just talk through what
I'm doing I have to write it down that slows my thought process down in
the best way to keep from doing things that I have to back-out later.
It's not just about not being distracted by voice and those on the
stream. It's about composing better thoughts all around. Plus there is
the calming music factor.

## Thursday, November 19, 2020, 12:10:01PM EST <1605805801>

I need to check out [`esh`](https://github.com/jirutka/esh) for basic
templates that can safely use the shell directly.

## Thursday, November 19, 2020, 12:03:04PM EST <1605805384>

I'm a little conflicted at the moment about whether to use base64 now
and encrypted file formats later or to just use the encrypted stuff now.
As soon as I start thinking about encryption my mind goes down the
rabbit hole of where to manage the single sign-on password:

* Do I run a daemon (like `ssh-agent`) that has it stored in memory and make `auth` just
  call into that daemon to get the data?

* Do I force the user to enter the password for *any* use of `auth`?

All of this seems like overkill since web browsers certainly do not do
any of that storing this data in the clear, but then again browsers
never contain the `client_secret` since that is always stored
server-side in the three-leg Oauth2 approach.

Then again, when creating a terminal application that used
3-legged-Oauth2 the user needs to create an *individual* application
registry with the service in order to do so. Saving the `client_secret`
value in a flat file is no less safe than storing an SSH private key
without a passphrase, a practice that is done all the time by
security-conscious professionals simply because it allows things like
`git` to work without typing in a passphrase every time.

Nope, no encryption until there is a need for it, but I should
definitely have it as an option for security conscious applications that
might be running on Internet-facing services.

## Thursday, November 19, 2020, 4:57:21AM EST <1605779841>

It occurred to me that Go is actually the perfect language to write a
little `gotmpl` utility that reads from a collection of cached
templates (both `text` and `html`). Sometimes all I want is the lower of
Go's templating system for random things and usually just want to
combine them with some YAML or JSON or just a list of stuff on the
command line.

There's too many cool things to build and too little time. I need to
tell someone about that so they can make it and I don't have to.

## Thursday, November 19, 2020, 4:18:20AM EST <1605777500>

I want to create a bash script or Go utility for my favorite methods to
add to a simple data struct:

* `String() string` - the `Stringer` interface as JSON
* `JSON() []byte` - compressed JSON buffer
* `Print()` - `fmt.Println()` of the string JSON
* `Parse(jsn []byte) error` - `json.Unmarshal()` wrapper
* `Load(path string) error` - `ioutil.ReadFile()` then `Parse()`

I should probably also make something that creates the `Example*` test
cases as well. Actually, I should just do one `ExampleData()` (or
whatever) and then just include a bunch of examples of using all the
related methods.

Maybe just a macro would be better than a generator because there is
nothing really dependent on the rest of the code.

## Thursday, November 19, 2020, 3:53:49AM EST <1605776029>

While doing the `auth.Data` struct and all the reading and writing and
saving and simple example testing I realize it would be a good exercise
to put add with the rest of the [language
challenges](https://rwx.gg/lang/cha), which reminds me I still need to
port all those others over there from the original Python days of
[SkilStak]{.spy}.

## Thursday, November 19, 2020, 2:27:58AM EST <1605770878>

So it looks like it's worth it to go with the `golang.org/x/oauth2`
package and see there that goes. In fact, it already has an
`oauth2.Config` struct that I can embed and give names to that I can
cache in locally retrievable ways. Still thinking of the best long-term
solution for all of that and how secure I want to make it.

I mean, if someone has access to your account they are already going to
be able to do all kinds of things to most people. The average person
will have at least one private key in their `.ssh` and `.gpg` that will
already be compromised. The `KeePassXC` does protect you somewhat from
that, but a skilled hacker might even be able to grab the private keys
from the RAM of the `ssh-agent`.

What I'm saying, I think, is that if things as sensitive as that are as
open as that for an average user then I simply don't have to fret about
a simple Oauth2 token --- or even client secret --- being saved in a
file. By the way, web browsers obviously don't lock up all the tokens
they cache without any other authentication required to use them. That
was the whole point of Oauth2 protocol to begin with.

I feel much better. JSON files will do just fine for this application.


## Friday, January 29, 2021, 8:07:57PM EST <1611968877>

I feel so shallow for not being able to think of anything but how much
more easily and quickly coded all [Caleb's "fuzzer"
code](https://youtu.be/2_ZaNBl6qNo?t=1476) could have been in Go. Caleb
is obviously a skilled coder, which strangely is more anomalous than you
might think for typical cybersecurity people --- especially pentesters.

One thing is for sure, Go is really going to rock the hacking world even
more as the up and coming generation realizes this true fact: Go is
actually better than Python for writing *all* secops-related code ---
especially anything with concurrency. That's *why* it was created.

Python just still has the lead in libraries and tools currently. But
that is changing very rapidly.

## Friday, January 29, 2021, 6:59:25PM EST <1611964765>

Started a list of [companies](/notes/companies) to help keep track of
the *really* good ones.

## Friday, January 29, 2021, 6:36:53PM EST <1611963413>

Gitea has users and organizations and repositories so I'm wondering if
having a monolithic Gitea instance for all repos might be the way to go.
We can have multiple domains with Giteas for each, or just one with all
of them organized underneath it. I'm thinking of having some overarching
Gitea domains:

Domain|Organization|Projects
|:-:|-|:-:
rwx.gg|RWX Community focused on supporting one another as autodidacts|rwx.gg,boost,skilz,auth,cmdtab
afk.works|Association for Federated Knowledge Workers|keg,kn,pegn.dev,know.sh

Then we can just mirror to GitHub.

God, after seeing all the momentum in the issues posted on Gitea it's no
wonder GitLab is suffering so much. I imagine GitLab has lost all
momentum from the open source community contributions. Gitea is clearly
a superior offering and is blazing fast built on Go at its core. GitLab
does stand a fucking change against Gitea on the one front and GitHub
--- especially with GitHub Enterprise and Microsoft's financial backing
--- on the other. I really, really feel bad for GitLab. That company is
going to evaporate in less than five years. Mark my words. So sad.

## Friday, January 29, 2021, 6:25:13PM EST <1611962713>

OMG the logo for Gitea is amazing. I'm so fucking done with GitHub
already, but spending 10 minutes on <https://gitea.io> has me completely
hating that I didn't port everything to it last year.

I'm imagining a day now where I can having nothing on my GitHub but
"find me on rwx.gg." Only the most fearless will take up the call.

Obviously, the next step will be a full subdomain to all users of
`rwx.gg` with accounts so that instead of `github.com/someuser` (which was
always stupid) we give *every* member their own subdomain as a part of
it. Rather than promoting a single monolithic service, we encourage
everyone to setup their own servers with Gitea on them, or GitLab,
thereby promoting open source to the fullest extend.

This is clearly the right thing to do. The rest of the mediocre, Silicon
Valley stoking, sheep/drones can stay on GitHub.

## Friday, January 29, 2021, 6:12:08PM EST <1611961928>

```go
import (
  "rwx.gg/auth"
  "rwx.gg/cmdtab"
  "rwx.gg/uniq"
  "rwx.gg/colors"
  "rwx.gg/term"
)
```

And yes, we can do better than `gh`. As cool as it is, it will always be
married to GitHub and I would rather promote a tool and muscle memory
that is service-agnostic and encapsulates the others. The average
developer is now pull repos from all over the place, not just GitHub. It
is possible that `git` clone could do it, but that doesn't add the level
of opinionated organization about how all those repos are stored
and managed locally.

```bash
repos clone rwx.gg/auth
```

I'm obsessed with what the Git paths and Go package import signatures
will look like now. Before I would have attacked people using their own
hosting for important package libraries, but there are so many ways to
provide rock solid longevity with the Go caching server and the
`replace` directive in `go.mod` now that no one need fear anything.
Besides, the ethos of Go is to *include* stuff directly rather than
depend on 100s of remote, unvalidated dependencies (like Node infamously
fucked up from the very beginning). In other words, if you are afraid of
a weird domain host that might to away some day, then just clone it into
your own or fork it. In fact, this will encourage me to do the same. The
packages hosted on `rwx.gg` will become a finely curated list of amazing
packages out there, some just simple forks, others improved upon. It
will be *way* more awesome than any fucking "awesome" list.

Oh my God, we have to do this.

## Friday, January 29, 2021, 5:50:52PM EST <1611960652>

A bit of quick research and comparison shopping between Netlify hosting
and Digital Ocean shows that running my own Kubernetes cluster with
Gitea as one of the services is completely doable. A single \$5/month
droplet gets 1 full terabyte of transfer. Netlify gives 100gb on their
free plan.

The more I look at the new offerings of Digital Ocean the more I realize
this is what I really want. While Netlify is amazing for getting a site
up quickly for most people --- especially when combined with GitHub for
automatic pushes --- it is something of a limiter to what I want to
eventually do with the RWX community. 

As for the cost, once I have a more traditional full-time job to go
along with the mentoring I'll have the money to support a full Digital
Ocean deployment and will also approach them about potential
sponsorships and hosting discounts. Hell, I might apply to work there
first. God knows they value open source individuality and have
positioned themselves as "the developers' cloud." 

I want to see DO succeed more than any other given my life-long focus
helping *everyone* become a developer. In fact, if you take the idea
from GitHub about being the "Facebook for Developers" and eliminate the
horrible Facebook association you have a corporate mission that seeks to
promote "developers, developers, developers" and *no one* does that
better than DO, absolutely no one.

I see my path emerging before me, and frankly GitHub ain't on it.

God it must be hard trying to keep up with all my changes in direction.
It will be fun for some people to say, "I told you so." I can hear them
now.

Seriously though, I've said many times publicly that I value
decentralized individuality over cloud simplicity. Centralization to the
scale we see with GitHub and the others is fucking bad for humanity. 

I can bring myself to be okay with hosting services, however. They are
centralized, for sure, but they are not controlling those using the
services to the degree that GitHub does. And if they ever tried to do
so, people can take their server images and deploy them someplace else.

I guess what I'm saying is that I support Amazon, Azure, GCP --- and
most of all --- Digital Ocean because they are centralized
infrastructure and not services. Locking people into services is far
more dangerous than locking people into a hosting provider because
people can pick up their containers and images and move when and if they
need. This promotes competition instead of lock-in to a specific
service.

I'm glad I came to this realization at this point in my refactoring and
house cleaning. It means all I need to do is clone all my repos locally,
back them up, and eventually creation my own hosting service for them.

GitHub be damned.

The real question is if I will maintain this level of commitment in a
day or so. God knows it will be a lot more fun to work with as a
community since I can get everyone to help support it and list their
support as a project on their resumes/cvs.

I mean the whole *fucking* point of Git is decentralization? GitHub is
completely and totally antithetical to that goal.

## Friday, January 29, 2021, 4:33:09PM EST <1611955989>

GitHub "Education" just denied my renewal as an educational institution
even though ...

* I was a founding member of their group and forum
* I founded a learning community and "educated" hundreds
* My people have flooded me with <https://skilstak.io/referrals>
* I've taught to private schools and community colleges

At first I was so angry I couldn't see straight. 

Then I remembered we are talking about such a dumb-ass culture at
GitHub, one that is okay with sending "Have an Octastic day!" at the end
of their "fuck off" notification with a little emoji in the subject of a
frown crying. How much of a emotional unintelligent ass do you have to
be so not understand that is *not* okay.

I fucking *hate* that GitHub is destroying GitLab's progress on every
front. I want nothing more than to see the culture of GitHub's
collective asshole-ness not be rewarded. 

In fact, I'm thinking of all kinds of ways I can actually just say
goodbye to GitHub entirely. But unfortunately they have a stranglehold
on source hosting now and visibility.

I would move to Source Hut, but not really an option. Just the tilde in
the repo paths is enough to not use it.

Hummm. 

I could do my own. Whitman made that work and did a great job of it.

I need to really think about this one. I at least need to stand up a
Gitea in-house server and evaluate it.

There are other ways to promote software and packages and community
besides buying into any one ecosystem. Linux proved that.

GitHub works because they make things so easy for developers and those
hiring them. But at the end of the day do I *really* need them and their
fucking "octokitty"? 

Hell no. My life is certainly not going to be better because I get more
likes and subscribes on any specific repo, or that I can set my active
status, or that I have "actions" and issues and a stupid-ass wiki. 

It would just feel so fucking good to be free from all the Silicon
Valley bullshit. That feeling might be worth dropping GitHub all by
itself. I bet Digital Ocean might even offer to sponsor host my stuff
for free if we get enough good stuff over there.

I'm angry right now so I need to wait before making any decisions here.
But I'm at least going to get a Kubernetes cluster working with a Gitea
instance running and go from there.

## Friday, January 29, 2021, 10:56:29AM EST <1611935789>

* Reviewed <https://pegn.dev> in light of KEG/KN changes.
* Discovered there is a hate-speech version of the Triskele. So what.
* Completed initial PEGN design and clothing merch idea.
* Migrated [`pegn-mode`](https://github.com/pegn/pegn-mode) Emacs mode
  to <https://github.com/pegn> org.
* Unicode added to PEGN-classes spec

Immediate work that needs to be done:

* Logo designed
* Emacs plugin
* Vim plugin
* Proper language server


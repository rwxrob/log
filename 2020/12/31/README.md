## Thursday, December 31, 2020, 5:10:29PM EST <1609452629>

After more research looks like Consul+Nomad is for "small to medium
sized businesses" while Kubernetes is for "Google scale" enterprises.
This would be consistent with analysis from my own community members who
have compared Kubernetes to Swarm and preferred Swarm for its lack of
unnecessary complexity. Let's face it, Google loves to overcomplicate
and overengineer things and always has but Kubernetes is the industry
standard (unfortunately) so I have to learn it first even though
Hashicorp is clearly a superior company on pretty much every level.

## Thursday, December 31, 2020, 4:34:37PM EST <1609450477>

Once again I learn a lot just by following the decisions of a single,
amazing company. 

Hashicorp --- the smartest tech company on the planet right now (that's
not even hyperbole) --- releases most of its latest stuff under Mozilla
Public License Version 2 (the new one). That got me to look at it all
over again. Turns out it is the perfect middle path between Apache (give
everything away) and GPL (restrict too much for most to use).

Now that I have [looked into
it](https://julien.ponge.org/blog/mozilla-public-license-v2-a-good-middleground)
I will be licensing (and relicensing) *everything* under MPLv2. It
protects trademarks, grants patents, is backed by Mozilla and more. I'll
do a better write up some day on the rest later along with a video.

## Thursday, December 31, 2020, 4:18:26PM EST <1609449506>

After reading through the
[HCL](https://github.com/hashicorp/hcl/tree/hcl2) spec it is *very*
clear that it is mandatory learning. It blows the freaking doors off of
TOML just for its JSON compatibility alone making it fit very nicely
between YAML (humans only) and raw JSON (machines only). It has native
Go parsing thanks to [fatih](https://github.com/fatih) (who fled the US
in 2020, by the way).

## Thursday, December 31, 2020, 3:43:04PM EST <1609447384>

Nomad 1.0 from Hashicorp came out recently. So far the best review of
Kubernetes v.s. Nomad is from [Fabrice
Aneche](https://blog.nobugware.com/post/2019/nomad_an_alternative_to_kubernetes/).
He shares my observation that "Hashicorp is synonym with quality." I am
constantly in awe of their creations. It is on my top five wish list of
places to work, but it would be *brutal* because expectations would be
so incredibly high. Still, they say a healthy bit of fear and
trepidation about the place you work is a good thing. It means you are
pushing yourself. I would definitely be pushed at Hashicorp.

I'm reminded by Fabrice's article of the following core technologies in
this space:

* gRPC
* Redis
* PostgreSQL
* Traefik
* NATS
* Consul
* HCL

Of course, I've been playing most with gRPC and ProtoBuf lately.

Redis is on my list of things to overengineer for fun and learning.

PostgreSQL I have been using since around 2004 when I printed all the
documentation and read it all to deploy it at IBM.

Traefik I've dabbled with as Whitman played with it a lot.

And, I believe one of our community members has a significant role in the
NATS project.

Consul is absolutely foreign to me, a Hashicorp cluster alternative to
Kubernetes, it seems.

HCL is [Hashicorp Configuration
Language](https://github.com/hashicorp/hcl/tree/hcl2) that attempts to
replace YAML. I'm seriously conflicted about it --- especially since
TOML was already there. It claims to be "compatible with JSON" but only
after going through their converter. It has both a "human friendly" form
as well as a "machine friendly" form. This means that JSON can easily be
transpiled into and from HCL.

The HCL discovery makes me inclined to believe that Hashicorp is one of
the few companies on planet Earth that would actually appreciate my
creation of [PEGN](https://pegn.dev) and its reference implementation in
Go.

The main take away, however, is that there are several players in the
cloud native and devops space and isolating areas within that space for
specialization is a necessary task to be a truly productive member of
any devops or cloud native application development team.


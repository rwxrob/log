## Tuesday, April 13, 2021, 12:12:04PM EDT <1618330324>

TIL that if you are not using CUDA 11 now you are really behind. Start
at least there if you are going Machine Learning (or anything) using it.

## Tuesday, April 13, 2021, 11:46:39AM EDT <1618328799>

Within five years there will likely be a consumer-facing OS distro that
is *entirely* managed by containers. Jess Frazzelle has already played
with this and my bet is that her collaboration with Brian Cantrill at
<https://oxide.computer> is something to that effect for the enterprise,
but it's just a matter of time before we have the equivalent of a NeXT
cube running nothing but containers.

Why? Because the value proposition of sandboxing *everything* is exactly
what modern security needs require. And the ability to instantly update
everything and restart it and reallocate resources as Kubernetes does
will *become* the new operating system. 

The Linux kernel is ideally suited for all of this due to its size. As
the embedded world settles on ARM, which is getting faster all the time
and has plenty of room to become a Node, and the Node requirements are
getting lower (k3os, BusyBox), the two will meet in the middle and we'll
end up with hardware specifically optimized for it (like we got with
Hypervisor, `cgroups`, even GPUs). 

Kubernetes does what no developer wants to do (or technically can do).
It optimizes the performance of whatever it runs to its needs based on a
policy that can space one core of 64. This has never been the
applications job. It's an OS thing. But current OSes don't do this.
Application developers are required to get really involved in managing
their concurrency. Kubernetes (or something like it) *removes* all that
thinking. Even the simplest languages with zero concurrency can suddenly
be fully and completely concurrent in ways that no single development
team would ever be able to touch, mostly because they never know what
else is running on the system. Kubernetes does.

The saying "Kubernetes is `/proc` for cloud" is not accurate, but does
kind of describe what is happening. Everything is an "inode" and
Kubernetes "objects" are like inodes, whether pointing to a running
process memory space, or to a link to something else, or to randomly
accesses block storage, or a single file in a specific format.

Also, with Kubernetes, the hardware is irrelevant so long as it is
compatible.

In short, the new operating system will be Kubernetes. It's just a
matter of time. Those who don't learn and understand it will be left
with their hat in their hands.

To the beginners out there I empathize, learning *everything* about
Kubernetes is equivalent of learning everything about how the internals
of an operating system work. The are equal in scope of learning and
understanding. Imagine having to understand the different architectural
internals (but not necessarily the code) of Microsoft Windows,
Macintosh, BSD, and Linux. That is the learning requirement equivalent
to keeping up with *all* the players in the Cloud Native space. You just
cannot survive trying to learn it all. You have to isolate the leaders
as best you can and focus on one of each. Then, you have to find an
employer who matches those things. Not unlike picking to work for a
Linux shop instead of a Microsoft shop.

All of this makes me think that a general Computer Science degree might
have more value in a Kubernetes world than it did before. In fact,
despite the overwhelming and unjustified cost of a college education
these days (at most places in the US) someone who *wants* to get really
into Cloud Native deeply probably should get a CS degree, perhaps from
WGU, the cheapest of all. Meanwhile, or during, they should learn the
Kubernetes stack and do development and lab construction at the same
time. I have a feeling the learning from *any* traditional CS degree
would directly translate to things listed on Kubernetes "concepts" page.

After all, just learning to code is no longer enough. You *must* learn
to code in a containerized, git context (not *just* DevOps, but
including it).

I think the term DevOps is going to fade away, much like "Responsive
Design" is now just assumed to be good web design. Developers will be
*assumed* to be DevOps people as well just like SRE transformed System
Administrators into "System Administrators who Code" (even though any
*real* system administrator has always been able to code, before Google
coined that shitty term).

Even if "DevOps Engineer" remains a separate role, it is always going to
be true that an equally qualified developer --- who has overlapping DevOps
skills --- will always win over the one who doesn't. Like developers who
can't use `ssh` --- or even the terminal. It is hard for me because I
personally assume people are aware enough see how obvious that
requirement is, but there are a lot of people who don't.

## Tuesday, April 13, 2021, 11:09:40AM EDT <1618326580>

Looks like Prometheus, as good as it is, absolutely sucks for things at
scale (like HPC ML). Long range queries for things like Kubecost make
Prometheus practically unusable. All the fan-boy obsession with
Prometheus is absolutely isolated to people who have no idea about this
kind of enterprise scale. Many large organizations are *quickly*
outgrowing Prometheus.

In other words, Kubecost + Prometheus = disastrously bad architecture
*at scale*. Thanos might to be the answer, or it could make it worse.

I'm so glad I didn't dive into Kubernetes metrics yet. It is *such* a
volatile space right now.

Also, I'm more than a bit annoyed that the Prometheus developers
obviously didn't consider enterprise scale when they created it. Not
even a slight level of enterprise architectural thinking went into that
product. It's another "get it out and beat to market to win" mentality
that is costing companies who have invested into it millions. This is
why there is still so much hot competition in these industry areas now
conglomerating around Kubernetes, which first conglomerated around Docker. 

One thing is for sure, there is a *lot* of Go development work on-going
now and in the future for all of these supplemental applications.
Prometheus, which was thought by many to be king of that space, is
turning out to really suck. People who think that something is actually
good because of bunch of big, well known companies are using it will
*always* be burned. Companies that build up talent to do a true
evaluation of the internals and architecture before deploying *anything*
will always win. They will have the courage to call out the bullshit and
protect themselves. Right now there isn't much more in that space,
Thanos is one, but it saves even more metrics that have to be kept and
managed and queried. Could be better, could be worse. We don't know
right now.

## Tuesday, April 13, 2021, 10:41:50AM EDT <1618324910>

TIL that `VOLUME` is really going to be important for the `lab` base
since it will allow `/home/you` to persist between different
`rwxrob/base` builds. In fact, for using Docker to use Linux it seems to
be an intuitive best practice.

The thing that tripped me up with volumes and mounts was my
understanding of the original "bind mounts" that mount across the Docker
boundary (and are significantly slower, apparently). Volumes created
with `VOLUME` are like disk drives with mount points that live inside
the Docker system. They aren't associated specifically with any one
image or running container. They are the direct parallel to a Kubernetes
PersistentVolume/PersistentVolumeClaim. In fact, in a simple way having
Docker installed is like having a "cluster" (in Kubernetes terms) but
without all the orchestration and the only things that live within it
are images, containers (running images), and volumes.

Cloud Native has several layers to learning it *beginning* with pretty
significant understand of how Linux works (storage mounts, partitions,
services, ports, processes, etc.). It seems right that CNCF would be
*under* the Linux Foundation for this reason. Here's the learning path I
propose (and need to diagram):

1. Docker User
1. Bash Terminal
1. Base Linux Knowledge
1. JSON YAML
1. Scripting (POSIX/Perl/Python)
1. Git/GitHub
1. Markdown / Pandoc / kn
1. Docker Developer
1. GitHub Actions, Packages, CI/CD
1. Kind (local Kubernetes)
1. Hardware (all of it)
1. Basic Go Development (including Templates)
1. Kubernetes (including Nodes)
1. Container Registries
1. Helm (Kubernetes "Package" Management)
1. Kubernetes Metrics / Graphana

## Tuesday, April 13, 2021, 9:45:09AM EDT <1618321509>

After completing the [`lynx`](https://github.com/rwxrob/lynx) repo and
container I realize there's no getting out of maintaining both such a
repo/container and a dotfiles with its own `Dockerfile` that will seem a
little redundant. I can get away from the redundancy with submodules (as
much as I hate them). I suppose if nothing more that will demonstrate
that I understand them and when its a good time to use them.

Re submodules, I noticed that the Kubernetes Python client uses them for
the `client` directory. It was freaking me out because other elements of
the repo content had broken links in them until I pull the submodules
properly.


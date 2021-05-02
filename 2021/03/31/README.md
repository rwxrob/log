## Wednesday, March 31, 2021, 10:15:33PM EDT <1617243333>

TIL that the <https://kubernetes.io> site has a lot of fatal flaws (from
my way of thinking) about its education approach. For starters, it uses
`minikube` which is *not* the way you would use `kubeadm` and such in
a real deployment. I'm hearing that `kind` is exactly the same and is
used by developers regularly to model the k8s space so that there are
not surprises.

So once again, I'm burned by a "let's make it easier to learn" tool
rather than using a *real* tool from the start.

## Wednesday, March 31, 2021, 11:51:16AM EDT <1617205876>

There is a lot of industry chatter about [Tekton
(Kubernetes)](https://duck.com/lite?kd=-1&kp=-1&q=Tekton (Kubernetes))
as it moves to be adopted as OpenShift "Pipelines". 

If Tekton gets traction and integration into OpenShift it will *destroy*
GitLab (more than it already is) because the IBM and CNF backing and ranking of
OpenShift could seriously sway high level CTO buying decisions. In fact,
I keep getting the sense that people actually don't *want* the
one-stop-shopping option GitLab provides. They want to plug and play
their own high-level infrastructure components. GitLab is essentially a
monolith, and most high-end IT shops don't usually like that level of
dependency and rigidity. 

I seriously cannot recommend GitLab for anything right now; from the
architecture perspective it makes less sense; from a sustainability it
makes less sense when the CEO says "I hope that someone will integrate
that into GitLab" in tweets revealing his dependency on open source
development instead of internal resources; from a usability perspective
the GitLab API is abysmal and there is still no `gh` equivalent in site;
from a market capitalization point of view there is no financial backing
like GitHub has. I really cannot get over these serious flaws, not even
for their perceived dedication to open source.

## Wednesday, March 31, 2021, 11:20:20AM EDT <1617204020>

As Kubernetes "gobbles up the world" people are considering if for
high-performance internal infrastructure things, that normally are
hosted in their own high-availability ways:

* DNS
* LDAP
* Kerberos
* NTP 

It is conceivable that even ActiveDirectory will someday be a Kubernetes
service, plugin, or in the control plane itself. 

This sort of stuff is really interesting because if it takes off it will
100% solidify Kubernetes as a core infrastructure component for *all*
enterprises and probably trickle down into mid- and small-sized
deployments as well (schools, startups, etc.). 

We are getting closer to turn-key, modular infrastructure for an entire
business than we have ever been in the past. It's a lot like installing
an app on your phone, just with a core infrastructure service for your
organization. Imagine just dragging a service icon over and having it
just set itself all up with a default configuration that you can then
adapt.

Terraform (and stuff like it despite it being immature at the moment)
are strong indicators that this is the way the industry is headed and
the money behind people that *want* this (the higher ups who want to
hire fewer people with higher expertise) is substantial.

One thing is absolutely clear, companies are expecting people in the IT
space to understand the following as well as they speak English:

* Linux (Ubuntu, RedHat, Alpine)
* Docker and Containers in General
* Bash Command Line and TMUX/Screen
* Vim Text Editing (without any customization)
* Basic POSIX Shell Scripting
* Python for Automation and Integration

There are other things that come to play beyond this fundamentals, but
even "Front End Developers" need to know this stuff. Seriously, it's not
optional if you want to get and keep a good IT job --- especially
because one 10x engineer with both developer and operations skills is
always going to be cheaper than 10 junior or mid-level engineers.

In other words, get senior as soon as possible.

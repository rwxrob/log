## Wednesday, April 28, 2021, 6:53:05PM EDT <1619650385>

Here are the naming conventions for the style guide.

1. Naming Conventions
   1. Imperative Verbs for Tasks, Skills, Like a Job Posting
   1. Nouns for Concepts and Terms (Verb Would Be *Grok*)
   1. Sentences for Principles, Articles, Rants

## Wednesday, April 28, 2021, 6:42:33PM EDT <1619649753>

Decided to delete the Twitch VODS so that they don't clutter up the
highlighted videos and distract people from them.

## Wednesday, April 28, 2021, 3:06:27PM EDT <1619636787>

Had to push back my two hours of SKILSTAK Twitch streaming stuff to 7pm
to make sure there's enough time to cover all the expectations from my
day job. They aren't particular formal or explicit, just an informal
expectation that I'm around --- particularly because I'm so new.

I'm also just going to delete all the stream VODs that are not those AMA
times and even those will likely be deleted as well after I get
highlights made from them.

## Wednesday, April 28, 2021, 2:45:27PM EDT <1619635527>

I really wish someone had told me that it is extremely rare to create a
Kubernetes Pod for *anything*. It's not mentioned on
<https://kubernetes.io> anywhere. For me, `Deployment`, `Service`,
`NodePort`, `PersistentVolume`, and `PersistentVolumeClaim` are the most
important "objects" to first understand because you need them to get
anything actually done.

In fact, the "official" site is absolute shit for getting started with
Kubernetes immediately in a *real* way.

Another complete fucking waste of time was setting up and using
`minikube` for *anything*. It's absolute shit for anything practical.

Honestly, it is so much better for beginners to immediately bite off the
trouble that `kind` is because it is more worth it long term. Most
people starting will not have a cluster they can blow up to learn shit.
The `kind` tool fills that space better than anything. 

The next best option when experimenting with Kubernetes to learn it,
which is absolutely the best way, is to use GCP or some other cloud
provider. But that can get expensive.

The next best option is to get a bunch of small multicore computers, old
ones even, and build an *actual* physical cluster locally as your
"sandbox" (as they say).

## Wednesday, April 28, 2021, 11:59:06AM EDT <1619625546>

Finding out that I should use Helm for delivering my modified version of
JupyterHub. I wanted to do that anyway, but misunderstood that "it was
overkill". I've been looking at Terraform scripts as well (for the
future). But they are *definitely* overkill and not really alternatives.
What I'm looking for specifically is an easy way to bundle and track
versioning on these changes and everything combined together.

Now I really need to see how Helm behaves in Kind and how much it
integrates with stuff from the registry. The bottom line, when it comes
to CN applications development identifying what stuff should
go into the container image (Dockerfile) what what goes into the
configuration (effectively though arguments) is a tough decision. Here's
a sample list:

* What goes into the Dockerfile?
* What registry should host the image?
* How configurable should the image be?
* How should the image configuration be done? (env, args, YAML, etc.)
* How much configuration should be Docker-ish?
* How much configuration should be Kubernetes-ish?

These are entirely new considerations for most applications developers,
who generally just think about how to package or containerize their app.
This is not just containerizing but anticipating all the different
configuration possibilities as deployed to Kubernetes, including things
like concurrent Pods and network services. Come to think of it, it is
the same stuff application developers thing about with a single
application, but scaled up to multiple applications combined together,
things like concurrency and consistent, persistent storage.

## Wednesday, April 28, 2021, 10:34:10AM EDT <1619620450>

Don't know if it is an official convention, but in Go code the docs
usually to not include parentheses when referring to functions and
methods, which makes sense because doing so implies that the arguments
list needs to be included as well. Plus, it makes for cleaner reading
and easier searching. For example, when searching through code quickly
to find the beginning of a function or method adding the initial
parenthesis isolates what I want and doesn't match all the stuff in the
documents. I know there are cleaner ways to do this that involve
language-specific plugins, but this works for any language, anytime.

Moral of the story: just use names of functions and method when
referring to them within in-code documentation.


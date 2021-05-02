## Tuesday, April 20, 2021, 11:24:36PM EDT <1618975476>

### On Getting Undressed

It occurred to me that the simple act of getting undressed can be
fraught with subtly stressful decisions that when made poorly affect
life in important ways. 

In short, peel off your clothes. I know. You've been taught that to do
so is less organized, that it creates more work later, that it creates
stress knowing those clothes on the floor or in the hamper are indeed
inside out.

But here's the thing. You *want* them inside out most of the time. After
all that's where the dirt and grime usually are. When they go into the
washer that way they will get cleaner turned out. Then, after they are
nice and clean you can turn them back again when folding them or putting
them away.

Peeling off clothes to get undressed also is by far the fastest way to
remove the clothes and when you need to get undressed you usually need
to do it quickly. Unless you are doing some sexy strip tease, getting
clothes off in the fastest way possible is way more important. Consider
the following:

* Saving someone's life at the pool (per the Life Saving merit badge)
* Taking a quick shower before an appointment
* Coming back home exhausted and just wanting to sleep
* Getting ready for sex (you've seen the movies)

All of these activities all benefit from getting undressed quickly. And
speaking of being undressed.

I'm also recently reminded how much better it is to be naked in bed.
We've long known (and taught) that getting naked even in a blizzard
within a sleeping bag is by far the most effective way to same someone's
life from hypothermia. But it is also so much more comfortable when
sleeping because there is so much less material to bunch up as you toss
and turn throughout the night. If you become dependent on your clothing
to keep you warm you inevitably end up having a crack in your clothing
during the night and that part of your body freezes. But if you go into
the night knowing that *all* of your body is exposed then creating a
safer barrier that protects your *whole* body heat gives you a better
night's sleep.

Sleeping naked does have its draw backs, however. The biggest one is
being at risk of having to get up quickly. This is why having a robe or
sarong nearby is absolutely essential, not to mention the warmest
and most efficient clothing option when you need to depart your warm
cocoon for whatever reason.

See this is why I need to finish `cmdtab-zet`. I need someplace to spew
these random thoughts without remorse or the cognitive overhead of
thinking too much about where to share them.

## Tuesday, April 20, 2021, 4:18:37PM EDT <1618949917>

Need to write a TMUX plugin that reads from the `tty` like screen key
and provides information updates in real time.

## Tuesday, April 20, 2021, 12:25:28PM EDT <1618935928>

Fuck. I hate that I'm going to have to give in and use a big fat ugly
prompt that puts my cursor on the following line. There's no other
option when creating meaningful, SEO-optimized directory names and URLs.
Having a meaningful branch (which is also mandatory) really pushes the
boundaries even further.

## Tuesday, April 20, 2021, 11:49:02AM EDT <1618933742>

Today after noticing how fucking long the GitHub repo names are getting
I'm seriously wondering what is the best way to organize labs. I'm
feeling like I should be using a monolith repo instead of a bunch of
tiny ones. In fact, why can't this just go into `rwx.gg` with all the
other content. People are more likely to want to follow a single repo
for changes than a bunch of tiny ones.

Recently it became clear (again) that the simplest approach is just a
`README.md` file that describes the activity rather than a complicated
system for validating, in other words, a Knowledge Node. It can contain
`Dockerfile` and other informational files and starting assets. 

One point of confusion is what to do about labs that involve creation of
GitHub repos and such. Again, the solution is to just say, "go create a
repo someplace."

## Tuesday, April 20, 2021, 11:25:53AM EDT <1618932353>

Realizing how completely valuable Kind is. The simple fact that you can
use local docker tags in place of container registry settings in pod
configurations is worth everything about it. I know that `minikube` does
*not* do this and I suspect that `microk8s` also does not because they
have different goals in mind. Because `kind` was and is being used to
test Kubernetes itself having these iterative conveniences is not only
very nice, but mandatory in a modern development environment.

The more I reflect I realize that I've been thrown completely into the
deepest end of the Kubernetes application development pool. I'm
customizing and extending an existing complicated multi-user application
(JupyterHub) so that is uses network attached storage that it identifies
from a query against the Kubernetes API (Python client) and alters the
core behavior for notebook identification. And to top it off modify the
web front-end to accept all the changes and prompt for user directory
entry, securely. I have a feeling getting the CKAD will be a *lot*
easier later after this project (if I decide to get it).

One thing is for sure, *every* assumption I've made over the last eight
years about what tech is required to learn for a beginner has been spot
on --- except one: Docker.

## Tuesday, April 20, 2021, 8:49:50AM EDT <1618922990>

(I really need to start using the `log` as a log and get the
`cmdtab-zet` done for the other Zettelkasten type of notes.)

Today I want to get the entire collection of JupyterHub components
working and installed as a Kubernetes deployment (since I don't think I
can do the entire thing just as a single pod). 

And I really need to document the entire process because there are
several interdependencies that are not entirely clear even to people who
know about this stuff. I'll keep this work under the repo for
`lab-jupyterhub-nas-ns`

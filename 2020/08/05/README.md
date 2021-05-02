## Wednesday, August 5, 2020, 7:50:03PM EDT [1596671403]

WSL
[sucks](https://askubuntu.com/questions/1230252/sleep-doesnt-work-on-ubuntu-20-04-wsl)
(and possibly 2 as well). Just wasted a bunch of time debugging a simple
loop with a sleep in it only to find that it is because WSL is fucking
trash. Now I have to port all my people back over to running PopOS in a
virtual machine which is what I started out doing but was tempted by the
ease of install for the WSL stuff.

I am *so* tired of being surprised by broken shit that should obviously
work like this. I will *never* recommend WSL to a beginner ever again!

## Wednesday, August 5, 2020, 5:11:00PM EDT [1596661860]

I could not be more pleased that my `Filter(r rune) bool` type from PEGN
is compatible directly with the entire `unicode` package from Go. This
means that anyone can use any of the comprehensive library of functions
as a `Filter` passed to the `Consume(f Filter)` method of the
`pegn.Parser` interface. I love it when a good plan works out.

## Wednesday, August 5, 2020, 4:54:19PM EDT [1596660859]

I take that back. The Apache 2 license must be included as well for
those times when I want to promote adoption by the most legally paranoid
organizations. It placates their worries much better than The Unlicense,
which I'll use for informal things. So that means:

1. The Unlicense (permissive, informal)
1. Apache 2.0 (permissive, formal)
1. GPLv2 (non-permissive, formal)

## Wednesday, August 5, 2020, 4:39:42PM EDT [1596659982]

I've decided there are only two software licenses I care to ever use for
software:

1. The Unlicense (permissive)
2. GPLv2 (non-permissive)

I figure people are going to do whatever they want anyway if you make
your source code public, so putting *any* license on it is just a
formality for the few times when someone will actually care about it.
Ask any developer in China what they thing about the GPL? Nevermind, you
can figure that one out and no one will even answer that question
anyway, they are too busy stealing all our best software and making
proprietary changes to release products that destroy ours at market.
Licensing, like so many things, is something they just laugh at in our
faces, like that one scene from Mr. Robot.

But it's not just China. Apple regularly steams ideas and stuff from
open source projects without letting anyone know. The reader they
implemented in Safari destroyed one such project. And when is the last
time you saw *any* attribution in any Apple screen.

In other words, none of it matters as much as I (and others) worry about
it. If you *want* people to give back their changes to in in GPLv2.
Otherwise, might as well just make it Public Domain. MIT and BSD will
just let them compile it in a way that no one can actually see that they
are in violation so we could *rarely* catch them anyway.

When I want permissive, I want it to be *really* permissive. When I want
to ask people to share their changes (and that's all) GPLv2 is really
the only license in town for me.

## Wednesday, August 5, 2020, 4:09:42PM EDT [1596658182]

I'm seriously thinking of writing (another) book, *Learning to Program
in Go as a First Language*. It would be fun and easy and take the same
tone as *Eloquent JavaScript*. It would be entirely based on my
challenges approach and mix in the essential concepts and terminology as
it comes up. That way there is always something going on to stay
engaged. Having recently really looked hard at Rust and also been doing
a lot with Go for PEGN I really feel like Go will be the *true* dominant
language of our time clearly taking the place of Python, Node, Java, and
much of C++ and some C.

I really believe learning to code *first* in Go would put the learner
light-years ahead of others by introducing types, when to make them
strict and when not, why to think in terms of what a thing can do
(interfaces) as its type rather than its underlying structure, and to
think internationally from the start in Unicode runes rather than just
bytes. Plus understanding the concurrency model (goroutines and
messages) doubles as preparation for how the Linux operating system
works.

## Wednesday, August 5, 2020, 4:01:21PM EDT [1596657681]

Skype has blown Discord away in professionalism, features, and
stability. I'm actively moving all SkilStak operations *off* of Discord
in any way. I will maintain the community there for RWX.GG but that is
it. Discord is an absolute disaster of a company and product. I once
admired their company spirit and such, but after multiple, objective
indications of how stupid their company is I have to stop. Their
engineer team is full of absolute buffoons with almost zero experience
who chose to blog about just how stupid and inexperienced they are
regarding their idiotic choice to pick Go in the first place and then
bash on it while deciding to switch to Rust, and then later chase
Erlang. I don't want any of my people anywhere near that catastrophe of
a company.

## Wednesday, August 5, 2020, 8:31:53AM EDT [1596630713]

Been reading a lot about running for those over 50 lately. A lot of
great insights from other runners [in the comments of this
page](https://trainright.com/tips-for-aging-runner-ultramarathoner-50-60-70/).
Another
[study](https://www.active.com/health/articles/why-too-much-running-is-bad-for-your-health)
that tracked 52,000 people over 30 years has some *very* interesting
results:

> However, the health benefits of exercise seemed to diminish among
> people who ran more than 20 miles a week, more than six days a week,
> or faster than eight miles an hour. **The sweet spot appears to be
> five to 19 miles per week at a pace of six to seven miles per hour,
> spread throughout three or four sessions per week.** Runners who
> followed these guidelines reaped the greatest health benefits: their
> risk of death dropped by 25 percent, according to results published in
> the journal Medicine & Science in Sports & Exercise.

That worried me a bit at first since I've been doing 10-13 miles a day
for the last few months. Then I read this:

> If you want to work out longer than 60 minutes a day: After the first
> 45 to 60 minutes of vigorous exercise, switch it up by doing yoga,
> strength training, or lighter activity like swimming--and don't race.
>
> Stick to walking or Yoga for one of your regular workouts for one
> extra day each week.

In other words, while trying to lose weight and wanting to keep more
active during the day --- without going overboard --- walking, strength
training, and yoga (my favorites combined with paddle boarding and
adventure cycling) are the key. 

My conclusion is to keep up the four hours a day of >55% heart rate
activity everyday and for three days (Monday, Wednesday, and Friday) go
faster for 60 straight minutes after warming up with a walk for about 15
minutes first. (My walking pace is 16 minutes per mile.) 

I'll be cutting my walks down to two hours (about 7.5 miles) and
sticking to shaded trails so that I don't have to pack as much water
making logistics easier. Then I'll hydrate when I return and immediately
do 60 minutes hour of Yoga, a variation on Ashtanga including "yoga pull
ups" and 12 minutes of svasana (laying on your back). Then I'll do my
regular 10 minutes of trataka (candle gazing meditation) with tones.

One of those days a week I'll add 60 minutes of 8-10 minutes per mile
running and work up to three of those "hard" days a week. These are the
"workout" days. The rest are just normal, every day life as usual.

My life as a developer living and working from home is *very* sedentary.
This is why I think three hours of walking or low effort cardio is no
where *near* over-training. It's just normal human activity that my body
is *expecting* me to do daily. Keeping the pace slow means that I can
get a recording device and take notes, write, and such while on my
two-hour daily walk/hikes.


## Tuesday, August 18, 2020, 8:22:49PM EDT [1597796569]

I am so tired of `else` statements. In fact, when I see people using
them you can almost be sure they are junior programmers, but not always.
One of the things I love most about Go is that most of the standard
community libraries shun `else` and `else if` like the plague. I can
honestly say that in five years of Go programming I have never needed an
`else if` --- not even once. I have used `else` on *very* rare occasion.

I actually just ran across something similar to this in advice on the
computer science stack exchange: [*Why* do people actually read that
shit?]

```
go if blah { return "something" } else { return "something else" }
```

This is completely stupid and forces the compiler to work unnecessarily
hard. I really love how triggered something as stupidly trivial like
this makes Rob Pike (my hero). Obviously the *right* way to code the
above is like this:

```go
if blah { return "something" } return "something else"
```

Why do so many lesser programmers have an issue with this? It is so much
easier and cleaner and avoids unnecessarily nesting keeping the code
left-justified as much as possible.

The thing that triggers me the most is what the first represents in
terms of code design think. It discounts that there is one best/default
path through the code, one *blue sky* scenario, and all the ifs are
exceptions to that. Here's another comparison in Python:

```python import sys

if len(sys.argv) >= 2 and (sys.argv[1] == "Rob" or sys.argv[1] ==
"Simon"):
   print(f"Woah {sys.argv[1]} you rock.") elif len(sys.argv) >= 2
and (sys.argv[1] == "Dork"): print(f"Um, no need to be rude.") elif
len(sys.argv) >= 2: print(f"Hi {sys.argv[1]}") else: print("Hi there.")
```

And as God intended:

```python import sys

if len(sys.argv) <2: print("Hi there.") exit()

if sys.argv[1] == "Rob" or sys.argv[1] == "Simon": print(f"Woah
{sys.argv[1]} you rock.") exit()

if sys.argv[1] == "Dude": print(f"Um, no need to be rude.") exit()

print(f"Hi {sys.argv[1]}")
```

By the way, the single biggest evidence that the Python language
designers have always had their heads up their asses is the absence of a
`switch` statement after 20+ years of Python (and of course significant
white-space). We got fucking f-strings before we got a switch statement.
The reason is obvious and the same reason multi-line anonymous functions
still don't exist. White-space fucked them. Read the archived emails. It
completely justifies that statement.

## Tuesday, August 18, 2020, 7:35:30PM EDT [1597793730]

I'm reminded of how successful the challenge pedagogical approach I've
been using and tweaking for years has been received by learners of all
ages. I do wonder if there is any formal academic science on my method.
I can say it has been following the scientific method of discovery and
revision even though any measurable metric has been the success and
deliverables of those learning and not some other formal measure. 

The method goes like this:

1. Identify the core concepts and skills.

1. Create challenges that combine the concepts and skills with very
specific requirements in bullet form that can be tested with or without
automation and understood by someone who is non-technical. They won't
know it, but these are akin to 
[user stories](https://duck.com/lite?kae=t&q=user stories) then will encounter
on the job.

1. Keep the challenges small, memorable, entertaining, and even silly so
they produce immediate dopamine responses promoting learning and
unstressed confidence and can be repeated as with exercises (and not so
much with larger projects, which are an important pairing as well).
Repetition makes humans feel safe which is why we obsess about it in
early childhood.
   
1. Provide helpful hints on how to discover useful information about how
to solve the challenges without any specific source in mind. While a
preferred text is fine, consider listing several sources --- even those
with contradictory approaches --- to promote critical thinking.

1. Outline the challenges in way that *generally* builds and reiterates
previous skills through repetition so the learner gains experience and
strength along the way.

1. Don't teach. Let the learner teach themself. Oversee the learning by
clarifying the requirements and tweak them as needed through a
sustainable challenge versioning system. This way the learner gains the
confidence not only in the material but their autodidactic ability to
successfully research, log, and learn on their own.

1. After a learner completes a challenge test the learner by having them
walk you through how to complete the challenge without looking at their
notes as much as possible. Being able to teach someone else how to do it
is the best measure of mastery. Use the opportunity for discussion and
clarification.

1. Have the learner store the completed challenges and notes they took
along the way to accomplish it in their own personal learning logs and
codebook repos for reference later.

This *challenges and projects* method models learning in the real world
and prioritizes mastery of one's own learning skills during the process.

## Tuesday, August 18, 2020, 7:30:53PM EDT [1597793453]

Looks like we don't really have to worry until the house sells. So we
are just packing up and getting ready to move quickly when the time
comes. It sucks because it deflates a lot of Doris's creativity and
depresses us because the wonderful yard she has created is just going to
rot but it is better than living every day as if we might have to move
out within the next seven days.


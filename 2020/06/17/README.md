## Wednesday, June 17, 2020, 5:17:41PM EDT [1592428661]

The CTF games <https://overthewire.org> and <https://picoctf.com> have
reminded me overwhelmingly that the secret to having fun learning is
gamification. I've always done it, but I sometimes move away from it a
bit as I get all teacher-y and start explaining stuff.

Well I'm here to report that returning to challenge-based learning is a
*massive* success. Every private mentored session starts with me giving
a challenge in terms of the specific outcome and not telling the person
*anything* about how to accomplish the challenge, only the key terms and
words they need to understand and research on their own to do it. The
reaction has been *overwhelming* --- so much that I really need to add a
point system to the whole thing eventually so people can have me check
them out and give them the points somehow, if not just encourage them to
keep track of them all somehow.

There are *so* many things that need to go into this new knowledge app.
I have to keep at it.

## Wednesday, June 17, 2020, 4:16:32PM EDT [1592424992]

After doing a few small challenge projects in Rust I'm finding how much
I *really* love Rust, not for the syntax, but for the absolute freedom
and seriously low-level of the language. It is *far* easier to integrate
C and C++ code with Rust than Go, and safer to do so. There are number
of other things bumping around in my head that are really annoying me
more than I care to admit about Go:

* **Go is unsafe by default.** You can relatively easily right broken,
unsafe concurrent Go code and likely won't even realize you are doing
so.

* **Go contexts are horrible.** I hate them. They are poorly conceived
and implemented. They feel so hack-ish to me.

* **Generics are being crammed in.** People are arguing about the
`generic(some)` syntax vs `generic<some>` and I have to admit the
contrarian position of avoiding the syntax for generics that has existed
forever in other languages is just plain stupid and annoying.

* **Go has OOP inheritance stink on it.** I actually read something
about the "diamond patterns" that can happen with "embedding" (code for
inheriting) other structures. It should surprise me since there was a
Java guy on the original design team for Go (who recently left). Rust
has more functional influence and smells a lot more like Haskell, which
is *so* much better.

* **Pike and original creators seem no longer engaged.** They rarely are
involved in the mailing list and having any direct input to the Go
project. It really feels like they are letting in languish and the
design decisions are much less informed of late. People on the list
reported problems with 1.14 but it got released anyway.

* **Brian Cantrill likes Rust, not Go.** I know this is a small thing
but I *really* respect his level of knowledge about languages and if he
has a problem with Go then I really have a problem as well.

* **Rust is industries ["best
chance"](https://thenewstack.io/microsoft-rust-is-the-industrys-best-chance-at-safe-systems-programming/)
for safe programming.** That's a pretty big statement from Microsoft of
all companies. If there is one thing the world needs, it is *less*
insecure code. That is almost entirely reason enough to get behind Rust
*no matter what*. The rise in cybersecurity needs will only get worse
and Rust is the safest systems development language on the planet, bar
none ('cept maybe Ada someone said) .

## Wednesday, June 17, 2020, 9:13:35AM EDT [1592399615]

I've turned on syntax highlighting by default in `kn` because the blank
line fix addresses it. This will result in substantially larger
knowledge base renders than with it turned off but will allow people to
provide their own loadable syntax highlighting. It is just a matter of
time before the default knowledge base template contains the JavaScript
to tap and pick from a number of different syntax highlight options that
the *reader* can set based on their preference. I cannot wait, actually,
that is something I have been wanting to do ever since I set all the
standard colors of the rendered Web version as CSS variables that can
very easily be changed and stored in the browser or even downloaded as a
JSON file.

As much as I want to do other things eventually, this work on `kn` and
the `README.world` is *so* important that it *must* take priority. When
fully realized the world will have an easy way to capture, maintain,
share, and consume knowledge according to the preferences of the
*reader*. Taken to the n-th degree this could become the foundation for
all knowledge, even proprietary knowledge that needs to be sold. I have
not encountered any other solution to this problem that incorporates so
much of what is already best practices.

By the way, I cannot wait to integrate OpenPGP signatures as well. Every
time I see a star by someone's name in Twitter indicating that Twitter
has graciously decided to confirm for the world that a person is who
they say they are I feel a little kick in the butt to get signing
working. This is a problem that already has a solution --- that no one
actually uses because they *think* it is too hard.

## Wednesday, June 17, 2020, 8:30:42AM EDT [1592397042]

I'm super annoyed that Firefox decided to actually make whitespace a
node that screws up pre-formatted blocks. There is simply no way around
it without a horrible JavaScript fix that does not work for text-based
browsing. 

I did find a fix for Markdown documents that I hate but will have to
start following. Always put the fence posts in a code fence on their own
lines and deal with the extra blank lines always at the beginning and
ending, which is easy enough through some style changes.

This goes for Pandoc div fences as well:

~~~markdown

Do this:

```js


console.log('hello')


```

And this:

:::co-pwz

No seriously.

:::

~~~

That makes it more readable and searchable anyway so I'm fine with that
convention --- especially since it gets entirely out of the way when
doing optional syntax highlighting.

## Wednesday, June 17, 2020, 7:59:27AM EDT [1592395167]

Even though Linus even came out and said 80 characters is too limiting
for line lengths today, and the fact that I have been pushing for
one-big-long-line paragraphs in Markdown paragraphs to play better with
panes that might be less than 80 characters I have adopted a 72 maximum
line width convention for my own YAML knowledge base data, including the
`Summary` and paragraph forms of data.

Here's the thing. Once you sign off on putting your data into YAML
instead of Markdown you are accepting that white space matters ---
particularly initial white space since it is a fundamental of YAML
syntax, structure and readability. Such is not that case with Markdown.
Having a super long text value wrap and break up the clean whitespace
lines to the left is simply so ugly and hard to process that I couldn't
take it. 

Luckily Vim and other editors will automatically do this whitespace
indentation for you. And since Python is still so popular with people in
the world they will be fine with it.

This works particularly well for a new knowledge node format I've called
`ParaList` which has a distinct topical sentence `T` and a paragraph
body `P`. I can see if the topical sentence is getting to long just by
seeing if it wraps. 

```yaml
---
Title:    Don't Be a Lazy Learner
Subtitle: Identifying an Anti-Autodidact
Quote:    This is all just too much talking. Query: true
Type:     ParaList

Summary: |
  Sometimes understanding how to become one thing means first
  understanding what that thing is *not*. Here's a list of
  characteristics and behaviors you will find in an *anti*-autodidact, a
  lazy learner who would rather make excuses than do the real work to
  learn on their own.

ParaList:

- T: They are bored and confused by words in general.
  P: The more words, the more they check out, spoken or written. Most
     have a ridiculously low vocabulary and don't ever let on how many of
     the words they don't understand in any given conversation. 

- T: They don't have the capacity or motivation to figure things out.
  P: They say shit like, "I don't get it" or "It's not working" or "I
     did what you said" or "The stupid computer won't..." or "What is
     happening?" They ask a lot of questions during movies.

- T: They want to be in the same space with people who *do* learn. 
  P: They are uncomfortable working from home. They wander into your
     cubical at work a lot. The feel safer in your presence because they
     don't on their own. They feel they need you close to learn, even on
     their own.
---

```

Typically such format constructs will have the topical sentence be first
and all bold while still remaining a part of the paragraph.

## Wednesday, June 17, 2020, 7:29:45AM EDT [1592393385]

YAML is the API of knowledge. I don't think I fully recognized the
genius that is behind the *full* and much derided version of YAML until
I started thinking of *all* my knowledge in terms that would fit into
one of a few self-made knowledge organization types. Turns out there are
only a few constructs we use to capture our knowledge and all of them
can be easily categorized as knowledge format types. I've been building
out the list made a few blog posts back and as I've been converting my
[RWX.GG]{.spy} knowledge base over I've been *loving* it in ways I'm
quite sure very few others will appreciate. Doesn't matter. I know Aaron
Swartz would approve. His is the only opinion I would work to win over.

One dilemma I am having, however, is how much to dismiss the idea that
all knowledge should be able to be written by *anyone*. I still maintain
that Pandoc Basic Markdown is the world's most universal and simple
format for knowledge without losing sustainability. But putting more of
my knowledge into the YAML section instead of the Markdown section could
be see as a move *away* from easy to attain technologies.

Basic YAML is *so* easy to learn and maintain and read that I feel like
this move is consistent with my primary goal of knowledge format
simplicity. If anything it might help people categorize their knowledge
as they capture it by pre-meditatively working from a few common
organizational formats that don't have anything to do with a heavy
syntax such as HTML --- or worse -- XML or the semantic web
specification.

One thing is for sure. Even if I do move my knowledge formats into a
form that requires learning YAML as well as Markdown and it puts it out
of reach from someone who just knows basic Markdown I feel I need to do
it anyway for much the same reason that a Mathematician would use LaTeX
within Pandoc to describe their knowledge. Some knowledge must be more
structured than simply a whole bunch of Markdown.

## Wednesday, June 17, 2020, 6:54:41AM EDT [1592391281]

Yesterday I had a lazy learner during the live session say, "This is
just all talk". The topic was "Get Linux" which requires an *enormous*
amount of discussion to get right. I made a big deal explaining how
important it is to assess the needs of the person to whom you are
recommending a Linux distro before just blurting out, "Manjaro is the
best!" 

People who make recommendations without considering the needs of the
people they are recommending too are irresponsible egomaniacs motivated
by something other than the welfare of those they claim to be helping.

Lazy learners have a few things in common:

* They are bored and confused by words in general. The more words, the
more they check out, spoken or written. Most have a ridiculously low
vocabulary and don't ever let on how many of the words they don't
understand in any given conversation.

* They say shit like, "I don't get it" or "It's not working" or "I did
what you said" or "The stupid computer won't..." because, in fact, they
don't have the capacity or motivation to even try a little to figure out
what is happening. 

* They generally want to be in the same space with you. They are
uncomfortable working from home. They wander into your cubical at work a
lot. The feel safer in your presence because they don't on their own.
They feel they need you close to learn, even on their own.

* They love mythology and Marvel movies. They don't have to think. The
don't even have to imagine. There are fewer words to confuse them. They
just plugin and go for a ride. This is also why they hate reading,
role-play, and sandbox video games.

* They are prone to religion and tutorials, which in many ways are the
same thing, a recipe for how to do something step-by-step without having
to think about *why* you are doing something. Just do what some says and
you'll have your app or your key to Heaven. It's the same appeal.
Working out how to make your own app or discovering modern ethical
behavior are hard, too hard for a lazy learner. They want to be told
what to do.

* They ask lazy questions like, "Which distro do you use?" or "Which
window manager is best?" or "What certificate do I need?" or "What
college should I go to?" Again, they would rather have a recipe than
analyze anything at all.

* They tend to be cheaters because they don't value learning at all.
They are more focused on what they can *get* than what they can learn.
They would hate Kant's categorical imperative if they even knew what
that meant.

* They generally lack self-awareness and avoid introspection with
distraction and urgency addiction. When you ask them what they want to
do with their lives --- or even the current day --- they struggle to
answer. Asking them what they are good at usually results in long
pauses.

* They are either super depressed or overwhelmingly over confident.

## Wednesday, June 17, 2020, 6:38:53AM EDT [1592390333]

While helping people during private mentoring I'm becoming more aware of
just how difficult it is to get a handle on one's own knowledge
management. In fact, I'm now convinced it just might be the single
biggest thing blocking people from doing their own learning, from
becoming a *true* autodidact. Without being able to *write down* what it
is that you are learning and learn from your own written self
assessments that you can search for later you just cannot learn
effectively. In lay terms, you cannot learn without taking good notes
--- especially if your notes are also your main text book.

This is a bit frustrating because the number of people who simply don't
even know how to form a sentence --- let along type it quickly and
coherently into a codebook --- is far too high. I think this was part of
the reason I was so frustrated later. I realized that my formula for
learning might simply not be as universal as I'd hoped because of this
*major* prerequisite. If you cannot read, write, and type you cannot
become an effective autodidact --- let alone create your own exercises
and execute your own activities and self-assessment. Learning to learn
is actually way harder than I have thought it to be, but like so many
things, because I surround myself with those who have already learned it
on their own I've had the impression that its not difficult at all.
Having them around me has confirmed a false bias and conclusion that
learning is easy, that it is innate, that it does not have to be taught.
It does.

In short, I need to have a boost for each of the RWX elements, reading,
writing, and executing. I also probably have to have one for basic
computer algebra.


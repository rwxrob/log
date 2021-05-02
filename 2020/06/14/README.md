## Sunday, June 14, 2020, 1:21:44PM EDT [1592155304]

Everyone knows how much I love Go. But something interesting has been
happening since fully adopting Bash concurrency and learning a bit of
Rust. Rust and Bash are squeezing out my personal need for Go. 

Let me explain.

In the old days you had shell and C. That was it. C was even called a
"high-level" language by Kernighan at the time. Today I'm finding the
equivalent to be Bash and Rust. Go replaces Python. But the space
occupied by Python is also becoming smaller, at least for me.

I'm not doing a lot of cross-platform general purpose and machine
learning programming. I'm not even doing a lot of terminal UI program
development or back-end web services development. These are Go's sweet
spots.

Bash has *completely* taken over almost everything I would ever need for
Python and Perl (and I never did use Node, thank God). In fact, now that
I am more fluent with `coproc` and `&` for backgrounding processes
efficiently Bash has taken over a *large* part of what I would grab Go
for before.

I also have been realizing just how bad Go is for beginners *when
specifically learning concurrency*. I used to think Go was great for
beginners because of its simplicity. But that is exactly why it is
dangerous. Go does not protect beginners in any way from writing unsafe,
concurrent code. In fact, it is even *more* likely because it is so easy
to write for beginners to write concurrent code with goroutines.
Beginners never learn the safeties built into the compiler to check for
race conditions and such. It is *never* covered in any material --- if
you can even find *any* up to date material at all. That's bad.

Meanwhile, despite the complexity of Rust for concurrency and general
syntax that I've been railing on because it is *so* hard for beginners
to get their heads around, when a beginner finally does learn
concurrency in Rust they get safety automatically. They have to forcibly
break the safeties of concurrency already in place. In fact, Rust is a
much safer language all around to learn, *far* more safe than Go even
though Rust syntax is *wildly* more complex than Go's.

Rust clearly replaces C and C++ for Unix philosophy compliant commands.
Rust is a *very* good candidate to rewrite all the old busted boomer GNU
code. Go isn't. In fact, it is a [wish](/wishes/) of mine that someone
would write a 100% compatible Bash shell clone under a permissive
license in Rust.

Then there's the what-would-I-require approach. 

What if I had to run a company and my very life depended on the team I
hire to be able to produce *safe*, robust code quickly that would remain
completely sustainable over time? Would I want to hire a bunch of Go
programmers who possibly came from the Node and Python community? Or
would I want the 10x developers who *understand* Rust and why it is so
significant, like Brian Cantrill. 

Picking Rust means rather than having to vet a potential Go programmer
by asking all kinds of questions about compiling with the profiler and
race condition checks I can simply ask to see an example of a
candidate's concurrent Rust code instead. It is *much* harder to
identify a Go programmer experienced with safe concurrent programming
than a Rust programmer of equal skill. 

Clearly if my life depended on it I would want Rust developers over
*all* of the others even if I had to spend 10x the effort to find them.
If I made a bad hire I'd still happy with the fact that it is nearly
impossible to write unsafe code in Rust. In other words, Rust covers me
on two fronts: (a) only really well informed and naturally good
programmers even learn Rust, and (b) beginning Rust programmer are
*more* likely to produce good, strong code that will stand the test of
time.

No wonder it seems like all the good Rust developer jobs are in Germany.

Rust makes it easier to filter out those who just aren't safe
programmers. If my life and company depended on it, the *value
proposition* of the Rust language is much more compelling. It just
depends on if Rust truly delivers on the promise of *safe* concurrency.
That's where I need to focus my research.

What I'm saying, I think, is that even though I've barely coded anything
of any significance in Rust I now see why the counter-intuitive notion
that Rust is better for beginners *despite* its complexity might, in
fact, be objectively true. This compels me to fully master Rust by
writing a few very significant projects in it --- specially things that
benefit from Rust's strengths: small run-time, no garbage collection,
memory safety, PEG <https://pest.rs> library, and raw speed.

Therefore, my plan is to entirely complete and grow `kn` into the
primary utility and keep it in Bash. Then I will supplement it modularly
by providing additional commands such as a `Pandoc Light Parser` in Rust
can be be used independently in the Unix philosophy integrated *into*
`kn` through regular command calls, just like I do with `pandoc` now.

## Sunday, June 14, 2020, 1:01:33PM EDT [1592154093]

Here are my needs when it comes my most common needs for tools and
languages:

1. Stuff to help me automate and simplify life on the command line
1. Stuff to create highly efficient, Unix-philosophy compiled commands
1. Stuff to make front-end web sites and apps
1. Stuff to make back-end web services

I imagine myself looking into the toolbox when I'm about to work on
something. 

* If I need to duck-tape a bunch of stuff together to make something
that just works I grab Bash.
* If I need to create a highly optimized command that can be duct-taped
I use Go, Rust or C.
* If I need a front-end web site or app I grab Markdown, HTML, CSS,
JavaScript, Pandoc, and Vue.
* If I need a back-end service I grab Docker, Go, Rust, Nginx, GraphQL,
PostgreSQL.

When it comes to getting shit done there is nothing faster than Bash. I
have objectively demonstrated that to myself over and over again. The
`twitch` tool, [[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[my `kn` utility](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn)](https://gitlab.com/rwxrob/kn), and my `repo` GitHub *and* GitLab tools
have been in Bash and will *never* be rewritten in any other language.
There just is no need. Now that I've discovered `coproc` and started
using `&` to background processes more I simply do not need a
complicated strictly typed language to achieve maximum concurrency as
fast as possible --- both in terms of execution *and* development speed.

## Sunday, June 14, 2020, 12:45:17PM EDT [1592153117]

So I have to admit Rust syntax and style is really bork, but I'm
definitely okay with it. It did cause me to reconsider my fetish for
2-space tabs that I took to some two years back after doing a lot of
JavaScript development. Now [Linus Torvaldz and everyone else agrees 80
characters is too limiting given modern terminal
widths](https://duck.com/lite?kae=t&q=Linus Torvaldz and everyone else
agrees 80 characters is too limiting given modern terminal widths) all
the arguments for 2-spaces really fall apart --- especially since four
spaces has been the standard for most languages for more than two
decades. It is one of the few things that Python, PHP, Perl and shell
coders generally all agree on. Plus it is just so much more readable ---
especially when disabling syntax highlighting of any kind.

So I have been slowly but surely changing all my code and writing to
include the new 4-space standard. It's amazing how much something so
seemingly trivial can produce *so* much work. 

I feel like I just can't get my feet under me lately with so much going
on. When I do run into old stuff, like my first knowledge base back in
2013 I realize how much progress I have made. The Knowledge Management
Utility (`kn`) that I have been working with during all of this is *so*
ideal because it just gets so much done so quickly. There is seriously
nothing faster than prototyping in Bash. Bash *blows away* my best
productivity with Python, Perl, Go and any other language I've used in
the past. 

It is really such a shame that more people *don't understand this fact*
because they haven't been exposed to it. But I'm doing everything in my
power to change that and shoot our collective productivity forward for
those with the good sense to truly consider and understand why. Just
like any age, most people will continue to simply no understand, but it
warms my heart to encounter someone line
[\@gamozo](https://twitch.tv/gamozo) and be like, "Woah, this dude
*knows* what I'm talking about." 

In fact, I find that people in the pentesting and security field almost
automatically understand where I'm coming from. That is enough
consolation for me since the %37 annual increase in demand for the
fastest tech career in the world is specifically full of those people.
We are all just hackers at heart even if we are doing the tools
engineering and not the pentesting. All the other Java and C++
developers can just play with their toys and leave us alone. I won't say
it is a cliche, but its a cliche. You either get it and are one of the
cool kids or you don't and frankly don't belong. No need to be mean,
just realistic. A *lot* of people just don't have what it takes to truly
master the terminal including Bash scripting an prototyping. Most don't
have the commitment and ability to even master touch typing, let alone
terminal skills. The world will always be filled with such people. They
aren't *bad* people or *stupid* people. They are just not hacker
material and never will be. The end. 

## Sunday, June 14, 2020, 10:44:55AM EDT [1592145895]

Today I opened up my Basic Markdown video to find a "dislike" for no
apparent reason. Humanity has invented very few things as fucking stupid
as "likes" and "dislikes". The Black Mirror episode about it doesn't
even come close to capturing it.

Someone can be a complete fucking moron and simply dislike something
voting it down. Then another dumb ass can upvote something else. *You
have no idea about the spineless cowards who refuse to take two minute
to justify their position.* 

The *only* reason like and dislikes exist is so that the service
providing them can suck in more shallow participants, ad revenue, and
money. In other words, once again marketing and ad revenue are
*destroying* authenticity and intelligent dialog.


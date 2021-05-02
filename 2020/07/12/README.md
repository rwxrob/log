## Sunday, July 12, 2020, 5:01:04PM EDT [1594587664]

Nothing like getting something great down on "paper" to motivate me to
do everything else to make it a reality. 

I love where the design of Knowledge Nodes is going --- particularly the
dynamic Node types that will ultimately display word maps by usage,
dependency trees, 2nd and 3rd level subscription recommendations, and
even some machine learning common usage patterns. 

The idea that I will be able to *visually* display my entire RWX
Knowledge Network out to two or three levels is so absolutely awesome
that I want to make it *today*! 

It is so hard to describe to people (including my wife) but when they
*finally* see this in action --- especially after we get a few hundred
people on the RWX Knowledge Net --- no one will even really want to use
Google again. Why use Google when I can search *all* the content from
everyone in my *customized knowledge network* instantly and locally? 

You won't even need a fucking web browser! Graphical knowledge net
browsers can run *entirely* on SSH connections and fallback to HTTPS
because they don't even need to access the Internet that much, only to
check in. *This* was the vision of RSS that never really came to pass. 

Seriously, this has very real potential to change the world in ways I
have always wanted. I hope Aaron would be proud. May this whole effort
succeed, for him.

## Sunday, July 12, 2020, 8:58:51AM EDT [1594558731]

What was I thinking? Just use `pandoc` you idiot! (That's me shouting at
me.) Even if did manage to create a PEG Golang parser (which I really
*want* to do because it would be fun) it makes no practical sense when
an entire project of brilliant people are supporting Pandoc *every day*.

So what if `pandoc` is a subprocess every time I call it. That's nothing
these days. Will speed rival Hugo? No, but it won't be as brain-dead as
Hugo either. Hugo was made by engineers, not academic and scientific
writers. That is why Pandoc has such a strong LaTeX influence and why R
make Pandoc its official documentation language.

If and when I hit a performance issue there are plenty of other ways to
address them:

* Create a daemon that automatically builds anything when changed. I
need this anyway to preview the rendering in pseudo-real-time.
* Cache AST parsing and word crunching so that it just has to be
recombined in a `make` like way.

Plus if I make this all about Pandoc I might even get some buy-in from
the Pandoc community itself, since Knowledge Net will be fundamentally
dependent on it. But hey, the WorldWideWeb was created by academics to
share information so why not?


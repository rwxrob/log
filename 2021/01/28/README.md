## Thursday, January 28, 2021, 9:07:53PM EST <1611886073>

Reminded today how little popularity really matters to me, obviously. I
don't stream to be popular. I stream to help and make social connections
with people who actually get and appreciate my stupid humor and rants.

Ran across someone today on Twitter who has a book, lots of speaking
engagements, and a fancy avatar but was one of the authors who wrote the
shitty code that actually got published that I had to fix in my version
of it after having read the book and being, "wait, what?"

I know this is just me stroking my own ego, but everyone needs a good
stoke sometime. 

And yeah, TJ is right. The more likely you are to hear from someone, the
less likely what they have to say is worth listening to.

I've never been famous nor sought fame really, but I'm a pretty good
communicator, and a communicator's gotta communicate. 

I've also been "blessed" (and cursed) with an overabundance of life
experiences that others find interesting enough to want me to recount.
Must have been part of my deal with the Universe before coming here.

One of the more sucky professional phenomenons I have noticed through
the years as a successful engineer is how much being really fucking good
at what you do can actually prompt others --- who are sometimes more
well known --- to find ways to silence, marginalize, or even attack you
without provocation while also using you as their "pocket" SME. 

I know that sounds like sour grapes (at best) and full-blown paranoia
(at worst). But at this point I have observed it so many times in my
life, and the lives of others, that I am sure it's a thing.

## Thursday, January 28, 2021, 6:36:53PM EST <1611877013>

Learning from Greg that there is a thing called
[LocalStack](https://duck.com/lite?kd=-1&kp=-1&q=LocalStack) technology
that uses containerd tech in order to emulate Amazon cloud services
locally for local development, including the AWS CLI and Cloud Formation
templates.

Obviously, the benefit for developers is amazing but for training and
education is also amazing. You wouldn't run this in production, but for
testing everything *before* you deploy.

## Thursday, January 28, 2021, 10:41:15AM EST <1611848475>

Realized that `kn` Actions can communicate by setting system environment
variables. If they need more than can call one another and connect their
stdin and stdout.

What's even crazier if that with Bash an Action can actually define and
export a function to be used by other subsequent Actions within that
running process. In other words, this allows first-class functions to be
used and passed between Actions.

## Thursday, January 28, 2021, 8:36:10AM EST <1611840970>

It's really becoming clear how valuable the UNIX philosophy is in all
things. Because of a real need for a "`sed` for JSON" we got `jq` which
standardizes a command-line query language for JSON (that frankly blows
away GraphQL). But when combining that simply solution with a solution
for a larger problem related to a query language for all of the
Knowledge Exchange Grid we can how compose URIs that contain implicit
queries drilling down into the data that we need directly.

I'm also sure of something else. 

We don't need no fucking HTML!

There I said it. HTML was a seriously bad design that has damaged *true*
knowledge exchange from the very beginning, but it was the best we had.
These days simplified Markdown and YAML have become the de facto
standards for knowledge capture and exchange. So fuck HTML! 😍


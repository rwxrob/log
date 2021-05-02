## Friday, November 20, 2020, 11:37:32PM EST <1605933452>

I'm going to spend my Friday night playing with symmetric cipher
encryption and the combining of all `auth` configuration data into a
single file. The more I get to thinking about all this caching stuff the
more it makes sense to just do it right and make sure nothing ever touch
disk unencrypted. I'll at least write the code for doing the encryption
and combine all the data into a single file.

I'm glad this occurred to me the other night with someone on the stream
from the hacker industry. He really brought home my original concern
about creating something --- everything --- in zero-trust environment
and how important that is today. It's the same way I approached the
infrastructure I helped build out for IBM that managed compliance
auditing on thousands of systems. I used GPG for all that so that
nothing hit disk that wasn't encrypted. Like anything, it could be
hacked with enough focus, but this was a *serious* inconvenience instead
of leaving everything on disk in the clear.

So yeah, I've never been a fan of writing anything in the clear to disk,
not even secure shell keys, which is one of the amazing things about
KeePassXC because of its `ssh-agent` integration I can have the
convenience of a public key without a passphrase because the application
must be running in order use any of the key pairs even without a
passphrase.

Everything that will use the `auth` package I'm writing will ultimately
be the same sort of thing. It also means that for applications that are
going to be making regular API calls will need a daemon that I can
interact with from the command line. The running service will only need
the passphrase once to start enough to decrypt the data store and then
from there stuff can live in memory, then I can dump the decryption key
from memory. That's the best I can do. If a hacker gets access to
memory, and pull stuff out of it, there's nothing that can save you at
that point.

There is another option I want to research a bit tonight. I need to see
what level FIDO U2F I might have in my YubiKey and just use that. That
would allow there to be three different levels of encoding and security,
flat (base64), symmetric encryption with a passphrase, and YubiKey with
encryption. These are the same (almost) as KeePassXC. 







## Friday, November 20, 2020, 5:50:25PM EST <1605912625>

This week I learned that one person I helped for several years started
their first tech job for \$100,000.

But, in stark contrast, another former member who left on their own (and
is now banned for lots of reasons) sought me out after being away for
more than two months.

Why?

To share with me their demented versions of what I wrote in confidence
to their parents to try and get him some help as they chose to leave.

This entire story is why I'm leaving mentoring as a main income. It's
also why I have had application interviews for more than two years. 

This person got in without any evaluation back in the day when they were
just referred by another member. Had I evaluated them, there is *no
fucking way* I ever would have let them in, mostly because of the
horrible parental dynamic. One of the parents is a particularly abusive
asshole.

This child does have serious learning disabilities. They are completely
obvious to any educator, which is abundantly obvious from the stories
over the years that this child shared with me about their "horrible"
public school teachers. The child was constantly blaming the teachers
for everything and sharing with me about it in our sessions. They were
clearly parroting the words and tones and attitudes of the parents they
chose to model. I would nod and try to get past it, but it ripped me up.

This family lives in the epitome of denial and entitlement. I should
have removed them much earlier, but I felt since they were here already
I needed to stick it out --- turning away other applicants --- as best I
could, which always fucks me over in the end, mostly because shit-heads
like this family always find a way to associate some fictitious greed on
my part. 

Anyone who knows me knows how fucking stupid it is to even insinuate I'm
out for the money. I've been offered jobs for \$250,000 from executive
consultants for Christ's sake. I *hate* when people hit me with that as
if to say:

"Why didn't you take it? You are stupid for not taking it. What's wrong
with you! You're obviously lying."

That is *exactly* how these fuck-faces project their own values on me to
deal with their own cognitive dissonance. I *could* pull out the actual
email and show them, but I don't. Instead, I figure out how I can get
these people out of my life as fast as possible, with the least amount
of communication as possible, so it doesn't affect other areas
areas of my life, including the amazing people I've helped, and am
continuing to help who just *get* it.

Suffice it to say, this parent is one of the most abusive, abrasive,
uncaring, disconnected, clueless parents I have ever had to work with
(but not abusive like one other one who has scarred me for life watching
how they dealt with their child). The entire tone of "You have some
*explaining* to do" was just seething with rage that didn't seek to truly
understand *why* their "loved" one was having trouble and how they could
seek further help. It wasn't one to apologize for being late *for every
fucking payment* even though they clearly had the money.

These *few* parents are the very reason I have such high standards for
admission into my community now, and sadly, they are the reason I'm
leaving main mentoring. I can do so much more for the world than deal
with even the risk of this shit. No wonder so many public and private
school teachers leave the profession within five years. 

First of all, I've never even fucking met this parent at all. Not even
spoken to them on the phone. Not a single fucking email. They just
didn't feel the need. They are absolutely, completely and totally absent
in their child's affairs including my mentoring community. 

After they left for reasons related to money and boredom, a word this
child would use for lack of any internal motivation to learn *anything*
asking to "just play Minecraft" and worse. I would do my best to walk
through every line of code they could, but they would complain
the whole time, *unlike every other member of my current learning community.*

So as they are leaving I shared *in confidence* my observations to help
them find help for someone with an obviously serious learning
disability. Rather than respond positively to what I wrote they torn
into me with, "You had better explain yourself" at which point it was
*completely* obvious that these completely disconnect parents had no
intention of doing *anything* substantial for their child, nor having
anything close to a productive conversation. So I didn't.

The parent started harassing me by phone messages and email, which I
just ignored. I had people to help. I wasn't giving this shit-bag a
second of my time. They had stolen an opportunity for another to be in
my community over the years. I have turned away about a dozen during
that time because I was full. But no. I'm the one *stealing* their money
and time.

Several months past. The harassment stopped, or so I thought.

Then, completely randomly, the child found me on Discord and shared their
interpretation of their parents' interpretation of what I had shared in
confidence.

> Why did you say mean things to my mom when I left? It's not like we
> didn't give you thousands of dollars just for you to say "he needs too
> much help" and not teach me anything else besides stupid codecombat.

There are so many things wrong with that I cannot cover them all without
giving away the identity. 

First of all, they *begged* to play CodeCombat instead of learning to
code from the terminal and to get this person to do *anything* was so
hard. I walked them through every CodeCombat session and encouraged them
to solve their own problems by helping them ask their own questions.
CodeCombat was the *only* thing *they* wanted to do besides fuck around
in Minecraft and do typing tests all day. But no, I wasn't "teaching"
them. 

*Teach* is a fucking horrible transitive verb. No one teaches anyone.
There are only learners and those helping them learn. Friere makes that
point abundantly clear even if the entire fucking educational universe
just doesn't get it.

The first words on most sessions with this person were "sigh" and when I
asked what was wrong they would say, "I just don't feel like coding. I'm
kinda bored" or "just my school sucks because..."  They hadn't done any
coding over the week or sought any of their own projects. Let's just say
that I have *zero* patience for anyone who claims to be bored today,
child or adult.

I *tried* to be understanding and patient. I really did. After all, this
person --- like so many others --- is a casualty of a system that forces
Friere's notion of "banker education" on unsuspecting victims. They
think they are "passive receptacles" to receive the wisdom and knowledge
only the *teacher* is allowed to learn and then regurgitate.

All I could do was disengage. It always hurts to do that, but there is
just no hope for that family and their approach to *everything* about
their family dynamics. I can't *fix* them and it is not my job to do so.

So I said this instead:

> Yeah that is not at all what I said, nor is any of it true, but I
> don't expect you to ever understand that, nor your parents. I wish you
> well, just not in my community.

Sure I wanted to ask how he even came to know about that *confidential*
email to his parents about sensitive issues I would never bring up in
front of him, but no. I just stopped.

One of the parents claims to be a successful self-help author, which
just makes it entirely comically sad. If I said the name some of those
reading might even know this person. It is a *fucking joke* that this
human being has a book of any kind on the topic. One thing that became
overwhelmingly clear was that this person has no *fucking* clue what is
going on with their child. Hell, I had to *convince* them that their
child needed *a fucking computer* after not getting one for over two
years. They *clearly* had the money. They just didn't want to spend it
on their child's critical learning. 

The worst part is that this asshole has no *real* intention of ever
finding out what is *really* going on with their child, that much was
also clear. They just fight to maintain their cognitive dissonance about
the situation to make themselves able to go on television and make
outrageously false claims with a calm hubris that --- to me --- is just
downright demonic. 

If you suck as a parent (like I often do) *just fucking own your
failure* instead of doubling down on how awesome you are so you can sell
your fucking book. Who are you, Trump? Oh right, they probably *did*
vote for him. They are the type. *This* is how society is failing, and
most don't even see it, mostly because they just can't or won't. We live
in a age of the worst kind of denial, and we might not survive it. 

Did I mention this family *always* paid one or two weeks late, after the
next block started. Tried to get away with being the *only* people
without a computer at home for their child. Tried to be the only people
to pay as late as possible. Tried to get away with whatever the fuck.
This mentality is *killing* humanity. In fact, I had to start a policy
about early payment just to cater to lowest common denominator people
like this. Zero respect for others. Zero shits to give about anyone but
themselves. In Trump's words about scamming people out of money he owed
them through frivolous lawsuits, "They just don't understand business"
or worse "They're losers, all of them."

So to these parents (and to all the millions of others like them) I just
have one last thing to say:

*You* are the losers and the world is *sick* of you.

## Friday, November 20, 2020, 2:50:27PM EST <1605901827>

Top skills to search for, in order:

1. gRPC
1. GraphQL
1. Websockets
1. REST
1. Oauth2
1. Go programming
1. PostgreSQL
1. Redis

There are a lot of alternatives to these things, but these are the ones
I *want* to work with because they don't suck.

Linux terminal will be a given. A lot will include NodeJS, but I'm only
looking at those if they are migrating off of that horrible piece of
shit.

## Friday, November 20, 2020, 2:46:28PM EST <1605901588>

Just posted that note and *boom* already stuff popping up on it. It
seems like the entire tech Internet is a-buzz with chatter about gRPC
right now. This one was literally [posted
yesterday](https://www.freecodecamp.org/news/grpc-server-side-streaming-with-go/).
The fact something is posted *on freecodecamp.org* about gRPC shows you
what I mean. It is quickly becoming mandatory learning, just like Go in
2014 when I made everyone learn it at [skilstak]{.spy}.

## Friday, November 20, 2020, 2:20:12PM EST <1605900012>

I want to [code Go gRPC applications](https://duck.com/lite?kd=-1&kp=-1&q=code Go gRPC applications).

Had a nice conversation with a recruiter about the *Cloud Platform
Software Developer* position that he reached out to me about. I get
contacted by recruiters frequently, but this one was intriguing mostly
because of how the position was described. It *really* nailed the
collection of skills I'm personally the most interested in (at the
moment). I've written at length about why that title is so significant
to me, and why I think there needs to be a collection of titles that I
keep on hand that frequently mean the same thing. For example, I think
that *Devops Developer* (which is a pretty bad title) and *Cloud
Developer* often contain the same skills, but the problem is that they
almost always involve AWS/Azure/GCP, which I really am not interested
in.

So here's what struck me during that conversation: a way to isolate
*every* potential position as quickly as possible in once sentence.
Here's how it might sound in conversation:

"So what are you looking for in a position?"

"I really just want to write gRPC code in Golang."

There you have it. That one simple sentence adds laser focus to not only
the positions that fit what I want, but to all the tech and skills I
need to prioritize. I just have to ask myself, "How will this help me
write and deploy gRPC application in Go?" to make the decision about how
much of my time to spend on it to prepare for such positions. So, for example,

Me: "Do I need to learn Kubernetes?"

Also me: "Not really, just enough to know how to submit stuff to it,
unless of course you want to use it to manage your own home lab of old
computers you've clustered together just to practice writing gRPC apps,
that you cannot *really* test without a hardware cluster (VMs just don't
feel as nice)."

And another one ...

"Do I need to learn Docker better?"

"Hell, yes, Docker and Git are tools you should have mastered at the
highest level. They are fundamental to *any* modern software
engineering."

And so on. The point is that *everything* hinges off of Go and gRPC, the
end. It saves everyone gobs of time because positions that require
NodeJS --- that do not also involve gRPC as a *primary* skill --- just
won't fit and I can eliminate them from the search. This is a good way
to filter the "Backend Engineer/Developer" positions from the
non-service-provider cloud development positions. 

Another amazing thing this little filter accomplishes is the *size* of
the company. Not many small shops that struggle to pay people and
provide health insurance are going to be deploying gRPC. This tech only
shows itself in larger organizations with a bunch of moving,
microservices parts. So just by saying I'm only interested in gRPC I
automatically eliminate a *ton* of companies that I would not be
interested in helping.

In a similar way, positions that are heavy on gRPC are also more likely
to be building their own internal clouds thereby removing yet another
dependency on a centralized cloud provider bringing diversity and
decentralization to our overall human IT intrastructure, something I
really believe in viscerally at my core. I just can't stomach promoting
more and more dependency on three major cloud providers. It's bad for
humanity. Focusing on gRPC --- particularly with Kubernetes as a
secondary priority --- in my search almost guarantees all the positions
will match this ethical priority of mine, but not always. People still
use `k8s` on centralized cloud providers, but it does really filter a
lot of cloud-dependent companies out of the potential positions pool.

## Friday, November 20, 2020, 2:08:21PM EST <1605899301>

So [\@markamatu](https://twitch.tv/markamatu) from the stream mentioned
something Stephen King has written in [On Writing: A Memoir of the
Craft](https://duck.com/lite?kd=-1&kp=-1&q=On Writing: A Memoir of the
Craft). He suggests writing "with your door closed" but editing "with
your door open" so that you can focus on the one and get feedback on the
other. This definitely applies to my case, and, who knows, maybe someone
else will take up the streaming as well to make their own contribution.
I imagine a world of work-from-home techs doing a lot more constant live
streaming as the world's software and organizations become more open
overall and more companies are okay with people sharing what they are
doing with the world.

Another YouTuber, Vasrias, says it this way, "Talking about your
thoughts, but coding in silence."

As usual, the answer is likely a balance between the two, but that's a
balance I've been unable to achieve for a simple reason: my sound board
sucks.

That's right. I had a nice one long ago that burned out. This crappy
little one won't even pipe desktop and mic into the same channel to
monitor from headphone or studio monitor speakers. That's important
because, as I wrote earlier, mixing music and voice is always a bad
idea. With the right setup, I just turn down the speakers so I don't get
feedback here, and swing the mic into place to switch quickly to "rubber
duck mode".

I'll have a better board on Sunday so we'll see. Being really proficient
at switching between those modes is a must for anyone wanting to get
into this stuff, for fun or profit.

## Friday, November 20, 2020, 1:58:43PM EST <1605898723>

So the new "cozy term" streams are working out *for me* for some it is
less valuable than "rubber ducking" while I'm doing the coding. Here's
the thing I need to figure out: when to do either (or both)? So here's
me just thinking through some of the pros and cons of each:

### Rubber Ducking Mode

Pros:

* People can hear exactly what I'm thinking as I think it and get some
  insights into ways they might approach their own problems
* I can better respond than just typing in chat

Cons:

* Fucking exhausting for long periods of time
* Seriously messes with my sleep patterns because for some reason
  talking makes me stay up more
* A lot of important conclusions I make never get captured in notes or
  anywhere because I broke through what was blocking me
* Have to deal with lag issues a lot

### Cozy Term Mode

Pros:

* Helps me *really* focus, more than without the "cozy"
* It's how I code normally when not streaming
* I get *so* much more stuff done, period
* I can complete more difficult projects 'cuz more focus
* People enjoy having the stream "in the corner" while working
* Can keep the stream on longer for people to conversate
* More thought goes into what I choose to respond to because I know I'm
  going to have to write it out
* More of what I think and conclude gets captured in my notes

Cons:

* People watch long pauses of nothing happening on the screen while I
  program stuff in my head
* I ignore people a lot more because I am so focused
* Absolutely no direct instruction going on, just learning by watching
* Chatting my responses is exhausting in a different way
* More of what I think and conclude gets captured in my notes

## Friday, November 20, 2020, 12:42:29PM EST <1605894149>

TIL there's a package called `term` (used to be `terminal`) that takes
care of all the tough stuff:

```
* Variables
* func GetSize(fd int) (width, height int, err error)
* func IsTerminal(fd int) bool
* func ReadPassword(fd int) ([]byte, error)
* func Restore(fd int, oldState *State) error
* type EscapeCodes
* type State
```

Ugh, I cannot believe I was still using Ioctl for so much of that stuff.
Don't be me. User `term` from the start.

## Friday, November 20, 2020, 4:52:47AM EST <1605865967>

```go
_ = something // shuts up compaints about not being used
```

## Friday, November 20, 2020, 4:08:32AM EST <1605863312>

Found this nice
[Gist](https://gist.github.com/bbengfort/ee6d3bda44b8cc8d10a26f66be9ced70)
from a guy doing essentially the same thing as `auth` but in a simpler
form and without any encryption or even encoding, just all JSON. Still
interesting to see that same approach. I like how he builds on the idea
of having a `.Token()` method (same as the `oauth2` package
`TokenProvider` interface) and then just injects interactivity if the
token for some reason is not available in the cache. I'm a little leery
of injection like that, however, because if you want to allow disabling
interactivity, say, to enable a non-blocking application that just logs
failures, then you would be unable to do that easily.

Instead I think `auth.Data` (which I will probably rename to
`auth.Config` just for consistency with all the other stuff) should just
implement the `TokenProvider` interface so that it can be used in place
of `oauth2.Token` when needed since it does also return an `error` to be
checked. Then the caller can decide what to do if the `Token` isn't
available, prompt or whatever.

I'm a bit annoyed that he calls it "Authentication" when it is just
"Authorization". I found a good [thread about
this](https://gist.github.com/bbengfort/ee6d3bda44b8cc8d10a26f66be9ced70)
that made me chuckle a bit. The Oauth2 spec goes to great lengths to
make sure only the word "authorization" is ever used in conjunction with
anything Oauth2 does.

## Friday, November 20, 2020, 3:26:49AM EST <1605860809>

Apparently Google has an "advanced protection program" to "keep
dissidents, politicians, and activists safe" that I really want to read
about. I still don't trust them for one second.

## Friday, November 20, 2020, 3:14:22AM EST <1605860062>

So `auth` has become primarily about safe storage of all my
authentication data (not passwords, per se). And
[\@taniwha3](https://twitch.tv/taniwha3) and I were talking in chat
about how to secure the stuff on disk in a zero-trust way. We got to
talking about ways to encrypt (not just encode) and I realized this is a
project I can stretch my YubiKey skills with. He mentioned [FIDO
U2F](https://duck.com/lite?kd=-1&kp=-1&q=FIDO U2F) is the way to go.
Also hearing about Google's "titan key" for the first time. Apparently,
FIDO U2F is only supported on the newer keys, so I have to check mine.
Been meaning to get one that uses regular USB instead of the smaller
USB3 form factor as well.

## Friday, November 20, 2020, 2:41:57AM EST <1605858117>

Looks like there's another [great tutorial on Oauth2 in
Go](https://tutorialedge.net/golang/go-oauth2-tutorial/) that includes a
complete server implementation. I'm glad I looked at it because, even
though it is targeted at managing clients on the server there is code
for keeping track of tokens and clients that I might be able to
integrate into something that a command line client app can use. Lines
of code like the following make me pause and thing I need to fully read
about them before creating my own store, even though I would like my
`auth.Data` to be larger in scope than *just* Oauth2.

```go
manager := manage.NewDefaultManager()
clientStore := store.NewClientStore()
```

I think for now I just need to get a specific client working with
Restream.io without focusing on the mock endpoints and such. I'll still
use `auth` to manage the `auth.Data` just so I have someplace to put my
tokens and such. Humm, I wonder if the Go package manages local token
storage already. I need to research that.

## Friday, November 20, 2020, 1:59:40AM EST <1605855580>

Why are hoodies so damn comfortable? Wearing one with the medieval music
on makes me feel like a monk or something, a coding monk. Lol. Okay, now
I'm laughing at my own jokes in my own log.


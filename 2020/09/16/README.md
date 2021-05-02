## Wednesday, September 16, 2020, 7:29:10PM EDT <1600298950>

Now that [SkilStak]{.spy} is essentially just a personal hobby/night job
and I'm down to 25 maximum members of my mentored community and that I
have the *entire* day off plus weekends enabling me to take on other
work and still maintain the community I realize how many other things
this deliberate down-sizing has enabled:

* Remaining members are hyper-dedicated and fully engaged
* Absolutely no entitled parental bullshit to deal with
* Simple `skilstak.sh` server with only a few people on it
* Direct shared-keyboard pair-programming with `tmux`
* Real terminal mastery without stupid web gimmicks
* Inexpensive, one-click backups on Digital Ocean
* Room to keep things fun and light
* No need for gimmicks (like SkilBux)
* Least possible overhead

In short *everything* is better. The words of [Daniel Pink in Freelance
Nation](https://duck.com/lite?kd=-1&kp=-1&q=Daniel Pink in Freelance
Nation) come to mind. They were something like:

> When small is strategic it can be better than scale.

His point is that staying small and nimble and personal is a very real
strategic business advantage. Events of the past year have certainly
born out that observation.

So far members are *loving* the return to what I was originally doing
when I started. I've noted this before, but I just keep having to write
about it because it is so pronounced. One day I will look back at the
time *before* the return of `skilstak.sh` and the modern
[SkilStak]{.spy} era.

I cannot fucking wait to get my [SkilBots]{.spy} back online.

## Wednesday, September 16, 2020, 5:17:45PM EDT <1600291065>

Reading through more of the job postings that usual today and was
laughing my ass off with my wife at the rampant spelling errors and
absolutely silly requirements listings. I swear half the people that
write that shit have no idea what they are even talking about. One of
the most subtle ones was "experienced with modern object-oriented
programming". 

Pfffhahahaha! "Modern OOP" is a fucking oxymoron.

I couldn't help but make and laugh at my own jokes about these people
who wouldn't know *true* object-oriented design from the shitty Java
mascot even if they pulled it out of their ass. My wife is so funny
about this. 

"You're the guy who can never be settled with a simple answer. You have
to give them the entire life-story and background of the thing before
you'll even answer at all."

She's right. But I'm in good company. Here's an excerpt from *The
Innovators* describing [John Mauchly](https://duck.com/lite?kd=-1&kp=-1&q=John Mauchly) citing "a
colleague" of his:

> An essential component of Mauchly's personality was that he liked to
share ideas---usually with a broad grin and a sense of flair---which
made him a wildly popular teacher. "He loved to talk and seemed to
develop many of his ideas in the give-and-take of conversation,"
recalled a colleague. "John loved social occasions, liked to eat good
food and drink good liquor. He liked women, attractive young people, the
intelligent and the unusual."

Mauchly would *definitely* have been streaming on Twitch and YouTube had
he not grown up in the 30s. Here's my favorite part:

> "It was dangerous to ask [Mauchly] a question, because he could
discourse earnestly and passionately about almost anything, from theater
to literature to physics."

Now I may not be *that* conversant in all those topics but I try to be.
It also reminds me of Dennis (@lastmiles) on Twitch as well.

I also find myself grateful to Cope ([Jim
Coplien](https://duck.com/lite?kd=-1&kp=-1&q=Jim Coplien)) for setting a
few of us straight who bothered to look past his difficult persona. I've
never met him, but the dude's absolutely right about all of it. Cope's
just an asshole (*ahem*, like me) about it for all the right reasons.
"Class-based" programming completely *destroyed* the OOP dream of those
who originally conceived it. That's reason enough to get pissed.

Don't get mad. Get busy. Don't get mad. Get busy. Don't get mad ...

## Wednesday, September 16, 2020, 4:09:45PM EDT <1600286985>

While on my run a few obvious portfolio applications came to mind that
match the skills I've recently concluded have the most hire-able appeal
(and therefore are the most likely to be needed on various contract
gigs):

* `kn`: Perhaps the most important app I might ever create. The `kn`
utility will be one-stop shopping for everything on the KnowledgeNet,
which is fundamentally a terminal user interface technology although
other tools can be built on top of it including --- of course --- the
progressive web app template that contains localized searching using the
`BaseQL` and `dtime` languages. Implicit in the creation of the `kn`
utility is the creation of the `know.sh`/`readme.world` registry, which
is essentially a simple cached dictionary of available knowledge bases
managed exactly like Go documentation. When someone queries for an
existing knowledge base URL the server checks for its public existence
and if found updates the internal Redis DB so that it can regularly
crawl to ensure it is still present.

* `pegn`: PEG + ABNF + EBNF + JSON. The foundation of all grammars. The
one meta-language to rule them all. The reference library implementation
is in Golang but I plan to port it to C, Rust, and vanilla JavaScript as
well. (See [pegn.dev](https://pegn.dev).)

* `ezmark`: Faster, simpler, one-parsing pass Pandoc Markdown parsed
with PEGN and a Golang reference implementation. The KnowledgeNet is
built on this so it needs to be created.

* `datamark`: Ezmark with universal data source conversion and
integration via AST composition.

* `baseql`: Simple query language of the KnowledgeNet parsed with PEGN
and a Golang reference implementation.

* `skilstak.app` / `skilz.sh` / `skilz`:  SkilStak is the app that
started it all. It's only fitting that version 2 prove that I can make a
fast CRUD app using modern "full stack" --- God I hate that term ---
technology. I once made a simple version of it to get my own skill stack
in order when I left IBM but it is time to make a fully functional
progressive web app using component-oriented, reactive front-end design
in Vue with a full GraphQL-to-Redis backend. (PostgreSQL is overkill and
I have *tons* of experience with it while at IBM.) We'll include a
command-line application as well that uses the `cview` terminal UI
framework as well. At the end of the day this is just another CRUD
application, just sexier. It could help a lot people track their own
skills and learning in their own way.

* `skilbot`: The bots are back in town, or at least they will be. I'm
not talking about some lame Discord bot (although that is still a fun
project for people to learn with). I'm talking about the return of the
concurrent skills attendants that monitor what a person is doing on a
*real* computer and chime in with information, challenges and the like.
In 2016 it was the most innovative thing I've ever done in terms of
direct skills learning and yet I let it fade due to other requirements.
I was also still thinking in proprietary terms and even coded in
self-destruct times into each bot. Time to bring it all back with a
fresh look. I love that the bots are really just system monitor
utilities that present a dashboard to the terminal and local web as
well. This means I can use them for my own little CTF-like competitions.
I'll need to be sure that the source of all the bots is public so people
can download and checksum validate their own lest they thing I'm trying
to hack them, at least for the public. I like `exercism.io` but it
leaves many things wanting.

* `gits`: The one Git services command-line utility to rule them all.
The world needs a single utility that deeply understands everything
offered by the vastly different APIs of GitHub, GitLab and any other Git
hosting service. Only then can there be balance. Only then can we
execute a single command to migrate an entire repo from one service to
the other without engaging a GUI at all.

* `live`: An edu-streamer/live-coder's favorite command line tool. This
will build on my popular `twitch` script (which has grown over to well
over 500 lines of bash) and integrates the Restream, Twitch, and YouTube
APIs with possible others to come later. There shouldn't be much work
here since Restream's API takes care of most of the heavy lifting in
terms of syncing everything up. This will include a server/daemon mode
that *displays* colored chat to the terminal suitable for including in a
TMUX pane.

* `k8s`/`k3s` Kit: Before one of my long-time community members
graduated (got a DevOps tech job at 18) he started a Rasperry Pi kit to
simulate and help in the training of actual Kubernetes setup. Such a
thing is rather hard to learn and *truly* master without actual
hardware. Virtual machine software can have unforeseen conflicts with
the low-level hardware and emulation technology required for it to all
really work. Pis are perfectly suited for such things. The idea isn't
novel. It's just useful. I really want to write a guide with
accompanying videos about how people can train themselves up to setup
and maintain a *full*, local cloud and experiment with microservices
setup and communications with gRPC. Such a thing is particularly needed
because beginners often have no way to get *actual* experience doing
DevOps work, which normally requires working for a reasonably sized
enterprise. Just like I ended up being named the corporate mail
administrator after sheepishly raising my hand when asked in a group if
*anyone* had SMTP mail experience (even though I just maintained my own
mail server at home), so too can such individuals position themselves
with at least initial DevOps experience to open similar opportunities.

* Doris' Sculpture Microcontroller Project: Doris still needs to get
some sculpture articulation working and has all the motors and
electronics for it. I plan on helping her get it all working with C
which will require some good concurrency patterns because of the
coordination between all the stepper motor modes.

Here's a list of all the tech on display in these projects:

Golang • GraphQL • Redis • HTML • CSS • JavaScript • REST • WebSockets •
Cview • Terminal UI • Linux • Bash • "Full-Stack" Web Development • Vue
• Progressive Web Apps • HTTP • YAML • JSON • JAMstack • Networking •
Hosting • Concurrency • Data Structures and Algorithms • Parsing
Patterns • Language Design • Domain Modeling • Docker • Kubernetes •
Devops • Microservices • gRPC • IoT • C • Rust

If that doesn't make me able to command a senior consulting and
development salary in the \$200K I don't know what will. In fact, after
finishing it all and putting it in a nice pretty portfolio package I'm
sure I have enough to go entirely freelance after a few years of
contracting. Of course, I'll be maintaining my highly selective mentored
community during all of it and continuing to create educational content
in video, audio, and written forms --- maybe I'll start my own
publishing model of buying it and getting forever access to the
accompanying knowledge base. If No Starch or whatever publisher doesn't
want to go for that it would not be too hard to self-publish today ---
even with paper versions.

There is something I do really need to learn: Linux distribution package
creation. I made tons of `rpm`s at IBM, but I have no experience
creating the others. It won't be that hard, but I really need to make
that second nature based on the amount of code I'll be putting out.

* Debian (`deb`)
* Ubuntu (`apt`)
* Arch (`yay`)
* RedHat (`rpm`)
* Suse (`zypper`)

Come to think of it. I need to stream how to create packages and polish
up those videos for others to consume as well. That will further two
goals as once.

## Wednesday, September 16, 2020, 1:18:50PM EDT <1600276730>

Putting together some notes on skills that I know that I need to polish
up specific examples of so I can justify the target contract jobs of
those types. So far looks like the most in-demand Go work (that people
are actually paying for) is in the "full stack" and required back-end
middle-ware and server software:

1. Golang
1. GraphQL (with REST understanding)
1. "Full Stack" Web Development
1. Microservices
1. gRPC
1. Linux

I haven't found any cybersecurity senior software engineering positions
but I'm sure they will eventually show up. If not, maybe I'll just need
to make a flagship product or two.

## Wednesday, September 16, 2020, 7:58:00AM EDT <1600257480>

I really need to get the base RWX KnowledgeNet template cleaned up since
I keep using it for different knowledge base sites. Hell, I even use it
for this site. Just so much work to do.

I thought of this because the [PEGN
specification](https://gitlab.com/pegn/spec) documentation turns out to
just be yet another one-node knowledge base.


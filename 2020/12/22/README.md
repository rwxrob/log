## Tuesday, December 22, 2020, 5:09:39PM EST <1608674979>

I was about to post a link to these posts about the GitHub stuff and
realized I have a greater need to build a knowledge base site search
interface than I thought because I will be moving this stuff around in
order to make room for new notes. 

My first inclination is to creation a standard way to link to the site
that invokes a localized search using JavaScript. That idea died quickly
because it would unnecessarily force a dependency on JavaScript.

Then a *good* idea crept into my brain: pre-render pages that contain
links to major keywords apart from the planned lexicon, a generated
index (in the truest sense of the word, like a book). Important words
are isolated, prioritized, indexed, and sustainably linked so that even
if things move, the index link never does.

The knowledge worker need for a workflow using this index approach is
very compelling. During the course of writing notes such a worker
realizes they want to share something about a given topic, in this case
GitHub. Then as they consider Tweeting about it they wonder what the URL
would be that won't change and would include any new writing on the
topic anywhere in the personal knowledge base. So they add an entry to a
special knowledge node type (`Index`) that renders search results of the
knowledge base for that term (along with any others that were added
previously). Then they post the URL to the localized entry in the
rendered index node as if pointing to an index in a traditional book.

Not only does this approach address the issue of sustainable links into
the knowledge base, but also deals with linking internally between nodes
when a single node is too limiting. Say for example the worker wants to
link internally to everything written on `vim`. There could be dozens of
nodes related to it. Some of those nodes are only mentioning `vim` and
not necessarily useful links. But those listed in the index node would
be so linking to something like `/dex/#vim` makes a lot more sense and
prevents tons of broken links when stuff moves around. In fact, by
strictly following this convention knowledge base authors are free to
move stuff around as they please. The 404 page simply needs to redirect
to the search index page and boom, a major obstacle to sustainable
knowledge management has been obliterated.

I've updated the brief [readme file on
this](https://gitlab.com/rwx.gg/kn/README). I think the `/dex/#`
solution is one of the more substantial thought breakthroughs I've had
in regard to all of this, and it was born from a real need I'm
experiencing right now.

## Tuesday, December 22, 2020, 4:52:12PM EST <1608673932>

My last post about GitHub really outpacing GitLab has really caused me
to look at the reality that Silicon Valley companies still seem to be
much more successful than those with other models. As much as I
absolutely love GitLab, their progress is being destroyed by GitHub.
Could the main reason be the in-house, in Silicon Valley, difference? Or
is something else going on.

There's also that whole ownership by Microsoft thing. Microsoft *does*
know "developers, developers, developers" and has always put them first.
Sanjay is really kicking ass and taking names. Microsoft is the sharpest
it has ever been (and God knows I'm not a Microsoft fanboy). Microsoft
is going to get some explosive growth with its current plan and
relationship with Nvidia (the real gorilla in the room). GitLab is still
trying to focus entirely on the CI/CD stuff, and while keeping the
integration tight I'm now thinking that it might actually be losing
because of it. Allowing integrations with market leaders in a modular
way, as GitHub is doing, is more in-line with the Unix philosophy.
GitHub does *one* thing really well (now): Git source management in a
social way. This laser focus allows them to free up resources for stuff
like the `gh` command line, which solidified GitHub's dominance on the
API front having been the first company to adopt GraphQL when it came
out. GitLab *still* doesn't have a full GraphQL API.

## Tuesday, December 22, 2020, 4:28:03PM EST <1608672483>

Since discovering I can push to both GitHub and GitLab without any
problem (no need for the mirroring function of GitLab), I'm really
feeling conflicted about continuing with GitLab or GitHub thing. GitHub
has really pulled away from GitLab in 2020 by providing many of the
things that GitLab pushed them to adopt:

* GitHub seems to be doing more, faster (SV perhaps?)
* Full command-line integration tool in Go
* Package repository hosting
* Template repos for creating new ones easily
* Elegant sponsorship integration
* Dark mode (which is far superior to GitLab)
* Friendlier personal profile catering to social
* Sharp social media card creation
* Far better searchability
* Integration with REPL.it and Digital Ocean
* Even more users than before
* Actions

Meanwhile GitLab still suffers from the following:

* No social media card support
* No command line interface
* Slower, clunkier interface
* Really abysmal support for Lynx browsing
* Bad (non-standard) Markdown support
* No command line integration
* Stalled work on GraphQL API
* Slowing adoption rate, fewer users

I had a similar conflict last year around this time. GitHub has
continued to *really* outpace GitLab. In fact, I'm not seeing anything
significant come from GitLab this entire year.

The issue above all others is longevity on the Internet. Now that
Microsoft owns GitHub it isn't going anywhere, ever. Microsoft is
blowing the IT world away right now. Longevity matters when deciding
where to host a stable library that will be imported from GitHub. In
fact, the following three considerations trump everything else:

* Longevity and sustainability
* Visibility to potential project participants
* Sponsorship promotion
* Issues and documentation

For all four of those GitHub currently *destroys* GitLab. I'm afraid I
already know what I have to do during this cleanup. I will be continuing
to support all code on both systems, but GitHub will become my new
canonical source. This means I have to learn `gh` fully. Because I'm
using it for issues and such I can drop the `gits` initiative since I
don't need to bother with them on GitLab.

It brings me great pain to have to make this change. I *love* GitLab as
a company and truly open source platform. I just cannot, in good faith,
continue to recommend it any further at this point based on the
objective facts before me. Beginners already have a lot to learn and
maintain, dropping even one thing they don't have to worry about is best
even if I wish I didn't have to push people away from GitLab as a
beginner.


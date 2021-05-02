## Friday, July 10, 2020, 9:23:42PM EDT [1594430622]

The more I dig deep into the Goldmark Golang Markdown library the more I
realize how bad it is, mostly because I have seen a very good AST
already (Pandoc). The author of Goldmark probably doesn't even know
Pandoc exists. So much for my Goldmark fascination. I sometimes hate
that I can actually look under the hood and see the shit for what it is
a lot of the time. Just the crappy autoidentifier code was enough to
throw it out for something that is actually specified (Pandoc). Every
quirk that Pandoc has is nothing compared to hack that Goldmark is.
Problem is, all the rest are even worse --- especially Blackfriday.

## Friday, July 10, 2020, 12:06:31PM EDT [1594397191]

That `vim-pandoc` plugin gets so many things wrong. I'm seriously
annoyed even though I should be grateful it exists in the first place. I
definitely need to make my own `vim-datadoc` plugin from scratch but
built on the ideas in `vim-pandoc`.

The official name for the syntax of all RWX Knowledge Nodes will be RWX
DataDoc Markdown. The emphasis is equally on the YAML data, not the
limited Pandoc Markdown of the document which is good since the YAML
data is *never* optional in a DataDoc.

Again, I have a lot of editing to do.

## Friday, July 10, 2020, 11:53:26AM EDT [1594396406]

This running has resulted in an explosion of brain power. I forgot how
much a slow recovery walk after a good 20-30 minute just hyper-charges
my brain with oxygen and great ideas --- even a new personal mantra
that's fun to chant to myself while running.

## Friday, July 10, 2020, 9:49:45AM EDT [1594388985]

I'm really struggling with a good alternative to Pandoc divs (`:::`). I
have really come to love them in my writing but the more I think about
them the more I realize pretty much everything I ever put into one
deserves its own knowledge node instead and a link. I have this problem
because I'm such a parenthetical writer. I am always by-the-way-ing this
or that instead of just focusing on the immediate topic. At least with a
link people can follow the tangents if they really want. 

I'm pretty sure serious publications handle this with the square bracket
syntax that refers to other articles.

\[[Here's yet another story about this.]\]

I like that approach the best I think. It is well-established and looks
pretty in my Vim editor because the brackets still force the text to be
highlighted even though they are escaped out with backslash.

Plus when parsing it all I have to look for 

Looks like I have a *lot* of rewriting to do. The good news is that I
will have a locked down writing style standard that I and anyone else
can follow if they want.

## Friday, July 10, 2020, 9:39:28AM EDT [1594388368]

Sometimes flexibility is the fucking devil. For example, allowing the
RWX Knowledge Net (yeah, that's the latest name I've been using) to be
anything *but* YAML and limited Pandoc Markdown is a huge disadvantage.

We can really see this with Hugo. It supports no less than three
"front-matter" (God I hate that term) structured data formats. What a
fucking nightmare! I am so glad to be free of that shitty design.

If there is one thing the last three decades of Web technology have
taught us it is that flexibility kills adoption and inhibits sharing.
This is why we still have YAML 1.2 spec from like more than *10 years
ago*. Smart designers do *not* want flexibility when it comes to things
like structured data formats. They want consistency.

So the RWX KN spec *only* allows a single YAML header and *optional*
body of limited Pandoc Markdown. Both are very solid standards that have
been in use for years.

## Friday, July 10, 2020, 8:53:58AM EDT [1594385638]

Back to masturbatory note taking. The idea that I could whip up a blog
for every one of these random, spontaneous thoughts was just stupid.
Notes are the organic stuff that bubbles up and needs to be caught right
away before it fades. Then an article (or *blog*) can be made from that. 

By the way, I fucking hate the word *blog*. It has lost all specificity.
Usually when people say "blog" they mean "piece" or "article" or
"chapter." The term is dead to me. I will silently look at others who
use it and quietly mock them inside. It's my prerogative.

No, instead I hereby asset the following moniker for this random brain
dumping. From now and henceforth it shall be called --- wait for it ---
*note taking*. I know. The level of my brilliance cannot be grasped.
\*tongue firmly in cheek\*


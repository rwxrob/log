## Monday, July 13, 2020, 2:44:42PM EDT [1594665882]

The Pandoc AST isn't bad, it's just not what I would do. It's too much,
doesn't match CommonMark and just so damn annoying sometimes. I mean,
`Inline.Smallcaps` Really?

The biggest problem of all is how much you cannot change it.

Goldmark grew their own AST as well. It's not horrible, just not very
well informed from experience looking at document structure for several
years as I have been, obsessing over this stuff.

None of the document and knowledge solutions have ever *started* with
the AST model and worked up. The closest thing we have to that was the
DOM and we know how that ended up.

Back when I was doing the ABNF for BaseML (later EzMark) one thing
really stood out. None of the existing Markdown formats --- from the
very beginning --- were able to be rendered inline. They all required a
first pass in order to parse *all* the block types and reattach the
reference links and such. That has *always* annoyed me. Each block
should be consumable and rendered immediately after it is read. 

I really am having a hard time just shutting up and using Pandoc. There
is so much bloat and overkill to use that method. Pandoc Markdown
doesn't even look CommonMark compliant.

What I really want to do is specify a superset of CommonMark that is
100% Pandoc compliant that can be rendered immediately and mastered very
quickly. I want RenderMark.

## Monday, July 13, 2020, 5:21:09AM EDT [1594632069]

Up early after a long sleep. Must have been that three hour run/hike on
Saturday. Feels good though. I can tell my old body is returning.


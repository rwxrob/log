## Wednesday, July 15, 2020, 4:49:13PM EDT [1594846153]

Great ideas from the stream today about rendering the `TexExpr` block
and `Tex` inline as SVGs that are inlined into the HTML rather than
depending on a JavaScript library *at all!*

## Wednesday, July 15, 2020, 4:27:32PM EDT [1594844852]

Big great discussion about MathJax or KaTeX and what to call the AST
element. Pandoc mistakenly called it `Math`.

```markdown

Here is a $\epsilon$ thing.

$$ \forall x \in X, \quad \exists y \leq \epsilon $$

```

So that turns into this:

Here is a $\epsilon$ thing.

$$ \forall x \in X, \quad \exists y \leq \epsilon $$

## Wednesday, July 15, 2020, 3:56:02PM EDT [1594842962]

Was reminded that a `{{.TOC}}` in the template is a good idea and that
TOC content is metadata *not* data that really has no place in the
`README.md` file itself which is just bothersome to the content
maintainer and redundant to those downloading the content who already
have the TOC heading data in the `BASE/json` file.

Also decided that `Heading` attributes really need to be mandatory to
allow `Heading` text to be changed without impact.

## Wednesday, July 15, 2020, 8:32:37AM EDT [1594816357]

I love that Go's creators were so fucking experienced that they could
leave `goto` in Go without shame. It seems like the entire world of
less-than programmers don't get why they made this decision. But if you
truly want to understand a specific case where it makes a *ton* of
difference in efficiency take a look at Go's own syntax parser. Yep,
there's `goto` in all its glory doing what it was *meant* to do in
spectacular fashion. These are yet more reasons to truly understand why
Go is a *far more thoughtfully designed language than Rust*. Very few
people on planet Earth would even understand an explanation of why that
is objectively true. But it is nice to know they do exist. I am such a
Rob Pike fanboy. There I said it.


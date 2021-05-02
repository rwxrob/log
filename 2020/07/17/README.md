## Friday, July 17, 2020, 6:51:31PM EDT [1595026291]

Cloudflare just went down reportedly because of a "bad router rule" in a
server in Atlanta taking out 1.1.1.1. The number of people depending on
that central DNS provider is proof of how stupid people are. The entire
point of DNS was to allow *distributed* DNS providers rather than have
everyone depend on a service. It really revealed how stupid some
companies are. GitLab was one of them. After seriously fighting with
GitLab's brain-dead flavored Markdown --- despite their claim to be
moving to CommonMark --- I've gathering up reasons to give GitHub
another look. But, honestly, I'm kinda tired of depending on *any*
centralized service at all at this point.

## Friday, July 17, 2020, 8:13:13AM EDT [1594987993]

Another amazing and unexpected advantage of writing in PEG is that you
can specify ordered priority such that things that are *more likely* to
occur in a language are examined first. This has never been something
any specification language has allowed an author to communicate. It also
brings forward some of the difficulties when a syntax would be easier to
parse *without* the preferred position when examining the input. For
example, `Text` is far more frequent than `Tex`. But checking for `Tex`
lexically is easier because you look for `$` and know you have it right
away instead of maintaining the priority and checking that `$` is *not*
present so that you can continue with the `Text` parsing. This does
cause a bit of redundancy in the parsing engine because to check for
`Text` I have to rule out `$` and then later have to check for `$` to
make sure I have a `Tex` inline. The cost is easily worth it, though,
given all of the code that would have to be evaluated otherwise leaving
`Text` as the plain option at the end of the list.

## Friday, July 17, 2020, 7:52:01AM EDT [1594986721]

I cannot overstate how amazing PEG positive and negative lookahead and
lookbehind are for specifying language grammars. It allows
specifications to directly communicate the code that needs to be written
including some idea of how much memory will be needed for any lookahead
specified by the grammar as well as how many previous states will need
to be saved (memoized) to assert any look behind.

This has been particularly useful when dealing with sets that can
include other sets except for one specific thing. This is impossible to
capture in EBNF or ABNF and requires resorting to "rhetorical"
specification syntax. 

Here's an example: Markdown *inlines*. Often one inline can contain most
of the others. In PEG you simple have to do a negative of the inlines
another inline cannot contain (rather than explicitly rewriting every
one of them).

```pegn 
Inline <- Text / Quote / Emph / Link / Pre Quote  <- (!Quote Inline)+
```


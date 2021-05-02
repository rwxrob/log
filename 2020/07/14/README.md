## Tuesday, July 14, 2020, 3:02:22PM EDT [1594753342]

While doing the PEG for KN Ezmark I realized that `BlockQuote` and `Div`
are effectively the same thing in the Pandoc AST. Both are containers,
but the `Div` is *far* superior to maintain and parse. In fact,
`BlockQuotes` have always been a pain in my ass. I've decided to try and
get away with dropping them entirely from Ezmark. I am sure some people
will scream and they can use other full parsers like Pandoc if they need
them.

This does mean that `Div` is actually a `SemDiv` because it is *not*
based on style. It denotes a semantic collection of content within the
current content such as a callout, note, or even an *actual* block
quote. People can use them for addresses and such as well. In fact, it
is the *exact same thing* as a `Fenced` syntax aware code block, but for
other stuff.


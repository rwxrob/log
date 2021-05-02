## Saturday, July 11, 2020, 8:38:29AM EDT [1594471109]

Woke with an idea to build the Pandoc AST into the core RWX Knowledge
Net specification. In fact, I can use Pandoc in two stages to prepare
for its eventual replacement as a parser and renderer, first to generate
the JSON AST (loaded into a Go struct) and then to render by piping the
JSON AST into the `pandoc` app for rendering. It will make the initial
tool need double the calls to `pandoc`, which I was trying to reduce,
but for a *very* good reason. Later I can keep `pandoc` as a renderer
(since people will always want a fully configurable Pandoc rendering
option) but I will replace `pandoc` as a parser with a native Go PEG
parser.


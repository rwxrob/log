## Monday, August 3, 2020, 12:02:58PM EDT [1596470578]

Need to consider how to add bounds limits to the `pegn.Parser` such that
when developers initialize the parser they can set specific sizes for
things overall as well as any semantic size and length limitations which
can be specified in PEGN which the addition of `MinMax` and `Count`.

## Monday, August 3, 2020, 8:40:04AM EDT [1596458404]

I've revised the PEGN specification to divide the `Definition`
non-terminal into `TokenDef`, `ClassDef`, `ParseDef`. This semantic
distinction will allow better code generation later. For example,
`TokenDef` can be rendered as a single file of constants, both single
runes and simple strings (like `<-` for example). `ClassDef` can be
rendered at simple boolean `Is*` functions. And the remaining `ParseDef`
definitions will be rendered as files each lower-cased and containing
only a single `Parse(p Parser) (Node, error)` function. The modularity
should be expanding and supporting grammars rather easy and allow more
precise re-rendering when the PEGN specification changes.

My biggest concern is separating out the convenience definitions from
the *actual semantic* Nodes that one wants in an AST. For example,
`Spacing` which is `(BlankLine / Comment)*`. Do I really want a
`Spacing` node with an identifier? Probably not. I *do* want the
`BlankLine` and `Comment` Nodes in the AST because they are significant
and could be used to re-render the code using a format tool, etc. I
don't really need the `Spacing` Node type. It is just a convenience to
make the grammar more readable.

On the other hand, when thinking about other possible code renders the
option of having more granularity in an event-based parser/handler is
actually a good thing. For example, say I want to handle `EndSpacing()`
for anything or more specifically `EndComment()`. I have the option. In
fact, the cost of a containing convenience Node like `Spacing` really is
not that bad since it is just 4-6 characters defining the containing
Node and its type.

So I think I just won't worry about it. If it is in the PEGN, it should
always be in the AST.


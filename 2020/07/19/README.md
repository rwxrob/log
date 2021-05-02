## Sunday, July 19, 2020, 6:17:42PM EDT [1595197062]

Getting the questions about why I'm not writing a book. I get that one a
lot. The simple answer is that books take too much time and knowledge
bases are more effective *if I can ever get them updated enough*. The
challenge is getting your knowledge into others view. But the plan for
Knowledge Net sharing and subs will cover that. I just have to fucking
finish it!

## Sunday, July 19, 2020, 9:34:11AM EDT [1595165651]

PEGn is *really* grabbing my attention. It's becoming that perfect thing
between ABNF, the original PEG (which has several substantial flaws in
the "example" syntax), and the myriad PEG parsing engines out there ---
all of which suck at creating *readable* grammars. PEGn will boast the
following when complete:

* Self-specifying PEGn grammar
* Most readable grammar specs on the planet
* Nearly identical semantics to original PEG "example"
* Semantic capitalization identifier naming conventions
* Full set of reserved classes and tokens
* Zero ambiguity semantics
* Full Unicode support

And eventually I plan on building the following tools for it as well:

* `pegn` - linter, validator, and code generator
* `vim-pegn` - vim plugin with PLS language server support

My code generator won't clutter up the grammar itself with inline code
(as cool as that is). Instead it will allow *granular* creation of the
different language renderings. This is substantially better than
*anything* else out there right now because they are all ***language
specific*** which destroys the usefulness and ubiquity of the grammar
itself. No, instead `pegn` will support *modular* code generation
support allowing different implementations of a rendered parsing even in
the same language. For example, say you want your grammar generated in
interface-centric Go versus struct-centric. Or say you want to generate
code that generates an AST, or other code that is focused entirely on
handling parse events. There are so many different ways to implement a
parser for different needs. The one flaw that *every* PEG-to-code
generator has right now is the inability to adapt to these needs and the
fucking gawd-awful grammar specification files that result.

## Sunday, July 19, 2020, 7:39:00AM EDT [1595158740]

Been really conflicted about when to use Go `interfaces` and when to use
`structs`. I tend to be a one thing or the other kind of guy. Using
`interface` gets you immense flexibility while `structs` work better
with marshaling and require *far* less code. I've decide to follow
Goldmarks' lead and create both my parsers leaning on `interfaces` more
even if that means a few accessors and mutators. I am probably too
abused by Java to look at them rationally. They probably do have good
use sometimes.


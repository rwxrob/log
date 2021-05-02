## Monday, July 27, 2020, 7:48:36PM EDT [1595893716]

Just hearing about the "bullet" method for note taking. Seems
interesting but I have a feeling that digitally thing form of logging
might be better for me so long as I have a way to search them.

I am partial simply to use the Pandoc Markdown div notation for this
stuff:

```
::: Reminder
Need to walk the dog.
:::
```

## Monday, July 27, 2020, 7:44:44PM EDT [1595893484]

Need to look into a book recommended from a friend called [Make It
Stick](https://www.amazon.com/Make-Stick-Science-Successful-Learning/dp/0674729013).
Wondering if it is new or just rehashing the old stuff we already know.

## Monday, July 27, 2020, 7:17:11PM EDT [1595891831]

Need to put an article together that has all the great, free code
sharing sites out there. Here's the best so far:

* <https://ix.io>
* <https://codeshare.io>
* <https://repl.it>

Those are my favorites --- especially `ix.io` which I can use from
within a `vi` session to send and receive specific lines and sections.

## Monday, July 27, 2020, 7:08:30PM EDT [1595891310]

Found out today that <https://codio.com> is on some Python version
previous to Python 3.6 because someone I'm helping cannot use f-strings.
This is the *standard* used by his university that costs him \$960 per
course. I'm fucking out of my find with how stupid that is.

## Monday, July 27, 2020, 4:22:41PM EDT [1595881361]

Had a good reminder today how important it is to keep the Go interfaces
in the *top* level of the package and the mostly private
*implementation* of those interfaces in their own second-level
subdirectories (subpackages). It makes the names work out perfectly.
Instead of ending up with a `parser.Parser` and `node.Node` you get
`pegn.Parser` and `pegn.Node`. This also allows the removal of the
redundant name in the constructors so instead of `parser.NewParser()`
and `node.NewNode()` you get `parser.New()` and `node.New()`.

To any old-school Java or C++ class-based OOP programmers who might be
reading this. Creating the top-level interfaces of the package feels
like writing the top of a class, and coding the specifics of the
subpackage subdirectory implementation files feels like the body and
methods of a class.

I have coded other Go stuff like this before, but this `pegn` package
really serves to illustrate how powerful the approach of public
interfaces and a private implementation can be in Go when combined. It
is definitely *not* the intuitive approach that I see beginners use, but
it is very clearly the most idiomatic Go design. I will be so glad to
use `pegn`, `ezmark`, `dtime`, `cmdtab` and other packages to
demonstrate this. I'm very motivated to get this really polished to show
how objectively simpler and superior Go coding is to Rust.

## Monday, July 27, 2020, 9:26:35AM EDT [1595856395]

The demand for PEGN parsing solutions will only increase as the tech
world continues to simplify the human-computer interface with text and
conversational interface layers. The demand for highly efficient and
sophisticated language grammars will also increase as will the demand
for software developers who understand them and can create them
properly. 

The `pegn` package I've been building falls directly into that space
seeking to meet the needs of developers who need to implement
domain-specific languages quickly and easily. There's no need for ever
developer to create a new PEG parser every time. There's not even a need
to redefine the most common tokens and classes used in any DSL. They are
all included in PEGN and the `pegn` implementations.

Very few people on planet Earth will even understand enough to grasp the
impact of something like this. But to those who do, this will be very
clear and appreciated. I just wish I could find more of such people.


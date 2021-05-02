## Friday, December 11, 2020, 4:08:52PM EST <1607720932>

Here's a summary of the main Go terminal UI modules:

Module | Usage
-|-
[`termui`](https://github.com/gizak/termui)|Charts and graphs
[`cview/tview`](https://gitlab.com/tslocum/cview)|Text heavy TUIs
[`tcell`](https://github.com/gdamore/tcell)|Basis for `cview`
[`gocui`](https://github.com/jroimartin/gocui)|Like `cview` but not
[`termbox`](https://github.com/nsf/termbox-go)|Deprecated but still in use

## Friday, December 11, 2020, 6:50:26AM EST <1607687426>

I've shifted from random enthusiasm about what this overengineered
resume project could grow into a centralized database store to a saner
focus on promoting an individual career database (of sorts) that just
happens to be able to produce specialized resumes (akin to views in a
database). This movement toward an individual tool allows a safer focus
on maintaining emails, phone numbers, and addresses within a personal
resume without doxing them in any way. Then someone making use of the
`resume` tool could decide which template to use to produce public views
of them. This makes me feel better about the direction.

## Friday, December 11, 2020, 4:33:16AM EST <1607679196>

After some experimentation with the automated documentation generation
from `protoc` it is clear that I *never* want to use inline style
comments because they are lost after all the tags in the Go code that is
generated and since structs in Go are presented exactly as they are in
the documentation that would make them unnecessarily ugly. Here's a
quick example:

```protobuf
message Foo {
  // better to write stuff here
  string thing = 1;
}

message Bar {
  string thing = 1; // than here, cuz ugly generated
}
```

## Friday, December 11, 2020, 3:32:27AM EST <1607675547>

A quick glance around the Internetz reveals no *obvious* AST parser for
the Protocol Buffer grammar. There is something in Antlr, but yeah.
Eventually, this is the kind of thing that would immediately benefit
from being captured in [PEGN](https://pegn.dev) because I could render
the parser code for it immediately and quickly make a `vim` plugin or
whatever for it.

If nothing more, this is a good example of why a *good* meta-language to
capture *any* grammar is such a powerful idea.

## Friday, December 11, 2020, 2:42:24AM EST <1607672544>

Need to create an addition to my Vi/m guide that covers the specific
most common key combinations during an edit session, for example:

Combo|Description
-|-
`dw`|Delete word (from beginning)
`bdw`|Delete word (from middle)
`cw`|Change word (from beginning)
`bcw`|Change word (from middle)

I think it's actually easier to remember these combos than the
individual commands themselves.

I've also been experimenting with `jj` and `kk` (along with `kj` and
`jk`) as an alternative to `Ctrl-[` (which I once really argued against
since only Vim supports that stuff.


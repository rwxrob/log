## Tuesday, March 2, 2021, 10:27:09PM EST <1614742029>

Learned that Git squashing really is only when you have a branch with a
*lot* of changes that are easily summarized as one major change to the
application/repo that goes with a particular version change. In other
words, don't sweat it. You probably do not need it. 

In fact, having a full and accurate commit history makes short work of
creating CHANGES files and such where a squash would make it harder.

## Tuesday, March 2, 2021, 9:55:39PM EST <1614740139>

The problem with `replace` and `go.mod` is a non-issue if you use best
practice of never committing anything with a message that does not
specifically match the files involved. This will result in a bunch of
commits that can be squashed but also never adding a `go.mod`
accidentally when being less precise about what gets committed in each
commit.

## Tuesday, March 2, 2021, 9:14:42PM EST <1614737682>

Considering the BusyBox approach again for `cmdtab` to turn commands
into REPLs that have their own completion and more. It could produce
several monolith commands that function as their own shells even on `sh`
(which doesn't have completion).

I can think of a dozen reasons to do this in just the grey-hat hacking
world.

## Tuesday, March 2, 2021, 2:53:44PM EST <1614714824>

Need to really standardize on language by convention for CRUD
subcommands, sort of like creating an API for humans. Thinking of the
following:

```
cmd (c|create) [<id>]      - create a new thing with optional name
cmd (e|edit) [<id>]        - open editor for thing by ident [or current]
cmd (d|del|delete) [<id>]  - delete a thing by id [or current w/ confirm]
cmd (l|ls|list) [<filter>] - list stuff [with optional filter]
cmd (q|query) [<query>]    - search for stuff in the stuff
```

Set and get stuff should just use the identifier and new value without
the `set` and `get` explicit.

Standardizing on these creates muscle memory that works across
different `cmdtab` commands.

There is some question about the `query` which could equally have been
`search`, `find`, `?`, or many others. I think `query` is best because
its short form is the least likely to conflict with other stuff. This is
what `yq` uses for that reason.

Note that there is no *replace* because that doesn't make sense. Use
`edit` or `update` instead.

This will make things intuitive for people using `cmdtab` commands.

## Tuesday, March 2, 2021, 2:45:43PM EST <1614714343>

Someone needs to do a full, fun meme comparing boomers to genx just for
fun:

Boomer|GenX
|:-:|:-:|
Stallman|Torvaldz

## Tuesday, March 2, 2021, 2:05:51PM EST <1614711951>

Reconfirmed that bare reference notation is indeed observed on GitHub.
Halle-fucking-lujah.

```
Here is a [RWX] link.

[RWX]: https://rwx.gg
```

In the past I have been somewhat against reference style links because
they separate the link from the occurrence in a way that can be
dangerous when cutting and pasting between document. 

However, the linking and references make much more sense when in the
context of a size-limited Zettel. Everything will *always* be on the
same screen in such cases. 

Moreover, this style of linking is directly workable on paper
dramatically simplifying the entire process when a computer is not
involved. Removing *all* cognitive overhead that would otherwise result
from a different digital format from paper is worth other potentials
risks all by itself. What I write on paper is *exactly* what I write on
the terminal. In fact, when I print hard copies of my Zettelkasten there
is *no* difference other than using a printer instead of a pen.

## Tuesday, March 2, 2021, 12:34:06PM EST <1614706446>

Coined the term *Zettelcast* or `#zetcast` for live streaming that is in
short digestible, topic bits. It just so happens that the Pomodoro time
is default to 25 minutes (which is the maximum lines we came up with for
a terminal-based Zettel, 80 cols x 25 rows).

I wonder if there is a domain open for it.

## Tuesday, March 2, 2021, 1:50:22AM EST <1614667822>

I cannot get over how cool it is that a Zettel from Luhmann's original
fit almost exactly the same amount of text as one 80 col x 28 row
text terminal. In other words, if you write much more than one terminal of
text, you are out of space. No extra indicators are really needed (but
we'll add them anyway.

## Tuesday, March 2, 2021, 1:22:52AM EST <1614666172>

[Communicating with Slip Boxes](http://luhmann.surge.sh/communicating-with-slip-boxes)


















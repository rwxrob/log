## Saturday, November 28, 2020, 1:43:29PM EST <1606589009>

As I was worked more on my `cmdtab` library today I realized that my
dream of doing code generation, instead of depending on `init` functions
as I do now, is completely doable just because of the consistent format
that the `cmdtab` files provides. In other words, I can add code
generation *to* `cmdtab` for those who want it. The command would be
something like `cmdtab gen` and would parse the `init` functions of the
files and generate code that would not even invoke any `init` function
at all at run time.

It's not like the `init` functions are bad. There is almost identical
performance between looking stuff up in a table/map of subcommands and
flowing through the logic of a massive switch.

It's just good to know I can add it either way. This means that any
hesitation I had about `cmdtab` using `init` has been obliterated.

## Saturday, November 28, 2020, 12:24:37AM EST <1606541077>

Out of curiosity related to the `iferr` tool (that I still haven't
figured out) I happened upon the [vim-go
tutorial](https://github.com/fatih/vim-go/wiki/Tutorial#beautify-it)
and ended up spending some time with it picking up the following really
useful tips:

* `[[` and `]]` automatically go to `func` definitions
* `K` mapped to open documentation (`:GoDoc`)
* Activated a *lot* of syntax color (off by default)
* `<leader>c` toggles code coverage syntax highlighting
* `<leader>i` information about what is under the cursor
* `dif`/`daf` delete inner/all of a function
* `vif`/`vaf` select inner/all function
* `yif`/`yaf` select inner/all function
* `gd`/`ctrl-t` jump to/back from a definition
* `:GoRename` when on a symbol of any kind

I almost need to make a flashcard program just to remember them all, but
they are so worth remembering.


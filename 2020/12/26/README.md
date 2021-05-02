## Saturday, December 26, 2020, 6:20:11PM EST <1609024811>

Discovered today (on accident) that the `gh` command (from GitHub) has
built-in tab completion with `complete -C gh gh` (like I have for
`cmdtab`). I opened a ticket on the `cobra` project for this, but it
might have already been there. I really need to go spelunking through
the `cobra` code to see if there is a `COMP_LINE` defined anywhere
within it. If so, that would be a good thing even though the scaffolding
required to create commands that use `cobra` is still butt ugly.


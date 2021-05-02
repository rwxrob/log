## Friday, January 15, 2021, 10:47:21AM EST <1610725641>

Observed that when pasting text into Vim that contains tabs (with `set
paste` or otherwise) that if more than 50% of the file results in lines
beginning with tab the entire file will be set to `noexpandtab` even if
if I explicitly set `expandtab` as the last line in my `.vimrc`.
Changing more than 50% of initial tabs to spaces causes the `:set
expandtab?` query to return the wanted `expandtab` setting. So this is
something that overrides all the other behavior that Vim does
automatically, very annoying.

The whole thing reminds me of that [one scene about tabs vs spaces on Silicon Valley](https://duck.com/lite?kd=-1&kp=-1&q=one scene about tabs vs spaces on Silicon Valley).

## Friday, January 15, 2021, 5:56:45AM EST <1610708205>

Decided to go with a separate repo for both `mim` (the utility) and
`mim-go` that standard library. This allows `mim-js` and family to be
created later so people can have a compatible API. I'm inclined to write
it in IDL eventually, but not during the inception phase.

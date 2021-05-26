Burned by bash parameter expansion today. For some reason `${line%% *`}
did not work on the last line of input leaving a space and an extra
trailing thing. I suspect it was because there is a tab there but could
not confirm easily. Moral of the story: if there is a JSON option
*always* take it. You don't have that ambiguity with `jq`.

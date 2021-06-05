Went to add randomization to arrays in `yq` and realized that I could
never contribute in good conscious to that project (as much as I support
it). There are so many design decisions I disagree with it is like
torture going through the code. I need to stay healthy so I can start
projects out the way I prefer for this kind of stuff and rally people
behind them. Turns out rather than work on `yq` at all, I would rather
contribute an addition to the `jq` parser that supports minimal `yaml`
syntax (which YAML parsers are required to support anyway). That is
where the true effort is needed. Then all that has to change is the
multicall name of `jq`, perhaps just a `yq` hard link. All the code base
would still be in the same project and supported there.

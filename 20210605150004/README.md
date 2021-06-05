Found yet another `yq` bug. People should stay the hell away from that
for anything in production. Thankfully, most use `jq` for that stuff
anyway (like at work). The following shows that for `|` string values
`yq` adds an additional new line for no fucking reason. I feel like a
shit for being so anal/OCD about this stuff, but that is *not* good.

```
rwxrob@live:quotes(main)$ yq e '.[2].Q' data.yml
A language is a tool. My hammer, however, is very left wing.
rwxrob@live:quotes(main)$ yq e '.[3].Q' data.yml
Go's method pattern is basically an inversion of control: instead of
the code being the base unit and attaching data to it, the data is
the base unit and you attach code to it.

```


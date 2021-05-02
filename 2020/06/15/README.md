## Monday, June 15, 2020, 9:43:09AM EDT [1592228589]

Looks like [Google's shell scripting
guide](https://google.github.io/styleguide/shellguide.html) agrees with
my conclusions on pretty much everything. It doesn't just validate my
conclusions on Bash but everything I keep saying about all the shitty
advice out there --- particularly on YouTube.

One thing that convinced me to go back to two-space indent was Google's
guide. The waste of space has started grating on me --- especially now
that YAML is being affected. I would rather have more levels of modern
nesting than a default that wastes space.

Also discovered `shellcheck` after reading the Google guide. This isn't
the kind of utility that I would have exposure to in my previous
POSIX-only life. It is an absolute *must* for beginners and will
definitely be the first thing I introduce, along with `bat` for
test-driven shell development.

I did discover that there is a `readonly` keyword which is the same as
`declare -r` which is far more useful when declaring global constants. I
also ran into an interesting quirk that prevents the use of any
`readonly` variable name *anywhere* else in the code. It throws an error
even when using `declare` within a function scope.

I confirmed again that `declare` is *exactly* the same as `local` but
learned that the `local` keyword accepts *all* of the same options that
`declare` does. Therefore I will begin using Google's convention of
`local` only for stuff within functions and `declare` only for global
stuff at the top and `readonly` for constants. While there is no
technical requirement to do so, this distinction makes for much more
readable code.


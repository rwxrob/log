## Friday, April 16, 2021, 8:59:43AM EDT <1618577983>

Fucking bug in the `testing` suite for Go that incorrectly identifies a
"formatting directive" in any functions called `Sprint`. I'm kinda
pissed.

## Friday, April 16, 2021, 8:06:40AM EDT <1618574800>

Most standard library routines that accept an `interface{}` or other
indeterminate thing or stuff use `a` so that it reads `func Do(a
Thing)`.


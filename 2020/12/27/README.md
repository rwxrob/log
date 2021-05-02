## Sunday, December 27, 2020, 10:48:31PM EST <1609127311>

Here's some [strong
evidence](https://www.sciencealert.com/humans-used-to-sleep-in-two-shifts-and-maybe-we-should-start-it-again)
(that my wife found) suggesting "biphasic sleep is a natural process
with a biological basis". I couldn't agree more, and I haven't done any
scientific research other than my own patterns and productiveness.

I particularly like the observation about "two periods of ...
productivity":

> [Biphasic sleep] provides two periods of increased activity,
> creativity, and alertness across the day, rather than having a long
> wake period where sleepiness builds up across the day and productivity
> wanes.

## Sunday, December 27, 2020, 8:40:26PM EST <1609119626>

Tonight I learned that just adding a `+build ignore` comment to the top
of a file in a Go package disables the entire file, which is much easier
than attempting to comment the whole thing out while you are still
working on it but want to `go run` or `go build` the rest of package or
command.

```go
// +build ignore
```

## Sunday, December 27, 2020, 8:32:28PM EST <1609119148>

I really need to use the CLDR/Unicode `gen.go` from the following repo:

<https://github.com/golang/text>

It is a great example of using `go generate` in a way that is entirely
in `go` using `go run` instead of shell or something.


## Sunday, March 14, 2021, 9:51:17PM EDT <1615773077>

Learning to add `CGO_ENABLED=0` forces CGO dependencies to be visible
during testing and development so they can be dealt with individually.
I'm surprised this is not a mandatory recommendation for more Go
tutorials. Not knowing that you are adding CGO dependencies is a big
fucking deal. In fact, every package should be shouting in bold if it
actually forces such --- not to mention if the package is actually
stupid enough to `panic` at any point.

## Sunday, March 14, 2021, 9:45:48PM EDT <1615772748>

TIL that `os/usr` uses `cgo` if "it can find it" (which is pretty much
always) and has to be specifically disabled with `osusergo`:

```go
// +build osusergo
```


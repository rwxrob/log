## Wednesday, February 10, 2021, 8:40:24PM EST <1613007624>



## Wednesday, February 10, 2021, 8:21:53PM EST <1613006513>

Finding it annoying that some of the standard libraries in Go don't
allow mocking of the inner stuff, but it is clearly for performance
reasons. For example, `user.Current()` returns a cached version if
already called.

However, I did find a way to get around this:

1. Create a package called `mockuser` that contains a `user` package.
1. Implement an identical `user.Current()` function
1. Return different stuff that points to your `testdata`
1. Import it with the explicit `user` nickname in your test code

This was much easier than I was expecting. For doing a large test of
something that could be catastrophic to a system that is a suitable
replacement to ensure nothing bad happens since the entire test code is
forced to resolve the `user` symbol to your mock.

I was foiled, however, because usually I want to test stuff that imports
`user` and it has no visibility into my mock. This is one of those times
when being able to mess with the symbol table directly would have come
in very nicely (like in Perl).

## Wednesday, February 10, 2021, 7:25:08PM EST <1613003108>

I keep getting tempted by `testify` but it is so bloated and unnecessary
for most all unit testing. The latest was getting a good way to test for
a panic. Here's a gem from Stackexchange (for once):

```go
func assertPanic(t *testing.T, f func()) {
    defer func() {
        if r := recover(); r == nil {
            t.Errorf("The code did not panic")
        }
    }()
    f()
}
```

## Wednesday, February 10, 2021, 7:12:48PM EST <1613002368>

TIL that `os.Executable()` is preferred since 1.5 over `os.Args[0]`
since it is more reliable across platforms and impervious to changes to
the first argument (as it sometimes done to convey meaning in `ps`
output). It is also a full path to the executable to allow validation
against any internal idea of executable path in the code that isn't
system dependent.

## Wednesday, February 10, 2021, 5:58:36PM EST <1612997916>

Struggling with decision so use `jsonconfig-go` or `jsoncache-go` as the
name. I feel like `config` is more relevant. I'll use `git` as example,
which uses `git config` even though it doesn't recognize any of the
freedesktop standard conventions. 

## Wednesday, February 10, 2021, 5:36:39PM EST <1612996599>

One of the most annoying things about the otherwise amazing `gh` command
line tool from GitHub is the lack of tab completion for the aliases I
have dutifully added. Had I added them using my shell script approach
they would be automatically detected. The pile of reasons to create a
`repo` script (probably Perl) that encapsulates `gh` and `gl` and
something for other local bare Git repos continues to grow.

## Wednesday, February 10, 2021, 5:33:30PM EST <1612996410>

More reasons to hate on GitLab:

* I have to be logged in to search it
* I have to wait through the browser Cloudflare confirmation before I
  can even open anything.

It is so sad to see such a great product fail to completely.

## Wednesday, February 10, 2021, 3:05:14PM EST <1612987514>

TIL that `readelf` is a thing that I did not know about:

```sh
readelf --all $(which ls)
```

## Wednesday, February 10, 2021, 1:07:08PM EST <1612980428>

I'm done with `exa` which doesn't even show how many hard links there
are. How fucking brain dead can an `ls` be? Fuck the colors and emojis
if it doesn't have the *base* functionality of the `ls` command.


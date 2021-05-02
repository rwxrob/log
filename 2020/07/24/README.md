## Friday, July 24, 2020, 8:18:26PM EDT [1595636306]

Turns out it is *way* too verbose. To me the tests are the best way for
someone to get acquainted with your code base. If you mess that up with
something like following boilerplate created with `gotests` you lose the
value of communicating what your package is about and how it works. In
fact, this just makes me want to use `Example*` more than `Test*` even
more. Everything becomes a part of the documentation and you are writing
it from the perspective of someone using it.

## Friday, July 24, 2020, 7:30:01PM EDT [1595633401]

Looks like exists already! I am so seriously blown away by this and it
has been around for a very long time. It even has test template support
with testify templates as an option.

```
go get -u github.com/cweill/gotests/...
go --all -w node.go
```

## Friday, July 24, 2020, 7:24:21PM EDT [1595633061]

It occurred to me that creating a tool to stub test cases would be
relatively easy just by walking the Go AST and matching the lowercase
file name with the specific interface or struct (assuming you use that
convention and they match).

## Friday, July 24, 2020, 6:41:57PM EDT [1595630517]

Realized there is real value in having *two* scripts directories in your
path, one for the good stuff in dotfiles that you can show off publicly
to others and another for all the quick and dirty shit that needs to me
made into something better eventually. Here's what they look like in
mine:

```sh
export PATH=\ SCRIPTS:\ SCRIPT_PRIV:\ ...
```

(Of course there is a lot more in that path after that.)

## Friday, July 24, 2020, 6:27:50PM EDT [1595629670]

I really need to find or make a tool that creates test case boilerplate
code for everything in a matching `_test.go` file.

After make a `note` command for like the 10th time I am realizing how
much I really need to fucking finish `kn`. I would use it ever five
minutes. It *must* be made!


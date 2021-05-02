## Sunday, April 25, 2021, 12:13:22PM EDT <1619367202>

I always forget `yaf` (as the compliment to `yif`) for yanking an entire
function including the signature line and brackets.

## Sunday, April 25, 2021, 11:18:15AM EDT <1619363895>

I have to remember there are two ways to get the type of a thing in Go.
I use the `select` method so much I often forget the `if` method to do
the same thing:

```go
if v,ok := a.(Thing); ok {
  // do something with v, which is a Thing
}
```

Or when have more than one potential type:

```go
switch v := a {
case Thing:
  // do something with v, which is a Thing
case Other:
  // do something with v, which is Other
default:
  // i have no idea what to do with this
}
```

## Sunday, April 25, 2021, 9:39:53AM EDT <1619357993>

Here's a trick for testing anything in Go  with `os.Exit()` (or
something like it):

```go
// go coverage detection is fucked for this sort of stuff, oh well, we
// did the test even if coverage falsely reports 50%
func TestExec(t *testing.T) {
  if os.Getenv("TESTING_EXEC") == "1" {
    err := Exec("go", "version")
    if err != nil {
      t.Fatal(err)
    }
    return
  }
  cmd := exec.Command(os.Args[0], "-test.run=TestExec")
  cmd.Env = append(os.Environ(), "TESTING_EXEC=1")
  err := cmd.Run()
  // ExitError is actually ProcessState
  // if e,ok := err != nil {
  if err != nil {
    t.Fatalf("process exited with %v", err)
  }
}
```

It's an amazing little trick since it actually calls its own temporary test binary (`os.Args[0]`) and has it just run that specific test. The environment variable is to prevent an infinite (but interesting) function recursion situation.

One thing that took me a while to notice is that there is *no* output whatsoever. All you get is the return value of the command that was executed. To get any kind of data back from the test of an executable like this you would need to create a temporary file and write to it. But still, this is pretty damn awesome for testing *any* executable.

I'm considering this for many of the highest level commands that I create that are difficult to test without actually calling them. Hell, you could even test things like tab-completion shell code generation that's designed to be evaluated by an `bashrc` file or something.

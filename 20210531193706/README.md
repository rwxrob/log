Hitting a need for `caller` from Perl in Golang. I've not run into a
language that deals with as elegantly. In conflict about how to pass
caller information to the method being called. I have had a
`Command.Call(args []string) error` method for some time. But I think a
using a `cmdbox.Call(name string,args []string,caller *Command)` might
be the way to go. This allows `cmdbox.Call` to set the most recent
`Caller` so that the methods themselves can inspect the caller Command.

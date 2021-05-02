## Sunday, April 18, 2021, 4:57:37PM EDT <1618779457>

I need to rip out the `subcommands` scaffolding of CmdBox and
reimplement it as *commands* that are mapped to an internal command
registry identical to the main `cmdbox.commands` but attached to each
`Command`. That is the graph-like command organization structure I was
looking for. Of course any of those commands could also have their own,
etc.

I can implement the shortcuts (for when tab completion isn't available)
at the same time.

Time for an overhaul.

## Sunday, April 18, 2021, 3:57:43PM EDT <1618775863>

I'm back to thinking there is really no need for anything beyond three
levels of depth for CmdBox:

```
<cmd> <subcmd> [<action>] [<parameters>]
```

I always stress out about the potential conflicts of composition at the
`<subcmd>` level.

Here's the deal.

A developer of a `cmdbox-*` module will not be aware (or care) about the
namespace conflicts of their command. Say someone creates one called
`print` that just prints whatever the argument is like echo. Someone
else will likely make one with that same name as well but it might send
something to a printer. Neither of these developers care (nor should
they) about the naming of their subcommand. That is something to be left
to the developer *composing* them together into a monolith to use, or to
an end user who installs the stand-alone version and just to decide
which one gets to be first in the path (or `mv` it to some other name).

The developer wanting to put them into a single monolith never gets the
opportunity to rename either of them during import since all that
happens at `init()` time long before `main()` is called. Nor does the
developer have anything they can declare to trigger a rename (since
declarations and initial assignment happen *before* `init()` time).

At the moment this leaves a developer in such a situation with a single
option: fork the `cmdbox-print` and rename it something else, then
import that one. Even though `cmdbox` files and repos are extremely
portable (often only a single file copy is needed if best practices of
keeping core code in separate libraries that only use the `cmdbox-print`
as the front-end UX wrapper) this solution is far from ideal. It's
rather annoying as well because usually *only one word has to change* to
give it a new name.

Time to go digging through the Go source for something that identifies
everything during the `init()` load process.

## Sunday, April 18, 2021, 2:48:11PM EDT <1618771691>

Hit another snap using containers with `you` as the account for this Go
stuff. They can't use GitHub without setting up an account to use it.
That's a complete killer of this learning lab container idea.

Looks like back to just plain old Markdown `README.md` pages that
describe what to do for the lab without any dependency on anything being
setup in a container. A derived registry of such labs would be easier to
maintain because it can point to repos or containers that have example
solutions all setup to examine but force the person learning it to set
it all up for themselves.

## Sunday, April 18, 2021, 2:32:58PM EDT <1618770778>

I'm seriously thinking about simplifying the entire lab concept into a
single `kind cluster create -f ...` since I'm headed down the
`docker-compose` path already and `kind` is definitely a better
investment.

I really prefer `docker` containers but the amount of setup, well, I
wonder if at that point it is just better to automate it with a shell
script and `kind`.

One of the reasons is long term. Say I get Gitea up and working in a
single container, what happens next? Eventually, I will have labs that
involve multiple computers, one with a database, another serving a REST
service, etc. In those scenarios I'll want to have the person learning
ssh/exec into a login system and from there do all the stuff. Each lab
at that point is literally a lab of computers abstracted as a `kind`
cluster by name. It's easier to help people learning get their heads
around the idea of connecting to that one login system and getting work
done.

I'm afraid at that pointing having a `lab` command is going to be the
easiest for people with zero skills to use to begin.

Another option is to have them just deal with the GitHub dependencies as
they would in the real world using private repos until they are ready.
That way they are learning the actual skills.

## Sunday, April 18, 2021, 2:21:20PM EDT <1618770080>

Arg, I hate that I have to build in GitHub dependencies on my own repos
into these labs. The whole point is for them to be stand alone. I really
don't feel like standing up my own git hosting service just to handle
all of these, but why the hell not. People might even end up realizing
they don't even need GitHub at all eventually. Imma try to add GitTea
setup to my base container and use that for Go code hosting. It it
works, it could be a good boilerplate for encapsulated labs that are
*truly* local only.

## Sunday, April 18, 2021, 1:56:26PM EDT <1618768586>

So frustrating sometimes that Go is *so* dependent on a Git hosting
service. Now that `go.mod` is pretty much mandatory, a move that is
worth of the Node governance team (what next `go_packages` or some
shit?). 

I'm frustrated because it completely defeats the possibility for
experimentation without *serious* scaffolding to prop it all up. This
makes instructing others in Go programming difficult to say the least
and overcomplicates experimental labs which have to either depend on an
Internet connection and something like GitHub or have to completely mock
that environment locally including a customized git account setup to
resolve the git addresses locally to bare repos or something.

## Sunday, April 18, 2021, 12:30:20PM EDT <1618763420>

I was fretting over naming conflicts and realized that they are
completely addressed by "registry" (side effects) package imports
because all the subcommands included for that CmdBox module are in that
modules package namespace. Each module gets its own package namespace
that is protected from all others. This resolves a problem I had with
the other method I was struggling with that had to come up with the same
sort of recursive tree within a single commands registry map. In other
words, `_` fixed *everything* without my really planning it that way. It
was just the right thing to do and turns out that works. The key is to
remember that every CmdTab command can only have one set of subcommands.

Renaming when there is a conflict can easily be resolved in the
`Add("mycmd","orig->another")` since the Add happens *after* the
`init()` of the  packages upon which that module depends.


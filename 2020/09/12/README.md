## Saturday, September 12, 2020, 10:02:03AM EDT [1599919323]

Decided to go for multi-streaming over Twitch subscriber building and
stick with just coding the software that is needed focusing on learning
through answering questions and demonstrating by example rather than
some particularly video curriculum. Watching the Bill and Ted [WiseCrack
video](https://youtu.be/GFD37HvGx6k) really helped me decide that this
is better overall for everyone's learning. When I write learning
material down it will mostly be references to where to find stuff, like
the phone book or user manual in Bill and Ted's phone booth. "You're on
your own, gentleman."

I'll have to change a few things about streaming:

* Need to be more aware that stuff is being viewed *everywhere*

* Might have to drop Twitch "affiliate" status but who cares I barely
crack 20 viewers at a time when I'm coding but the people who join are
*so* much better making for a much better "studio audience" for the rest
who I won't even see in the chat. You have to be good enough to find
your way onto my Twitch channel to even join.

* Do still need to write a mark-to-youtube tags converter so that I can
just upload the text file and get the same marks in YouTube since for
some reason Twitch does not push them automatically. They are pretty new
YouTube additions, so maybe that is in the works.

## Saturday, September 12, 2020, 7:59:09AM EDT [1599911949]

I'm reminded of the elegance of the idiomatic Go directory organization
for commands and library packages. Having a `cmd` and then putting
another directory with the name of the command (`pegn`) allows the
inclusion of user-land functions in between, inside the `cmd` directory
itself (`lint.go`). This keeps these files from cluttering up the clean
library directory at the top level containing them both. But even more
valuable is the ability to write tests and benchmarks within the `cmd`
directory for those commands so you don't have to recompile the command
itself every time you want to test and build some sort of additional
tests against the command execution instead of just another function
call. This meshes perfectly with my `cmdtab` organization as
well that promotes putting each subcommand into its own file.


## Monday, March 30, 2020, 12:30:03PM EDT [1585585803]

Have a look at Dave Abrams talk on POP as it relates to OOP.

Also need to look for [OOP operating
systems](https://en.wikipedia.org/wiki/Object-oriented_operating_system).
Still need to discover if any substantial operating systems have
survived that were written in pure OOP.

Also some [problems with
OOP](http://doc.cat-v.org/programming/bad_properties_of_OO) written in a
very formal way.

## Monday, March 30, 2020, 11:25:36AM EDT [1585581936]

Finally! What looks like a half-decent [Golang
tutorial](https://www.tutorialspoint.com/go/index.htm). Doesn't look
like it covers `go mod` though (but none do, not even the books).

## Monday, March 30, 2020, 10:25:38AM EDT [1585578338]

Need to look into Olive for video editing on Linux. And apparently
Blender is useful for video editing as well these days.

[tryhard-mode](rwxrob.mp4)

Came across the idea of having terminal/video themes based on the day.
Beginner day might be pleasant and with blue while TryHard day might
have red or tmatrix or something so that people can distinguish them
easily in the VODs.

Also need to look into YouTube-DL for downloading videos without need
for using the service. Also works for Twitch.

## Monday, March 30, 2020, 10:16:33AM EDT [1585577793]

While demonstrating how to deploy a site from GitLab to Netlify I
realized that the `rw` tool really needs to have a CI/CD mode so it can
be used from Netlify and applied to published Pandoc Markdown so that
the HTML is generated on Netlify and not stored in the Git repo itself.
That would allow people to keep Markdown notes in GitLab or GitHub using
the online editor there without *any* need to run the renderer locally.
It comes at the cost, however, of performance and would not be very
sustainable for very large knowledge nodes.

## Monday, March 30, 2020, 10:01:54AM EDT [1585576914]

Here's a case study from a group that ultimately realized capturing,
managing, sharing, and maintaining knowledge as Markdown source was a
[good
idea](https://caitiem.com/2020/03/29/design-docs-markdown-and-git/).

How to do run a TMUX within a TMUX:

1. start new tmux session
2. split pane
3. unset TMUX in pane 2 # this allows tmux in tmux
4. start new tmux session in pane
5. repeat 1-3
6. run tmux attach -t <target-session> # this is opens the shared
session



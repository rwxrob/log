## Wednesday, April 21, 2021, 11:35:21PM EDT <1619062521>

Still so torn over long or short directory names for KEG nodes. On the
one hand short makes easier to use but long is easier to search and for
web SEO. But, I really feel like this is the same rule with unique
identifiers. A good unique identifier should never have any semantic
value.

For example, say you create a blog post within a directory that matches
the title. Then the title changes. You are stuck with the URL that is
broken.

In fact, I'm inclined to go the other way. To give everything a unique
`isosec` identifier that will *never* change. Links to that particular
resource will always work and the name can change to whatever. This is
how file systems and databases work, but is it friendly enough for
people today?

I think so --- especially if you have some sort of index to them to look
into. In that sense it is very much a pointer.

If I take this to its conclusion you get something like this for KEG
content:

```
/dex
/zet/reg
/zet/<isosec>
/log/<isosec>
/lab/<isosec>
/doc/<isosec>
/term/<term>
```

This groups things by their type, not category, and not name.

## Wednesday, April 21, 2021, 11:26:30PM EDT <1619061990>

After playing with it some more it's clear to me working with real
clones is better for me than bare repos. I just have to add `../` to
work trees and the branch names end up looking like the main repo as
well in the directory. By adding a `-<issuenum>` I also am sure to get
something unique so that the branch names do not have to be crazy long.
Instead, I can save that for the lab directory names themselves that
land in slugs for URLs and need the length for SEO. So here's the
process:

1. Get into the main repo or clone if needed
1. `git worktree add ../<reponame>-some-thing-<issuenum>`
1. Change into the new work tree directory (which should tab complete)
1. Do the work and push to upstream so others can follow
1. Add comments to the issue for discussion
1. After testing, optionally create a PR, and merge into main
1. Remove the work tree and branch locally and remotely

## Wednesday, April 21, 2021, 10:57:07PM EDT <1619060227>

On second thought, we need verbose branch names to make any sense to
others sorting through them. I read about one persons process where they
add `-<issuenum>` to the end of the branch and use that to associate the
branch with an issue where all the conversation about the development is
taking place. I suppose that is a good way to go.

## Wednesday, April 21, 2021, 10:45:13PM EDT <1619059513>

I wonder if it would just be easier to create an issue for each main
branch of work and use that as the name instead of the long name. After
all, a work tree is an entire copy of the repo not just a subdirectory.

## Wednesday, April 21, 2021, 7:11:00PM EDT <1619046660>

Just learning about `git worktree add` (and company) today from @rwxeax
and I gotta say it is exactly what I was looking for. It allows the
ongoing work on several concurrent projects within a single repo. This
compliments (more than replaces) using a quick `git branch dev` (or
something) to do minor fixes and tweaks such as to my dotfiles. The
`worktree` approach is ideally suited for ongoing lab on
<https://rwx.gg> so that I can keep adding to them and only publish them
when they are ready. Combined with the zero-cognitive-overhead
Zettelkasten approach these Zettels can be added to the working trees
for such writing until an "article" (or book even) emerges. 

I do need to make sure that such branches are also pushed otherwise
there's a risk to losing your work along the way. Also this allows
others to participate on authoring that branch for a more collaborative
authoring experience that doesn't step on other KEG content.

## Wednesday, April 21, 2021, 5:04:51PM EDT <1619039091>

I wasn't expecting to realize that reading to learn sticks better ---
not only when I write about it and exercise/execute on what I've read in
intervals --- but when the source is from a book or graphic interface. 

I don't fully understand why, or if that is a general thing. It just
feels like I remember it better there is variety in the prose, font,
headers, and page layout. Perhaps that is part of the approach of the
Head First series and why they put crazy pictures in different places.
Our brains respond to those images and latches on to help our memories.

Moral of the story? When reading to learn look for stuff with lots of
visual interest. But when reading to get information quickly, definitely
use a text-based browser with a consistent font and search interface.

## Wednesday, April 21, 2021, 1:56:33PM EDT <1619027793>

I'm realizing that the standard (but slightly annoying) use of
`/usr/bin/env <whateverthefuck>` is really more relevant in the
container world than in other places because people might be using the
same thing in a vastly different location depending on which container
or host OS. That has always been the reason, but working with containers
lately has really brought that home.

However, people should write most things for containers in POSIX shell
which is *always* at `/bin/sh`.

Python is the real stinker in this bunch since could be any number of
places, and at any particular version. Thankfully, that is overcome by
containerization. And if you are creating a container then you can be
sure the script has the explicit path rather than `/usr/bin/env` before
you `COPY` it into the container.

So I guess, no, `/usr/bin/env` still sucks as bad as it always did.
Maybe people find comfort using it for installations and such, but if
you are using it for that you can take a moment and read through it, and
change the first line. After all, if you are not reading random
installation shell scripts before running the you will end up fucked
(like I was after running the Anaconda installer, what a piece of shit).

## Wednesday, April 21, 2021, 12:19:55PM EDT <1619021995>

TIL that `goodfirstissue` is a GitHub issue label/tag that indicates an
issue that is good *for contributors to get started with on the
project.* This is a very critical thing to get out to the community
because this is one way to get involved with Open Source projects, which
are also some of the best ways to improve skills and even find jobs. I'm
going to start making sure to tag issues that are particularly open with
this, as well as `helpwanted`.

## Wednesday, April 21, 2021, 10:55:54AM EDT <1619016954>

Noticed that the optimal settings to get a Dell Latitude 5411 to display
well from TMUX connected into my main streaming computer are the
following:

* Ubuntu Mono Nerd Font (there's a Windows variation as well)
* Laptop Font Size: 21
* Desktop Font Size: 30

Laptop ends up being 97 width while desktop is 95 but there are no
visible lines or anything if you use my borderless TMUX binary.

## Wednesday, April 21, 2021, 2:50:58AM EDT <1618987858>

66 is the number of thy counting, no more, no less. That is the biggest
a directory name can be without pushing my prompt beyond even being able
to display it on two lines. Lately, I've been prone to create rather
large directory names that match the titles word for word. 66 is a nice
round, evil number.


## Saturday, December 19, 2020, 6:22:10PM EST <1608420130>

Now that I've accepted my vimism fate (so long `vi` purism) there are
all kinds of possibilities that are just for my personal fingers. Here's
a rather obvious one. The default page down mappings are completely
brain dead and murder on my left hand, not to mention completely
unintuitive:

```vim
" Better page down and page up
noremap <C-j> <C-d>
noremap <C-k> <C-b>
```

And another thing, I'm fucking done apologizing for doing *everything*
in vim, even when helping beginners in the beginner boost. That's right.
I'm dropping VSCode completely from the *Learning Web Design*
walkthrough and never even discussing it other than to tell them to go
get an editor and install it.

## Saturday, December 19, 2020, 5:41:29PM EST <1608417689>

I cannot overstate my joy at discovering the rather obvious solution to
`git` committing to multiple repositories by adding extra origins.
Looking over old notes I had a TODO to setup a backup system for my git
stuff just in case. But just adding a single secondary origin addresses
that entire risk in a very elegant way.

In addition, I get a "green dot" on both GitHub and GitLab for doing so
and I can easily teach this technique to anyone in 10 minutes. No more
does anyone have to belabor the decision to host on GitLab or GitHub.
You can do both simultaneously and no one can tell the difference. They
can fork, add issues, and live their lives without the fear that I'm
going to rip away source. In fact, when I accept merge requests and pull
down the changes I simply need to `git push` to sync them to GitLab,
which is *by far* the most practical way to keep the repos coordinated.

Obviously, adding the canonical source is essential in the `README.md`
file --- especially for Go package modules.

## Saturday, December 19, 2020, 7:41:09AM EST <1608381669>

After discovering this cool little trick with multiple origins I thought
why not post to Source Hut as well. Then I saw that URLs have tilde's in
them by default which makes it impossible to have a meaningful, clean
URL for Go imports and other systems that depend on URL to source
repositories. That is a *major* oversight on the part of the Source Hut
designers. No wonder the very amazing `cview` project abandoned it when
they got serious. I guess some people have to learn the hard way.

## Saturday, December 19, 2020, 7:31:11AM EST <1608381071>

TIL that the easiest way to keep GitLab and GitHub in sync is simply to
push to both of them at the same time (instead of messing around with
all the GitLab mirror stuff):

```
git remote set-url --add origin git@github.com:rwxrob/auth.git
```

This is so much easier than everything I was doing before. I need to
remember to include this in `gits` when I get to that eventually.


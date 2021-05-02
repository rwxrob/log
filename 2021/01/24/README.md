## Sunday, January 24, 2021, 1:24:20PM EST <1611512660>

Now that we can just use `em` for media queries. It will save you a lot
of hassle to just use `rem` and `vh` and `vw` for everything *except*
media queries (use `em`). Looks like `px` are only used to set root font
size these days. I'm kinda glad all of this is getting standardized
(more than in 2014, at least).

Here's [ the
bug](https://medium.com/@barrypeng6/why-should-not-use-rem-unit-in-media-query-5645d0163ce5).

## Sunday, January 24, 2021, 8:45:53AM EST <1611495953>

Just added this repo as well with log and everything. The cool thing
about that is that I have a portable version of my KEG knowledge base
anywhere I want to go. Say I had to grab exactly one thing with me
before leaving the room. The USB stick would be in, constantly synced
with my most valuable personal content, with or without an Internet
connection. Doing the same thing for dotfiles as well.

Essentially, it's like having two core repos, one private and one
public, and making sure you have them with you wherever you may want to
go.

## Sunday, January 24, 2021, 8:35:09AM EST <1611495309>

Love the new local Git repo strategy for dealing with my private repos.
I documented it in my Git notes but here it is anyway.

```
cd # to get home
mkdir priv
cd priv
git init
git init --bare /media/rwxrob/06CF-482C/priv.git
git remote add bak /media/rwxrob/06CF-482C/priv.git
git push --set-upstream bak master
```


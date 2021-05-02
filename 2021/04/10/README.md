## Saturday, April 10, 2021, 4:25:21PM EDT <1618086321>

It seems that people tend to leave out the `v` when using semver tags
for Docker:

```
docker build -t shykes/myapp:1.0.2 -t shykes/myapp:latest .
```

It doesn't stop you from tagging however you want, just seems to be a
common practice. I've confirmed this with those who know best.

## Saturday, April 10, 2021, 4:21:03PM EDT <1618086063>

TIL that Docker will get getting rootless once it adds `cgroupsv2`
support. https://docs.docker.com/engine/security/rootless/>

## Saturday, April 10, 2021, 3:53:31PM EDT <1618084411>

If you get `denied: requested access to the resource is denied` with
`docker push` you probably forgot to add your account qualifier
(`rwxrob/some` and not `some`).

## Saturday, April 10, 2021, 3:45:01PM EDT <1618083901>

So it turns out the `_` in some images on hub.docker.com are because
they are owned by Docker. So I can't make one. 

## Saturday, April 10, 2021, 3:41:28PM EDT <1618083688>

TIL that the move to hard links for BusyBox is likely because a hard
link does not consume an inode preventing inode starvation on smaller
embedded systems and increase speed overall.

## Saturday, April 10, 2021, 11:02:35AM EDT <1618066955>

Another presentation needs to be "Git as LMS."

## Saturday, April 10, 2021, 10:42:16AM EDT <1618065736>

This whole learning lab container thing plays really nicely into the
name "skill stack" (SKILSTAK) since you are literally stacking lab
containers up in your "finished" pile.

## Saturday, April 10, 2021, 9:28:37AM EDT <1618061317>

"Edge Computing for Education" localized containers that do not require
network access that "phone home" when network access is detected and
allow local web site and applications development via local web browser
access or terminal command line.

I really need to get good at this stuff and turn SKILSTAK into a IT
Specialist training organization focused on Edgy Education. I can see
the presentation titles now, "Education on the Edge" or "Edge-U-Cation".

## Saturday, April 10, 2021, 9:11:45AM EDT <1618060305>

My goal is to drag Bob along with me (and maybe iscreaman) to ISTE in
2022 to present about the use method of using learning lab containers in
technical education for both practical and financial advantages.

## Saturday, April 10, 2021, 9:01:55AM EDT <1618059715>

The more time I invest in the creating Learning Lab Containers and fret
over the possible redundancies in written content I realize that we
might have been coming at this entirely backward. 

Traditionally, a bunch of written content is made and the *doing* stuff
(exercises, projects, etc.) comes after the fact as an afterthought as
if to say, "Read this first, then if you want do something with it." 

This makes sense because authors are arrogant bastards who put their
words in higher priority than your learning what they are blabbing on
about. (I'm probably guilty of this.)

Instead, what if the focus was *first* on what the *learner* is going to
do, and then on explaining what they *might* need to get them through
the learning on their own, *without a dependency on the author's words.*

So the idea is that all I make is modular *learning lab containers*
with all the description in `README.md` and then pull them all together
eventually into a guide or web site. Using this approach, I can apply
the best of Zettelkasten methodology to overall process of creating and
publishing interactive learning content. This allows an organic approach
as labs are developed as needed without thought or cognitive overhead
for where that lesson specifically fits into a larger outline. The
outline and organization can come later as you maintain a Zettelkasten
register of learning lab material.

Eventually, the amount of content will produce a site or book almost by
itself by just connecting the stuff that has been organically created
over time.

## Saturday, April 10, 2021, 8:14:31AM EDT <1618056871>

Now that it has become clear that containers are really the way to do
tech education by bundling everything into a `lab` the questions remains
what to call them, and what are some other simple conventions to keep
things consistent. Here's a start:

* Put them on GitHub (primarily) to find easily
* Name them `lab-` to make the easier to find
* Always include a `README.md`
* Keep the title simple and specific (<=52)
* Start every title with *Learn*


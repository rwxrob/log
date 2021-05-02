## Tuesday, April 27, 2021, 6:50:58PM EDT <1619563858>

Wondering what the best `interface{}` cast idiom is:

```go
var cmd *Command
if v,ok := a[0].(*Command); ok {
  cmd = v
}
if cmd == nil {
  ...
}
```

I'm thinking I need a snippet generator for that.

All I'd have to do is enter the following, position the cursor on that
line, and send that line to `snip` with `!!snip`. In fact, I think you
could do that without all the extra since you want fatal errors early
and the result would be the same --- especially if I'm trapping panics.

```go
var cmd *Command
```

And then perhaps only

```go
cmd := a[0].(*Command)
```

God, I cannot wait to get CmdBox finished so I can finish `cmdbox-snip`
for this sort of thing. The world needs a new snippet framework that is
entirely built from Go `text/template` templates and *fucking works from
the command line requiring no fucking plugins*.

## Tuesday, April 27, 2021, 6:45:47PM EDT <1619563547>

I need to make sure to add `yaf` and `yif` to the (new and improved) Vim
tutorial. They are so important.

## Tuesday, April 27, 2021, 1:32:31PM EDT <1619544751>

It really chafes me that the good people at GitHub have not the sense to
include underlines in their markdown rendering. People who have trouble
seeing color and contrast cannot see the links without hovering over
them. That's just fucking irresponsible.

I'm particularly pissed because I have higher standards than that and
this forces me to render all my stuff for the Web in addition to just
having a repo. I was hoping to put off that step until I got more
content into it. Nope. Have to do it right away (before the boost).

## Tuesday, April 27, 2021, 1:25:11PM EDT <1619544311>

One of the worst violations of Zettelkasten method is allowing the
unlimited size of a given Zettel. This doesn't create the cognitive
pressure required to push out the better thread and node graph of ideas.

## Tuesday, April 27, 2021, 1:18:50PM EDT <1619543930>

Need to add a conventions style guide for writing, probably under the
topic of my Zettelkasten method. Here's a standard way to link that also
prints well:

```markdown
* [[*See Luhmann's Own Words About Zettelkasten Method*]](https://luhmann.surge.sh)
* [[*20210427132158*]](/zet/20210427132158)
```

* [[*See Luhmann's Own Words About Zettelkasten Method*]](https://luhmann.surge.sh)
* [[*20210427132158*]](/zet/20210427132158)

I think this is the best way and allows for the same use on paper.
Obviously, linking to the zettel identifier directly is something
convenient for the register and for the less common need to interlink
specific zettels.

## Tuesday, April 27, 2021, 1:24:21AM EDT <1619501061>

Ya know, I really need to make the Beginner Boost its own repo. That way
I can tag it and have it just live on its own without the hassle of
being rendered. Hell, that would be plenty to have the boost until I
finish `kn` for the rendering later. But I don't even fucking need the
rendering. People need to get used to following things in GitHub anyway.
That way people can be notified if and when things change. No need for
the extra publishing hassle. It also means that others could
collaboratively add content to it. Looks like
<https://github.com/rwxrob/boost> it is.

## Tuesday, April 27, 2021, 1:03:08AM EDT <1619499788>

Decided to go with a traditional "curriculum" outline for the Beginner
Boost content. I'm estimating using 25 minutes on each line item (my
standard ZettelCast and Pomodoro timer amount). The boost runs from
May the 4th to July 31st, a little over 12 weeks (64 days total). Each
day will be two hours long, but I'm only planning three ZettelCasts per
day (even though several will be very far under the 25 minutes). That's
192 total ZettelCast sessions and videos for a total of about 80 hours
of total video content.


```
      May 2021             June 2021             July 2021        
Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  
                   1         1  2  3  4  5               1  2  3  
 2  3  4  5  6  7  8   6  7  8  9 10 11 12   4  5  6  7  8  9 10  
 9 10 11 12 13 14 15  13 14 15 16 17 18 19  11 12 13 14 15 16 17  
16 17 18 19 20 21 22  20 21 22 23 24 25 26  18 19 20 21 22 23 24  
23 24 25 26 27 28 29  27 28 29 30           25 26 27 28 29 30 31  
30 31                                                             

```

Originally, I wasn't going to cover the actual stuff, but rather send
them on their way to learn it on their own. But I figure covering my own
sample exploration of the material and concepts and skills will be
something they can put on to get them excited to do their own
experimentation (as in, the Bob Ross school of coding).

I suppose I could go ahead and throw it all up on Udemy as well even if
I make it also free on YouTube. I'll have to look into that. It is
likely that would not be that much more work and would just put it in a
place where people will search for it. (Ouch my pinky is sore from Yoga
today.)

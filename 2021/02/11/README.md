## Thursday, February 11, 2021, 6:58:18PM EST <1613087898>

Finally finished [`rwxrob/conf-go`](https://github.com/rwxrob/conf-go)
to do all the JSON configuration conventional dirty work of storing
stuff in the right place.

## Thursday, February 11, 2021, 5:24:02PM EST <1613082242>

Looks like Discord has really fixed their broken sound and video issues
that forced me to move to Skype for mentoring. It's a good thing too
because I am planning on doing live mentoring with small groups of no
more than three. The first group looks like it will be a bunch of 12
year olds learning to code and make videos games using Phaser, which
should make for great viewing by a number of people who watch Twitch and
YouTube. We will all be in the same video chat room on Discord so people
can join and watch the different participants rather than just waiting
for me to show them on the screen.

So far it is being well received by the candidates, but I need
authorization from the parents to do it since it will be public and
saved forever on YouTube. I'm giving them a break on the cost since they
will be combining the time. Most of theme would do it at the same rate
just to get the Internet channel exposure (these first three already
have Twitch streaming setup).

## Thursday, February 11, 2021, 4:11:46PM EST <1613077906>

Still experimenting with live streaming during "monitored mentoring
sessions" that only require me to monitor the screen next to me and
ensure they don't get stuck during their work. It requires that I mute
the live stream currently because I can't risk having someone ask for
help and having it come through the desktop audio. 

This morning I forgot that I was muted in OBS, so there's that to
remember.

Also, after going through a "stand by" screen need to remember to bring
up the live streamed screen and not the mentored one. It's not really
that hard, just something to remember.

Just noticing as well that my `screenkey` setup needs a different mode
for monitored mentoring since it shows up on the other screen and not
the one that is streamed.

## Thursday, February 11, 2021, 1:27:22PM EST <1613068042>

Fastest method to get the keys from a Golang Map:

```go
// Keys returns a sort list of keys from the Data
func (js Config) Keys() []string {
	keys := make([]string, len(js.Data))
	n := 0
	for k, _ := range js.Data {
		keys[n] = k
		n++
	}
	return keys
}
```

The `make` gets rid of the slower requirement for an `append`.

## Thursday, February 11, 2021, 8:53:59AM EST <1613051639>

Noticed that there is `path.Join()` and `filepath.Join()` and I don't
know the difference other than `filepath` is the one used in every
example I've seen in the last three years. 

I found some of my old code that uses `path` and changed it.

Thanks to @afrology from stream I learned that `path` observes slashes
while `filepath` does the expected UNIX thing and cleans them up along
with dots.


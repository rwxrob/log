## Monday, January 25, 2021, 7:06:50PM EST <1611619610>

If the future is meta programming (writing declaration of what programs
should do) then the future syntaxes will be JSON and YAML and things
like Protobuf because they are the most declarative languages on the
planet (along with SQL).

More of our time as developers is being spent connecting and
configuring things rather than writing new code.

Could the future of IT be *mostly* configuring things rather than
building new things? Eventually most things will get built, then it's
just a matter of making it all work together.

I mean, companies are using third-party applications and open source and
just configuring them for their environments. Less money on new
development, and more on configuration and maintenance. 

I wonder if that means the SRE role actually has more of a future than I
imagined. Perhaps it just means that the "developers" are sort of like
database administrators where the databases are clusters of
configurations and domain models.

It probably means that the new development opportunities will be
associated farther on the edge where hardware sensors and things still
need to be coded at a lower level. Database integration is getting
easier and easier.

## Monday, January 25, 2021, 6:54:09PM EST <1611618849>

There is just *nothing* out there to do raw YAML custom schema
validation. I've been searching for an hour and asking on the `#yaml`
IRC channel.

I did discover that the JSON-Schema proposal is moving along in the IETF
and will likely be the best way to *universally* define precise schemas
for such data.

And there's nothing that says I can't write a JSON Schema definition in
YAML (which will be way easier to read).

It's pretty clear at this point that YAML and JSON are here to stay, a
forced marriage made in tech Hell.

## Monday, January 25, 2021, 3:14:23PM EST <1611605663>

Decided to go with `rec` within a `log` directory for saving video (or
audio) recordings. There's definitely a difference between a video and a
recording. A video generally means something that was produced for
publishing (despite the generic term). The term "vlog" has been taken by
people talking to the camera mostly. So it seems like "recording" is a
most accurate term for what I'm doing, which is just recording what I'm
doing. You can't really call it a "stream" because it's a recording of a
stream.

## Monday, January 25, 2021, 9:01:28AM EST <1611583288>

Recently learned that `apt search <thing>` is not *actually* the same as
`apt-cache search <thing>` (which works better). I had read that
dropping the `-cache` was the same thing. But that's a lie.

It could be true that this is the way it is on Linux Mint. But it
definitely does not work the same way on PopOS!

## Monday, January 25, 2021, 8:50:51AM EST <1611582651>

I continue to be intrigued by the [Vivaldi web
browser](https://duck.com/lite?kd=-1&kp=-1&q=Vivaldi+web+browser) ---
particularly because of the quality of the people who continue to
recommend it to me. I think I need to give it a look.

## Monday, January 25, 2021, 8:26:55AM EST <1611581215>

One of the main cleanup activities I must do is change all my scripts
library to have zero insignificant dependencies on anything else, such
as for dumb shit like colors and usage output. Makes is much harder to
share them. 

This means I need to create tools for adding these useful things more
easily in an independent way, like snippets.

## Monday, January 25, 2021, 8:01:26AM EST <1611579686>

By the way, I forgot to mention that Ez-Lynx is still on (a simple shell
script that configures an installation of Lynx for a specific user). I
just cannot give up how much easier Lynx is to read than W3M because of
indentation of paragraphs and such that seems to be hard coded.

## Monday, January 25, 2021, 7:51:23AM EST <1611579083>

Having that thing where I have so much to get done that I don't know
where to start. Most important thing I have go get done is a full online
profile cleanup so I look respectable to SMEs vetting my job
applications next month.

I'm on it.

## Monday, January 25, 2021, 6:38:14AM EST <1611574694>

Been meaning to set a key binding for `:set paste` for years. Using
`:map` shows all the Vim keybindings, which is a start. I've tried `set
paste` in my `.vimrc` and learned just what a bad idea that is because
it turns off all mappings while in insert mode (which usually isn't an
issue but I've become partial to `zz` and `jj` and the like (in my old
age) for replacing the pinky-stomping alternatives to escape. (Don't
worry I'm still plenty able to use `Cntl-[` or `ESC` when the situation
requires.

Looks like I'll be trying out Tim Pope's [unimparred
plugin](https://github.com/tpope/vim-unimpaired) for a while.

## Monday, January 25, 2021, 6:36:00AM EST <1611574560>

Adding the concept of shortcut to my KEG node schema for bookmarks.

```yaml
- T: Gordon's Art Work
  L: https://www.deviantart.com/zephyrwork
  B: gordon
```

## Monday, January 25, 2021, 6:27:17AM EST <1611574037>

Just discovered [surfraw](https://surfraw.org) and I'm already sold on
their introduction line:

> Surfraw liberateur is capable of navigating speeds that leave GUI
> tainted idolaters agape with fear and wonder.

In fact, the name is apparently an acronym for *Shell Users
Revolutionary Front Rage Against the Web*. 

Vive la revolution!

Now that's my kinda people.

Looks like it is my `?` and `??` and `???` to the nth degree and
includes pretty much everything most terminal users would ever care to
search these days, but it's an interactive shell rather than something
that will get saved in my shell history.

It's also hosted on GitLab for all the right reasons (which
unfortunately are overwhelmingly rendered [irrelevant](https://www.youtube.com/c/rwxrob/search?query=github) to most modern
developers.

## Monday, January 25, 2021, 5:10:30AM EST <1611569430>

Through random experimentation we have concluded a few things about Lynx
and w3m:

* W3M is absolutely the best *default* experience.
* Lynx requires *tons* of customization to be usable .
* W3M's annoying lack of indentation is unreadable.
* Thou shalt lie about user-agent in either one.
* W3M has way better information (`=`).
* W3M has way better internationalization support.
* Browsh is out of the question since requires Firefox.
* W3M loads CSS if it can be found (ex: table border).
* There are a ton of `-o` options with W3M still to consider.

By the way, here's a user-agent that works:

```
"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_8_0) AppleWebKit/537.1 (KHTML, like Gecko) Chrome/21.0.1180.79 Safari/537.1 Lynx"
```

Make sure you put that all on a single line.

## Monday, January 25, 2021, 3:45:47AM EST <1611564347>

Look like `w3m` might actually *finally* be better than Lynx. People
have claimed it was better for years, but the last time I compared it
was no contest. Up until recently my reasons for picking Lynx had more
do to with bad decisions from the `w3m` team:

* It tried to hard to render graphics
* It was just slower for text browsing
* It wanted to be a graphics browser, still

But it turns out that many of advantages of `w3m` are overtaking Lynx:

* Better support for HTML5 elements
* Zero tweaking out of the box
* Vim bindings by default
* Modern concurrency
* Just plain faster
* Image loading no longer automatic


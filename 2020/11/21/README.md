## Saturday, November 21, 2020, 10:25:49PM EST <1606015549>

Holy shit. My fan just took off from just one Restream preview window
being opened and when I closed it everything is fine. Must have hit some
kind of threshold.

## Saturday, November 21, 2020, 8:52:11PM EST <1606009931>

Struggling with how to handle the possibility of multiple redirections
happening at the same time. At one point I had each `App` have their own
port so as to not conflict. But since they all have to do the same thing
I think having a map with the `state` in it would be better mostly
because it is wasteful to fire up multiple HTTP servers when one is fine
so long as it knows about the different sessions it is dealing with.

One way to deal with it is to timeout the entries if no one asks about
them within a given amount of time. I do think `state` should be the
index key for those because you might theoretically have more than one
redirect in different flows and need to make sure they line up.

## Saturday, November 21, 2020, 7:01:56PM EST <1606003316>

Live coding has really caused me to do all the things I have been
meaning to and just been putting off. For example, just the tweaking of
simple stuff like `rulerformat` makes reading vim status *so* much
easier (and frankly *way* better than that fucking airline shit, which I
did play around with for a while, and then came to my senses).
Ironically, the transparency made me create a better configuration all
around.

The reason, I believe, is because everything I am doing is to make it
easier for a non-initiate to understand and therefore I end up making
things easier for me as well.

## Saturday, November 21, 2020, 6:55:23PM EST <1606002923>

So after a request to fix `screenkey`, which after what looks like a
full hour of futzing with it (for the better) I found this great
[documentation on
it](https://github.com/wavexx/screenkey/blob/master/README.rst). Turns
out the thing is written in Python. Anyway, TIL that if you hold down
two of the special keys (control, alt, or command) that it turns it off
temporarily so that passwords are not printed to the screen. Obviously,
that requires a high level of attentiveness. But I think if I do it that
I could get used to it --- especially when I'm doing a lot of note
taking and don't need to make all of that visible. Like just now.

## Saturday, November 21, 2020, 5:47:37PM EST <1605998857>

I really need to get `screenkey` working in a way that is safe. Ideally
it would shut off if certain applications were running, or if I had
certain scenes set in obs. I do have a good way to turn the screen off
these days so that is not as big of a deal, but it would be absolutely
ideal if anything from my password manager never printed. I need to test
it because I don't think cutting and pasting things ever gets sent to
`screenkey` in the first place. Definitely need to add it to my *Focus
Mode* streams.

## Saturday, November 21, 2020, 5:09:39PM EST <1605996579>

Even though I fucking hate Dev.to because of their shitty, unnecessary
dependency on JavaScript to read anything on their *forum* site (Tim
Berners-Lee is wincing even now to learn about it), I did find this nice
[simple
benchmark](https://dev.to/pmalhaire/concatenate-strings-in-golang-a-quick-benchmark-4ahh)
I was too lazy to do myself. Long story short, always use `+` to
concatenate strings when you can.

## Saturday, November 21, 2020, 4:26:30PM EST <1605993990>

I was typing yet another `if err != nil` when I remembered seeing a tool
somewhere about that. While off researching it I looked through the
rather long list of [Go tools](https://godoc.org/golang.org/x/tools) and
realized I *really* need to do a meticulous review of every tool there
is. For example, `goimports`, which is now built into `vim-go` by
default has saved me *hours* in fixing my `imports` section. Now I don't
even have to think about it. I also just remembered there *is* a way to
move packages and resolve all the package name changes. It's `gomvpkg`.
I still haven't found anything for `nil` but the other stuff is worth
mentioning.

## Saturday, November 21, 2020, 9:31:38AM EST <1605969098>

I feel like I'm always that guy that obsesses about something that is
broken with an API enough to want to do my own. Just realizing that the
current `oauth2` standard Go package has nothing in it about
*refresh_token* expiration (not `access_token` which is fine). There is
a built in assumption that refresh tokens don't expire. I noticed that
the Restream API even sends the expiry of the refresh token as well as
the access token, but the Go package has no concept of it, and neither
does the built in token refreshing in the returned `http.Client` it
gives. The place that I would check doesn't even return an error so I
have to check for random unauthorized errors from the client and then
trigger a new `.Authorize()` call.

## Saturday, November 21, 2020, 4:53:17AM EST <1605952397>

While writing all the Oauth2 stuff it occurred to me that, well, this
has been around a long time and *surely* someone else has already
created a way to debug Oauth2 flow stuff (that requires a web server).
Sure enough <https://oauthdebugger.com/> exists and does exactly that.
No need to create my own mock server. I don't suffer from
not-invented-here syndrome *that* badly. God I wish I would have found
that last week, but this journey has been extremely educational.

Except for when I just tried it looks like it is only for testing
*servers* not client implementations. 

## Saturday, November 21, 2020, 4:17:39AM EST <1605950259>

I find myself once again annoyed that I cannot *write* YAML reliably in
Go (or any language for that matter). The complex nature of YAML with
comments and such makes it impossible to do anything with.

I know the right thing to do is just to edit the JSON (like all VSCode
plugins seem to allow). But I just kind wish YAML did it. 

TOML isn't any better.

@taniwah3 reminds me that YAML --- the full specification --- actually
allows for the execution of code and really should never be trusted. He
mentioned needing a spec for "light YAML" and I could not agree more.
That kind of thing would be short work once PEGN is complete. Hell, the
parser would even be automatically generated from the spec. Looks like
something to add to my wish list.

## Saturday, November 21, 2020, 3:42:33AM EST <1605948153>

Added more to the [`gotmpl`](https://gitlab.com/rwxrob/gotmpl) wish.

Also, I am realizing that base64 encoding the cache files for `auth` is
really just a waste of time because if anyone sees it they can get the
secrets from it anyway. So rather than test and debug all that just
going to skip it for now and put that effort into getting an *actual*
encrypted cache working later.

## Saturday, November 21, 2020, 2:05:22AM EST <1605942322>

I'm really fighting the draw of OOP right now. Like having been in a
cult. "It is me or the cult?" I'm inclined to put all the `auth` package
functions as methods on the new `Collection` struct. Ugh, it just makes
too much sense. I feel another branch coming on.

## Saturday, November 21, 2020, 1:55:28AM EST <1605941728>

After a fair amount of research it looks like I still have to maintain
some form of cached key generated from the YubiKey, so that complicates
matters a bit more than I want to inject into this project at the
moment. I really need to look around more for high-level Go modules that
manage this stuff from the terminal rather than some fucking Python
graphical application (like `yubikey-manager` does).

So, for now, I'm back to my medium-grade obfuscation, which is really
just client secrets and tokens in flat text on disk, but that is what
all web browsers do, so it isn't *that* bad. I'll have to quell my
security OCD for the moment so I can get something done. I went into
this just wanting to grab the Websockets chat messages from Restream,
and here I am off in the woods looking up `cgo` libs for security
devices. I do love a good rabbit hole, after all they are the best way
to learn --- especially when there really isn't any kind of time
constraint on this other than my own. While I do beat myself up for not
getting shit done oft times, I do have to take a moment to celebrate how
intensely fortunate I am that I even have the fucking drive to go down
*any* rabbit hole. Just a cursory glance of whatever everyone else is
doing on this fine Friday night proves my point. I'm so glad so much of
that doesn't draw me anymore. I would rather study the FIDO2
specification than *anything* else right now. Okay, that is pretty
demented. \*sign\*

One *really* good thing that came out of that entire rabbit hole was
putting everything into a single-file collection. I would have
implemented the whole thing without doing that before, but the need to
have everything in a file is what allows the whole file to eventually be
encrypted. So yeah.

## Saturday, November 21, 2020, 1:08:04AM EST <1605938884>

I'm a bit conflicted whether to use YubiKey (FIDO2 U2F) in my little
`auth` module because doing so automatically adds a `cgo` dependency
removing built in ability to compile cross-platform (as Go allows by
default, one of its greatest strengths). I figure I'll get it working
and then add some sort of build parameter for those who do not want to
do this. Besides, they may have covered this in the `libfido2` Go
module that wraps the C library. I see a bunch of platform specific
stuff in there. I do know that building will require installing the
`libfido2-dev` package on Linux at least, which leads me to believe the
build is no longer truly cross-platform. We'll see.

## Saturday, November 21, 2020, 12:21:15AM EST <1605936075>

Found this interesting [blog
post](https://blog.madewithdrew.com/post/statically-linking-c-to-go/)
from a self-proclaimed "non C coder" who managed to use cgo's static
linking despite how spread out all the information is about it. It's
definitely on my todo list and makes me even more sure that Go is the
right general purpose, statically compiled, C-compatible, strict-typed
language to recommend. The level of ease with which you can include C
code is just astounding. You lose cross-compilation ability, but you
lose that anyway when incorporating C libraries for anything. The world
really hasn't latched onto this, it seems, like they have to Python C
stubs, but then the Python world realizes how easy it is to wrap C code
with Go I have a feeling the momentum will just continue. NumPy,
TensorFlow, etc. all make Python popular only because Python has good
and full bindings for them. But it's only a matter of time before Go
catches up. All the ability is there. I imagine Rust will be a better
pick for most *really* high performance stuff, but I need to check out
the garbage collection tweaks and tuning in cgo before making any
conclusion there.

And god do I hate C++, here's yet another reason to hate it:

> cgo can link against C libraries, but not C++ (see swig for this)


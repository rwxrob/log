## Friday, November 13, 2020, 11:36:43PM EST <1605328603>

A few conclusions about integrating <https://developers.restream.io>
with my terminal-based live streams:

* Websockets API is read only for chat but do-able
* No part of the API support posting chat message to everyone
* Using "Bot" will sync any messages from service to all services
* Bot syncing does include emojis (but not Twitch icons)
* Still okay with terminal only (emojis) because reasons
* Twitch IRC is likely the best for posting messages
* *Eventually* should encrypt the client secret

Wondering if the *primary* chat entry tool should just be Discord since
it has the best support for Markdown including code formatting. Then
when I need to send something quickly could just use something to paste
into Discord or could have a Discord bot that does the post for me. But
it's really not that hard to post to Discord.

## Friday, November 13, 2020, 6:21:18PM EST <1605309678>

Been helping a really talented artist get back into web game development
with Phaser3 and I have to say they have really improved the
[documentation of the API](https://photonstorm.github.io/phaser3-docs).
Looks like they also discovered JAMStack web publishing (finally). But
my biggest impression is just how amazing TypeScript makes projects of
this size.

TypeScript makes a lot of sense for a specific type of project, one that
is rather large and requires a *lot* of code but that *must* be written
in JavaScript, such as pretty much ever modern web-based game.
TypeScript has replaced Flash as the go-to language for such things.

Looking at the Phaser3 codebase I'm reminded that there *is* a specific
requirement set that lends itself well to the object-oriented paradigm.
Anything involving games fits very well into that space. Hence C++, C#,
and even Rust popularity with game development. Another (lesser) case is
stuff that involves graphics programming of any kind given that the GUI
is abstracted into widgets. This is the very reason SmallTalk was
created in the first place inspired by other similar systems from the
[Elgelbart's Mother of all Demos](https://duck.com/lite?kd=-1&kp=-1&q=Elgelbart's Mother of all Demos).

## Friday, November 13, 2020, 6:16:25AM EST <1605266185>

TIL that `strconv.ParseInt("0x1A",0,32)` is a thing. The `0` says to
infer the base from the prefix of the string. Not intuitive, but staring
me right in the face in the second paragraph of the `strconv`
documentation.


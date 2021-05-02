## Thursday, November 26, 2020, 10:34:07PM EST <1606448047>

The more I think about this `live` tool and where to put all my emphasis
when it comes to the chat portion of the stream, the more I think
Discord is really the way to go. Here's some reasons why:

1. Discord is *primarily* a chat service
1. Discord keeps messages around and if you pay even longer
1. Discord enables long-term connections
1. Discord supports anonymity for those who wish
1. Discord is something people already have
1. Discord supports limited Markdown in messages
1. Discord is informal and fun
1. Discord is stable ... enough
1. Twitch is forcing people to watch long ads
1. Twitch is moving *off* of IRC
1. Twitch has zero transcoding, YouTube is free
1. Twitch had better discoverability, but not that much
1. Twitch API is wonky and inconsistent
1. People will join the community, not just twitch live stream
1. People will have a place to go when the stream is offline
1. People can chat with others in different servers while watching
1. Discord server becomes a community home

I figure if I make a bot that represents myself (which I need to check
on, because at one point they seriously frowned on that) then I just
have to have the bot login and post everything to Discord. Then I can
relay everything from Restream to Discord or let the Restream Bot do
that instead. 

## Thursday, November 26, 2020, 10:23:43PM EST <1606447423>

As I dive back into Websockets in Go it looks like the landscape has not
changed that much from the last time I looked (which was like four years
ago or more). Here's a [good
comparison](https://www.mindinventory.com/blog/how-to-use-websockets-in-golang/)
if anyone else is looking. The low-level GOBWAS looks very interesting
for things that are much more demanding of performance. But for my
little [`live`](https://gitlab.com/rwxrob/live) utility that sucks down
the Restream.io chat via websocket buffers I am thinking
[`gorilla/websocket`](https://duck.com/lite?kd=-1&kp=-1&q=`gorilla/websocket`) is still the way to go. It's an external
dependency (unlike the standard library version) but oh well, I have at
least two other dependencies already.

## Thursday, November 26, 2020, 1:59:49AM EST <1606373989>

So while trying to fix my <https://rwxrob.live> page with the
Restream.io embed that is broken I randomly found the place in my Twitch
preferences where I turned on "only verified email addresses can chat"
and it got me to thinking, "Humm, I wonder if that is why the people in
my chat are so much more well behaved than before." Maybe not, maybe
just because there are a lot fewer people, higher quality people. Just a
thing that made me go, "Huh."


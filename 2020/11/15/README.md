## Sunday, November 15, 2020, 7:54:50PM EST <1605488090>

God I hate when even an IETF RFC can't be in sync with what everyone
uses out there. Something as simple as `expires` with the UNIX epoch
time stamp is *not* part of the standard. Instead you get the completely
brain-dead `expires_in` but from what time? Thankfully at least
Restream's API gives an `expires` with the exact second, but otherwise
it has to be guesstimated, which is why I'm renewing if within 10
minutes just to be safe. I'll use the `expires` field if there is one,
otherwise I'll calculate it before caching and keep that 10 minute
buffer for renews to play it safe.

## Sunday, November 15, 2020, 5:36:06PM EST <1605479766>

I swear, object-oriented programming has ruined me. I *still* think of
everything as a object with methods from the very beginning when just
data and functions will be better most of the time. Caught myself this
time and really simplified the `oauth` domain model, but I really have
to keep on it.

## Sunday, November 15, 2020, 2:32:40PM EST <1605468760>

Noticing that <https://developers.restream.io> really puts a lot of extra
unnecessary, redundant shit into their token JSON. The
[RFC](https://tools.ietf.org/html/rfc6749#section-3.3) thankfully calls
out what *must* be included. All this is going into
<https://gitlab.com/rwxrob/oauth> so I don't have to remember it all the
time.

Here's all that is specified:

```json
{
  "access_token": "7e61c8a5e2f99404730c511de6580412e618da35",
  "expires": 1520280099,
  "expires_in": 3600,
  "refresh_token": "0e633c3343a2df84b1526f4c2e6993ff17e05cab",
  "scope": "profile.default.read channels.default.read chat.default.read stream.default.read",
  "token_type": "Bearer"
}
```

I also noticed that only `refresh_token` is specified. There is nothing
about communicating how long the `refresh_token` is valid before it
expires. It appears the protocol specification says *nothing* about
that. So you end up with a bunch of extra stuff for it that is someone's
idea of what it should look like instead of anything reliable. 

I'm going to take the approach that one can simply assume the refresh
token is for an extended period of time and when attempting a refresh
with it if there is a failure than simply grab an entirely new token
using the full Oauth2 user authentication cycle.

## Sunday, November 15, 2020, 2:19:36PM EST <1605467976>

One of the ways that Oauth2 is so broken is the assumptions surrounding
the `redirect_uri`. While there is a caution and explanation as to why
the TLS protocol (tunnel encryption) is not required, most applications
I have used so far use query strings that contain the token rather than
attempting to post to the URL instead, which is a really good thing
because without that little over site using Oauth2 for *anything* from
the command line would be impossible. As it stands, we can always set
the `redirect_uri` to `http://localhost:8080` and bring up a temporary
server to receive the data as if it had been included in the response
itself. 

I cannot figure out if sending the `code` as a query string was by
design or just a happy fluke. Actually, it makes more sense when you
consider that we do not get a direct response from the user
authentication step, which requires the use of the web hook, which, if
it had been POST, would *never* have worked on local `redirect_uri`
locations.

Lucky for me there is no way they can ever change that without releasing
a *very* breaking change to the entire framework.

## Sunday, November 15, 2020, 12:50:23PM EST <1605462623>

I *really* need to remember the following for `tmux`:

* `!` - `break-pane` default key (instead of `z`)
* `list-keys` - lists all the bindings

## Sunday, November 15, 2020, 12:09:31PM EST <1605460171>

So turns out Oauth2 is quite a
[mess](https://en.wikipedia.org/wiki/OAuth#Controversy) but it is
clearly the standard and so need to create it. Creating a module for use
with the terminal command line to get over as much of the web dependency
as needed. Got is working, but now need to create a struct to match the
RFC for what a *token* is.


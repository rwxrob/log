## Sunday, September 20, 2020, 4:16:42PM EDT <1600633002>

Apparently there is no good way to allow people to subscribe to anything
you are doing. There really needs to be an open alternative to all the
greedy Patreon clones.

## Sunday, September 20, 2020, 12:39:29PM EDT <1600619969>

I really need to write more about the critical problems of depending on
Golang's internal `json.Unmarshal()`. When there are no parse errors but
the types don't match up the result is a struct that is left with empty
or zero values and no indication of the error. One person reported this
problem in an enterprise application that misinterpreted `"true"` a
`false`" because it was a string instead of a boolean and therefore was
ignored. 

The remedy to this potential problem is to *always* check the object
after unmarshalling it to ensure it has what you need. In my case. I'm
just unmarshalling into a plain `map[string]interface{}` and
individually checking for values that I then assign. This is safer than
the reflection method that uses tags and not any slower. For higher
performance unmarshalling the internal reflection based code is horrible
anyway and you likely want to create your own JSON parser to get around
the several substantial quicks of it.

## Sunday, September 20, 2020, 11:01:41AM EDT <1600614101>

Been thinking (and discussing) the challenge of testing applications
that depend on services with credentials and interactive HTTP sessions.
Need to look into that more, particularly "cassette/vcr" libraries with
HTTP request playback (as mentioned by
[\@purplepinapples](https://twitch.tv/purplepinapples),
[\@elgemingu](https://twitch.tv/elgemingu), and others).


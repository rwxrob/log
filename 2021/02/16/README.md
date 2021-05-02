## Tuesday, February 16, 2021, 10:51:00PM EST <1613533860>

Dropping the live chat from YouTube was the best thing I've done
with YouTube all month and not because it silenced everyone, because the
resulting videos have the amazing Chapters sidebar that is disabled if
you have live chat in your archives.

## Tuesday, February 16, 2021, 10:47:37PM EST <1613533657>

What if we made the logo for KEG to be a bearded spider in a web
drinking beer from a keg?

## Tuesday, February 16, 2021, 10:24:21PM EST <1613532261>

Once again @green_jenny schools me on stuff I've sort of heard about but
cannot remember where:

[Go To Considered
Harmful](http://www.u.arizona.edu/~rubinson/copyright_violations/Go_To_Considered_Harmful.html)

## Tuesday, February 16, 2021, 8:05:14PM EST <1613523914>

Rairden found the Gamozo clip of him ripping on Python. Makes me
chuckle and remember that *serious* hackers and 0-day finders "fucking
hate Python." [Here's the
clip](https://clips.twitch.tv/RespectfulCourageousHorseradishBudBlast-9EU55E2e3PKrpdGi>.

## Tuesday, February 16, 2021, 5:30:35PM EST <1613514635>

Reminded that when doing my cloud hosting evaluation that the strength
of the CLI API is really a core criterion. AWS apparently dominates in
this space, which explains why I hated it so much. I only used their
shitty web API the entire six months I tried it.

## Tuesday, February 16, 2021, 5:07:55PM EST <1613513275>

Watching the views dynamically go up and then decline in YouTube is sort
of funny. People come on in looking for coding and find a bunch of
documentation and specification writing. But that's required as well.

## Tuesday, February 16, 2021, 10:49:55AM EST <1613490595>

Looks like the RFC3339 format (a highly specific form of ISO8601) does
not allow for removal of the delimiting dashes and colons, but colons
appear to be a problem for more than one filesystem and are not friendly
to URLs (even though they are allowed).

This leaves me with the decision for log file names that must work with
both.

## Tuesday, February 16, 2021, 12:52:59AM EST <1613454779>

Watching some great "hacker" streams and they all start out the same:

* Big gaudy prompts that are unintelligible
* Python with all the intellisense maxed out
* "Try hack me is the shit!"

I love what they are doing and can't find any fault with them doing it
live. Makes it so fun. Just makes me chuckle a bit. Here I am feeling a
little bit indulgent changing my dollar prompt from white to gold.

## Tuesday, February 16, 2021, 12:42:49AM EST <1613454169>

I really don't know why it took me so long to turn back on that window
titles and status bar in tmux now that I've switch back to windows
instead of panes. So glad I did though. It will really help everyone
watching as well because they'll be able to see what is actually
running. 

By the way, that is yet another reason to use `exec` in scripts as the
last thing you do because it updates to the correct name in the tmux
status bar rather than just putting `sh` for everything.

By the same token, a compiled Go program will *always* be better than
any script because the binary of a script is always just the name of the
interpreter and not the actual name of the code that it is running. 

I especially love that people will be able to see more and more `perl`
appearing in the status bar as well.

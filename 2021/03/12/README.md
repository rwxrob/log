## Friday, March 12, 2021, 2:15:49PM EST <1615576549>

I finally figured out where OBS goes when when I accidentally go to
another Gnome desktop. It minimizes it. Just have to 'Show OBS' from the
icon, but for a while I thought it was still running in the background
but no longer available to monitor, which scared me now knowing if it
was running or now.

## Friday, March 12, 2021, 9:37:47AM EST <1615559867>

I'm going back to Apache 2.0 license for all my package stuff because it
is just simply the most trusted license by the enterprise world and most
of the stuff I make it stuff I personally want to use for enterprise
clients who will trust it more. 

So, in other words, my selfish motivation to use what I made and want
has trumped my dedication to opposing shitty companies like Apple who
take BSD and never tell anyone about it. If I use MPL I may very well
not even be able to use the very software I've written to be the most
effective, `cmdtab` comes to mind.

## Friday, March 12, 2021, 7:50:19AM EST <1615553419>

I've been thinking about making my `rwxrob` notes and Zettelkasten into
something that is immediately live as a web page rather than being
forced to to a git update every time. While I find value in having Git
to backup the content, I'm realizing that the nature of a dynamic
knowledge node on the exchange grid makes it unfriendly to the source
code management best practices for Git repos that contain actual source
code. 

For example, when I have a quick thought I have a title for it but end up
having to create a good commit message as well. This defeats the
"fleeting" nature of a knowledge capture throughout the day.

Instead, I'll just make remote edits to a live site in Markdown only and
have a running build process that used `pandoc` or `kn` to render the
changes as HTML and update the meta data. If I do it remotely, I can use
ssh to open a remote edit session without even noticing the difference.
Emacs users could do the same.

That same daemon process monitoring for changes can be set to
periodically commit to Git as a backup system with a generic commit
message that simply summarizes the changes. The Git description for such
a repo will obviously have to show this distinction. For those following
changes on the repo through GitHub this provides less noise throughout
the day as well. In fact, each local render and metadata update could be
locally committed and once a day the entire Git repo could be pushed
rather than every time something changes. The important thing is that I
would never have to think about it (until --- and if --- it stops
working).


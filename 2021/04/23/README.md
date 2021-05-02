## Friday, April 23, 2021, 9:51:58PM EDT <1619229118>

Wondering if I need to keep *truly* POSIX compliant, or just *container*
POSIX compliant. For example, `mkdir -p` works on `busybox` and `alpine`
images but does *not* work on AIX and Solaris operating systems.
Honestly, most of the stuff I am creating already is assumed to be on a
Linux workstation or container --- especially stuff in my `dotfiles`
repo. So I guess I won't sweat it. 

Creating *scripts* that are POSIX compliant (will work with `ash`,
`dash`, etc.) definitely *is* a requirement. So POSIX *shell code* and
not necessarily POSIX tools.

## Friday, April 23, 2021, 7:47:13PM EDT <1619221633>

I've also just realized that over-the-shoulder mode allows me to focus
on the `#rwx` IRC channel as well as the twitch one.

## Friday, April 23, 2021, 7:36:19PM EDT <1619220979>

I've realized there are really two modes of streaming, hearkening back
to the first days of streaming in December 2019:

1. Over the shoulder
1. Interactive

In over the shoulder I'm getting stuff done, often from a laptop that is
TMUX-ed into the session that is being streamed. All I see is a plain
Gruvbox terminal and whatever the TMUX session reveals. I have no
visibility into the number of people watching or anything like that
(unless I open my own channel in a web browser). When in this mode
people are tuning in for something aesthetically pleasing with a little
code involved. Therefore, I'll continue to do the transparent
backgrounds with subtle music and sound effects. That way people can put
it on to fall asleep to if they wish. The goal of this mode is peace and
calm along with some accidental instruction here or there. Readability
is not as important as the experience. I can also play whatever music I
want. Getting muted does matter because people can mute me themselves
without fear of losing anything. Also, I can change the topics in the
titles to be sure people know what I'm working on in that moment. That
and the branch names should be enough to give them a clue about what I'm
actually doing.

In interactive, or cam mode, I have my voice and camera on and am
directly responding to immediate questions and making videos to be
highlighted about stuff. I was doing this before, but this time I make
sure that I'm in in an opaque Gruvbox terminal because it is as if I was
in front of a class demonstrating things and visibility is the priority.

I've gone through this phase before, so it must be the right thing. The
biggest difference is now that people will be able to quickly
distinguish between "over the shoulder" mode (that can be muted) and
"interactive" mode that shouldn't be muted because I'll generally be
saying something.

## Friday, April 23, 2021, 4:31:02PM EDT <1619209862>

Open credentials == managing credentials as software.

## Friday, April 23, 2021, 3:34:15PM EDT <1619206455>

Toying with the idea of adding back the Open Credential thing as a part
of SKILSTAK this time. Basically, I'd be directly ripping off the method
that works for scouting with merit badges and rank advancement, but
making it more real and related to technology. Scouting, after all, has
always been about self-directed learning.

What would the terminology be?

* *rank* - names for different levels that aren't necessarily
         vertically linear
* *boost* - an accelerated review of what learning is needed 

## Friday, April 23, 2021, 7:12:54AM EDT <1619176374>

I have noticed the convention for shell scripting to make some
variables uppercase. I believe the reason for this is the universal
global nature of these variables and the lack of distinction from
aliases and commands, which are always lower case.

I also noticed that POSIX shell scripts have no problem calling
functions that will set variables within the scope of the caller and use
them. This means that such functions also initialize these variables
within the function to ensure their initial values are what are
expected.

The best example of really solid POSIX shell scripting that I have ever
encountered is the Docker install script. (I have a copy in my [dotfiles]
under `install`.) It is an absolute work of art and I'll be using it
regularly to show what amazing POSIX shell code should look like. In
fact, I plan on extracting a style guideline from it (unless I can find
a better one).

[dotfiles]: <https://github.com/rwxrob/dotfiles>


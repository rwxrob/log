## Thursday, April 22, 2021, 3:37:14PM EDT <1619120234>

Here's my latest process revision to how I get work done:

1. Create a Git repo on GitHub (if not already)
1. Change into that repo
1. Create an issue for the work to be done
   1. Label the issue 'enhancement' or 'bug'
   1. Use the issue to discuss work
1. Create a work tree directory next to main dir
  1. Use the same name but with a dash and brief name
  1. Include the issue number and a dash at very end
1. Change into the work tree directory 
1. Do the work
1. Eventually, create PR (if needed) or just merge into main 

## Thursday, April 22, 2021, 3:29:44PM EDT <1619119784>

It's becoming clear what the main tools and languages are for the
Server-Side Beginner Boost:

* Terminal
* Docker
* Linux
* Bash Interactive Shell
* Vim Editor (minimal customizations)
* Screen and TMUX
* Git/GitHub/`gh`
* POSIX (ash/dash) Shell Scripting
* Python Scripting
* Basic Web (HTML/CSS/JavaScript DOM)
* Go Programming
* Basic Networking (`nmap`, `ping`)
* Secure Shell (`ssh`)

## Thursday, April 22, 2021, 3:10:05PM EDT <1619118605>

Here are a few changes to the SKILSTAK AMA time:

* Always streaming with cam and mic
* Always a consistent font and screen
* No more transparency
* More serious, but still fun (hopefully)

And other changes:

* Dropping the coworking stream (since cannot promise)

## Thursday, April 22, 2021, 2:33:03PM EDT <1619116383>

TIL that you should almost never use a Pod during development and use a
Deployment instead. This is because you are going to change things up
and you cannot do that directly with a Pod. I wish I had heard about
this a *long* time ago.

## Thursday, April 22, 2021, 1:49:07PM EDT <1619113747>

Alacritty finally crapped out. It's just not ready for anything serious
yet. I can't even explain all the subtle things wrong with it. It simply
stopped responding. It also does not have full ANSI terminal escape
support, which I think is a big part of the problem. 

One specific thing is how it gets all fucked up when in full screen and
a Windows notification fires off in the upper right. For some reason it
completely resets the position of the content in the terminal. It's bad
enough getting annoyed by the notification. It's worst when it blows
away your position and cursor location. That bug alone is worth dropping
Alacritty for Windows (and therefore anything, since why do it if it
doesn't work anywhere). 

Thankfully, the Windows Terminal is much better. I threw it out because
I was so pissed about how hard it is to manage the configuration file.
But I'm over that now. So I spent the time to configure my Windows
Terminal and it was worth every second. It even does my Ubuntu Mono Nerd
Font without a problem.

I now prefer to do all my work from a laptop again, which is bad for my
stream because I'm generally not sitting at my desk much anymore. Even
though that is nice for a while, there's something about lounging in a
supine position that provides for more calm and less physical
distraction. Whatever the reason, I've always coded better from a chair
or bed. I think a lot has to do with keeping my legs warm and core
*disengaged* so that the extra body stress is out of the way. I also
find myself getting into a zen state where I control my breathing (and
sometimes forget to breath).

In short, sitting in *any* chair or standing is bad for getting into
flow state. There are too many physical distractions. The other night I
coded from bed for five hours straight without even the slightest
fatigue.

## Thursday, April 22, 2021, 10:37:07AM EDT <1619102227>

Wanna job in cloud-native? Learn go!

Another reason learning Go is really mandatory for any cloud-native
engineer is because documentation of important tools such as `kind`
points *directly* to the Go source code to document structures. This is
even more significant than learning Go `text/template` (which is used in
several essential tools --- particularly that involve filtered output).

## Thursday, April 22, 2021, 10:29:00AM EDT <1619101740>

I need to add `/todo/<isosec>` to my KEG content list.


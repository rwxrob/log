## Wednesday, February 12, 2020, 1:32:30PM EST [1581532350]

Would it be okay to entirely drop the Senior Software Engineer track? I
mean, it is implied in Senior Cybersecurity Engineer. Let's face it,
there is not time to learn Vue and all the sysops stuff for most people
before they leave to college or wherever. I'm thinking a conversation
about what Vue and React are, and what PWAs are, is as far as I take
them. All of those tops are a good year of focus for most.

Eliminating the extra web stuff allows them to get into Golang
programming more. Since the shift almost no one has been able to make
time for Go and shell. Then again, most of them do no coding during the
week but while they are here, something that continually annoys me and
motivates me to drop them and seek others who are seriously focused on
cybersecurity, admin, and ops. The streaming has revealed that there are
potentially people out there to follow --- and pay --- for those spots
vacated by the once-a-week game developers in my community. There's
still a lot of consideration before making that decision. Perhaps a
waiting list for those online who might want to do it. But knowing that
it the eventual direction really allows me to focus on the specific
content needed for my ideal group of community members.

Instead I could approach the web development from two angles, how to
quickly publish results are participate in the README World Exchange of
knowledge (blogs, etc.) and how to break into them. That means focusing
on HTTP, `curl` and such and less on image formats for gaming. I mean,
the material is there for those who want to continue on that path on
their own, but I could laser focus on the Cybersecurity and Linux
certification above all.

That really feels like the right thing to do. I've chopped so much, but
chopping that makes so much sense. In fact, following on the idea of
building on existing content rather than creating all my own content I
could piggy back off the WGU focus and alter it, injecting it with LPIC
instruction and preparation for OSCP and one or more network
certifications. By opening focusing on these things from the beginning
--- and stating so up front --- I end up with a hyper-focused community
on what I believe is not only the most employable tech occupation, but
the one the world most critically needs. In fact, I could see what is
needed for these people to get the certified web developer certification
that WGU requires and focus on them getting that if they want just for
the paper even though they would far surpass their requirements.

## Wednesday, February 12, 2020, 1:23:59PM EST [1581531839]

After deciding to go with a new [skilstak.sh]{.spy} I'm realizing a lot
of other changes I had in mind are now very easy.

Perhaps the biggest is that new members don't have to have their own
Linux system. They just have to have access to a computer. That's it.

This opens up the possibility to offer mentoring in some way to others
who are just starting out and want to learn the shell without setting up
a Linux machine at first.

This motivates people to learn Bash enough to customize their own
`bashrc` files. In fact, I could provide the basic one and then
*require* them to customize their own as an exercise. I love this
because my modular refactor of my `config` fits right into this because
they can copy what they want incrementally into their own.

I've also concluded that my fear of having people become dependent on
the server (as opposed to their own) is unfounded. History has shown
that everyone starts up their own server as soon as possible once they
have the skills. It's like the drive many have to build their own
computer instead of use the one provided to them by the school lab. So I
need not fear an imagined dependency on SkilStak. Hell, I have so few
members I could offer an unlimited account for veterans who reach a
certain level. Nah, they would have their own server at that point.

## Wednesday, February 12, 2020, 12:30:18PM EST [1581528618]

Had a night to sleep on the new direction and a good long walk with my
wife discussing it.

The main paths to Senior Cybersecurity Engineer and Senior Software
Developer will remain, along with the common foundation, but the
question remains as to whether to allow multiple paths through the same
initial content or to require everyone to take the same consistent path
mostly for practical reasons, not particularly because that is the
*best* path. 

Every school on the planet pretty much creates one consistent path for
everyone, but I have the unique opportunity to vary that path based on
the individual. However, when I do vary the path it seems like after the
person completes the stuff they are interested in that they are never
motivated to do the important stuff they need. This simply prolongs a
situation that might have been detected and dealt with from the vary
beginning. 

In other words, I need the filter back that I once had, and that filter
is ***command line terminal for everything***. There is simply no better
filter for those who will eventually decide this isn't their thing. And
let's fact it, I don't want to waste my personal time helping anyone who
doesn't agree with the essential need for these skills, the most
fundamental of which is the command line. There are a lot of honorable,
needed occupations that do not emphasize the command line, I would just
rather focus on those that do. The end.

I've all but decided to drop the \$30/month static IP and rebuild the
original skilstak.sh remote cloud system for everyone. My highest
quality people came out of here when I used that approach and the
ability to log in from *anywhere* really drove their learning to new
heights. Anyone with SSH and a terminal could do anything and didn't
have to stress about saving it to GitHub or even setting that up
initially. I think I've underestimated how significant that barrier is
for absolute beginners. As soon as we have to do `ssh-keygen -t ed25519`
their eyes glaze over. *But* if they have had time to get used to a
remote command line --- that is very consistent --- when the time comes
to learn that command and setup GitHub they are like, "Oh, so it's just
another command to add to my collection." 

This indirectly makes a statement about VSCode as well. While it
addresses the same hurdles it presents a whole bunch of its own. But
unfortunately the hurdles VSCode presents are very specific and
overcoming them provides no additional value to other endeavors.

I'm reminded of the absolute hay-day that was [SkilStak]{.spy} during
the era of command-line first. Our first lesson was how to use `ssh`.
Our second was how to navigate the command line. Third was how to edit
files remotely from the terminal. This initial focus on the command-line
clearly set the mood and expectations for every single class to follow
--- for the better. I need that back.

So, what's the plan? Simply to add [skilstak.sh]{.spy} back in full
force and to train everyone up on it immediately. We will divert from
our current Web focus to terminal CLI skills --- following the Linux
book rather closely --- and return to Web stuff up on the server. I'll
provide a web server for everyone that *does not require Git* and people
can preview their development immediately as they do it.

The biggest challenge that remains will be the transferring of images up
to the remote system. But honestly, that is a matter of learning `scp`
which they have otherwise not had a reason to learn up to now.

REPL.it still does not remain a good options because the ability to
customized your `bashrc` file simply does not exist and --- most of all
--- REPL.it *requires* that one have a web interface.

This feels remarkably good and will ridiculously simplify my next lab
rebuild. Come to think of it, the nature and availability of
high-quality terminals now for all operating systems has removed the
initial motivation for using the colored VSCode terminal completely.

Most importantly, however, this focus on the ability to be productive
*with nothing but a command line* is the *core value and skill* that
[SkilStak]{.spy} has always been about. Anything else --- no matter how
justified by specific occupational pursuits --- simply doesn't belong
here. The ultimate priority is on pentesting, systems administration,
SRE/DevOps, and Full-Stack web development *which requires robust
knowledge and skill with the backend command line interface*.

A few things will be significantly different:

* **A password longer than 40 characters will be required.** Public keys
are safer, but they are less flexible and using them is more likely to
cause a beginner to leave their private key cached on some unsafe
computer from which they connected. This is a strange, rather rare
situation where logging in with a password is safer overall than using
keys. I'll go forward with my security auditing plan to ensure guessable
passwords are cracked and I get notified. In fact, since no one will
die, I'm tempted to give visibility to the /etc/shadow file to everyone
to practice their cracking skills. It will *seriously* motivate people
to maintain *good* passwords. It will instill the proper paranoia that
we should *always* expect someone to have access to that file and be
able to brute force it, 'cuz they will. This is one example of something
completely counter-intuitive that no one else would ever consider, but
emphasizes learning skills and habits of highly-skilled cybersecurity
professionals. It will also seriously encourage people to login often.

* *Everyone will get their own subdomain.* I have a small enough
community now that there is no reason not to give them one. Eventually
they will move off to Netlify or their own subdomain but that is
secondary now. The primary priority is on command line navigation and
development.

* *Members will be encouraged to hack other members (within reason).*
They do it anyway every time I set this up. So encouraging it and
managing that expectation will cause people to behave more like they are
going to DefCon and be *really* prepared and safe with their content.
I'll have a hard and fast rule about destructive hacks, but nothing
about being able to hack them and leave their stuff someplace else for
them to recover easily. This will light a fire under those who are
intrinsically attracted to cybersecurity and specifically to pentesting.
If the risk of being hacked and the "trouble" to protect yourself is too
much for anyone, well, they probably don't belong here in the first
place.

* *Everyone will have a web server.* Automatically everyone will get a
web server and a range of ports then can use to bring up their own
services for experimenting with tunneling, websockets, gRPC, and more.

* *Keybase integration.* Keybase will be the common way to share files
between members and a *very* easy way to add images and such to the
system without having to necessarily learn how to use `scp` (which we
will still learn).

* *Significant, ongoing capture the flag games will be emphasized.*
There is nothing more fun that this. It is what shapes their interests.
Even those most interested in creating games of their own are
overwhelmed so much by Easter eggs and hacking *real life* games that
they can focus on little else once they start. *There* are my core
community members and I want more than anything to free time to focus on
this stuff. 

* *Web development de-emphasized.* There will still be web development
enough to get the WGU CWD certification but nothing more. A fundamental
understanding of web pages and such is essential for everything --- but
especially for cybersecurity and bug bounty efforts.



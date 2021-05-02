## Thursday, January 21, 2021, 7:48:32PM EST <1611276512>

Added `git commit` after at the end of the
[log](https://gitlab.com/rwxrob/dotfiles/-/blob/master/scripts/log)
script.

## Thursday, January 21, 2021, 7:42:55PM EST <1611276175>

Cancelled Netlify analytics. The more I get (back) into GitHub and
realize all the stuff they've added the more I realize Netlify doesn't
offer anything I really need. In fact, I'll be slowly migrating off of
Netlify and back to GitHub pages. If and when I need anything Netlify
provides (such as form submission handling) I'll just make a form
handler subdomain on Netlify and just use that, or maybe I'll give
Heroku another look.

It is so amazing how the dynamics of the tech market change over even a
few months. I really love Netlify, but GitHub is rendering them
irrelevant very quickly --- especially with GitHub actions and web
hooks. I don't particularly like that Microsoft/GitHub is destroying the
competition right now, but it is clear to me at this point that they are.

## Thursday, January 21, 2021, 9:24:44AM EST <1611239084>

So my inauguration video --- that contains absolute *zero* copyrighted
material --- has been claimed by NHK, a shitty Japanese company for no
reason whatsoever. My four hour video with commentary and coding has
been completely blocked from view and I'm not hopeful that the dispute
will end up resolved well.

I'm so angry I could spit. In fact, it's all caught live.

## Thursday, January 21, 2021, 7:25:06AM EST <1611231906>

Other day I heard someone refer to Cloud Native and DevOps people
as "YAML programmers" (as a joke of course). But it's worth noting since
YAML has become *such* a foundational skill to have. Like Perl, there is
good YAML and bad YAML. Most who write YAML do not take advantage of its
best strengths: whitespace, comments, alignment. This human readability
and maintainability is what distinguishes it from everything else. No
application should ever *write* YAML since it will *never* get the
spacing correct and will discard all those aspects of YAML that make it
so great.

## Thursday, January 21, 2021, 6:28:03AM EST <1611228483>

So [\@juciybit](https://twitch.tv/juciybit) just taught me a new word:
[yak shaving](https://duck.com/lite?kd=-1&kp=-1&q=yak+shaving). It's when you solve a larger problems by solving a
bunch of smaller problems that seem irrelevant at the time. Not to be
confused with [bike shedding](https://duck.com/lite?kd=-1&kp=-1&q=bike+shedding).

There is a scene from [Malcolm in the
Middle](https://www.youtube.com/watch?v=AbSehcT19u0) about it.

## Thursday, January 21, 2021, 6:20:22AM EST <1611228022>

After a few days of "rolling my own" personal productivity tools and
knowledge management scripts I have never been more convinced that
sometimes you actually do get to "reinvent the wheel" because it's
*your* wheel. Obviously, that adage applies to things in the industry
but too often people are hobbled by searching for the perfect tool when
throwing something together quickly with Bash (or whatever their
preferred glue/scripting language is) would be faster and more
sustainable for *them*.

There are *however* several core utilities that make cobbling together
personalized utilities all that much easier:

* Linux 
* Gnome
* `bash`
* `vim`
* `perl`
* `auth`
* `curl`
* `xclip` 
* `jq`
* `yq` 

And these basic data formats:

* Simplified Pandoc Markdown
* YAML
* JSON


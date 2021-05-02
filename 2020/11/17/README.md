## Tuesday, November 17, 2020, 9:48:59PM EST <1605667739>

Need to take some time and really read through all the [Oauth2 Golang
library](https://duck.com/lite?kd=-1&kp=-1&q=Oauth2 Golang library). I
still need need a little tool to keep cache tokens and such for command
line apps that use Oauth2, but the bigger stuff should probably use one
of those libraries.

I definitely need to play around with
`redirect_uri=urn:ietf:wg:oauth:2.0:oob` which indicates to any Oauth2
server that the response is local and the data is okay to be presented
to the query string in the response allowing it to be pulled out (cut
and paste) into the terminal prompting for it. 

However, I want to do more than that, I want to pass that data directly
to a temporary HTTP server that then passes it within the same runtime
to the client side within the command line app effectively taking care
of the cut and paste step doing it internally.

## Tuesday, November 17, 2020, 4:55:03PM EST <1605650103>

Finally figured out what was wrong with `gruvbox` for Vim. It has the
background set to `#262626` instead of `#282828`, which I actually like
better so I set my terminal background to the same instead of changing
the `gruvbox` plugin. I don't know why there is such a difference
between them when they come from the same project repo, but oh well.

## Tuesday, November 17, 2020, 3:27:10PM EST <1605644830>

Just discovered that YouTube does an awesome job of creating subtitles
provided the audio is really clear and good. Yet another reason I should
pay attention to how I pronounce things and such. It also means that I
don't need to favor IRC chat over audio. And --- once again --- it
proves overwhelmingly that the Restream approach provides the best
overall value for the most people. Add closed captioning to the list of
things that you get for free with YouTube live streaming that you don't
with Twitch. (YouTube, remember, also offers free transcoding that
requires you to be partner to get on Twitch reliably.) Twitch, however,
has a much better chat interface with its support for IRC. 

## Tuesday, November 17, 2020, 3:50:05AM EST <1605603005>

Wouldn't you know it. After clicking on the Restream bot I never checked
the terminal IRC I have been using and sure enough there it was. Vierra
from the live stream community reminded me. It's ugly as sin but it
works. I'm still going to complete the `oauth` module (and the
`restream` app) just 'cuz. If nothing more I need to slug through the
angst of Oauth2 fully in order to grok it fully.

## Tuesday, November 17, 2020, 3:07:22AM EST <1605600442>

Okay so my goal for the next few hours is to get the `RequestToken()`
function finished and working along with a `mock` handler for testing
locally instead of needing an actual Oauth provider.

Here's some good Oauth2 resources found during this session:

* <https://256stuff.com/gray/docs/oauth2.0/>

## Tuesday, November 17, 2020, 2:25:31AM EST <1605597931>

Just one more entry about this schedule stuff.

I fucking love working in the wee hours of the morning when everyone
else is asleep. I get so much done! I get a little giddy sometimes, so
weird, I know. 

Here's a revised schedule based on my current sleep patterns that I'm
going to attempt to maintain for a few months to see how things go. I
think the secret is not to push the physical workouts more than 90
minutes so that I don't need all that extra time repairing my body, just
enough to maintain endocrine balances and stuff. Then I just need to
watch what I eat to keep any extra weight off, which I have to do anyway
so as to not knock myself out in a carb coma.

Hour|Activity
-|-
11am| Up / *Eat (light)* / Family / Reading / Bathroom
12  | Outside / Run / Walk / Yoga
1   | *Eat* / Shower
2   | Live Coding / Project
3   | Live Coding / Project
4   | Private Mentoring / *Snack*
5   | Private Mentoring
6   | Private Mentoring / *Eat*
7   | Private Mentoring
8   | Private Mentoring
9   | *Eat* / Walk Dog / Family / Relax
10  | Sleep
11  | Sleep
12  | Sleep
1   | Sleep
2   | Up / Coffee / *Snack* / Live Coding / Project
3   | Live Coding / Project
4   | Live Coding / Project / *Eat*
5   | Live Coding / Project
6   | Relax
7   | Sleep
8   | Sleep
9   | Sleep
10  | Sleep

I've read that REM happens after 90 minutes of sleep so I believe that
having two longer sleep cycles per day is better than a bunch of 20
minute naps and the science backs that up. Since REM is the *only* time
that your body regenerates --- including your cognitive abilities --- it
is crucial to not skimp on that. I know when I'm doing it well because
when I wake up I'm filled with active thoughts and ideas about what I
was working on and don't feel groggy at all.

I think the best benefit of this schedule is the *incredible* amount of
productivity I find during the early morning time. There is something
magical about having chillhop music on while the rest of the world is
slumbering. It is so relaxing, and God knows I need relaxation to keep
alive today.

## Tuesday, November 17, 2020, 1:42:36AM EST <1605595356>

Watching the NASA Live from Space Twitch feed has really lit a fire
under my ass. Live streaming has completely changed the world. It is
truly 2020. I can do *even* more to more human along in a good
direction.

## Tuesday, November 17, 2020, 1:18:59AM EST <1605593939>

*Senior Software Engineer (Full Stack Developer)*, that's my new title.
I'll be *Project Lead* and *Architect* as well. Imma give those titles to
myself now that I'm going to build out three full SaaS projects over the
next year:

* `skilstak.io` - personal skills management app
* `skilz.dev` - portal of vetted learning resources
* `mim.directory` - decentralized knowledge network

I'll be offering others titles as well as I offer core responsibilities
to as many as who want them from my private mentored community first,
then my live stream community. 

The goal is to have all of these major projects completed and ready to
potentially fund by Jan 1 2022, if not earlier. Mim will be ongoing
throughout the entire year, while the two SaaS apps will be one after
the other. We might finish before that, but not going to push it. I want
this stuff to be done right.

## Tuesday, November 17, 2020, 1:04:44AM EST <1605593084>

It's gonna be a bitch to kick my new sleep pattern. Perhaps starting to
run/walk will help later. Currently, I have a thing where my body is
used to 4 hour sleep sessions twice a day. For example, I went to bed at
9:30pm or so and just got up as if it were the morning with my brain
firing on all cylinders and ready to code. I'm not really sure I *want*
to break it however. I get some serious shit done these days in the wee
hours of the morning because there is literally nothing to distract me,
that I don't put in front of myself.

Another thing I've picked up on is that if I listen to music while I
code and don't use voice I can hold my concentration even I live stream.
At least this way people can hang out and watch. When I want to engage
with them, of course, I can be more focused and even on camera
eventually. But I really don't need to be *on* the stream because as
much as I want to help people I know I can help them best by just coding
really great stuff and *fucking finishing it.*

I've been thinking of the side-gigs I've written about in the past and
had a real change of heart about a lot of it:

* Writing any kind of book is useless until I finish Mim, the
  Decentralized Knowledge Network.

* Udemy courses, while nice as a hobby, are secondary to creating tons of
  great software and having people watch as I do that instead.

* Basics are covered *enough* by other resources and the truly best
  resources are the specs and manuals, such as the Bash `man` page.

* People who need to be spoon fed material don't interest me. You either
  are an autodidact (or are working to become one) or your not. I'm not
  going to waste my time trying to convince you.

* Live streaming everything I do has be best possible hope of motivating
  others to learn the skills that I use rather than talking about them.
  When someone sees me using these skills, there just is not argument.

* Working for the *right* company provides consistent insurance and a
  steady supplemental income, plus it exposes me to opportunities to do
  things that scale that I simply do not get on my own.

* Working for the *right* company allows me to help others to acclimate
  to a good enterprise environment and keeps me connected.


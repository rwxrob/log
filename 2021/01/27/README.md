## Wednesday, January 27, 2021, 8:09:47PM EST <1611796187>

The biggest [root access
bug](https://www.theregister.com/2021/01/26/qualys_sudo_bug/) in
Linux/Unix was discovered recently in `sudo` allowing *anyone* on *any*
such system to have root access nearly immediately. 

Aren't you glad you never trusted your system in the first place?

Zero trust is the only way to approach security. You should never save
anything to disk on a multi-user system that doesn't have encryption,
and even then, with `sudo` giving everyone root access there is a strong
chance such systems already have key-loggers installed.

This bug affects millions of computers right now and has for more than a
decade. So for the foreseeable future *no one* should be using
multi-user access to anything, unless you trust each person with root
access.

## Wednesday, January 27, 2021, 7:27:52PM EST <1611793672>

Just had the best idea while working on the `kn` tool related to the KEG
URI format. 

Why not allow a limited `jq` query?

```pegn
KEGURI <-- 'keg:' Node JQ? ('@' Domain)?
Node   <-- (!'.' visible)+ ('.' (!'.' visible)+)*
JQ     <-- # jq query 
```

Examples:

```
keg:md.lang.Summary@rwx.gg
keg:log.2021.01.03@rwx.gg
keg:cv.Employment[].Entity@rwx.gg
```

The limited `jq` is enough to then pass it further to `jq` if needed.

```
keg 'cv.Employment[].Entity@rwx.gg' | jq '.Name,.Address'
```

`keg` becomes the `curl` of the Knowledge Exchange Grid but better because
it uses the latest cached pull of a knowledge node instead of a fresh
net query every time.

This could be far more useful and valuable than GraphQL could ever be
because it is universal. GraphQL is way more complicated than it really
needs to be. You can tell `jq` was created by people who are much better
data query designers than the Facebook people behind GraphQL. For one
thing the `jq` designers adopted the concept of pipes, which is far
superior to the block hell that is GraphQL.

## Wednesday, January 27, 2021, 4:41:28PM EST <1611783688>

I'm wondering about the cross-over between `live` and `kn`. The argument
could be made that live streaming is a form of recording knowledge not
unlike logging and therefore should be managed under the `kn` tool as a
set of plugins. Perhaps creating a `kn-live` plugin set and repo would
be better. The number of people who will not be live streaming is very
high and bloating the `kn` tool with that seems like a bad idea.

This is definitely the right direction since `live` can leverage the
framework, configuration, and content from `kn` where it would be more
difficult as it's own thing.

But would it be better for `kn-live` to be a composition of other social
media and streaming plugins:

* `kn-twitter`
* `kn-discord`
* `kn-slack`
* `kn-youtube`
* `kn-twitch`
* `kn-github`
* `kn-gitlab`

Why do I feel like an event model is emerging here?

## Wednesday, January 27, 2021, 4:21:34PM EST <1611782494>

Fasted possible way to get the full path to the currently running Bash
script:

```bash
if [[ $0 =~ ^/ ]];then
  echo "$0"
else
  echo "$PWD/${0//\.*\//}"
fi
```

## Wednesday, January 27, 2021, 11:45:07AM EST <1611765907>

Yet another reason to use `gh repo clone <repo>` after you have forked
something is that it updates the upstream master automatically making it
easier to keep the latest changes to the original code synced into your
forked copy.

## Wednesday, January 27, 2021, 9:30:00AM EST <1611757800>

Great insight from [\@lambduh](https://twitch.tv/lambduh) about the
requirement to "publish or die" in the academic world. Just goes to show
that the community of knowledge workers is vast and relevant. These
people all need to be able to capture there knowledge in real time and
polish into publications and other ways of sharing later. In other
words, the world needs KEG.

## Wednesday, January 27, 2021, 7:52:52AM EST <1611751972>

I'm going through a sort of depressed frustration right now with how
long it takes to realize *any* idea. I feel like I'm flooded with them
but don't have the physical capacity to execute on them, not even if a I
had team of a dozen people. It will pass. It always does. 

When people want to understand why I get so pissed at "I'm bored"
comments and broken technologies that slow me down this is why. Every
time I have to open a graphic browser for something I could have
searched and read in fraction of the time in a text browser I lose my
shit because it just reminds me how much the mediocre masses don't give
a shit about such efficiencies.

It's not that people don't want --- or can't help --- its just that I
can't get them up and running fast enough. Getting someone up to speed
to be able to help is extra work all by itself. This is exactly why the
`kn` tool is *so* important because if people truly want to help they'll
be able to follow my thinking and sort of get in line with it offering
suggestions and stepping up with solutions without any ramp up. 

One great example of this working successfully is all the work Quint has
done on PEGN. I haven't had to tell him anything about it. He's just
followed the work and experimented with it, and tuned into my live
streams related to it. Now he'll be the first to deploy a PEGN solution
into a professional environment. He's found countless bugs with the API
itself and created his own code generator. I just had to get the spec
out of my head into a base grammar and the rest took off from there. I
suppose that is something I should look to for modeling with other
projects.

## Wednesday, January 27, 2021, 7:31:31AM EST <1611750691>

I've had no less than four different knowledge manager apps in different
forms of Bash and Go over the last five years. I don't bemoan any of it,
but find I keep getting better at identifying what matters most. I've
put the details of latest thinking in a new [`kn`
repo](https://github.com/rwxrob/kn).

## Monday, March 2, 2020, 8:39:45PM EST [1583199585]

After hacking my way into <https://www.hackthebox.com> (don't forget the
`www`) and watching the earlier OSCP guy's video it has become clear
that there is another mid level between G0CT and OSCP that involves
everything needed to even create an account on hackthebox. It requires
significant JavaScript knowledge as well as HTML and HTTP and base64
encoding. Those are not beginner things in the slightest.

## Monday, March 2, 2020, 5:34:51PM EST [1583188491]

This [guy](https://youtu.be/kdobdnQ2sGw?t=132) says that his "report"
was 240 pages of markdown and screenshots converted to PDF. So yeah,
knowledge source management is a *critical* dependency skill in all of
this. Love that this validates including it in G0CT as well as
everything with the README World Exchange.

Good [advice](https://youtu.be/kdobdnQ2sGw?t=291) on the "memory buffer
overflow" machine:

> "Setup your payload and shell code so you can go back to it, not you
> ... That way there's no need for them to regenerate shell code.
> There's no need for them to create their rhosts and rport. Make it
> one-way so you can callback to it, not to you."

The callback is the thing running that grants access. He's saying to put
all that code on the remote machine so that the overflow code calls that
and not something that initiates a call for that code from your local
system. That's pretty obvious stuff because that is exactly what a
backdoor is, opening something you can login to the remote target.

Reading that the term "enumeration", which has a rather specific meaning
in the software world just means capturing your discovery results as the
initial phase.

::: Enumeration is used to gather the below
 * Usernames, Group names
 * Hostnames
 * Network shares and services
 * IP tables and routing tables
 * Service settings and Audit configurations
 * Application and banners
 * SNMP and DNS Details

Enumeration can be performed on the below.
  1. NetBios Enumeration
  2. SNMP Enumeration
  3. LDAP Enumeration
  4. NTP Enumeration
  5. SMTP Enumeration
  6. DNS Enumeration
  7. Windows Enumeration
  8. UNIX /Linux Enumeration :::

Enumeration is more than nmapping, it is "enumerating" all the
information available from a given port. So SNMP has a *lot* of
information about the system (`snmpwalk`). 

The fact that "enumeration" is considered a basic foundational skill for
OSCP implies there is a *lot* of base learning required far beyond what
I was planning for G0CT. I happen to know a lot of it, but someone who
hasn't been a system admin or doing any patch auditing is going to
really feel left in the dark on that stuff. Something like G0CP -> ????
-> OSCP that would contain all the material from lpic-0, klcp, lpic-1,
network+, a+, security+, but just not suck so badly.

Apparently this guy "took a lot of breaks" which is going to be really
important for me. At least the test is from the safest place you can
find and not their testing center. Instead of "try harder" he suggests:

> "Take a break and try your process again."

I really love that. Trying harder means you'll just produce cortisol and
it will block you from seeing what will be obvious to someone else or
yourself after you've take a good enough break.

I love that he didn't use Metasploit at all. I fucking hate it. It's a
script-kiddy thing.

Also he says don't waste time on kernel exploits even though the kernel
versions are old because they are not intended to be the main vectors.

He finished in eight hours but he sounds like he was really prepared.

## Monday, March 2, 2020, 5:21:23PM EST [1583187683]

So the first thing I learned about the OSCP process is that it takes up
to a month just to get your packet and lab access after your
application, and another full month before your request to take the
actual test goes through. That means there is at least two months of lag
time for those who might not even need that long to do everything (which
I definitely will).

This means that there is no way I could reasonably hit the OSCP by
DefCon, instead DefCon will be an amazing way to tap the minds of a
bunch of people who have received theirs and potentially record them to
share with others. If anything DefCon is sort of a mandatory expense (to
me) to covering as much as I can during the process and documenting it
for everyone.

I also need to spend most of my free video watching time watching all
the others who have received their OSCP and start cataloging them.

## Monday, March 2, 2020, 5:11:36PM EST [1583187096]

Can I just say how fucking happy I am to be *free* of concern for
teaching and keeping up on web shit. The only thing I ever want to learn
about it is how to hack it. It has created such a level of stress for so
many years. It is a good skill and creating a JAMstack site is required
learning, but all the rest? Fuck no. I'm done. It's so completely
liberating. Mostly I'm just happy to be rid of the entire web
development --- specifically JavaScript community --- which is filled
with horrendously horrible human beings.

## Monday, March 2, 2020, 4:51:42PM EST [1583185902]

Perhaps the coolest thing about the OSCP is that it fundamentally
*forces* you to build your continuous learning skills and creativity.
This is exactly what terrifies people because they haven't been taught
to do research and learn on their own. They've had their creativity
beaten out of them by the school system. The OSCP demands high technical
skills, but more than anything it requires solid research and
self-evaluation skills.

## Monday, March 2, 2020, 4:32:28PM EST [1583184748]

Found a great [OSCP
resource](https://niiconsulting.com/checkmate/2017/06/a-detail-guide-on-oscp-preparation-from-newbie-to-oscp/)
that I think does a good job covering what people should expect. It was
interesting that Assembly and memory buffer overflows are a part of the
OSCP. That definitely puts the OSCP in the category of not-for-noobs. In
fact, unless you have done some C coding I have a hard time recommending
it to anyone.

I found the resource while looking for the *required* languages for the
exam. Obviously having a really solid handle on shell scripting is
required (which I have), but specifically I'm wondering if they have a
Python bias anywhere in their requirements.

One thing mentioned is the amount of research required to complete the
55 labs of different difficulties. It made me smile that I can research
faster than 99.9% of the rest of the population with Lynx and the
techniques I've developed over the last 20 years. Hacking is really
about knowledge more than skill. It confirms my selection of content for
the G0CT I'm creating. Reading the overview of OSCP prep is also good to
make sure I have all the building blocks leading up to any tech career,
but specifically for someone headed to the OSCP. Linux, for example, is
not fundamentally required to become a web developer. But it is for
pentesting for sure.

## Monday, March 2, 2020, 4:15:09PM EST [1583183709]

I'm so glad that my subscribers went down by two. I know that is a weird
thing to say, but the reason is because it means that people are
self-filtering, which is great. Here are the people who leave:

* Those who think setting up a ton of desktop-specific hotkeys is
actually a good idea.

* Those who think game development is the only thing that matters.

* Those who think for some reason that old guy with the beard has
nothing important to say.

* Those who are offended by my opinions but unwilling or unable to
challenge me on them even though I'm *very* open to new ideas.

* Those who have no fucking problem sucking every second of my time
online without offering anything in return to those in the room.

There. That's all I needed to get off my chest. Now on to stuff that
matters.

## Monday, March 2, 2020, 11:18:03AM EST [1583165883]

Did about an hour of research on [SourceHut.org](https://sourcehut.org)
and ultimately concluded the following:

* Obsessed with FSF in the best way.
* Great principle engineers with C and Go in their main profiles.
* 64% Python Flask implementation, 3% Go.
* REST API with no public plans for GraphQL.
* No Twitter account.
* Highly transparent business with financials etc.
* SSH into containers used in CI.
* Mercurial support.
* Minimal search ability.

![Source Hut Languages](srht-languages.png)


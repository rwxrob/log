## Saturday, April 24, 2021, 3:14:54PM EDT <1619291694>

I went ahead and encapsulated that previous log post into its own
package function `util.MockStdin(str)` along with `util.UnmockStdin()`
within the [CmdBox] package.

[CmdBox]: <https://github.com/rwxrob/cmdbox>

## Saturday, April 24, 2021, 1:58:45PM EDT <1619287125>

Here's how to replace `os.Stdin` for Go testing. Since `os.Stdin` is
just an open file pointer (`*os.File`) you can just trade it with a file
that you open.

```go
	// replace os.Stdin
	f, err := os.CreateTemp("", "")
	if err != nil {
		t.Error(err)
	}
	t.Logf("CreateTemp: %v\n", f.Name())
	_fmt.Fprint(f, "5 true gophers")
	f.Seek(0, 0)
	orig := os.Stdin
	defer func() { os.Stdin = orig; os.Remove(f.Name()) }()
	os.Stdin = f
```

## Saturday, April 24, 2021, 1:45:36PM EDT <1619286336>

Calming down from the frustration of TEKSystems asking me to "take just
15 minutes" to fill out a "Competencies" form that would have taken me
two hours to fill out just to get what is in my resume into it. I've
never understood such dumb-ass systems and am convinced they are more
busy work that value.

In short, I refused to do it without being paid for the time. I'm not
looking forward to dealing with the fall out, but I cannot let them just
sit back and pretend that it is "for my benefit" when I don't fucking
need it to get a job, anywhere. I strongly suspect it is information
they are going to sell to someone else. So I'm like, if you need this
information pay someone to copy it from my well-prepared CV into your
shitty Oracle system, or, you can pay me my hourly rate. 

Bottom line, people and corporations do *not* respect you. They never
have. They will suck every fucking free cent and second out of you they
can. They only care when it costs *them* money. Then, suddenly, they will
"re-evaluate" the effectiveness of the system. They will keep on sucking
it out of your while you let them out of some unjustified fear that you
can't do fine without them. Well, I can.

If I sound pissed it is because I am. They misrepresented this activity
and expected me to just get in line and blew away my Saturday morning in
both time and spirit. I'm angry. Best of all, my wife supports me in
this. I didn't say anything inappropriate. I just let them know that I
felt the task was misrepresented and that it angered me that they asked
me to do it. Most wouldn't say jack shit. They just wouldn't do it.

## Saturday, April 24, 2021, 11:37:33AM EDT <1619278653>

As I look over my current <https://github.com/rwxrob/rwxrob> repo I
can't help but fear changing everything to use `isosec` identifiers. I
know *why* it is a good thing. Luhmann proved that. I just don't think
anyone else will see the value in it. They will just see a bunch of
numbers all over the place and wonder why I did it that way. 

Fundamentally, no one understands this value until they have had to deal
with reorganizing data on a massive scale. I'm on my fifth time through
this. This is why I'm convinced Luhmann discovered Zettelkasten *after*
he had been a professional for a while and in order to supercharge his
learning to get the position he wanted as fast as possible. He was
driven by immediacy, as am I. 

## Saturday, April 24, 2021, 10:45:18AM EDT <1619275518>

Been thinking that the new [rwx.gg] should actually just be a big
Zettelkasten, but I'm afraid of stuff not being baked again. The main
reason is the value of isosec unique identifiers.

It's a toss up between that and putting it into my own main Zettelkasten
and moving it over. 

Then there is the question of how baked to make my own personal ZK site.
Right now it is just a GitHub repo, which is fine. I don't use
`rwxrob.live` for anything significant these days. Also, there's
something to be said for using a `github.io` domain because they are
free and won't fade away after I pass on (which hopefully isn't for a
while, but still). The [rwx.gg] site, on the other hand, would either
need to be maintained by someone else to keep it up to date, or it could
just fade away and no one would mind because all the content might have
been covered elsewhere by then.

* `zet/<isosec>` - rough zettels, including text and video forms
* `lab/<isosec>` - learning labs (formerly "codebook")
* `data/<ident>` - `yq` query-able data in `data.yml`
* `def/<term>` - term definitions, encyclopedia like 
* `cal` - calendar of events in YAML, gen as `README.md/index.html`
* `week` - weekly schedule
* `log/<isosec>` - time-based log entries (not topics, that's zet)
* `work/<isosec>` - work to be completed usually by a certain time
* `pub/<ident>` - publications, articles, blogs, pdfs, videos
* `reg` - main ZK register, always created by hand
* `dex/<word>` - word index (generated)

After repeating that (I've written it before) it occurs to me that
nothing I am doing for [rwx.gg] cannot be contained in one of these
areas.

The KEG types concept is coming back as well. This stuff is organized by
type more than category or content:

* Zettel - a single zettel (slip), both "fleeting" and main
* Lab - exploration and learning content with some structure
* Data - structured data in YAML/JSON for any purpose
* Definition - definition of a term or concept
* Calendar - calendar of upcoming and past events in YAML
* Schedule - weekly general schedule in YAML and generated
* Work - work to be accomplished usually by given time
* Publication - polished content suitable for publishing
* Register - Zettelkasten register, labels and isosec refs
* Index - auto-generated index of words occurring throughout

Yep, that covers everything. I do have a few other KEG types that I've
used but wouldn't need:

* CV - curriculum vitae (resume) in YAML and generated
* Endorsement - professional endorsement (under CV usually)

I think the key here (like they learned with other semantic web efforts)
is to allow people to expand and define their own types. I've already
covered this in other areas by providing YAML/JSON for the JSON-Schema
of the type definition (which is so widely supported now its
ridiculous despite how bad it is).

[rwx.gg]: <https://rwx.gg>

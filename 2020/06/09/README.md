## Tuesday, June 9, 2020, 9:45:12PM EDT [1591753512]

Realizing that I have to have a solid look at the data model for RWX
before getting too much further into adding content to it. I'm up to
some 200 or so nodes and the organization is starting to weigh a bit
like it always does when I do a refactor. This time, however, it is
rather obvious that YAML and partials are the answer.

There are a few specifics I have to work out for the common YAML meta
data fields. I have a solid `Category` and `Type` grouping defined from
before all this happened. But there are other state properties that need
to come into play in order to allow them to be displayed in indices
without a problem but also without providing *any* broken links. Here's
what I'm thinking so far:

--------------
--------------------------------------------------------------------------------------
Field         Description --------------
--------------------------------------------------------------------------------------
Title         Most important and 100% relevant even if rhetorical.

 Query         Set to anything (`true`) to activate an external search
 query hyperlink for the Title. 

 Subtitle      Snarky or clarifying addition. Not necessarily relevant.
 More rhetorical.

 Category      Specifies the *topic* of content. (ex: boost, course,
 howto, review)

 Type          Specifies the *format* of content. (ex: article
 (default), table, log, revlog, walkthrough, schedule, toc, index, list)

 Summary       Only requirement is that it be a single paragraph/line.
 Should cover everything from reading the whole thing including premise
 and conclusion with as much justification for the conclusion as
 possible. Reading the whole thing should be for those who want the
 details. This is the TLDR but better. In many cases the Summary might
 be all that is needed --- particularly for definitions.

 Created       Optional date and time in ISO (without the T) when the
 original content was created. Particularly useful for articles. 

 Updated       Last date and time in ISO of any official update or
 errata fix. Different than the Created time stamp.
 
 Planned       A rhetorical or ISO date or time span when this
 particilar node can be expected to be complete and available for full
 reading and use. This field allows the framing of content in an
 organized way without creating broken links. While having a Summary
 available along with Planned is preferred it is not required.

 ExpiresOn     Exact date on which this content will definitely have
 expired if not at least checked for relevance. If omitted let the
 auditing tool decide on a default age based on the Updated, Created or
 last modified dates.

 PreReqs       Stuff that is *good to know* and *strongly recommended*
 before consuming this node. This node cannot exist without the other
 prerequisite nodes also existing and being up to date. Critical+
 relationship. Not only will this node be omitted if a prereq is not
 available, but the prereqs should be consumed *before* this node.

 DependsOn     Creates a composition relationship with the node or
 external content referenced meaning that if the dependency changes or
 is removed that this node should be made immediately defunct until the
 dependency can be resolved or a new dependency can be established. This
 means, for example, that if a dependency returns a 404 during a link
 scan that the node is *omitted* entirely until the link is resolved.
 Critical relationship.

 SeeAlso       Set to a list of any Markdown string containing local or
 exteral links, references, or even just words referring to things the
 reader should look into. *Be generous in adding entries --- especially
 those that objectively and rationally take an opposing position to
 conclusions in the content --- in order to encourage examining a bredth
 of input and data on the topic. Loose relationship.
 
 
 Deprecated    A text field explaining why the node is *old* enough to
 be ignored but *leave* it so that others understand that it *is*
 deprecated in case other external nodes have linked to it.

 Contributors  The Name and site ID of anyone who has contributed to
 this specific node. The ID is also the canonical link to
 `/contrib/<ID>/` which any contributor can add and update for
 themselves at any time with a merge request. The Contributors of the
 root node (.) are those who have contributed to more than 20 specific
 nodes in such a way that being listed as a main or default contributor
 makes more sense.

 Video         The full URI to the accompanying video be it on the Web
 or elsewhere. If this is set any indeces created will have a television
 emoji 📺 that links directly to the video so as to make more sense than
 is possible through any sort of video service playlist organization
 even if such is in place as well.

 Audio         Same as Video but Audio. If Video can be consumed simply
 as Audio as well then just use Video instead. This distinction is more
 about the help application that will be used than the format itself.
 However, whenever possible *all* content should be consumable
 *entirely* as written text with *everything* else being secondary
 unless absolutely required to convey the knowledge (review of music or
 video, for example). Always take a progressive approach to knowledge.
 First words, then *supplement* the words with images, audio, and video.
 In other words, prepare *everything* as if for someone with visual and
 hearing impairements. Aethsethic appeal is fine so long as it does not
 put the content out of reach for *anyone* unnecessarily.

 TODO          Stuff that remains to be done on this node. However,
 never leave a node with significant stuff on the TODO list *unless* you
 have set `Planned` as well to indicate that work is, in fact, in
 planned for this node. --------------
 --------------------------------------------------------------------------------------

Well that was more than I was planning on. But looks good. I'll need to
move it into the `/contrib/guide/metadata/` at some point. Feels good to
have it done though because now I don't have to change the *format* and
organization *yet again*. Having a more structured YAML-centric
knowledge base is definitely the way to go.

One thing that occurs to me writing up the `Planned` explanation is that
I can frame the content that needs to be written and allow very specific
contributions from others in the community who may be willing to flesh
out the rest of the node, which prompts me to add a `Contributors` list
to each node.

I did notice some redundancy between hyperlinks in the `Summary` and
entries in `SeeAlso` but I suppose that is fine since both fit on the
same screen when editing. Generally I think `SeeAlso` will tend to have
more in it since it will include opposing sources as well eventually.

`Categories` are going to be a little tricky, but probably worth it.

----------
-----------------------------------------------------------------------------
Category   Description ----------
-----------------------------------------------------------------------------
`boost`    Just to get beginners going. Not necessarily remedial
content, but content that leaves a lot for the person to figure out on
their own. Even something like the `Join Us` welcome node is a boost
because it doesn't get into the particulars of how to join Discord and
such. If it did it would be a `walkthrough` instead. If it where just a
bunch of marketing speak tying to convince people to join then it might
be an `article` instead. (By the way, that stuff usually goes in the
root/cover node.) ----------
-----------------------------------------------------------------------------

Because of the nature of Pandoc templates there also needs to be a bunch
of mechanical properties that have nothing to do with the meta-data
itself. Since these are all related *specifically* to pandoc template
generation (or whatever other rendering format or rules) they *must*
begin with an underscore (`_`).

------------------
-----------------------------------------------------------------------
Tag                Description ------------------
-----------------------------------------------------------------------
`_boost`,          Same as `Category` but required for simple Pandoc
boolean templates. `_article`, etc.           ------------------
-----------------------------------------------------------------------

## Tuesday, June 9, 2020, 9:44:32AM EDT [1591710272]

I'm really glad I took some time to really dive into the new partials in
Pandoc 2.9.2. It is rather obvious at this point that the Pandoc team is
moving toward structured data documents with an emphasis on YAML. It's
amazing the conclusions like-minded people tend to make when they are
all working on the same problems because they are things that *they*
need. This was the *exact* reason that I created Hugonot and FADB back
in the day. I was obsessed with TOML and thought that it was the best
structured data format for such things. Clearly the right format is
YAML. I especially believe that now that I understand YAML linking and
types which allow YAML to move deeply into the database space, not just
configuration files. People hate on YAML for having significant
whitespace and normally I would agree, but this *isn't* a programming
language and readability and stylistic expression --- without
sacrificing consistency --- is really the dominant priority. Most of the
time when I encounter a YAML hater they have not even tried to use it
once --- typical.

So I am facing a real dilemma but I think I know the answer already. I
just have to write it down to process it. It might be more informative
to recount how I arrived at it.

The first few knowledge bases I created for skilstak.io, the Essential
Web, the Knowledge Net and SOIL were all focused on content contained in
Markdown. At first I forced myself to use only [Basic
Markdown](https://rwx.gg/lang/md/basic/) but even before that I was
using something from 2009 and didn't even  allow long single lines as
paragraphs. I would never have allowed "meta data" into the Markdown and
thought that mixing the two was a violation of separation of concerns. I
abhorred Jekyll for "front-matter" and having forever ruined the
cleanliness of *pure* Markdown. A lot of people don't know that having
YAML --- or anything --- at the front of a Markdown file was *never*
original Markdown and still is *not* a part of CommonMark even though
Pandoc and others wisely allowed it. I now have enough experience to
realize keeping the metadata with the Markdown is preferred because it
allows the file to be migrated rather easily. In fact, YAML specifically
allows other body text to come after the YAML section. So in a very real
way Pandoc Markdown files are, in fact, YAML files with Markdown in
them, which brings me to the main point.

Knowledge bases are *at least* half structured YAML data, and half free
form written content. But the more I factor out knowledge into automata
that can be aggregated in any number of ways --- in order to remove
redundancies --- the more I realize even a traditional concept like
chapters gives way let alone the whole notion of a book. Instead,
indexes that aggregate titles, links, and summaries make way more sense.
Taken to its full form you get dynamically composable documents that
either an author *or reader* can organize for themselves in a cafeteria
style approach to knowledge consumption.

This isn't hyperlinking but definitely builds on the idea. I abandoned
self-populating dynamic documents with the essential web. But I find
myself doing about the same things now as I create utilities for
aggregating the knowledge. The simplest form is an index. A bit more and
you get a long index with summaries. But it isn't much further to load
the whole knowledge node, statically or dynamically. This means that
books, guides, and such can be *compiled* in different ways much like
source code.

I am shaking my head at all the *massive* failures to accomplish similar
things, ReadTheDocs, GitBook, Wikis, and more. None of them successfully
understood and acted on the fundamental concept of factoring knowledge
into the most finite form and then aggregating them back *without regard
for any particular target format or rendering*. All of them assume
something about the final output.

I'm more that a little annoyed that humans haven't figured this out
already and created something to do this instead of having to create it.
But I take solace in the fact that the very brilliant people on the
Pandoc project seem to have arrived more at that conclusion than any
others with Pandoc 2.8 and partials. This allows the finite knowledge
form to be a YAML document with text fields that *include* Pandoc
Markdown. Conclusion? ***YAML all the knowledge.***

Seriously, JGM and the gang are just so fucking amazing on so many
levels. They bring practicality to everything they do rather than just
creating yet another over-engineered piece of shit like so many
knowledge solutions out there are that came from engineers (like
Restructured Text, Gatsby, Hugo, even Jekyll). The Pandoc team has
*authors* as their priority and *never* forgets who is using the
product. The others seem to always target *coders* instead, which is why
they continue to fail over and over again.


## Saturday, June 13, 2020, 11:34:18AM EDT [1592062458]

Feels good getting all those `Types` captured. Now time to rip apart the
entire "studio" and reorganize the house. It's nice to have the weekend
"off" but I've just filled it up again with other shit to do.

## Saturday, June 13, 2020, 10:23:23AM EDT [1592058203]

The list of knowledge node `Type`s is shaping up nicely. It's evolved a
bit from earlier versions which did not allow nodes to be contained
within others. This directory organization --- along with the
constraints on node directory IDs --- has made for several improvements
that were not possible before.

-------------
--------------------------------------------------------------------------------------

 Paragraph     Just a single paragraph which Pandoc Mardown emphasis.

 Unordered     Simple, one-level list containing markdown that will be
 rendered by looping through and loading the template partial specified
 for the node. By default each item in the list is a simple unordered
 list item with a bullet.

 Ordered       Simple, numbered, one-level list containing markdown that
 will be rendered by looping through and loading the template partial
 specified for the node. By default each item in the list is a simple
 numbered list item. Numbered means numbered, not lettered.

 Blockquote    Same as Pandoc Markdown.

 Verbatim      Same as Pandoc Markdown.

 Code          File contains only code in a given language.

 Article       (Default) Akin to a "page", "document", magazine article,
 blog post, definition, encyclopedia entry and such.

 Spec          A specification can be as informal as a challenge to test
 skills doing different programming tasks or as formal as a corporate
 project RFC. `Stories` contains the user stories, sentences or
 paragraphs describing examples of how stuff will work. Stories are
 usually no more than three lines of text. More formal specs can include
 `Reqs` lists to fulfill the full
 [INVEST](https://scrumandkanban.co.uk/what-makes-a-good-user-story/)
 characteristics of a good spec. Think of how a highly skilled team of
 professional hackers would outline an op, or what corporate client
 might want built into an application. Both are `Spec`s with `Stories`
 and `Reqs` describing the *outcome* at each step along the way to
 success.

 HowTo         Step by step, walkthrough of a how to execute a specific
 or generic task often outlines in a `Spec` node. Each step must have a
 summary of the step, followed by a detailed explanation and
 demonstration of how to do it. Use header levels to group and
 implicitely number the steps. There are no special YAML traits. Usually
 a single `HowTo` contains several `Prereqs` to help avoid maintaining
 an excessively hyperlinked body. Adding the `Spoilers` boolean will
 progressively reveal all headings and paragraphs incrementally.
 
 Log           Cronological listing where each second level header is a
 time stamp the format of which is defined for the knowledge base or
 individually in the YAML for a given node. Order is irrelevant since
 that is a matter of sorting for the consumer of the data, which can
 easily be altered through DOM manipulation with JavaScript, for
 example.

 Collection    A list of maps specified in a `Schema` header using YAML
 `!!` notation for the basic types `float`, `str`, `list`, `map`,
 `bool`, `timestamp`, `set`, `binary`, etc.

 ParaList      Similar to a `Bulleted` list but each item is a simple
 paragraph with an initial topical sentence that is usually bolded.

 NumParaList   Same as `ParaList` but numbered. Numbered means numbered,
 not lettered.

 Table         Simple table where `Fields` are specified and each record
 in the list is also a list. Generally a `Collection` is preferred for
 its superior ability to capture complex data structures.

 Image         Single image.

 Video§        Single video reference. Usually video will not be stored
 locally. If so, the rendered node will contain an embedded player for
 the video. If the URL is external *and* Internet access is detected the
 video should be embedded using the default video partial or one for the
 specific node if available. A `thumbnail.png` matching one full frame
 of the video resolution should always be included. Any additional
 Markdown can be included in the body of the node to annotate the video.
 Nothing should refer to any specific video service using minutes and
 seconds notation instead to allow the viewer to find the location in
 the video themselves. Can be combined with other node types and will
 render differently depending on the combined type. When combined, the
 `Title`s are identical.

 Audio§        Essentially the same as video but without a
 `thumbnail.png`. Can be combined with other node types and will render
 differently depending on the combined type. When combined, the `Title`s
 are identical.

 ImageMap§      An image with clickable regions that link to internal
 nodes and external resources. Rendered as a `map` in HTML.

 Diagram§      Any large image of any type that can be displayed inline
 as well as providing a link to a file containing the diagram. Usually
 contains annotations as well.

 Slides        Follows the specific Pandoc slides format conventions.

 Chart§        Any of a number of chart format types. A fallback
 `chart.{png,jpg,svg}` must be provided but rendering formats can
 progressively replace it with interactive chart renderings of any kind.

 Quiz          Simple YAML list of `Q`s and `A`s where the questions are
 single paragraphs of Markdown of reasonable size, which can contain
 images, and the answers are regular expressions for every possible
 accepted answer. Renderers can progressively allow the answers typed in
 and validated in real time. There will never be multiple choice of any
 kind, ever. Just a list of human-readable acceptable `Answers` that
 match the regex that can be revealed with a click or tap on mobile
 devices.

 *Outline*     An automatically generated node that recusively examines
 all the nodes listed by ID in the `Outline` property and creates a
 *plain* indented outline by title only.

 *Bookmarks*   An automatically generated node that reads the `Titles`
 of all the listed nodes in the `Bookmarks` property and links them to
 their IDs and URLs. Can include both knowledge nodes and external Web
 URLs.

 *Catalog*     An automatically generated node that reads *all* YAML
 properties from all of the listed nodes within `Catalog` making the
 data within them available to the template renderer. Rendering depends
 completely on the target rendering format.

 *Redirect*    A simple redirect to another page. The `Redirect` points
 to the new location. These are picked up by renders and collected into
 whatever form of redirection functionality is available for the
 rendered format. For example, an HTML renderer gathers them into a
 `_redirects` file.

 *Aggregate*   An aggregate of knowledge nodes into a single node
 containing all the content from the aggregate nodes in the order listed
 in `Aggregate`. Useful for composing books, articles, courses, and such
 from existing nodes. Nodes listed in `Aggregate` may be local or
 remote. If remote a full URI is required and the remote node must fully
 comply with knowledge node specifications, which are mostly just to
 have a `README.md` file contained within the URI and that only local
 dependencies marked with `./` will be pulled over.

 *Latest*      An automatically generated node that recursively examines
 all the nodes within itself for those with the latest changes and
 displays them. Ignores and other criteria are passed to the `Latest`
 property. -------------
 --------------------------------------------------------------------------------------

* *Italics* indicates an node that is mostly automatically generated
node.
* `§` indicates a node that can be combined with any other node that is
not *italicised* or also marked with `§`.

I'm really glad to see the notion of optionally inlined header includes
again. That was a part of the original Essential Web design in 2014.

## Saturday, June 13, 2020, 10:05:42AM EDT [1592057142]

Feeling really triggered by something as simple as an unnecessarily
complicated URL like those on the completely brain-dead documentation
site <https://readthedocs.org>. Here's an example, the URL to their
"Getting Started" page: 

<https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html>

Yeah right, like anyone is every going to commit that to memory. How
fucking stupid do you have to be to build a system that results in URLs
that span more than a screen of text?!

You know what this *should* have been?

<https://en.docs.tech/intro/start>

But that is too much to expect from a bunch of Python-loving, Sphinx
pushing, non-writers. Perhaps they thing that URL will do more for their
SEO (like I once did). It doesn't.

Sphinx is *so fucking stupid!* Oh my God, I'm so triggered. 

You can tell engineers made it and not anyone who actually has to write
for a living. You know how stupid their designs are just by noticing
their focus on Python and reStructuredText. Hell, they don't even use
standard Markdown nor even seem to know what Pandoc is.

This triggers me because it is --- once again --- an example of people
designing things *without even imagining how the shit is going to be
used*. People *completely* put out of their mind the person using what
they are designing.

Don't get mad, get busy, Rob. Don't get mad, get busy.

What we need is not yet another application or site, we need some
standards and best practices for the content *itself* first and then any
application can be layered on top of that.


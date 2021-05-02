## Saturday, May 1, 2021, 2:43:39PM EDT <1619894619>

Another thing I realized is that if I keep the titles under 50
characters they can double as git commit messages. The longer titles are
actually better in the Register instead. This provides something of
value in the notifications that people receive.

If there is no title, then the first 50 characters of the first
paragraph should be used.

## Saturday, May 1, 2021, 2:27:45PM EDT <1619893665>

I'm glad I sat on the KEG stuff for a while. The more I get into the
*proven* Zettelkasten method the more I realize how many of the KEG
bases it covers. This is because when properly implemented a
Zettelkasten is just a file system, literally. Because of this, it has
*direct* parallel terminology with computer file systems:

* index -> `README.md` ZK register
* inode -> unique directory with isosec name

The concepts for a knowledge node all still apply. But a single
knowledge node is just one entry in the ZK directory/register.

The recent discovery to organize into one repo per KEG ZK was really the
final discovery. A repo is directly parallel to a "kast" (box). What I
was struggling to find a name for before (KEG site, root KEG node, root
node) is just a Zettelkasten. I am inclined to call them KEG Zets
because "zets" is plural of "zettels" which is "slips" or "notes". I
like that term because I promotes a conversation about the *true*
Zettelkasten method. In this way, KEG will be fundamentally constructed
on they very sound and established organization methods of Zettelkasten.
We simply expand modestly on what the definition of a "slip" is using
our own KEG Node concept (KEG Node == KEG Zettel + assets).

Then again, just calling them "KEGs" is fine also. Often, "KEG repo"
will be used. A "KEG repo" will be the GitHub. A "KEG site" is a web
site generated from a KEG. Hell, we could make KEG have double meaning:

* KEG = Knowledge Exchange Grid
* KEG = Knowledge Exchange Graph

When used with an indefinite article ("a") the single instance of a
Knowledge Exchange Graph could be implied.

I really love that a Zettelkasten "register" *is* a graph that is
*always* maintained by hand to produce the positive cognitive effect for
which ZK has become famous.

## Saturday, May 1, 2021, 1:49:16PM EDT <1619891356>

Decided on a pretty radical change how I manage my own stuff. It's back
to a decentralized model for me. The topical directories will all be in
their own repos but each and every one will follow a Zettelkasten
indexed model:

* `/README.md` - main Zettelkasten "register"
* `/20210501141545/` - Zettel KEG Node
* `/doc/` - optional generated web content

That's it. Following the Zettelkasten method complete eliminates the
need for outlining, manifest, and stuff because that is *always* done by
hand (on purpose) to promote the cognitive process that makes
Zettelkasten so effective (without preventing any kind of web generator
to do its thing).

The `rwxrob/rwxrob` repo will link to these. This way people can follow
only the stuff they care about instead of getting bombarded with notices
every time I make a log update, for example.

* `log`
* `note`
* `vid`
* `lab`
* `faq`
* `def`
* `cv`
* `todo`
* `plan`
* `rant` - combines in `craplist`
* `quote`
* `story`
* `week` - weekly average schedule
* `code` - personal code of conduct
* `hero`
* `wish`
* `tip`
* `pub` - polished publications, pdfs, books, articles, posts
* `url` - bookmarks
* `assets` - images and bigger things used across repos/sites

So long as there are in their own directory *that* directory can be the
`KN` path. Or, people can use the `git submodule` approach.

Here's how stuff will be consolidated:

The Beginner Boost stuff will be in the following:

* `boost`
* `boost-c`
* `boost-go`
* `boost-py`

The `boost` includes many things that could get their own boosts but are
only minimally covered:

* `bash`
* `vim`
* `tmux`
* `lynx`
* `sh`

These won't be included in the Beginner Boost stuff. When there is
overlap with introductory stuff like in `boost` (for example, `vim`
survival is covered in the boost but not extensive `.vimrc`
configuration, which is in `vim-boost`).

* `boost-bash`
* `boost-js`
* `boost-vim`
* `boost-docker`



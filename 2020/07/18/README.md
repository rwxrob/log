## Saturday, July 18, 2020, 1:43:31PM EDT [1595094211]

Got `tinout` moved over to <https://gitlab.com/rwx.gg/tinout> and
push-mirroring to GitHub. I've decided *nothing* goes into rwx.gg that
isn't *at least* version 1.0 or higher. I want to have someplace where
people can go and be reasonably sure that stuff will usable.

## Saturday, July 18, 2020, 11:56:35AM EDT [1595087795]

Having writer's remorse over writing that slam on tags and structs. As
usual the truth is in between them. In fact, I *love*
`github.com/ghodss/yaml` (and so does the Docker project) for parsing
YAML into structs with the least amount of hassle --- when structs make
sense.

I've been really second guessing my decision to move to interfaces for
all the `knowledge` package stuff. After all these things *are* just
static data. I'll move to struct approach for the AST from Ezmark before
I make a final decision on the `kn` stuff.

## Saturday, July 18, 2020, 11:15:32AM EDT [1595085332]

After facing the quirks of JSON and YAML tagging yet again I went ahead
and wrote [Golang YAML/JSON Tags Actually Suck](/golang-tags-suck/).


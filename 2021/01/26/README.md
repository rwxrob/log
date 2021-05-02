## Tuesday, January 26, 2021, 7:14:44PM EST <1611706484>

Going through the Google Bash script guidelines again and noticed the
`foo() {}` preference over `foo () {}`. I really don't like it. But oh
well.

## Tuesday, January 26, 2021, 6:18:23PM EST <1611703103>

Just realized another good reason to make `give` (soon to be `share`)
into something that points to the GitHub version (instead of a new copy
in ix.io every time) is to cover the stuff under license for the
dotfiles repo itself (Mozilla Public License Version 2).

## Tuesday, January 26, 2021, 5:35:27PM EST <1611700527>

Following on that last thought I'm thinking the main commands I will be
using every day are pretty limited:

Command|Why
|:-:|-
`vim`|Edit files
`git`|Managing code and knowledge source
`kn`|Managing all knowledge as it occurs
`keg`|Packaging, sharing, and tapping (searching) KEG
`live`|Managing a live stream and interacting with community
`repos`|Managing git repos hosted in multiple locations
`sk`|Manage my personal privately mentored community

I wish I could calculate how much time I spend in any particular command
or app during the day. It'd just be interesting to me.

In fact, `kn` will be the most used tool I have (besides `vim`). I plan
on using it for tweeting and everything else. I got to thinking that I
still want a record of anything I tweet so I need to make a log entry
for each. After all, Twitter is just "micro-blogging".

But the above main tools have a lot of dependencies (which aren't
particularly bad given the UNIX philosophy):

Command|Why|Owner
-|-|-
`auth`|API authentication|Me
`youtube`|YouTube API integration|Me
`twitter`|Twitter integration|Me
`twitch`|Twitch API integration|Me
`github`|GitHub integration|GitHub
`gitlab`|GitHub integration|Me
`yq`|YAML queries|Other
`jq`|JSON queries|Other

## Tuesday, January 26, 2021, 4:43:31PM EST <1611697411>

I'm realizing that most of what I have in my personal scripts directory
could be replace by a single `kn` script with multiple subcommands.

## Tuesday, January 26, 2021, 4:41:18PM EST <1611697278>

For streaming it is more important to have a powerful CPU than GPU. OBS
and the RTMP Nginx plugin don't use the GPU.

## Tuesday, January 26, 2021, 11:17:00AM EST <1611677820>

The more I get into creating the `kn` tool the more shell specific
functionality I realize will eventually need to be hard-coded into Go
(or whatever target language). Here are some specific examples:

* `date -d` notation (ex: yesterday, 6pm tomorrow, etc.)
* `yq`/`jq` query language

These two grammars are fundamental to everything I'm doing so far.

I'm convinced the `jq` query language will become a de-facto standard
for parsing and outputting JSON and YAML data (not unlike `xpath` for
XML). This means compiled applications are going to need to hard code 
query strings. The question is, are there libraries for such things in
Go or Rust or whatever. There's a good chance that `yq` supports it
because it is already written in Go and even if not, the syntax parsing
code could be extracted into a generic library for such things. But if
memory serves, it uses some horrible form of `lex`. Yet another reason
to get PEGN grammars *really* off the ground. We could capture the
entire grammar for `jq` and generate automatic AST parsers for them that
could be embedded in anything.

Another option is to just leave it all in shell and let someone else
worry about creating software that requires a compiled binary. I don't.
😜

## Tuesday, January 26, 2021, 5:51:19AM EST <1611658279>

Ya know, it just makes the most sense to standardize KEG log file
structure to be by day. Perhaps calling it KEG daily log or KEG journal
is better. I'll keep log for now, as in "captain's log" or "scientific
log". 

Forcing the standard default to be by day just simplifies everything
when creating tools that use it, which I recently encountered while
integrating recording logs.

Have I mentioned how much I *hate* the term "blog"? No one uses it
properly. Originally, it meant "web log" and was chronological with
entries being short. A "post" to a blog doesn't semantically work. A
"post" is something you hang up more akin to an article or something you
put on a bulletin board. People are stupid. They will find a way to
destroy perfectly good words.

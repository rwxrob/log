## Thursday, January 14, 2021, 6:30:22AM EST <1610623822>

Finding out some cool stuff about the `gh` command after being a little
put off by it not supporting removal of repos by default. Turns out you
can add aliases and even full script integration just in the YAML
configuration file. It is pretty damn cool and prevents me from having
to create a wrapper bash script.

By the way, creating a repo is always better with `gh repo create
<repo-name>` than from within a repo since it does the `git init` for
you. But, if you happen to have a repo already, then (despite the
incorrect notification about adding a directory) it will create the repo
from the contents of the current repo.

For example, here is how you add the missing `rm` subcommand:

```
gh alias set rm 'api -X DELETE "repos/$1"'
```

The downside of using `gh` for everything is that it locks you into a
workflow that is GitHub specific when, in fact, people often have repos
hosted on different services. It would be great if someone could start a
project that encapsulated the APIs of the different services providing a
single command line interface utility to all of them. This was my intent
with the `gits` project, but I can see it I will likely not do anything
more on it because I'm [sold on staying with
GitHub](https://www.youtube.com/c/rwxrob/search?query=github).

So, I guess means I have become subject to their plan to lock people
into GitHub because of the ease of use of their API and command-line
utility. Oh well. I have other shit to do.

## Thursday, January 14, 2021, 4:33:22AM EST <1610616802>

Remember that whole saying about a "picture is worth 1000s words." Yeah,
that's complete bullshit.

I was conflicted about adding images to this log in that last entry to
show the GitHub interface. But then I realized I really don't like nor
need images at all. Adding content that depends on them automatically
excludes a large number of people from benefiting not to mention the
complete waste of storage for what could become a lifetime's worth of
knowledge in a single repo.

Clearly the most sustainable option is to just describe well with words
what to look for or the appearance of the thing. This can be read from a
conversational UI tool or sent to braille keyboards and so on.

## Thursday, January 14, 2021, 4:27:43AM EST <1610616463>

Turns out the reason my commits stopped being verified was because I
changed my email.  Even though I added another email to the *same* key
(see previous entry) it was not working on GitHub. The commit was
showing that it was signed by the correct key, but somehow GitHub did
not recognize the new email.

The solution was to *delete* the previous GPG public key from my GitHub
account and add back the exported public key *after* adding the
new email to it.

```
gpg -a --export rob@rwx.gg |xclip
```

After doing this the GitHub GPG key listed displayed *both* emails
instead of just the one. Commits then began being verified correctly by
either email address in the signatures.

For the record, I tried just adding another GPG key but was blocked for
it being "identical" even though it clearly was not. Hence the reason
for removing it completing and adding it back.

## Thursday, January 14, 2021, 3:01:33AM EST <1610611293>

Just realized that changing my email in `.gitconfig` has caused by
commits to no longer be signed and therefore not show as verified. I
just had to add another identity to the GPG key:

```
$ gpg --edit-key <key-id>
gpg> adduid
Real Name: <name>
Email address: <email>
Comment: <comment or Return to none>
Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? O
Enter passphrase: <password>
gpg> uid <uid>
gpg> trust
Your decision? 5
Do you really want to set this key to ultimate trust? (y/N) y
gpg> save
```

TIL my CmdBox is far closer to `base` from `go` than that fucking Cobra
monstrosity ever was. Ironically, I had no idea what I was creating was
going to be so close in base design. I love that my default design
senses are in line with the Go original founding and tooling team that
the shit that people have thrust on us in that piece of steaming shit
stuff down all of our throats in cloud-native because they all use Cobra
(and have lost the fucking minds, collectively). I mean, seriously, who
the FUCK thought forcing every single application that uses Cobra to
source a 500+ line shell script for *every fucking application* was a
good idea. Just complete and total lack of foresight and basic software
design sense, but they rushed it to market and got the "market" share
and not everyone uses it. Not me, I *never* will. Not only is it a
shit-stain of a package, but is seriously freaking insecure. Those
completion shell scripts are riddled with basic security flaws that
`shellcheck` would find in two seconds, but for some idiotic reason that
team either doesn't know about it, or just doesn't fucking care, which
is worse because everyone is putting dependencies on this shit into
their cloud-native software.

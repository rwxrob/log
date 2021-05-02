## Thursday, April 1, 2021, 2:37:13PM EDT <1617302233>

Need to note that terminal width for streaming is 91, which is a Ubuntu
Mono Nerd Font at size 31 on main screen, and size 21 on the 15"
Dell Latitude 5411 (which is not a 16:9 aspect ratio). This way to don't
force the screen to resize when remotely TMUX-ing in.

There is an annoying off-by-one error that causes the `stty resize` to
change by one height when switching between the two. 

## Thursday, April 1, 2021, 1:16:49PM EDT <1617297409>

It might make more sense to use `minikube` for isolated cases where one
doesn't want the network and other changes to affect the current system
(since it uses a virtual machine).

## Thursday, April 1, 2021, 11:55:20AM EDT <1617292520>

Reminded today what a pain in the ass Git submodules are. I've always
hated them. Just having a separate repo is so much easier.

## Thursday, April 1, 2021, 10:24:19AM EDT <1617287059>

I'm really glad to see Google moving to make more money from
infrastructure contracts rather than invading all our privacy. I find
myself actually rooting for GCP as an alternative to Amazon if for
nothing more than healthy competition.

I have been known to be exceptionally harsh on Google, but it was never
about the people who are there, nor was it the tech. Google has lots of
solid technology (and some really shitty stuff as well). What has always
bothered me was the domination of search and the brokering of our
privacy. If and when the company moves off of these priorities I *could*
become a Google Fanboy (just as I could become a Microsoft fanboy under
the right conditions, although that has waned somewhat given how shitty
WSL2 has been for me).

And as @ygbsm brought up on the community stream, "containerized
deployments should help with mitigating the cost/inertia of switching
cloud service providers to help facilitate that competition."

In short, time to learn GCP, it's a career imperative for my current
employer and will be likely for others.

## Thursday, April 1, 2021, 8:59:03AM EDT <1617281943>

Three prominent Cloud Native engineers and presenters have now
recommended `kind` for localized development. The developer of `kind`
actually received an award from Cloud Native Foundation one year for it
(even though <https://kubernetes.io> still annoyingly only mentions
`minikube` in all of its learning materials). Hopefully, this will make
dealing with persistent locally mounted volumes easier.


## Thursday, March 25, 2021, 3:30:19PM EDT <1616700619>

I've decided to RTFM on docker rather than do anything else.

## Thursday, March 25, 2021, 2:01:48PM EDT <1616695308>

I asked around at work and discovered that most follow the same workflow
process of at doing all the do all the container building and
experimentation locally (on work laptop and home labs) and then when
ready to upload them to the dev cluster at work.

This is the DevOps equivalent of doing coding locally and git committing
with a pull request when ready. The overlap is real.

One difference is that often the containers that are being developed are
to be used in conjunction with others running other services. When
considered at scale, this means my measly little, 8gb RAM laptop just
ain't going to do it, which leaves the equivalent dilemma that network
engineers face. They require more than one system working together to do
anything significant in development and testing. Network engineers can
sometimes pull this off with multiple VMs running on the same system.
But that is out of the question on an 8gb RAM system.

Conclusion: to do *anything* serious with DevOps from the ops or the dev
side really requires a home lab cluster or two, which can be done
virtually, or physically.


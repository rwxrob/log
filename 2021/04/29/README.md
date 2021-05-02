## Thursday, April 29, 2021, 11:47:19PM EDT <1619754439>

Just realized that since YAML doesn't care how much indentation is for
the first item that it doesn't even need a here-document to look nice.

## Thursday, April 29, 2021, 11:35:20PM EDT <1619753720>

Hit a *major* point of confusion when combining shell scripts and YAML
for cloud-native stuff. Tabs are *required* by POSIX for indentation.
They are defined by the standard. It's not a debate. But YAML files
forbid tabs for indentation. This means combining the two in the same
file is problematic at best.

The unfortunate conclusion is that I refuse to use indented
here-documents at all with YAML in shell scripts. You can do it, and it
looks absolutely amazing. And you know people will. Some will say
that the YAML will never need to come out of that shell script. 

However, when some poor sod copies and paste it with a graphic editor
they'll be in for a really bad day because the new YAML file will have
both tabs and spaces in it. White-space only indentation is a fucking
pain as it is enough to get right.

One thing is for sure. Everything I have *ever* said about learning `vi`
is being validated by all of this stuff.

## Thursday, April 29, 2021, 9:28:48PM EDT <1619746128>

I've decided to allow myself to use Bash for "patches" and installations
to Kubernetes clusters instead of just POSIX shell for no other reason
than the following construct (which automatically formats itself):

```bash
 kubectl apply -f - <<-EOM
    apiVersion: rbac.authorization.k8s.io/v1
    kind: Role
    rules:
      # ...
      - apiGroups:
          - ""
        resources:
          - pods/exec
        verbs:
          - create
          - get
  EOM
```

This makes for beautiful and readable shell code that would be unbearable in a code review were it done with only what POSIX shell supports (no support for `-EOM`.

## Thursday, April 29, 2021, 3:18:25PM EDT <1619723905>

After participating in a Domino support call it is clear that the
closest thing to a conventional (not standard) way to implement changes
to a Kubernetes cluster is to create an image (or update to an image),
transfer that image into the internal repository somehow, and run a
shell script (bash specifically) that contains a large percentage of
YAML being `cat`-ed into `kubectl`. 

In other words, the artifacts for a project (like mine currently) to
deliver are simply a shell script and an image or two (or three). That's
it.

Indeed, all the Helm shit is overkill. After looking through the Helm
code and seeing what shitty architecture it is, I want nothing to do
with it unless they fucking require it. There are so many layers of
unnecessary complexity in Helm, and the fact that their web team is so
fucking stupid they require JavaScript to use it scares me to death. All
you have to do is look at the template insanity. There might not be
another, better way yet (Helm is the only thing I know of), but I
(personally) consider it over-engineered shit, but I myself still don't
know shit about any of this. I can just shell this stuff.

My concerns have been warranted, however, by the sheer fact that they
had to completely abandon and discard "tiller" with Helm 3. That's a
sure sign of shitty architecture to begin with. We should give them the
benefit of the doubt, for sure, and allow agile approach, but there are
just too many red flags there. If Helm is so wonderful why isn't Domino
(a well established Kubernetes application and project) creating
releases in Helm and allowing changes like the one we did today to be in
Helm charts?

The reason is *exactly* what we did today. We reviewed every fucking
line of that shell script together to be sure we knew exactly what it
was going to do to the environment. The fact that is was simple shell
scripting meant that all the reviewers on the call could participate and
reduce risk exposure even more by making things more legible and
immediately clear. Having this thing as a shell script and the container
itself in a Dockerfile with the changes captured in commit history in
Git someplace is the way to do. Helm hides all of that with a 'just
trust us' approach that would have taken far longer to review ---
especially if they used those fucking God-aweful Helm templates that
aren't even that *actual* thing.

In short, Imma learn containers inside and out, backwards and forwards,
and I'll do all my work in simple POSIX shell as much as possible (bash
if needed) for all of the reasons Domino did. It simplifies change
review, and that's the most important criterion of all.

## Thursday, April 29, 2021, 3:03:03PM EDT <1619722983>

Need to look into Taints and Tolerations in Kubernetes soon.

## Thursday, April 29, 2021, 12:50:29PM EDT <1619715029>

It would seem from this article that Windows and Mac users don't even
need to use Kind and they can refer to images directly without
indicating the registry.

[[*Build Docker Kubernetes-ready Applications on your Desktop*]](https://www.docker.com/products/kubernetes)

## Thursday, April 29, 2021, 9:30:59AM EDT <1619703059>

Discovered another piece of shit web site: <https://artifacthub.io>
Can't even view the thing without JavaScript enabled. Why are people so
*fucking* stupid?

Opened an [issue] so they can attempt to rationalize their
might-as-well-be-Flash shitty reasons for doing this. 

[issue]: <https://github.com/artifacthub/hub/issues/1284>

Perhaps that will slow the adoption of this crap. This is an early
project under Cloud Native foundation and could easily become a standard
for distributing Helm charts. That's how I found out about it.
JupyterHub hosts their Helm charts there.

The very fact that we are going down the broke-ass registry path for
charts really worries me. This has been proven over and over to be an
anti-pattern. That is why Go uses just GitHub or any Git repo and
checksums everything. This Helm shit is headed down a very, very bad
road. Clearly, the team does not have long experience with macro
architectural designs that have proven to fail.

God, I fucking *hate* web developers these days. So fucking clueless and
so destroying the Web with this shit. They don't even give a shit that
anyone without JavaScript (including some who have it off for security
and accessibility reasons) can see their site. What kind of uncaring
shit-fuck do you have to be to allow that? Most of them probably promote
crypto-currency in their spare time.


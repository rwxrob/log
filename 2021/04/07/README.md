## Wednesday, April 7, 2021, 11:34:48AM EDT <1617809688>

Here are the most important `Dockerfile` lines to master:

```dockerfile
# Switch from the root user to the nobody user                               
USER 65534
```

People forget to do this all the time and expose all sorts of security
vulnerabilities. It's like the 90s all over again. People leave this off
all of the time.

## Wednesday, April 7, 2021, 11:30:33AM EDT <1617809433>

Reminded how essential full knowledge of Alpine and BusyBox is for *any*
Cloud Native development and administration. It's even more important
than understanding Ubuntu Linux. Of particularly interest is the fact
that BusyBox only supports POSIX shell and nothing more and that Alpine
uses the `apk` package manager, which is the next most important package
tool to master (after `apt` and before `rpm`). 


## Thursday, April 15, 2021, 1:05:59PM EDT <1618506359>

TIL that you need to create the directory with the proper ownership and
permissions *before* you bind-mount it with `docker -v` otherwise the
default created version will have restrictive `root` perms that will
likely discount the reason you used a bind-mount in the first place
(usually to edit stuff with tools on the local host).


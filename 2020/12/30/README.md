## Wednesday, December 30, 2020, 3:44:10AM EST <1609317850>

I *really* need to read the Command Line book from Neal Stephenson.

## Wednesday, December 30, 2020, 3:29:14AM EST <1609316954>

*Update: I was wrong and so are most of the concerns in the article.
Submodules are fine when combined with tagging and locking down to a
specific version (as described in the comments of the article). In that
way, they are no different than Go imports that lock down a specific
version and have to be cleaned to update to the latest explicitly on
purpose.*

Turns out Git submodules are the devil. I was actually starting to like
them, but admittedly had not really pushed them hard. I thought having
to `git pull` changes to the submodule was just an annoyance, but it
goes *far* beyond that. 

Big thanks to [\@vierra01](https://twitch.tv/vierra01) for the heads up and the
[link](https://codingkilledthecat.wordpress.com/2012/04/28/why-your-company-shouldnt-use-git-submodules/).
He's hit pretty much every one of these problems in the professional
wild. 

God I love my community. They are saving the lives of other
technologists (including me).


## Friday, October 30, 2020, 11:16:48PM EDT <1604114208>

Just found out that using a GitHub raw URL includes a token in the query
string that expires after seven days but makes that resource available
to anyone with the URL --- including those watching my live stream.

## Friday, October 30, 2020, 2:14:27AM EDT <1604038467>

I finally got around to reinstalling the [Vimium](https://duck.com/lite?kd=-1&kp=-1&q=Vimium) plugin. I had been
using it for years and for some reason --- probably all my renewed Lynx
usage now that I have searching mapped to `?` and `??` from the command
line --- it is really amazing and allows me to use my computer almost
entirely without a mouse. In fact, so far I have found no reason for my
fingers to ever leave home row. Now that I have my computer hooked up to
a big screen and a long keyboard that makes this old man very happy.
Sometimes it can be the little things like this that make all the
difference.

## Friday, October 30, 2020, 12:55:32AM EDT <1604033732>

The pain in my hands --- especially my pinky fingers --- from hours on
end of keyboarding is finally happening as I draw closer to my mid 50s
which has brought me to do something I swore I never would. 

```vimscript
" Map <ESC> key to jj
inoremap jj <Esc>
cnoremap jj <Esc>
inoremap kk <Esc>
cnoremap kk <Esc>
inoremap kj <Esc>
cnoremap kj <Esc>
```

Why the enormous betrayal to my former self?

It's complicated but boils down to the following logic based on recent
discoveries:

* I already have vimisms burned into my muscle memory.
* `Escape-[` does not work on international keyboards.
* `Alt-jklh` is just as strenuous as no mapping and vimism.
* Vim + TMUX + Bash *is* an IDE of sorts.
* Emacs still isn't worth using (to me).
* I don't have to use it, but its there when needed.
* I already fidget with `j` and `k`.  

The biggest blow to my pure `vi` ego was realizing by beloved use of of
["magic wands"](https://rwx.gg/vimagic/) (the exclamation point) has
always been a vimism in the way that I have been using it. But so has
`gw`, all the spelling help, macros (which I only allowed myself to use
within the last month and now could never go back to not using them).
There are just too many Vim-only things that I already use. So why not
yet another small thing that gives my pinkies a wonderful rest.

The alternative, which I seriously considered for a full day, was to
throw out all my Vim muscle memory along with Vim itself and use Emacs
for everything significant and `nvi` for configuration edits. This is
what Linus Torvaldz does as well as many other amazing developers and
technologists. This seems to be the preference of the Academic set as
well as the entire BSD community. But, after much consideration, such a
change is just too late for me. Besides, there is a monstrous risk that
doing such a thing would turn out to *still* be not as good as Vim.
Given the mappings I have set in *everything* else to use "Vi mode", and
the simple fact that many of those things can't even be set to Emacs
mappings, even if the Bash command line defaults to it, I simply cannot
justify it even though logically I would want to attempt that for a full
year as an experiment if I were younger.

I can say this. After using the `jj` hack just a day it has made a
*significant* difference. If this continues I simply won't be going back
--- especially since I plan to do a lot more writing and coding over the
next few years of my "retirement".

What about all those whom I mentor? Well they will always be able to
make their own decisions, but I intend to introduce this immediately to
all of them so that they can be saved from having to type `Esc` all the
time. There is no sense for a young person to burn that shit into their
brain. Most of them already live with the arrow keys anyway. One even
uses the mouse. I'm getting soft in my old age.

They say the biggest danger to progress is dogma. So there is no shame
in my saying that the guy I once knew who got angry at the notion of
doing something so radical as this was just stupid, and that guy was me.
Yep, I just called myself stupid, but anyone *else* stupid enough to
call me stupid, or tuck away this small victory and bring it up again,
well, they can just go fuck themselves. The beauty and wonder of getting
old is all the fucks I don't have to give about small, shallow people liking me. 

Give it a try and make your *own* decision.


## Saturday, March 14, 2020, 6:10:13PM EDT [1584223813]

Woah, I just found a legitimate use for the style tags from HTML5 that
are attributes *instead* of CSS. The following works in a text browser
but does *not* work with CSS:

```html

<th align=left colspan=3>Weekdays</th>

```

## Saturday, March 14, 2020, 5:42:10PM EDT [1584222130]

I'm reminded that in the `rw` tool I need to be sure and detect a
localized `template.html` file rather than use the site-wide one
automatically --- especially now that YAML can be combined with partials
to provide very powerful static view renderings. This essentially turns
every README subdirectory into its own stand-alone page as needed while
allowing them to share common resources for maximum sustainability.

## Saturday, March 14, 2020, 1:04:26PM EDT [1584205466]

Been suffering through "NOVICE mode" in Lynx and forgot to change it to
"ADVANCED" which clears all the crap at the bottom.

## Saturday, March 14, 2020, 1:01:05PM EDT [1584205265]

God I LOVE Twitch community? Solved a stupid annoying thing I have been
working on for years:

```tmux

bind-key -n C-y send-prefix

```

This allows you to use a different prefix (`C-y`) for nested sessions
(TMUX *or* screen). Still need to test it though.


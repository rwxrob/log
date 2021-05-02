## Saturday, September 26, 2020, 9:48:45AM EDT <1601128125>

I think I'm finally coming to terms with my favorite naming conventions
in Go despite their departure from the standard. Thankfully, I'm not the
only one.

* Use `snake_case` for *anything* that is private
* Use `UpperCaseCamel` for all things public
* Use `ALLCAP_SNAKE` for constants

That seems reasonable enough for me to stick with for my projects at
least. It feels more like I'm coding C and since it all gets compiled
down, readability is far more important than compiler efficiency and how
fast something can be written. Besides I *hate* writing capital letters.


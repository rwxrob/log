Just got burned by a variadic `func` signature with `interface{}` types.
I should have known better. This is why I'm leery of generics. Because
my function signature was so loose I missed an easy error that type
checking would have easily forced me to see long ago. This is the kind
of error that makes it into production and comes back to bite people in
the ass later and is the reason Guido (father of Python) says "we have
learned through sad experience that larger projects require strict type
checking".

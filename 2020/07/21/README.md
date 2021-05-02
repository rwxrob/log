## Tuesday, July 21, 2020, 3:47:47PM EDT [1595360867]

TIL that Golang used reflection to implement the "built in"
unmarshalling. That means no one should ever use it of they actually
care about the performance of their JSON parsing. Instead, I will
*always* implement `UnmarshalJSON` myself to ensure stuff gets where it
needs to be as fast as possible *without reflection*. Seriously,
reflection is pretty damn close to the devil.


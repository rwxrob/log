## Saturday, August 8, 2020, 7:49:11AM EDT [1596887351]

Even if PEGN doesn't grow into anything anyone else would ever use it
has already helped me immensely. Here's an example of how I can simply
and easily incorporate it into *any* communication about the syntax of a
thing:

```go
// Parse returns a top-level pegn.Node (Grammar,1) with four attributes.
// The first is the universal language identifier (ULI or UniLangID) in
// all caps "PEGN". The second, third, and fourth attributes are the 
// semantic major, minor, and patch version numbers. No support for 
// semantic version extensions is supported or planned. The ULI,
// however, may contain an extension indicated by a dash (-) followed
// by any alphanumeric ASCII characters.
// 
//   UniLangID <- upper{2,12} (DASH alphanum{1,20})?
func Parse(p pegn.Parser) (pegn.Node, error) {
   // TODO return nil, nil
}
```

My addition of classes (`upper`, `alphanum`), tokens (`DASH`), and
limits (`{2,12}`, `{1,20}`) allows me to quickly and easily communicate
the *exact* specification without the complications of something like
BNF notation. PEGN is simply the most readable technical specification
language I've ever encountered, even if I did take Bryan's idea and ABNF
and just combined the best of them together. But synthesis is often the
essence of innovation.

I've been watching Voyager and have been on the episodes containing
Leonardo Da Vinci and I find myself relating to his frustration with
"idiotas" who see only a person falling into the river trying to fly and
not the thoughtful, courageous, scientifically creative "maestro" at
work. Am I "maestro"? Hardly like he must have been. But I relate to his
frustrations which are not dissimilar to Babbage's during his life.
Reading *The Innovators* has also put me into a perpetual imaginative
state where I am regularly in the presence of *true* greatness and
innovation even if I struggle to produce my own. The world is full of
absolutely amazing human beings who are almost always impossible to
find. They are too busy getting shit done. I just need to mentally place
myself in their company

I also must avoid those who think playing a video game 10 hours a day is
any way to expend the precious time granted to them. I love video games
as a art form, but you don't see me spending 10 hours a day fawning over
any art. There is art appreciation and then there is self-distraction
and addiction. With so many other opportunities to learn, grow, and
connect why waste time on such things?

The secret (for me) is to learn to "cancel" the rest who insist on such
monumentally tragic wastes of time, who throw their fucking lives away
for whatever reason, no matter how justified. I want nothing to do with
them. They frustrate and trigger me. This is why when I start to sense
that a person I mentor is gravitating toward just wanting to make and
play games all day I tend to find an excuse to get rid of them
relatively quickly unless they are young and don't know better.


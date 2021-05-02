## Saturday, July 25, 2020, 9:29:44PM EDT [1595726984]

TIL that <https://cypress.io> is a thing for testing JavaScript. Looks
promising. Need to take a look at it.

## Saturday, July 25, 2020, 3:51:38PM EDT [1595706698]

Recently I was reminded how easy it can be to accidentally defeat the
entire point of using sustainable interfaces instead of structs ---
especially if you are creating an internal struct that implements the
interface as the same time that you are designing the interface.

Here's a method I had initially created correctly, but didn't catch the
very obvious mistake until later.

```go
func (n *node) AppendChild(c Node) {
   if n.c1 == nil {
      c.(*node).mum = n  // DOH!
      n.c1 = c
      n.cN = c
      return
   }
   n.cN.AppendAfterSelf(c)
}
```

Casting the incoming `Node` `c` into a `*node` is a whopping error
because it forces all `Nodes` past to it to *also* be `*node*` pointers.
But that goes against the entire point of interfaces. I should be able
to pass *anything that fulfills the `Node` interface* and obviously
something else might be different.

Here's how I corrected it to work with *any* Node, not just my own
specific implementation:

```go
func (n *node) AppendChild(c Node) { 
   if n.c1 == nil {
      c.SetParent(n)
      n.SetFirstChild(c) 
      n.SetLastChild(c) 
      return
   }
   n.cN.AppendAfterSelf(c)
}
```


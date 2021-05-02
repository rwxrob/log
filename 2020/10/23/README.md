## Friday, October 23, 2020, 2:53:30PM EDT <1603479210>

Need to explore the option of using the Golang `go/ast` package for
adding prefixes to avoid namespace conflicts when generating one-file
code from PEGN grammars without having to maintain two nearly identical
copies of that code. Such a tool might even be worth having just on its
own for when people want to embed the content of another existing
package to remove the external dependency but don't want *any* change of
having name collisions or aren't (for whatever reason) okay putting that
code into a subpackage of their projects.


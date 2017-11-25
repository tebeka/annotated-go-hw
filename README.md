# Annotated Go "Hello World"

## Idea

Have lines of "hello world" in Go annotated interactively.

Have code like the below with some markers (`[ℹ]`) they will get a popup (or
something else) which describes this part of the code.

```go
package main // [ℹ]

import ( // [ℹ]
	"fmt"
)

func main() { // [ℹ], [ℹ]
	fmt.Println("Hello Gophers ☼") // [ℹ], [ℹ]
}
```

## Topics

### `package main`

* Code is in packages
* [How to Write Go Code][write]
* The `main` package

### `import`

* `GOPATH`
* vendor
* `go get`
* `dep` ?
* `import _` (and rename)
* Exported names
* Hierarchy

### `func main`

* Writing functions
    * Return values?
    * Variadic functions?
* The main function
* Curly braces and C influence

### `fmt.Println`

* Function calls
* Exported variables & package prefix

### strings

* Unicode
* runes
    * For loop

### go tool

* `go build`
    * Static executable
    * Cross compile
* `go run`

[write]: https://golang.org/doc/code.html

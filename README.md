# Annotated Go "Hello World"

## Idea

Have lines of "hello world" in Go annotated interactively.

Have code like the below with some markers (`[ℹ]`) they will get a popup (or
something else) which describes this part of the code.

```go
package main

import (
	"fmt"
	"net/http"
)

func handler(w http.ResponseWriter, r *http.Request) {
	fmt.Fprintf(w, "Hello Gophers ☼\n")
}

func main() {
	http.HandleFunc("/", handler)
	http.ListenAndServe(":8080", nil)
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
* Hierarchy (`net/http`)

### `func handler`

* Curly braces and C influence
* Writing functions
    * type after name
    * Return values?
    * Variadic functions?
* `w` interface
* `r` - Pointers (but not `r**`)
* Will run in goroutine

### `fmt.Fprintf(w, "Hello Gophers ☼\n")`

* Function calls
* Exported variables & package prefix
* strings
    * Unicode
    * runes (for loop)
* `Fprintf` first argument is `io.Writer`

### `func main`
* The main function

### `http.HandleFunc("/", handler)`

* function are objects
* routing

### `http.ListenAndServe(":8080", nil)`

* `:8080` -> all interfaces
* nil - no default arguments
* HTTP/2
* `ListenAndServeTLS`


### go tool

* `go build`
    * Static executable
    * Cross compile
* `go run`

[write]: https://golang.org/doc/code.html

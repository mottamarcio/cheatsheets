## GOLANG

## Golang Cheat Sheet

**Basic Syntax:**

  * **Hello World:**

```go
package main

import "fmt"

func main() {
  fmt.Println("Hello, world!")
}
```

  * **Variables:**

```go
var age int = 30
var name string = "John Doe"
isAdult := true // Short variable declaration
```

  * **Data Types:**

      * `int`, `int8`, `int16`, `int32`, `int64`
      * `uint`, `uint8`, `uint16`, `uint32`, `uint64`
      * `float32`, `float64`
      * `string`
      * `bool`

  * **Operators:**

      * Arithmetic: `+`, `-`, `*`, `/`, `%`
      * Comparison: `==`, `!=`, `>`, `<`, `>=`, `<=`
      * Logical: `&&`, `||`, `!`

  * **Control Flow:**

      * `if-else`
      * `for` loop
      * `switch` statement

**Intermediate Concepts:**

  * **Functions:**

```go
func add(x int, y int) int {
  return x + y
}
```

  * **Arrays and Slices:**

```go
var numbers [5]int = [5]int{1, 2, 3, 4, 5}
var slice []int = numbers[1:4] // Slice from index 1 to 3
```

  * **Maps:**

```go
var ages map[string]int = map[string]int{
  "John": 30,
  "Jane": 25,
}
```

  * **Structs:**

```go
type Person struct {
  Name string
  Age  int
}
```

  * **Pointers:**

```go
var x int = 10
var ptr *int = &x // ptr points to x
```

  * **Methods:**

```go
func (p Person) greet() {
  fmt.Println("Hello, my name is", p.Name)
}
```

**Advanced Concepts:**

  * **Interfaces:**

```go
type Shape interface {
  area() float64
}
```

  * **Goroutines (Concurrency):**

```go
go func() {
  // Code to be executed concurrently
}()
```

  * **Channels (Communication between goroutines):**

```go
ch := make(chan int)
ch <- 42 // Send value to channel
value := <-ch // Receive value from channel
```

  * **Error Handling:**

```go
if err != nil {
  // Handle error
}
```

  * **Packages:**
      * `fmt` - formatted I/O
      * `os` - operating system functionalities
      * `net/http` - web server and client
      * `encoding/json` - JSON encoding and decoding

**Tips and Tricks:**

  * Use `gofmt` to format your code.
  * Use `go build` to compile your code.
  * Use `go run` to compile and run your code.
  * Use `go get` to download and install packages.
  * Use `godoc` to view documentation.

**Resources:**

  * **Official Golang website:** [https://golang.org/](https://www.google.com/url?sa=E&source=gmail&q=https://golang.org/)
  * **A Tour of Go:** [https://tour.golang.org/](https://www.google.com/url?sa=E&source=gmail&q=https://tour.golang.org/)
  * **Effective Go:** [https://golang.org/doc/effective\_go.html](https://www.google.com/url?sa=E&source=gmail&q=https://golang.org/doc/effective_go.html)
  * **Golang Standard Library:** [https://golang.org/pkg/](https://www.google.com/url?sa=E&source=gmail&q=https://golang.org/pkg/)
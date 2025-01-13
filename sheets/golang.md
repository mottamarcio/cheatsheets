## **Golang Cheat Sheet**

### **1. Basics**

#### Hello World
```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
```

#### Variables and Constants
```go
var name string = "Go"
var age int = 10
version := 1.18       // Short declaration
const Pi = 3.14       // Constant

// Multiple variables
var (
    a = 1
    b = 2
    c = "Golang"
)
```

#### Basic Types
- **int**, **float64**, **string**, **bool**
- Zero values: `0`, `0.0`, `""`, `false`

#### Functions
```go
func add(a int, b int) int {
    return a + b
}

// Multiple returns
func divide(a, b int) (int, error) {
    if b == 0 {
        return 0, fmt.Errorf("cannot divide by zero")
    }
    return a / b, nil
}
```

#### Control Structures
```go
// If-else
if x > 10 {
    fmt.Println("Big number")
} else {
    fmt.Println("Small number")
}

// For loop
for i := 0; i < 5; i++ {
    fmt.Println(i)
}

// Switch
switch day := "Monday"; day {
case "Monday":
    fmt.Println("Start of the week")
default:
    fmt.Println("Other day")
}
```

---

### **2. Data Structures**

#### Arrays
```go
var arr [5]int          // Array of size 5
arr[0] = 10             // Assign value
fmt.Println(arr[0])     // Access value
```

#### Slices
```go
numbers := []int{1, 2, 3}
numbers = append(numbers, 4)          // Add element
sub := numbers[1:3]                   // Slice [start:end]
```

#### Using `make`
```go
s := make([]int, 5)      // Create slice of length 5
m := make(map[string]int) // Create map
```

#### Maps
```go
m := map[string]int{
    "one": 1,
    "two": 2,
}
m["three"] = 3                     // Add key-value
delete(m, "two")                   // Delete key
value, exists := m["one"]          // Check existence
```

---

### **3. Structs and Methods**

#### Struct
```go
type Person struct {
    Name string
    Age  int
}

p := Person{Name: "Alice", Age: 25}
```

#### Methods
```go
func (p Person) Greet() string {
    return "Hello, " + p.Name
}
```

#### Pointers
```go
p := &Person{Name: "Alice"}
p.Age = 26                  // Dereference automatically
```

---

### **4. Concurrency**

#### Goroutines
```go
go func() {
    fmt.Println("Running in a goroutine")
}()
```

#### Channels
```go
ch := make(chan int)

// Send
go func() { ch <- 42 }()

// Receive
value := <-ch
fmt.Println(value)
```

#### Buffered Channels
```go
ch := make(chan int, 2)
ch <- 1
ch <- 2
fmt.Println(<-ch)
```

#### Select
```go
select {
case val := <-ch1:
    fmt.Println(val)
case <-time.After(time.Second):
    fmt.Println("Timeout")
}
```

---

### **5. Error Handling**

#### Error Type
```go
err := errors.New("something went wrong")
```

#### Custom Errors
```go
type MyError struct {
    Msg string
}

func (e MyError) Error() string {
    return e.Msg
}
```

#### Panic and Recover
```go
defer func() {
    if r := recover(); r != nil {
        fmt.Println("Recovered:", r)
    }
}()
panic("Something went wrong")
```

---

### **6. Testing**

#### Simple Test
```go
package main

import "testing"

func TestAdd(t *testing.T) {
    if result := add(2, 3); result != 5 {
        t.Errorf("Expected 5, got %d", result)
    }
}
```

#### Table-Driven Tests
```go
func TestAdd(t *testing.T) {
    tests := []struct {
        a, b, expected int
    }{
        {1, 2, 3},
        {2, 3, 5},
    }

    for _, tt := range tests {
        result := add(tt.a, tt.b)
        if result != tt.expected {
            t.Errorf("Expected %d, got %d", tt.expected, result)
        }
    }
}
```

---

### **7. Standard Libraries**

#### File I/O
```go
content, err := os.ReadFile("file.txt")
if err != nil {
    log.Fatal(err)
}
fmt.Println(string(content))

err = os.WriteFile("file.txt", []byte("Hello"), 0644)
if err != nil {
    log.Fatal(err)
}
```

#### HTTP Server
```go
package main

import (
    "fmt"
    "net/http"
)

func handler(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintln(w, "Hello, World!")
}

func main() {
    http.HandleFunc("/", handler)
    http.ListenAndServe(":8080", nil)
}
```

---

### **8. Tips and Tricks**

#### Defer
```go
defer fmt.Println("Executed last")
fmt.Println("Executed first")
```

#### Interfaces
```go
type Shape interface {
    Area() float64
}

type Circle struct {
    Radius float64
}

func (c Circle) Area() float64 {
    return 3.14 * c.Radius * c.Radius
}
```

#### Generics
```go
func Sum[T int | float64](a, b T) T {
    return a + b
}
```

---

### **9. Tools**

- **`go fmt`**: Format code
- **`go run`**: Run the application
- **`go build`**: Build the binary
- **`go test`**: Run tests
- **`go mod init`**: Initialize a module
- **`go get`**: Fetch dependencies

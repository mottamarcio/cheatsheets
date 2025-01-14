## **Golang Cheat Sheet**

### **1. Básico**

#### Hello World
```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
```

#### Variáveis e Constantes
```go
var name string = "Go"
var age int = 10
version := 1.18       // Declaração curta
const Pi = 3.14       // Constante

// Múltiplas variáveis
var (
    a = 1
    b = 2
    c = "Golang"
)
```

#### Tipos básicos
- **int**, **float64**, **string**, **bool**
- Valores zero: `0`, `0.0`, `""`, `false`

#### Funções
```go
func add(a int, b int) int {
    return a + b
}

// Retornos múltiplos
func divide(a, b int) (int, error) {
    if b == 0 {
        return 0, fmt.Errorf("cannot divide by zero")
    }
    return a / b, nil
}
```

#### Estruturas de Controle
```go
// If-else
if x > 10 {
    fmt.Println("Big number")
} else {
    fmt.Println("Small number")
}

// If com inicialização
if num := 10; num%2 == 0 {
    fmt.Println("Número par:", num)
} else {
    fmt.Println("Número ímpar:", num)
}

// For loop
for i := 0; i < 5; i++ {
    fmt.Println(i)
}

// For com range
numbers := []int{10, 20, 30}
for index, value := range numbers {
    fmt.Printf("Index: %d, Value: %d\n", index, value)
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

### **2. Estruturas de Dados**

#### Arrays
```go
var arr [5]int          // Array de tamanho 5
arr[0] = 10             // Atribuir valor
fmt.Println(arr[0])     // Acessar valor
```

#### Slices
```go
numbers := []int{1, 2, 3}
numbers = append(numbers, 4)          // Adicionar elemento
sub := numbers[1:3]                   // Slice [start:end]
```

#### Uso de `make`
```go
s := make([]int, 5)      // Criar slice com tamanho 5
m := make(map[string]int) // Criar mapa
```

#### Maps
```go
m := map[string]int{
    "one": 1,
    "two": 2,
}
m["three"] = 3                     // Adicionar chave-valor
delete(m, "two")                   // Deletar chave
value, exists := m["one"]          // Verificar existência
```

---

### **3. Structs e Métodos**

#### Struct
```go
type Person struct {
    Name string
    Age  int
}

p := Person{Name: "Alice", Age: 25}
```

#### Métodos
```go
func (p Person) Greet() string {
    return "Hello, " + p.Name
}
```

#### Ponteiros
```go
p := &Person{Name: "Alice"}
p.Age = 26                  // Dereferência automática
```

---

### **4. Concorrência**

#### Goroutines
```go
go func() {
    fmt.Println("Running in a goroutine")
}()
```

#### Canais
```go
ch := make(chan int)

// Enviar
go func() { ch <- 42 }()

// Receber
value := <-ch
fmt.Println(value)
```

#### Canais bufferizados
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

### **5. Tratamento de Erros**

#### Tipo de Erro
```go
err := errors.New("something went wrong")
```

#### Erros personalizados
```go
type MyError struct {
    Msg string
}

func (e MyError) Error() string {
    return e.Msg
}
```

#### Panic e Recover
```go
defer func() {
    if r := recover(); r != nil {
        fmt.Println("Recovered:", r)
    }
}()
panic("Something went wrong")
```

---

### **6. Testes**

#### Teste simples
```go
package main

import "testing"

func TestAdd(t *testing.T) {
    if result := add(2, 3); result != 5 {
        t.Errorf("Expected 5, got %d", result)
    }
}
```

#### Testes baseados em tabela
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

### **7. File I/O**

#### Ler Arquivo com `os.Open` e `bufio.NewReader`
```go
package main

import (
    "bufio"
    "fmt"
    "os"
    "strings"
)

func main() {
    file, err := os.Open("file.txt")
    if err != nil {
        fmt.Println("Erro ao abrir o arquivo:", err)
        return
    }
    defer file.Close()

    reader := bufio.NewReader(file)

    for {
        line, err := reader.ReadString('\n')
        if err != nil {
            if err.Error() != "EOF" {
                fmt.Println("Erro ao ler o arquivo:", err)
            }
            break
        }

        line = strings.TrimSpace(line)
        fmt.Println(line)
    }
}
```

#### Escrever em Arquivo
```go
package main

import (
    "fmt"
    "os"
)

func main() {
    file, err := os.Create("file.txt")
    if err != nil {
        fmt.Println("Erro ao criar o arquivo:", err)
        return
    }
    defer file.Close()

    _, err = file.WriteString("Hello, World!\n")
    if err != nil {
        fmt.Println("Erro ao escrever no arquivo:", err)
    }
}
```

#### Ler Arquivo Inteiro
```go
content, err := os.ReadFile("file.txt")
if err != nil {
    fmt.Println("Erro ao ler o arquivo:", err)
    return
}
fmt.Println(string(content))
```

---

### **8. Dicas e Truques**

#### Defer
```go
defer fmt.Println("Executado por último")
fmt.Println("Executado primeiro")
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

#### Genéricos
```go
func Sum[T int | float64](a, b T) T {
    return a + b
}
```

---

### **9. Ferramentas**

- **`go fmt`**: Formatar código
- **`go run`**: Executar a aplicação
- **`go build`**: Compilar o binário
- **`go test`**: Executar testes
- **`go mod init`**: Inicializar um módulo
- **`go get`**: Baixar dependências

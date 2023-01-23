# Go Programming Cheat Sheet

## Boiler Plate Information

Start every file with the package declaration/name

```go
package packageName
```

Import statements come next ex.

```go
import (
    "fmt"
    "os"
    "strconv"
)
```

Executing file needs to contain the main function.

```go
func main() {
    // Main body of the program
}
```

## Conditional Statements

If, If Else, If Else If, and Switch Statements

```go
if condition {
    //do stuff
} else /*else if*/ {
    // do other stuff
}

switch variable {
case condition 1:
    // do stuff
case condition 2:
    // do stuff
case condition n:
    // do stuff
default:
    // do this if none of the conditions are met
}
```

## Loops

For looping Go only has the for construct, there are no while loops. to simulate a while loop look at the second example.

```go
// standard for loop
for i := 0; i < 10; i++ {
    fmt.Print(i*i, " ")
}
fmt.Println()

// simulating a while loop
i := 0
for {
    if i == 10 {
        break
    }
    fmt.Print(i*i, " ")
    i++
}
fmt.Println()

// iterating over the elements in an array etc.
aSlice := []int{-1, 2, 1, -1, 2, -1}
for i, v := range aSlice {
    fmt.Println("index: ", i, " value: ", v)
}
```

## Getting User Input

For user input you can use ```go fmt.Scanln()``` when not using command line arguments. The following code example shows using ```fmt.Scanln()```

```go
fmt.Printf("Please give me your name: ")
var name string
fmt.Scanln(&name)
fmt.Println("Your name is", name, "?\nHello, ", name)
```

For command line arguments are stored in the  ```os.Args``` slice. ```os.Args[0]``` is always the name of the executable. The remaining arguments are what comes after the name of the executable and are separated by space characters unless in quotes.

## Arrays & Slices

The length of an array is found by the ```len()``` function.

```go
aSlice := []int{0, 2, -1, 1, 76, 42}
sliceLength := len(aSlice) // should be 6
```

## Concurrency

The concurrency model uses what are called **goroutines**; to create a goroutine use the ```go``` keyword followed by a predefined or anonymous function.

**Channels** allow goroutines to communicate and exchange data.

## Converting from int to String

```go
input := strconv.Itoa(n)
// FormatInt(int64ToConvert, Base (10, 8, 16, 2))
input = strconv.FormatInt(int64(n), 10)
// string() converts int into ASCII/Unicode character
input = string(n)
```

## Maps, Slices, Structures

For making slices

```go
aSlice := []int{}
// or with the make() where first is array/slice type
// second is the capacity of the array
makeSlice := make([]int, 5)
```

For creating maps:

```go
// create a map using map literal
m := map[string]int{
    Key: Value
}
// or create a new empty map
m = make(map[string]int)

// delete items from a map
delete(Map, key)
```

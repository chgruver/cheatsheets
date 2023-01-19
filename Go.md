# Go Programming Cheat Sheet

Start every file with the package declaration/name

```go
package <package name>
```

Import statements come next ex.

```go
import (
    "fmt"
    "os"
    "strconv"
)
```

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

For user input you can use ```go fmt.Scanln()``` when not using command line arguments. The following code example shows using ```fmt.Scanln()```

```go
fmt.Printf("Please give me your name: ")
var name string
fmt.Scanln(&name)
fmt.Println("Your name is", name, "?\nHello, ", name)
```

For command line arguments are stored in the  ```os.Args``` slice. ```os.Args[0]``` is always the name of the executable. The remaining arguments are what comes after the name of the executable and are separated by space characters unless in quotes.

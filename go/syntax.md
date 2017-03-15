# Go Syntax

##### Variables

```go
var i int = 1
var a, b int = 1, 2
var (
someBool bool = true,
someInt int = 1
)

// implicit
c := 1
d, e := 2, true

```

##### Pointers

```go
var i int = 5

// zero value is nil
var j *int

j = &i

// dereference
var a int = *j

// indirecting
*j = 6
```

##### Struct

```go
type Person struct {
name string
age int
}

aPerson := Person{"John Doe", 25}
aPerson.age += 1

aPointerToPerson := &aPerson
aPointerToPerson.name = "Jane Doe"

anotherPerson := Person{name: "Joe Bloggs"}
```

##### Arrays & Slices

```go

// Arrays are fixed size
var arr [5]int

arr2 := [3]int{1,2,3}

// reference to section of an array, changing element in slice changes underlying array
var slice []int = arr2[0:1]

// slice literal, builds the underlying array
lit := []int{1,2,3}
 
lit[1:] // 2 3
lit[:3] // 1 2 3
lit[:] // 1 2 3

len(lit) // number of elements in a slice (zero value is nil)
cap(lit) // number of element in the underlying array (zero value is nill)

// using make and append
a := make([]int, 5) // allocate a zero'd array of 5 elements
a = append(a,1) // append 1 to the slice
fmt.Println(a[:]) // prints 0 0 0 0 0 1
 
// using range on slice - to drop index use _, value - to drop value use index
for index, value := range lit {
 // index in slice
 // value in slice
}
```

##### Maps

```go
// use make to initialise a map
m := make(map[string]string)
m["theKey"] = "theValue"

var litM = map[string]string{
	"oneKey": "OneValue",
	"TwoKey": "TwoValue",
}

litM["oneKey"] = "ChangeValue"
delete(litM, "TwoKey")
value, ok = litM["TwoKey"] // ok will be true or false
```

##### Methods

```go
// functions with receiver argument between the func keyword and the method name
type Person struct {
	name string
	age int	
}

func (p Person) Print() string {
	return p.name + " " + strconv.Itoa(123)
}

func main() {
	v := Person{"jon", 40}
	fmt.Println(v.Print())
}

// methods can be defined on types other than struct but type must be in same package
// thus not primative types

// pointer receiver are more common, allow for modification of underlying value

func (p *Person) Print() string {
	p.name = "NewName" // changes value
	return p.name + " " + strconv.Itoa(123)
}
```

##### Interfaces

```go
// No explicit implements keyword, a type implements an interface by implementing its methods
type Person struct {
	name string
	age int	
}

type Printable interface {
	Print() string
}

func (p Person) Print() string {
	return p.name + " " + strconv.Itoa(123)
}

func main() {
	var v Printable = Person{"jon", 40}
	fmt.Println(v.Print())
} 

// Every type implements the interface (zero methods)
interface{}

// type assertions
t := i.(T) // says that the interface i holds the type T if this false causes panic

// safe type assertion
t, ok := i.(T) // if this is correct then ok will be true and T will contain the value
t, ok := i.(string)

// type switches
switch value := i.(type) {
case string:
 // value is string
case int:
 // value is int
default:
 // unknown type, type remains interface i
}
```

##### Errors

```go
// No throws 
// error is a built-in interface
// check error returned from functions against nil, error value that is nil implies success
import (
	"errors"
	"fmt"
)

func run(n string) (string, error) {
	if n == "Hello" {
		return "World",nil
	}
	return "", errors.New("SomeError")
}

func main() {
	
	val, err := run("d")
	
	if err == nil {
		fmt.Println(val)
	} else {
		fmt.Println(err)
	}
}
```

##### Goroutines

```go
// Concurrency in Go
go funcName()

// use channels to communicate between Goroutines
// "Don't communicate by sharing memory, share memory by communicating." https://talks.golang.org/2012/splash.article
// send and receive values using <- operator
// channels need creating before use
chan := make(chan int) // channel that receives send ints

chan <- 1 // send to channel
i := <-chan // receive from channel and assign to i
// send and receive until the other side is ready allowing for synchronisation without locks

// buffered channels, second argument to make
chan := make(chan int, 2) // sends buffered channel blocks until buffer is full, receive blocks when buffer is empty

// channel can be closed by the sender, only if the receiver needs to be told
close(chan)

// receiver can check for closed channel by using second parameter from receiver
n, ok := <-chan

// also 
for i := range chan {
// this would loop while channel is not closed
}

// wait on multiple channels using select
select {
case <-chan:
// some operation
case <-otherChan:
// another operation
default:
// run if no other case is ready
}
// if both are ready will select at random

```

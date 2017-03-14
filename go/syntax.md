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
```

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


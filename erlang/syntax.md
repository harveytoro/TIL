## Erlang Syntax

##### Comment

```erlang
% this is a comment
```

##### Variables
- Must start with capital letter.
- Single assignment.
- Variable with value is called bound. Otherwise Unbound

```erlang
X = 1. 
```

##### Atoms
- Represent constant values.
- Start with lowercase letter followed by alphanumeric characters (including _ and @).
- Can use single quotes to have atom start with capital letter, or use non-alphanumeric character.

```erlang
'atom', `+`
```

##### Tuples
- Common practice is to add what tuple is used for as first element (as erlang has no type declarations).
- Can be nested

```erlang
Person = {person, {name, harvey}, {age, 23}}. 
```

- Use pattern matching to get value.

```erlang
{_,{_, Me},_} = Person.
Me. 
  Harvey
```
- Underscore is used as an anonymous variable, several occurances do not have to bind to same value.

##### Lists
- Store arbitrary number of elements.
- Individual elements can be of any type.
- First element = head, all others = tail

```erlang
I = [1,2,3]. 
```

- Use pattern matching to get elements.

```erlang
[X | T] = I. 
X. 
  1
T.
  [2,3]
```

- [] represents an empty list.

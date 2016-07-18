## C# Implicit / Explicit Operators

Implicit operator: User-defined type conversion operator (without casting).

```C#
public static implicit operator SomeType(int convert)
{
…
}

// Usage
SomeType variable = 5;
```

Explicit operator: User-defined type conversion operator (with cast).

```C#
public static explicit operator SomeType(int convert)
{
…
}

// Usage
SomeType variable = (explicit)5;
```
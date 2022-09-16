Keywords = Palavras-Chave

---

### Variables & Mutability
* Variables are *immutable* by default, once a value is **bound** to a name, you can't change that value.
* Immutable variables cannot be assigned values twice.

the keyword `mut` can be added in front of the variable name to make them mutable.

for example: `let mut x = 5;`

---

### Constants

*Constants* are values bounded to a name that are not allowed to change.

- Constants don't use `mut`.
- You declare them using the `const` keyword.
- The type of the value *must* be annotated/declared.
- Is important to notice you must always annotate the type.
- Can be declared in any scope, local or global scope.
- assign constants only for constant expressions, not the result of something else.
- Naming convention for constants is to use all uppercase letters with underscores between words.

---

### Shadowing
- You can declare a new variable with the same name as a previous variable.
- The second variable is what the compiler will see when you use the name of the variable.
- The second variable overshadows the first variable.
- taking any uses of the variable name to itself until either it it itself is shadowed or the scope ends.

```rust
fn main() {
    let x = 5;
    {
        let x = x * 2;
    }
}
// output: x = 12
```

---

### Data Types

- Rust is *Statically* typed, which means that it must know the types of all variables at compile time.

**Scalar Types**
- A *scalar* type represents a single value.
- Rust has 4 primary scalar types: Integers, Floating-Point Numbers, Booleans, and Characters.

**Integer Types**
- An *Integer* is a number without a fractional component.
- Can be signed or unsigned and has an explicit size.
- *Signed* (e.g i32) or *Unsigned* (e.g u32) refers to whether it's possible for the number to be negative.

**Floating-Point Types**
- Numbers with decimal points.
- Rust's floating-point types are `f32` (32 bits) and `f64` (64 bits).
- The `f32` is a single-precision float, and `f64` has double precision.

**The Boolean Type**
- Boolean type in Rust has 2 possible values: `true` and `false`.
- Specified using `bool`.
- The main way to use Boolean values is through conditionals (e.g if statements).

**The Character Type**
- Rust's `char` type is the language's most primite alphabetic type.
- They are specified with single quotes.

---

### **Compound Types**
*Compound types* can group multiple values into one type.

**The Tuple Type**
- A tuple is a general way of grouping together a number of values with a variety of types into one compound type.
- Have fixed length.

e.g:
```rust
fn main() {
    let tuple: (i32, f64, u8) = (193, 6.4, 1);
}
```

- Tuple is considered a single compound element.
- Destructure the tuple to get the individual values out of a tuple.

```rust
let tuple = (193, 6.4, 1);
let (x, y, z) = tuple;
```

**The Array Type**
- Another way to have a collection of multiple values is with an array.
- Every element of an array must have the same type.
- Have fixed length

e.g:
```rust
fn main() {
    let a = [1, 2, 3, 4, 5];
    let b: [i32; 5] = [1, 2, 3, 4, 5];
}
```

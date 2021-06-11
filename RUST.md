# Rust Notes

```
The relationships between various data types in Rust are established using traits. 
```

```
A large part of learning Rust is understanding how the standard library traits operate, 
because that's the web of meaning that glues all the data types together.
```

```
Traits are interesting because there's no one-to-one correspondence between them and concepts from mainstream languages. 
It depends if you're thinking dynamically or statically. 
In the dynamic case, they're rather like Java or Go interfaces.
```

```
Composition is more important in Rust for the obvious reason that 
you can't inherit functionality in a lazy way from a base class.
```

```
Basically, Rust is introducing some friction here
, and not-so-subtly pushing you towards returning values from functions directly. 
Fortunately, Rust has powerful ways to express things like "operation succeeded and here's the result" 
so &mut isn't needed that often. 
```

```
Passing by reference is important when we have a large object and don't wish to copy it.
```

```
A C programmer pronounces & as 'address of'; a Rust programmer pronounces it 'borrow'. 
This is going to be the key word when learning Rust. 
```

```
Borrowing is the name given to a common pattern in programming
; whenever you pass something by reference (as nearly always happens in dynamic languages) or pass a pointer in C. 

Anything borrowed remains owned by the original owner.
```

## References
- [Rust: Gentle Intro](https://stevedonovan.github.io/rust-gentle-intro/)

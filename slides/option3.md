+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
# Optional

```rust
fn maintenir_altitude(altitude: i32, securite: Option<i32>) {
    voler(altitude + securite)
}
```

```
error[E0277]: cannot add `Option<i32>` to `i32`
 --> src/main.rs:6:20
  |
6 |     voler(altitude + securite)
  |                    ^ no implementation for `i32 + Option<i32>`
  |
```

En 🦀, le type `null` **n'existe pas**. A la place, il existe un *Enum* appelé `Option` qui possède deux variantes : `Option::None` et `Option::Some(T)` (où `T` est votre valeur).

Ainsi, tout endroit du code où l'on souhaite permettre une absence de valeur utilise en fait le type `Option`.

# 🛫 🛬
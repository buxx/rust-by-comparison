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
    match securite {
        Some(securite_valeur) => voler(altitude + securite_valeur),
        None => voler(altitude),
    }
}
```

```rust
fn maintenir_altitude(altitude: i32, securite: Option<i32>) {
    voler(altitude + securite.unwrap_or(0))
}
```

# 🛫 🛬
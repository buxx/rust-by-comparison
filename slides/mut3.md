+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
En 🦀, une variable est immuable par défaut.
Pour pouvoir la modifier, on doit utiliser le mot-clef `mut`.
Et toute signature qui voudra *pouvoir modifier* une variable devra l'indiquer.

```rust
struct Vol { altitude: i32 }

fn journaliser(vol: &mut Vol) { /** [...] */ }
fn maintenir_altitude(vol: Vol) { /** [...] */ }

pub fn main() {
    let mut vol = Vol { altitude: 15000 };
    journaliser(&mut vol);
    maintenir_altitude(vol)
}
```

# 🛫 🛬
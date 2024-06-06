+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
```rust
struct Vol { altitude: i32 }

// `&mut` indique que cette fonction demande que la variable `vol`
// soit donné par référence et d'être mutable.
fn journaliser(vol: &mut Vol) { /** [...] */ }
fn maintenir_altitude(vol: Vol) { /** [...] */ }

pub fn main() {
    let mut vol = Vol { altitude: 15000 };
    // `&mut` indique que l'on donne une référence mutable
    // `vol` peut donc avoir changé !
    journaliser(&mut vol);
    // C'est donc probablement une mauvaise idée de faire
    // s'enchaîner ces deux appels
    maintenir_altitude(vol)
}
```

Ce qui est important ici c'est :

- On sait à la lecture du code si une variable peut changer lors d'un appel

# 🛫 🛬
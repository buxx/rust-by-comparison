+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
# Gestion d'erreur

```rust
fn calcul_altitude() -> i32 { /** [...] */ }

fn maintenir_altitude(altitude: i32) -> Result<i32, ErreurDeVol> {
    // [...]
    Ok(altitude_atteinte)
}

pub fn voler() {
    // `calcul_altitude` retourne un nombre
    let altitude = calcul_altitude();
    // `maintenir_altitude` retourne un type `Result`
    match maintenir_altitude(altitude) {
        Ok(altitude_atteinte) => afficher_cockpit(altitude_atteinte),
        Err(erreur) => alerte_cockpit(erreur),
    }
}
```

En 🦀, il n'y a pas de mécanisme d'erreur particulier.
Comme pour `Option`, il existe un enum `Result` qui est possède deux variante.
`Result::Ok(T)` (où `T` est votre valeur quand c'est ok) et `Result::Error(E)` où `E` est votre valeur quand il y a eu une erreur.

## 🛫 🛬
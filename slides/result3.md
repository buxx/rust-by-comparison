+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
# Gestion d'erreur

```rust
pub fn voler() -> Result<(), ErreurDeVol> {
    let altitude = calcul_altitude();
    maintenir_altitude(altitude)?
}
```

Si l'on souhaite faire remonter l'erreur au lieu de la gérer directement,
il existe le `?` qui fait un simple `return` de l'erreur si il y en a, ou récupère la valeur du `ok`.

De la même manière que le `Option` il existe un ensemble de fonctions associés
à ce type `Result` pour nous aider.

En bonus, il est possible en un coup d'œil de savoir si une fonction
n'échouera jamais (ex. `calcul_altitude();`) ou si elle peut
échouer (ex. `maintenir_altitude(altitude)?`).

## 🛫 🛬
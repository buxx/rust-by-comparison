+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
# Threads

```rust
error[E0382]: assign to part of moved value: `vol`
  --> src/main.rs:14:5
   |
12 |     let mut vol = Vol { altitude: 15000 };
   |         ------- move occurs because `vol` has type `Vol`, which does not implement the `Copy` trait
13 |     thread::spawn(|| voler(vol));
   |                   --       --- variable moved due to use in closure
   |                   |
   |                   value moved into closure here
14 |     vol.altitude = 0;
   |     ^^^^^^^^^^^^^^^^ value partially assigned here after move
```

En 🦀, le contrôleur de possession des variables empêche cela. Il sera impossible de compiler un code où une variable peut être utilisés et modifiés à plusieurs endroits en même temps.

Le développeur est alors dans l'obligation de gérer explicitement le "partage" des données à l'aide des diverses solutions existantes. `Rc`, `Mutex`, `Channels`, etc.

Ces contrôles s'appliquent pour du code asynchrone comme pour les threads.

# 🛫 🛬
+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
# Switch/Matchs

```rust
error[E0004]: non-exhaustive patterns: `Event::SurchauffeMoteur` not covered
  --> src/main.rs:11:11
   |
11 |     match event {
   |           ^^^^^ pattern `Event::SurchauffeMoteur` not covered
   |
note: `Event` defined here
  --> src/main.rs:4:5
   |
1  | enum Event {
   |      -----
...
4  |     SurchauffeMoteur,
   |     ^^^^^^^^^^^^^^^^ not covered
   = note: the matched value is of type `Event`
help: ensure that all possible cases are being handled by adding a match arm with a wildcard pattern or an explicit pattern as shown
   |
13 ~         Event::SousPuissanceMoteur => alerte_cockpit(),
14 ~         Event::SurchauffeMoteur => todo!(),
   |
```

En 🦀, les matchs doivent être exhaustifs.

# 🛫 🛬
+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
# Threads

```typescript
// [...]

let vol = new Vol(15000);
// l'exécution de `voler` sera asynchrone
Promise.resolve(voler(vol));
// Toute modification de l'objet `vol` aura des conséquences
// sur le code de `voler`. Elles seront imprévisible
// et dépendantes de la vitesse d'exécution.
vol.altitude = 0 💀
```

Une des trois pires sources de bugs du monde logiciel provient de code
asynchrone ou parallélisé. 

## 🛫💥 😭🪦
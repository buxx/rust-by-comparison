+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
# Gestion d'erreur

```typescript
try {
  // Something which can `throw`
  maintenir_altitude(15000)
} catch (error) {
  // Act according to
}
💀
```

Certains langages utilise le mécanisme de "jet" d'erreurs. Cela implique pour
le développeur de potentiellement "attraper" l'erreur à travers **toute** la pile
d'appel. C'est fastidieux et complexe. Beaucoup de cas d'erreurs ne sont pas gérés
là où il devrait, voir traverse la pile complète et plante le programme.

## 🛫💥 😭🪦
+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
# Typage

```typescript
atteindre_altitude(vol.altitude + altitude_de_securite) 💀
```

Les langages qui ne contrôle pas réellement les types ne peuvent
pas garantir que cette ligne de code fonctionnera toujours. Rien
ne garantie que `vol.altitude` et `altitude_de_securite` sont
additionnable entre eux ni même qu'ils sont additionnable "tout court". 

En 🦀, il sera strictement impossible de compiler un code qui peut échouer
lors de cette addition.

## 🛫💥 😭🪦
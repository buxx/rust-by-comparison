+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
# Mutabilité

🐍 Js/TS
```python
vol = Vol()
vol.altitude = 15000
# `journaliser` peut modifier les valeurs de `vol`
journaliser(vol)
# L'intention était de voler à 15000 pieds,
# mais rien ne garantie que `vol.altitude`
# ne vaut pas désormais `0`
maintenir_altitude(vol) 💀
```

La plupart des langages ne permettent pas de voir,
à la lecture du code, si une valeur peut subir des modifications.

# 🛫💥 😭🪦

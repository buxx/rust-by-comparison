+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
# Mémoire

🐍 Js
```python
def radar():
    for signal in signaux():
        traiter_signal(signal)
    # 💀 La mémoire utilisé pour `signal` n'est pas
    # libéré à la sortie de la boucle
```

# 🛫💥 😭🪦

Les langages à "ramasse miette" exécutent à interval régulier une procédure
qui détermine si des objets sont à supprimer de la RAM.
C'est très complexe : à la sortie de la boucle, il peut y avoir des références
à `signal` qui ont été "diffusées" depuis `traiter_signal`.

Résultat💥: On ne maîtrise pas l'impact mémoire de ses programmes.
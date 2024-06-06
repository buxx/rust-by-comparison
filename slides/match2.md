+++
background-color: black;
color: white;  

article {
    margin-top: 0
}
+++
# Switch/Matchs

```python
class Event(enum.Enum):
    PerteAltitude = 0x000
    SousPuissanceMoteur = 0x001
    # Ajouté récemment
    SurchauffeMoteur = 0x002

# [...]

match event:
    case Event.PerteAltitude:
        alerte_cockpit()
    case Event.SousPuissanceMoteur:
        alerte_cockpit()
    💀
```

La gestion de l'évènement `SurchauffeMoteur` a été oublié dans ce `match`.
Le programme ne crashera pas et on pourrais même ajouter un cas de gestion de l'évènement inconnue. Mais vous tuerez quand même vos passager car les pilotes n'aurons pas
été informé de l'avarie.

Python/Typescript ne permet pas de valider l'exhaustivité des switch/match.

## 🛫💥 😭🪦
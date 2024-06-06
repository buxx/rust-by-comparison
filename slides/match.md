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

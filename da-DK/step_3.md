## Vis en besked

--- task ---

Åbn [Sense HAT-emulatoren](https://trinket.io/mission-zero){:target="_blank"} til Mission Zero-projektet.

Her kan du se, at der automatisk er blevet tilføjet tre linjer kode for dig:

```python
from sense_hat import SenseHat
sense = SenseHat()
sense.set_rotation(270)
```

![Et skærmbillede af Trinket Sense Hat-emulatoren med tre linjer startkode er vist i ruden til venstre.](images/sense-hat-emulator2.png)

Denne kode opretter forbindelse til Astro Pi og sørger for, at LED-displayet på Astro Pi vises på korrekt vis. Lad koden stå, for du får brug for den.

--- /task ---

--- task ---

Måske kunne du efterlade en hyggelig hilsen til de astronauter på ISS, der arbejder i nærheden af Astro Pi? Lad os rulle (scrolle) en besked hen over displayet.

Tilføj denne linje under den anden kode:

```python
sense.show_message("Astro Pi")
```

--- /task ---

--- task ---

Tryk på knappen **Run** (Kør) og kig på, mens beskeden `Astro Pi` ruller hen over LED-displayet.

![Trinket Sense HAT-emulatoren kører et prøveprogram, der ruller teksten "Astro PI" hen over LED-matricen med hvide bogstaver](images/M0_1.gif)

--- /task ---

For at få vist en anden besked kan du skrive præcist, hvad du ønsker mellem anførselstegnene (`""`).

--- collapse ---
---
title: Hvilke tegn kan bruges?
---

Sense HAT kan kun vise tegnsættet Latin 1, hvilket betyder, at kun følgende tegn er tilgængelige. Øvrige tegn vises som `?`.

```
+-*/!"#$><0123456789.=)(

ABCDEFGHIJKLMNOPQRSTUVWXYZ

abcdefghijklmnopqrstuvwxyz

?,;:|@%[&_']\~
```

--- /collapse ---

--- task ---

Du kan også ændre den hastighed, som beskeden ruller med hen over displayet med. Tilføj en `scroll_speed` (rullehastighed) til den kodelinje, du allerede har, som følger:

```python
sense.show_message("Astro Pi", scroll_speed=0.05)
```

Beskedens standardhastighed er `0.1`. Hvis du gør talværdien mindre, ruller beskeden hurtigere og hvis du gør talværdien større, ruller beskeden langsommere.

--- /task ---

### Vælg et navn til de nye Astro Pi -computere

--- task --- Vi vil navngive Astro Pi-computerne efter to inspirerende europæiske forskere. Der er hundredvis af mænd og kvinder, der har bidraget til videnskab og teknologi. Deltagere kan foreslå deres egne navne eller vælge fra vores liste over forslag (vær sikker på, at du bruger den engelske version af navnet):


[Ada Lovelace](https://en.wikipedia.org/wiki/Ada_Lovelace){:target="_blank"} 
[Alan Turing](https://en.wikipedia.org/wiki/Alan_Turing){:target="_blank"} 
[Caroline Herschel](https://en.wikipedia.org/wiki/Caroline_Herschel){:target="_blank"} 
[Edsger Dijkstra](https://en.wikipedia.org/wiki/Edsger_W._Dijkstra){:target="_blank"} 
[Hedy Lamarr](https://en.wikipedia.org/wiki/Hedy_Lamarr){:target="_blank"} 
[Hypatia](https://en.wikipedia.org/wiki/Hypatia){:target="_blank"} 
[John Edmonstone](https://en.wikipedia.org/wiki/John_Edmonstone){:target="_blank"} 
[Marie Curie](https://en.wikipedia.org/wiki/Marie_Curie){:target="_blank"} 
[Nikola Tesla](https://en.wikipedia.org/wiki/Nikola_Tesla){:target="_blank"} 
[Tycho Brahe](https://en.wikipedia.org/wiki/Tycho_Brahe){:target="_blank"}

For at stemme skal du starte din besked med ordene "My name should be" (på engelsk). Hvis du f.eks. vil stemme på Ada Lovelace, ser din kode således ud:

```python
sense.show_message("My name should be Ada Lovelace")
```

Hvis du ønsker at stemme, *skal* din besked starte med disse ord, ellers vil vi ikke automatisk kunne tælle den med.

--- /task ---




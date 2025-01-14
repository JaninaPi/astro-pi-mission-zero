## Mõõda õhuniiskust

Astro Pi-l asuv niiskuse sensor mõõdab ümbritseva õhu niiskust, mis on vajalik kosmoses valitsevate tingimuste kohta andmete kogumiseks.

![Trinket Sense HAT-i emulaator, kus on käivitatud näidisprogramm, mis kerib niiskuse väärtust valgete tähtedega üle LED-maatriksi](images/M0_3.gif)

Astro Pi mõõdab ISS-i niiskust protsentides vee kontsentratsiooni kohta õhus.

Osa sinu ülesandest on panustada ISS-i meeskonna igapäevaellu, seetõttu annab nende teavitamine sellest, et õhuniiskus kosmosejaama pardal on normaalses vahemikus, neile suuremat kindlust.

[[[generic-theory-what-is-humidity]]]

--- task ---

Õhuniiskuse mõõtmiseks lisa see kood:

```python
humid = sense.get_humidity()
```

See koodirida mõõdab valitsevat õhuniiskust ja säilitab mõõdetud väärtuse muutujas `humid`.

--- /task ---

--- task ---

Õhuniiskust mõõdetakse väga täpselt, st säilitataval väärtusel on suur kümnendkohtade arv. Sina võid väärtuse ümardada mistahes kümnendkohtadega arvuks. Näites ümardasime me ühe kümnendkohaga arvuks, aga teistsuguse täpsuse saavutamiseks muuda numbrit `1` selliseks kümnendkoha arvuks, mida soovid näha.

```python
humid = round(sense.get_humidity(), 1)
```

--- /task ---

--- task ---

Valitseva õhuniiskuse kuvamiseks ekraanil keritava sõnumina tuleb lisada see koodirida:

```python
sense.show_message(str(humid))
```

See `str()` osa konverteerib õhuniiskuse numbri tekstiks selle jaoks, et seda saaks kuvada Astro Pi-l.

--- /task ---

--- task ---

Samuti võid kuvada õhuniiskust mõne teise sõnumi osana, selleks pead oma sõnumi osad ühendama kasutades `+`.

```python
sense.show_message( "It is " + str(humid) + " %" )
```

--- /task ---

Tõeline Astro Pi mõõdab õhuniiskust enda ümber, aga sina võid niiskuse liugurit Sense HAT-i emulaatoril liigutada simuleerimaks niiskuse muutusi ja testimaks oma koodi.

![Nimega kuvatõmmis Sense HAT-i emulaatorist, koodiaken vasakul ja emulaator paremal. Niiskuse reguleerimiseks kasutatav liugur on ringitatuna paremas ülanurgas](images/humidity-slider.png)

**Märkus:** Sa võid mõelda, miks õhuniiskuse liugur näitab niiskust täisarvuna, aga need mõõtmise tulemused, mis sina saad, näitavad kümnendkohti. Emulaator simuleerib tõelise sensori väikest ebatäpsust, seetõttu võib sinu poolt nähtav õhuniiskuse mõõtmise tulemus olla natuke suurem või väiksem sellest väärtusest, mis sa liuguriga tegelikult määrasid.

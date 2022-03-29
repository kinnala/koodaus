{{#include header.md}}

# Ehtolauseet ja silmukat

## Rivien suoritusjärjestys

Kuten jo aiemmin mainittiin, koodin rivit suoritetaan
järjestyksessä ellei jokin ohjelmointikielen rakenne muuta
järjestystä.  Tälläisiä rakenteita ovat mm.

- ehtolauseet `if`, `elif` ja `else`
- silmukat `while` ja `for`

Nämä rakenteet mahdollistavat suuren osan tietokoneen
mielenkiintoisista käyttötarkoituksista, esim.
silmukoiden avulla voidaan toistaa samoja rivejä
tuhansia kertoja tai ehtolauseiden avulla voidaan
suorittaa muuttujan arvosta riippuen eri rivit.

## Totuusarvo ja vertailu

Ehtolauseiden ja silmukoiden kanssa käytetään totuusarvomuuttujia,
joiden tyyppi on `bool`.
Totuusarvo on joko `True` (tosi) tai `False` (epätosi).
Esimerkiksi ehtolauseessa arvolla `True` suoritetaan eri
rivit kuin arvolla `False`.
Totuusarvoja määritetään usein vertailujen avulla.

Tässä on muutamia usein käytettyjä vertailuja:

- `==` eli *yhtä suuri kuin*
- `!=` eli *eri suuri kuin*
- `<` eli *pienempi kuin*
- `>` eli *suurempi kuin*
- `<=` eli *pienempi tai yhtä suuri kuin*
- `>=` eli *suurempi tai yhtä suuri kuin*

```python,editable
x = 14
y = 12
z = x < y
print(z)
```

<button onclick="evaluatePython(0)">Suorita</button>
<br>
<br>
<textarea class="output-python" style="width: 100%;" rows="6"></textarea>

### Harjoituksia

1. Kokeile erilaisia vertailuja muuttujan `z` määrittelyssä.
2. Kokeile tulostaa muuttujan `z` tyyppi `type()` funktion avulla.

## Ehtolause

Ehtolauseessa totuusarvon perusteella suoritetaan eri rivit.
Oheisessa esimerkissä tulostetaan eri teksti totuusarvomuuttujan
`enemman_koiria` arvosta riippuen.
Huomaa, että ehtolauseessa suoritettavat rivit pitää *sisentää*,
eli rivien alkuun laitetaan aina sama määrä välilyöntejä.
Python on tarkka siitä, että kaikilla sisennettävillä riveillä
on sama määrä välilyöntejä.
```python,editable
koiria = 1
kissoja = 2
enemman_koiria = koiria > kissoja
if enemman_koiria:
  print("Koiria on enemmän kuin kissoja.")
else:
  print("Kissoja on enemmän (tai yhtä paljon) kuin koiria.")
```
<button onclick="evaluatePython(1)">Suorita</button>
<br>
<br>
<textarea class="output-python" style="width: 100%;" rows="6"></textarea>

Yllä lauseke `"Koiria on enemmän kuin kissoja."` on merkkijono.  Merkkijonoista
opitaan lisää seuraavassa luvussa.

### Harjoituksia

1. Kokeile kasvattaa koirien määrää kuvaavan muuttujan `koiria` arvoa siten,
   että ehtolause suorittaa eri rivit.

## Silmukka

## Totuusarvojen yhdistely

<!-- ## Esimerkki -->

<!-- Oheinen koodi suorittaa seuraavia operaatioita uudestaan -->
<!-- ja uudestaan kunnes lopputulos on yksi: -->

<!-- - Jos luku on parillinen, jaetaan se kahdella -->
<!-- - Jos luku on pariton, kerrotaan se kolmella ja lisätään yksi -->

<!-- Voit kokeilla suorittaa koodia eri alkuarvolla `x`, mutta pohditaan seuraavaksi -->
<!-- vaihe vaiheelta miten se toimii. -->
<!-- ```python,editable -->
<!-- x = 14 -->
<!-- while x != 1: -->
<!--     print(x) -->
<!--     if x % 2 == 0: -->
<!--         x = x // 2 -->
<!--     else: -->
<!--         x = 3 * x + 1 -->
<!-- print(x) -->
<!-- ``` -->

<!-- <button onclick="evaluatePython(1)">Suorita</button> -->
<!-- <br> -->
<!-- <br> -->
<!-- <textarea class="output-python" style="width: 100%;" rows="6"></textarea> -->

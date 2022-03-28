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
Tällaisen muuttujan arvo voi olla joko `True` (tosi) tai `False` (epätosi).
Esimerkiksi ehtolauseessa arvon ollessa `True` suoritetaan eri
rivit kuin arvon ollessa `False`.
Totuusarvoja määritellään usein vertailujen avulla.

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

1. Kokeile erilaisia vertailuja ja muuttujien `x` ja `y` arvoja.
2. Mikä on muuttujan `z` tyyppi? Kokeile `type()` funktiota.

## Ehtolause

## Silmukka

## Totuusarvojen yhdistely

## Esimerkki

Oheinen koodi suorittaa seuraavia operaatioita uudestaan
ja uudestaan kunnes lopputulos on yksi:

- Jos luku on parillinen, jaetaan se kahdella
- Jos luku on pariton, kerrotaan se kolmella ja lisätään yksi

Voit kokeilla suorittaa koodia eri alkuarvolla `x`, mutta pohditaan seuraavaksi
vaihe vaiheelta miten se toimii.
```python,editable
x = 14
while x != 1:
    print(x)
    if x % 2 == 0:
        x = x // 2
    else:
        x = 3 * x + 1
print(x)
```

<button onclick="evaluatePython(1)">Suorita</button>
<br>
<br>
<textarea class="output-python" style="width: 100%;" rows="6"></textarea>

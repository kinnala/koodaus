{{#include header.md}}

# Python laskimena

## Laskutoimituksia

Python on monipuolinen ohjelmointikieli.  Lisäksi se on kätevä laskin.
Hyödyllisiä peruslaskutoimituksia ovat

- yhteenlasku `+`
- vähennyslasku `-`
- kertolasku `*`
- jakolasku `/`
- potenssi `**`
- jakojäännös `%`
- jakolaskun kokonaislukuosa `//`

Laskujärjestys on tuttu matematiikasta ja sitä voi muuttaa sulkeilla.
Vastaus saadaan tekstinä ruudulle funktion `print()` avulla:

```python,editable
print(7 * (3 - 1))
```

<button onclick="evaluatePython(0)">Suorita</button>
<br>
<br>
<textarea class="output-python" style="width: 100%;" rows="6"></textarea>

<!-- ### Tehtävä: Korkolaskentaa -->

<!-- Jos alkupääoma on 1200 € ja siihen lisätään 3 % vuosikorko 5 vuoden ajalta, -->
<!-- saadaan lopulliseksi pääomaksi -->
<!-- \\[1200 \cdot \left(1 + \frac{3}{100}\right)^5.\\] -->
<!-- Suorita alla oleva koodi laskeaksesi lopullisen pääoman likiarvon.  Saatko muokattua koodia laskemaan lopullisen -->
<!-- pääoman 5 % vuosikorolla?[^vastaus1]  Kuinka monen vuoden jälkeen lopullinen pääoma on yli 2000&nbsp;€, jos -->
<!-- vuosikorko on 5 %?[^vastaus2] -->
<!-- ```python,editable -->
<!-- print(1200 * (1 + 3 / 100) ** 5) -->
<!-- ``` -->

<!-- <button onclick="evaluatePython(1)">Suorita</button> -->
<!-- <br> -->
<!-- <br> -->
<!-- <textarea class="output-python" style="width: 100%;" rows="6" disabled></textarea> -->

## Muuttujan määritteleminen

Koodi suoritetaan rivi kerrallaan ellei jokin ohjelmointikielen rakenne vaikuta
järjestykseen.  Aiempia tuloksia käytetään uudelleen määrittelemällä
*muuttuja*.  Muuttujan nimi voi olla esimerkiksi `x` ja arvo `3`, joka
kirjoitetaan muodossa `x = 3`.  Tämän jälkeen `x` viittaa arvoon `3`.
Muuttujan nimi voi sisältää kirjaimia, numeroita ja alaviivan `_`.  Muuttujan
nimi ei voi kuitenkaan alkaa numerolla.

```python,editable
x = 3
muuttuja = 3 * x
toinen_muuttuja = muuttuja * muuttuja
print(toinen_muuttuja)
```

<button onclick="evaluatePython(1)">Suorita</button>
<br>
<br>
<textarea class="output-python" style="width: 100%;" rows="6"></textarea>

## Arvon muuttaminen

Nimensä mukaisesti muuttujan arvo voi muuttua.  Mahdollinen käyttötarkoitus
on esimerkiksi summamuuttuja, jonka arvoon lisätään aiempia tuloksia.
Muuttujan `x` nykyiseen arvoon lisätään `3` kirjoittamalla
`x = x + 3`.
Tämän voi lyhentää muotoon `x += 3`.
Erilaisia lyhennemerkintöjä ovat

- lisäys `+=`
- vähennys `-=`
- kertominen `*=`
- jakaminen `/=`

Muuttujalle voi määritellä myös kokonaan uuden arvon.

```python,editable
x = 0
print(x)
x = x + 3
print(x)
x += 3
print(x)
x = 0
print(x)
```

<button onclick="evaluatePython(2)">Suorita</button>
<br>
<br>
<textarea class="output-python" style="width: 100%;" rows="6"></textarea>

## Muuttujan tyyppi

Arvon lisäksi jokaisella muuttujalla on *tyyppi*.
Python sisältää seuraavat
numeroihin liittyvät tyypit:

- `int` eli kokonaisluku, esim. `3`
- `float` eli liukuluku, esim. `3.0` (desimaalierotin on piste)
- `complex` eli kompleksiluku, esim. `3j`

Muuttujan tyypin saa selville funktiolla `type()`.
Eri numerotyypeillä voi laskea varsin
vapaasti ja muunnokset tapahtuvat usein automaattisesti.
Esimerkiksi kahden kokonaisluvun jakolaskun tulos
on automaattisesti liukuluku.
Muita myöhemmin opittavia tyyppejä ovat mm. `bool` eli totuusarvo,
`list` eli lista ja `str` eli merkkijono.
Uusia tyyppejä voi tehdä myös itse.
<!-- Muita usein käytettyjä tyyppejä ovat -->

<!-- - `bool` eli totuusarvo, joko `True` tai `False` -->
<!-- - `tuple` eli monikko, esim. pari `(0, 1)` -->
<!-- - `list` eli lista, esim. `[0, 1, 2, 3]` -->
<!-- - `range` eli lukujono, esim. `range(4)` vastaa monissa yhteyksissä listaa `[0, 1, 2, 3]` -->
<!-- - `str` eli merkkijono, esim. `"kolme"` -->
<!-- - `dict` eli hakemisto, esim. `{1: 3, 2: 2}` -->
<!-- - `NoneType` eli puuttuvan arvon `None` tyyppi -->

<!-- Yllä mainituista tyypeistä puhutaan myöhemmin lisää. -->

```python,editable
x = 5
y = 2
z = x / y
print(type(x))
print(type(y))
print(type(z))
print(z)
```

<button onclick="evaluatePython(3)">Suorita</button>
<br>
<br>
<textarea class="output-python" style="width: 100%;" rows="6"></textarea>

## Tehtävä: Koodin tulkinta

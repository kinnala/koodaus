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

Laskujärjestys on tuttu matematiikasta ja sitä voi muuttaa sulkeilla.
Vastaus saadaan tekstinä ruudulle komennon `print()` avulla:

```python,editable
print(7 * 8)
```

<button onclick="evaluatePython(0)">Suorita</button>
<br>
<br>
<textarea class="output-python" style="width: 100%;" rows="6" disabled></textarea>

### Tehtävä: Korkolaskentaa

Jos alkupääoma on 1200 € ja siihen lisätään 3 % vuosikorko 5 vuoden ajalta,
saadaan lopulliseksi pääomaksi
\\[1200 \cdot \left(1 + \frac{3}{100}\right)^5.\\]
Suorita alla oleva koodi laskeaksesi lopullisen pääoman likiarvon.  Saatko muokattua koodia laskemaan lopullisen
pääoman 5 % vuosikorolla?[^vastaus1]  Kuinka monen vuoden jälkeen lopullinen pääoma on yli 2000&nbsp;€, jos
vuosikorko on 5 %?[^vastaus2]
```python,editable
print(1200 * (1 + 3 / 100) ** 5)
```

<button onclick="evaluatePython(1)">Suorita</button>
<br>
<br>
<textarea class="output-python" style="width: 100%;" rows="6" disabled></textarea>

## Muuttujan määritteleminen

Koodi suoritetaan rivi kerrallaan ellei jokin komento vaikuta järjestykseen.
Aiempia tuloksia käytetään uudelleen määrittelemällä muuttuja.  Muuttujan nimi
voi olla esimerkiksi `x` ja arvo `0.3`, joka kirjoitetaan muodossa `x = 0.3`.
Tämän jälkeen `x` viittaa arvoon `0.3`.

```python,editable
x = 0.3
print(3 * x)
```

<button onclick="evaluatePython(2)">Suorita</button>
<br>
<br>
<textarea class="output-python" style="width: 100%;" rows="6" disabled></textarea>

[^vastaus1]: n. 1532 €

[^vastaus2]: 11 vuoden jälkeen

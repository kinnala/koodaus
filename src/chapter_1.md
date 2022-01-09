<script src="https://cdn.jsdelivr.net/pyodide/v0.18.1/full/pyodide.js"></script>
<script>
function setup(pyodide) {
  var setup_code = `
import sys, io, traceback
def run_code(code):
    out = io.StringIO()
    oldout = sys.stdout
    olderr = sys.stderr
    sys.stdout = sys.stderr = out
    try:
        exec(code, {})
    except:
        traceback.print_exc()
    
    sys.stdout = oldout
    sys.stderr = olderr
    return out.getvalue()
`
  pyodide.runPython(setup_code)
}

async function main() {
  let pyodide = await loadPyodide({
    indexURL: "https://cdn.jsdelivr.net/pyodide/v0.18.1/full/",
  });
  setup(pyodide);
  return pyodide;
}
let pyodideReadyPromise = main();

async function evaluatePython(i) {
  let pyodide = await pyodideReadyPromise;
  try {
    let editor = document.getElementsByClassName("ace_editor")[i].env.editor;
    pyodide.globals.code_to_run = editor.getValue();
    let output = pyodide.runPython('run_code(code_to_run)');
    document.getElementsByClassName("output-python")[i].value = output;
  } catch (err) {
    document.getElementsByClassName("output-python")[i].value = err;
  }
}
</script>

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
Aiempia tuloksia voi käyttää uudelleen määrittelemällä muuttujan.
Muuttujan nimi voi olla esimerkiksi `x` ja arvo `0.3`, joka kirjoitetaan
muodossa `x = 0.3`.  Seuraavilla riveillä `x` viittaa arvoon `0.3`.

### Tehtävä: 

```python,editable
x = 0.3
print(3 * x - 0.9)
```

<button onclick="evaluatePython(2)">Suorita</button>
<br>
<br>
<textarea class="output-python" style="width: 100%;" rows="6" disabled></textarea>

[^vastaus1]: n. 1532 €

[^vastaus2]: 11 vuoden jälkeen

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

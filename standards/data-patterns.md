# Data Patterns

Patrones de datos para apps sin servidor.

## localStorage

Usar para:

- Preferencias.
- Datos pequenos.
- Ultimo estado de la app.
- Borradores.

No usar para datasets grandes.

Patron:

```js
const STORAGE_KEY = "miniapp:v1";

function loadState(fallback) {
  try {
    const raw = localStorage.getItem(STORAGE_KEY);
    return raw ? JSON.parse(raw) : fallback;
  } catch {
    return fallback;
  }
}

function saveState(state) {
  localStorage.setItem(STORAGE_KEY, JSON.stringify(state));
}
```

## IndexedDB

Usar para:

- Muchos registros.
- Archivos procesados.
- Historiales largos.
- Busqueda local persistente.

## JSON import/export

Toda app con estado propio deberia poder exportar un backup.

```js
function downloadJson(filename, data) {
  const blob = new Blob([JSON.stringify(data, null, 2)], {
    type: "application/json"
  });
  const url = URL.createObjectURL(blob);
  const a = document.createElement("a");
  a.href = url;
  a.download = filename;
  a.click();
  URL.revokeObjectURL(url);
}
```

## CSV

Usar PapaParse cuando:

- Hay importaciones complejas.
- Hay comillas, separadores variables o archivos grandes.

Para exportes simples, generar CSV manualmente con escaping correcto.

## SQLite/WASM

Usar `sql.js` o `DuckDB-WASM` cuando:

- El usuario necesita consultas.
- Hay joins, filtros avanzados o agregaciones.
- El dataset entra razonablemente en memoria del navegador.

## Scraping client-side

Opciones viables:

- Pegar HTML.
- Subir un archivo HTML.
- Fetch a fuentes con CORS habilitado.
- Pegar texto y parsearlo.

No depender de scraping remoto universal.

# Mini Apps Builder

Meta-workspace para crear mini apps client-side en un unico archivo HTML.

La idea: pedir una herramienta concreta, recibir un `.html` completo y abrirlo directo en el navegador. Sin backend, sin build step obligatorio, sin levantar servidor. Ideal para calculadoras, dashboards, recetas, parsers, scrapers client-side, herramientas de aprendizaje, reportes locales y utilidades pasajeras pero bien hechas.

## Filosofia

- **Single-file first:** la salida principal es un `.html` autocontenido.
- **Client-side only:** HTML, CSS y JavaScript vanilla.
- **Sin servidor:** la app debe poder abrirse con doble click.
- **Herramienta real:** la primera pantalla es la experiencia usable, no una landing page.
- **Datos portables:** JSON import/export como backup universal.
- **Persistencia local:** `localStorage`, `IndexedDB` o SQLite/WASM cuando aplique.
- **CDNs permitidos:** librerias modernas por CDN si agregan valor claro.
- **Estetica consistente:** cada app debe sentirse pulida, organizada y lista para usar.

## Estructura

```txt
mini-apps-builder/
  AGENTS.md
  meta-system-prompt.md
  README.md
  apps/
    README.md
  prompts/
    app-request-template.md
  data/
    README.md
  templates/
    single-file-app.html
  standards/
    app-checklist.md
    aesthetic-packs.md
    data-patterns.md
    design-system.md
    output-contract.md
  examples/
    recipe-scaler.html
    json-dashboard.html
```

## Uso Con Codex

En otra PC:

```bash
git clone <repo-url> mini-apps-builder
cd mini-apps-builder
```

Despues, en Codex, pedi algo como:

```txt
Lee AGENTS.md y meta-system-prompt.md.
Quiero una mini app single-file en apps/ para analizar un CSV de gastos.
Debe tener filtros, graficos, import/export JSON y estetica Ledger Sharp.
```

Codex deberia:

- leer `AGENTS.md`;
- usar `meta-system-prompt.md` como contrato principal;
- consultar `standards/`;
- generar la app final dentro de `apps/`;
- dejar datos locales en `data/`.

`apps/` y `data/` estan ignorados por git para evitar subir cosas privadas o generadas.

## Uso Manual

1. Abrir `meta-system-prompt.md`.
2. Pegar ese prompt como instruccion base cuando se pida una mini app.
3. Agregar el pedido concreto:

```txt
Quiero una mini app para planificar recetas semanales.
Debe importar/exportar JSON, generar lista de compras, escalar porciones y permitir marcar favoritos.
```

4. La respuesta esperada debe ser un unico archivo HTML.

Las mini apps finales van en `apps/`. Los archivos de `examples/` son solo referencias de estilo y estructura.

## Esteticas

Las esteticas viven en `standards/aesthetic-packs.md`.

- `Workbench Calm`: default utilitario, claro y sobrio.
- `Studio Glass`: mas visual, para generadores creativos.
- `Ledger Sharp`: compacto y tabular, ideal para dashboards.
- `Notebook Warm`: editorial, bueno para recetas y aprendizaje.
- `Tokyo Mono`: B/W, monocromatico, serio, sleek, ideal para runbooks y herramientas tecnicas.
- `Graphite Hacker`: oscuro, monocromatico, monospace, graphite/charcoal con naranja calido.

## Tipos de apps ideales

- Recetas, listas, planificadores y generadores.
- Calculadoras y simuladores.
- Dashboards de CSV/JSON.
- Extractores desde texto, HTML pegado o archivos locales.
- Herramientas de aprendizaje, flashcards y quizzes.
- Inventarios, trackers, checklists y mini CRMs personales.

## Limites asumidos

- Sin backend no hay secretos seguros en cliente.
- Scraping remoto puede fallar por CORS; preferir pegar HTML, subir archivos o usar fuentes con CORS habilitado.
- Para datasets grandes usar IndexedDB, SQL.js o DuckDB-WASM en vez de guardar todo en `localStorage`.

## Publicar En GitHub

El repo esta pensado para publicar solo la fabrica, no los outputs locales.

Antes de pushear:

```bash
git status --short
git add .
git status --short
```

Chequea que no aparezcan archivos privados de `apps/` o `data/`.

Luego:

```bash
git commit -m "Initial mini apps builder workspace"
git branch -M main
git remote add origin <repo-url>
git push -u origin main
```

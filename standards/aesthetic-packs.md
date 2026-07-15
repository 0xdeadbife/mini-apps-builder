# Aesthetic Packs

Las mini apps pueden compartir arquitectura y cambiar de piel visual. Si el usuario no pide una estetica, usar `Workbench Calm`.

## Workbench Calm

Default general.

- Fondo claro gris verdoso.
- Superficies blancas.
- Lineas sutiles.
- Acento azul.
- Segundo acento verde.
- Ideal para herramientas de uso diario.

## Studio Glass

Mas expresiva, sin volverse decorativa.

- Fondo con imagen, textura o color profundo.
- Paneles con transparencia leve.
- Bordes suaves.
- Ideal para generadores creativos, moodboards y escritura.

## Ledger Sharp

Compacta y precisa.

- Tablas densas.
- Colores sobrios.
- Tipografia numerica clara.
- Ideal para calculadoras, finanzas, dashboards y comparadores.

## Notebook Warm

Mas editorial y humana.

- Fondo papel suave.
- Tipografia comoda.
- Secciones tipo cuaderno.
- Ideal para recetas, aprendizaje, diarios, planificacion y contenidos.

## Tokyo Mono

Monocromatica, seria y sleek. Inspirada en herramientas tecnicas japonesas/neo-tokyo sin caer en neon, hacker cosplay ni decoracion cyberpunk. Debe sentirse como un producto interno premium: sobrio, preciso, legible y durable.

- Paleta B/W con grises calibrados: black, ink, graphite, zinc, mist.
- Sin acentos cromaticos fuertes por defecto; usar blanco, gris claro o un gris frio para estados activos.
- Colores funcionales extremadamente contenidos: success/warn/danger deben ser grises tintados, no semaforo saturado.
- Fondo casi negro, superficies apenas elevadas, bordes finos y limpios.
- Tipografia principal sans seria y legible: `Inter`, `IBM Plex Sans`, `Geist`, `ui-sans-serif`, `system-ui`.
- Tipografia de codigo/datos monospace: `JetBrains Mono`, `IBM Plex Mono`, `SFMono-Regular`, `Consolas`, monospace.
- Usar monospace solo para comandos, rutas, IDs, tablas densas, contadores y valores tecnicos.
- Titulos con sans, peso medio/semibold, sin estetica terminal.
- Componentes sobrios: topbar, segmented filters, command cards, compact tables, code blocks, side notes.
- Code blocks con buen contraste, padding generoso, line-height claro y acciones discretas.
- Microcopy directa y seca: `Copy`, `Export`, `Reset`, `Filter`, `Output`, no exceso de brackets o glyphs.
- Evitar `::`, `[OK]`, `>_`, scanlines, glow, gradientes visibles, orbs, bokeh, emojis y ornamento hacker.
- Cards pocas y utiles; preferir paneles planos, listas compactas y separadores.
- Ideal para cheatsheets, pentest notes, technical runbooks, dashboards serios, internal tools, coding aides y analizadores.

Tokens sugeridos:

```css
:root {
  color-scheme: dark;
  --bg: #08090a;
  --surface: #0f1012;
  --surface-2: #151619;
  --surface-3: #1c1e22;
  --text: #f1f2f0;
  --text-soft: #c9cbc8;
  --muted: #8f928d;
  --faint: #5f635f;
  --line: #25282c;
  --line-strong: #363a40;
  --active: #e7e8e4;
  --active-contrast: #08090a;
  --success: #a8b2a3;
  --warning: #b8aa8a;
  --danger: #b59a96;
  --radius: 6px;
  --shadow: none;
  --font-ui: Inter, "IBM Plex Sans", Geist, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  --font-code: "JetBrains Mono", "IBM Plex Mono", "SFMono-Regular", Consolas, monospace;
}
```

Reglas de composicion:

- Usar espacio negativo como lujo principal, no efectos.
- Los controles deben parecer instrumentos, no badges decorativos.
- Los labels de formularios van en sans o small caps suaves; los valores tecnicos en monospace.
- Botones primarios monocromos: superficie clara con texto oscuro, o borde claro con fondo oscuro.
- El estado activo debe ser claro por contraste, no por color llamativo.
- Si una pantalla se ve "AI dashboard template", reducir: menos cards, menos chips, menos sombras, menos texto explicativo.

## Graphite Hacker

Oscura, monocromatica y tecnica, inspirada en themes locales graphite/charcoal con acentos naranja calido. Debe sentirse como una herramienta hacker sobria, neo-retro-tech y sleek, no como una interfaz gamer neon.

- Fondos graphite, charcoal y blackened gray.
- Superficies en grises oscuros muy cercanos entre si.
- Bordes finos en grises medios con contraste bajo pero legible.
- Acento principal naranja calido, tipo amber/copper/burnt orange.
- Acentos secundarios muy contenidos: slate claro, muted zinc o verde terminal apagado solo para estados.
- Tipografia monospace en toda la UI o, como minimo, en titulos, controles, tablas y datos.
- Usar stacks tipo `JetBrains Mono`, `Fira Code`, `IBM Plex Mono`, `SFMono-Regular`, `Consolas`, monospace.
- Permitir simbolos tipo Nerd Fonts, Font Awesome o glyphs tecnicos para acciones y estados, siempre con fallback textual o `aria-label`.
- Componentes compactos: toolbars, panels, tabs, command bars, inspector panes, tables.
- Detalles visuales: brackets, carets, prompt marks, separators finos, counters, status chips, scanline sutil si no distrae.
- Radios chicos, sombras casi inexistentes, foco en lineas, contraste y ritmo.
- Ideal para parsers, scrapers, dashboards tecnicos, analizadores, calculadoras logicas, herramientas dev y workbenches locales.

Tokens sugeridos:

```css
:root {
  --bg: #0b0d0e;
  --surface: #111315;
  --surface-2: #181b1e;
  --surface-3: #202428;
  --text: #d7d7d2;
  --muted: #8d918b;
  --line: #2c3033;
  --accent: #d9822b;
  --accent-2: #a86224;
  --success: #7a9b68;
  --danger: #c46a5a;
  --warning: #d6a45d;
  --radius: 6px;
  --font-ui: "JetBrains Mono", "Fira Code", "IBM Plex Mono", "SFMono-Regular", Consolas, monospace;
}
```

Buenas microcopias visuales:

- `>_` para consola o entrada.
- `[#]` para items numerados o entidades.
- `[OK]`, `[WARN]`, `[ERR]` para estados compactos.
- `::` como separador tecnico.
- `cmd`, `src`, `out`, `trace`, `queue`, `buffer`, `index` para labels cuando tenga sentido.

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

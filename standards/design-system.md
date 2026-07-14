# Design System

Base visual para mini apps client-side.

## Principios

- Herramienta primero, explicacion despues.
- Densidad util.
- Controles previsibles.
- Contraste suficiente.
- Poco ornamento.
- Jerarquia clara.

## Layout base

- `app-shell`: contenedor general.
- `topbar`: titulo, subtitulo corto, estado, acciones globales.
- `workspace`: grid principal.
- `panel`: zonas funcionales.
- `toolbar`: acciones locales, busqueda, filtros.
- `table-wrap`: tablas responsivas.

## Tokens sugeridos

```css
:root {
  --bg: #f6f7f3;
  --surface: #ffffff;
  --surface-2: #eef1ec;
  --text: #18201d;
  --muted: #65716b;
  --line: #d9dfd7;
  --accent: #266ef1;
  --accent-2: #16875d;
  --danger: #b42318;
  --warning: #a15c07;
  --radius: 8px;
  --shadow: 0 10px 30px rgba(24, 32, 29, 0.08);
}
```

## Componentes

- Botones primarios para accion principal.
- Botones secundarios para acciones frecuentes.
- Botones fantasma para acciones de bajo peso.
- Inputs con label.
- Tabs para vistas.
- Chips para filtros activos y estado.
- Tablas para datos comparables.
- Cards solo para items repetidos o paneles funcionales.
- Toast o status inline para feedback.

## Mobile

- Toolbar con wrap.
- Tablas con scroll horizontal.
- Paneles en una columna.
- Botones tactiles con alto minimo de 40px.
- Evitar texto diminuto en controles.

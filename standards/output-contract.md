# Output Contract

Toda mini app generada desde este workspace debe cumplir este contrato.

## Formato

- Un unico archivo `.html`.
- Debe incluir `<!doctype html>`.
- Debe incluir CSS en `<style>`.
- Debe incluir JavaScript en `<script>`.
- Debe poder abrirse con doble click en el navegador.

## Dependencias

- Permitidas por CDN.
- Deben estar justificadas por valor funcional.
- No usar frameworks de aplicacion por defecto.
- No usar assets locales salvo que esten embebidos o sean opcionales.

## Persistencia

Por defecto:

- Estado pequeno: `localStorage`.
- Estado mediano: `IndexedDB`.
- Backup: export/import JSON.

La app debe seguir siendo util aunque el storage este vacio.

## Exportes

Incluir al menos uno cuando aplique:

- JSON para backup completo.
- CSV para tablas.
- Markdown para texto estructurado.
- PDF o imagen para reportes visuales.

## Seguridad

- No pedir ni guardar secretos.
- No incluir claves privadas.
- Si usa una API key publica, explicar que no es segura en cliente.
- Validar entradas del usuario.
- Escapar contenido dinamico si se inserta como HTML.

## UX minima

- Estado vacio.
- Estado con datos de ejemplo.
- Estado de error.
- Confirmaciones destructivas.
- Responsive mobile/desktop.
- Acciones globales visibles.

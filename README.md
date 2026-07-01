# Generador de PDF — AMF

Generador de documentos PDF para **Alfonso Montero Executive Transportation** (AMF),
servicio de traslados ejecutivos aeroportuarios en Colombia.

Aplicación web de un solo archivo (`index.html`), sin build ni backend: se abre
directamente en el navegador.

## Secciones

- **Tarifas** — Genera una hoja de tarifas con diseño premium (tema oscuro + dorado).
  Editor en vivo con presets por ciudad (Bogotá, Medellín), servicios, recargos,
  condiciones, etc. Descarga en PDF con alto dinámico según el contenido.
- **Certificación / Hoja Membretada** — Genera certificaciones de servicio en hoja
  membretada A4 (header/footer con onda dorada, logo, firma digital opcional).
  El texto es editable en vivo. Se exporta a PDF de una sola página usando la
  impresión nativa del navegador (Guardar como PDF), para máxima fidelidad al preview.

## Uso

1. Abre `index.html` en el navegador (o sírvelo con cualquier servidor estático).
2. Cambia entre las pestañas **Tarifas** y **Certificación**.
3. Edita los campos: todo se auto-guarda en el navegador (`localStorage`).
4. Descarga / guarda el PDF con el botón superior derecho.

## Tecnología

- HTML + CSS + JavaScript vanilla, sin dependencias de build.
- [html2canvas](https://html2canvas.hertzen.com/) + [jsPDF](https://github.com/parallax/jsPDF) (vía CDN) para la exportación de Tarifas.
- Impresión nativa del navegador para la Certificación.

## Archivos

- `index.html` — La aplicación completa (editor + preview + exportación).
- `hoja-membretada-AMF.html` — Documento base de referencia del diseño de la certificación.

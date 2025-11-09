 # Especificación de diseño — Paleta, tipografías y tamaños

Fecha: 2025-11-09

Objetivo: definir tokens visuales mínimos para la landing del IPN (paleta de hasta 5 colores, familias tipográficas, escalas de tamaño y comprobaciones WCAG AA) y proporcionar ejemplos en Markdown.

## Paleta (máx. 5 colores)

| Nombre | Hex | Uso sugerido | Nota de contraste (con blanco #ffffff) |
|--------|-----:|-------------|----------------------------------------:|
| Púrpura institucional | #682444 | Color principal (botones, acentos, headings) | Contraste alto vs blanco — adecuado para AA |
| Blanco | #ffffff | Fondo principal, fondos limpios | N/A |
| Gris claro | #f5f0f3 | Fondos alternos, paneles suaves | Usar para secciones alternas |
| Gris oscuro | #333333 | Texto principal (parágrafos) | Contraste elevado con blanco — cumple AA para texto normal |
| Azul acento | #006494 | Links secundarios, acentos CTA alternos | Buen contraste con blanco — buen color secundario |

Notas:
- Incluye el púrpura institucional `#682444` como color principal. El resto son neutrales/acentos para mantener legibilidad.
- Estas cinco cubren fondo, texto, acento y paneles. Mantener combinaciones de alto contraste para texto (ej. `#333333` sobre `#ffffff`).

## Familias tipográficas (2–3 familias)

1. Sans (primaria) — `Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial` (uso: body, UI, navegación)
2. Serif (display / headings alternos) — `Merriweather, Georgia, "Times New Roman", serif` (uso: headings alternativos y citas)
3. Monospace (opcional) — `"Fira Code", "Fira Mono", "Courier New", monospace` (uso: código o datos técnicos)

Recomendación: usar las families locales/sistema para evitar dependencia obligatoria de Google Fonts; si se desea, se puede añadir `Inter` y `Merriweather` desde Google Fonts en una versión posterior.

## Escala tipográfica (tamaños y pesos)

- Tamaño base (body): 16px (1rem)
- H1: clamp(1.8rem, 3.2vw, 2.5rem) — peso 700
- H2: clamp(1.4rem, 2.6vw, 1.9rem) — peso 600
- H3: 1.25rem — peso 600
- Body / p: 1rem — peso 400
- Small / meta: 0.875rem — peso 400

Ejemplo CSS (variables):

```css
:root{
  --color-primary: #682444;
  --color-white: #ffffff;
  --color-surface: #f5f0f3;
  --color-text: #333333;
  --color-accent: #006494;

  --font-sans: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
  --font-serif: Merriweather, Georgia, "Times New Roman", serif;

  --fs-base: 16px;
  --fs-h1: clamp(1.8rem, 3.2vw, 2.5rem);
  --fs-h2: clamp(1.4rem, 2.6vw, 1.9rem);
  --fs-h3: 1.25rem;
}
```

## Ratios de contraste (WCAG AA)

- Texto normal: contraste mínimo 4.5:1
- Texto grande (>=18pt regular o 14pt bold): contraste mínimo 3:1

Combinaciones recomendadas desde la paleta:
- `#333333` (texto) sobre `#ffffff` (fondo) — cumple AA para texto normal.
- `#682444` (púrpura) sobre `#ffffff` — cumple AA para texto normal y tiene buen peso para headings/CTAs.
- `#006494` (azul acento) sobre `#ffffff` — cumple AA para enlaces/CTAs secundarios.

Si en algún caso se usaran colores de menor contraste, reservarlos sólo para elementos gráficos o para texto grande/semigráfico.

## Ejemplos en Markdown

### Heading (H1)

Formación técnica ligada a la industria

### Párrafo (body)

Programas, prácticas profesionales y formación continua diseñados para impulsar carreras y conexiones laborales.

### Botones

- CTA principal: fondo `#682444`, texto `#ffffff` — ejemplo: **Solicita información**
- CTA secundario: borde `#682444`, fondo `transparent`, texto `#682444` — ejemplo: *Guía para padres*

---
Si quieres, aplico ahora uno de estos cambios en el CSS (por ejemplo: añadir las variables y reglas tipográficas). Actualmente aplicaré ese único cambio al CSS para que el proyecto use los tokens aquí definidos.

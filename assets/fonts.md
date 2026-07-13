# Fuentes de marca

Sistema tipográfico oficial (brandbook pág. 29): **tres familias con roles definidos.**

| Rol | Fuente | Pesos | Carácter / uso |
|-----|--------|-------|----------------|
| **Títulos · display · números** | **Lemon Milk** | Display (mayúsculas) | Geométrica y sólida. Titulares, displays y números. Es también el wordmark del imagotipo. |
| **Subtítulos · kickers · etiquetas** | **Nunito** | SemiBold · Bold · ExtraBold | Redondeada y cercana. |
| **Contenido · párrafos · texto corrido** | **Prompt** | Light · Regular · Medium | Limpia y legible. |

> **Justificación:** Lemon Milk ancla los titulares a la identidad del imagotipo (rigor); Nunito aporta
> calidez en subtítulos y etiquetas; Prompt sostiene el contenido extenso. Equilibran los dos lados del
> Mentor: el rigor del display y la cercanía del texto.

## Disponibilidad
- **Nunito** — gratis (Google Fonts): https://fonts.google.com/specimen/Nunito
- **Prompt** — gratis (Google Fonts): https://fonts.google.com/specimen/Prompt
- **Lemon Milk** — **NO es libre**. Dos notas clave:
  - Para el **logo** no la necesitas: el wordmark ya viene **vectorizado** en `/assets`.
  - Para **títulos** donde no tengas Lemon Milk licenciada, usa **Nunito Black** (o **Jost 700**) como
    *fallback* de display. Así se ve en el propio Figma del brandbook hoy.

## Web (CSS)
```css
/* Familias libres (Nunito + Prompt) */
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@600;700;800&family=Prompt:wght@300;400;500&display=swap');

h1, h2, .display { font-family: 'Lemon Milk', 'Nunito', sans-serif; font-weight: 900; text-transform: uppercase; } /* fallback Nunito si no hay Lemon Milk */
h3, h4, .kicker, .label { font-family: 'Nunito', sans-serif; font-weight: 800; }
p, .body { font-family: 'Prompt', sans-serif; font-weight: 400; }
```

## Descargas
- Nunito: https://fonts.google.com/download?family=Nunito
- Prompt: https://fonts.google.com/download?family=Prompt
- Jost (fallback de display, libre): https://fonts.google.com/specimen/Jost

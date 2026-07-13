# AI Kit — cómo generar piezas de marca con IA (sin que invente la identidad)

> Guía para cualquier persona de Actuaria que use IA. Léela antes de pedir una pieza.

## ⚠️ Lo primero: qué SÍ y qué NO puede hacer cada IA

Las **IAs de imagen** (ChatGPT-imágenes / DALL·E, Midjourney, etc.) **NO navegan repos ni descargan
archivos**. Generan píxeles desde texto, así que **siempre inventan el logo y las fuentes** aunque les
pases la URL del brandbook. Pedirles «lee el repo y usa el logo» **no funciona** para reproducir la
identidad exacta.

| Necesitas… | Usa… | Por qué |
|------------|------|---------|
| Logo / tipografía **exactos** (gift card, banner, credencial, post) | IA de **código** (Claude, Cursor…) que genere **HTML/CSS** + los archivos de `assets/` | Sí lee archivos → resultado pixel-perfect |
| **Fondo / ilustración / textura** (sin logo) | IA de **imagen** con hexes literales | Aceptable como material de apoyo |
| Meter el logo en una imagen | **Adjunta el PNG del logo** como referencia y pide *componer*, no *dibujar* | El modelo no puede recrear el logo; solo colocarlo |

**Regla de oro:** el logo y las fuentes **no se generan, se insertan** desde `assets/`.

---

## Activos oficiales (enlaces directos / raw)

Logo (usar SIEMPRE estos archivos, no redibujar):
- Color (fondo claro): `https://raw.githubusercontent.com/renatopuente-ux/actuaria-brandbook-ai/main/assets/actuaria-logo-color.svg` · [PNG](https://raw.githubusercontent.com/renatopuente-ux/actuaria-brandbook-ai/main/assets/actuaria-logo-color.png)
- Negativo (fondo oscuro): `.../assets/actuaria-logo-negative.svg` · `.png`
- Mono navy: `.../assets/actuaria-logo-mono-navy.svg`

Tokens (fuente canónica de color/tipografía):
- `https://raw.githubusercontent.com/renatopuente-ux/actuaria-brandbook-ai/main/tokens/tokens.json`

Fuente: **Nunito** — ver [`assets/fonts.md`](./assets/fonts.md).

### Valores literales (pégalos en el prompt, no dependas de la URL)
- Navy `#151F47` · Azul `#3061AA` · Naranja `#DF5E2D` · Superficie `#E8ECF4` · Neutro `#D9DEEB`
- Naranja sobre navy → usar `#FFBBA1` (contraste AA)
- Tipografía: **Nunito** (400–900). Proporción de color **60/30/10** (navy/azul/naranja).
- Símbolo: **velero** de 3 partes (vela mayor navy, foque naranja, casco azul) + wordmark «ACTUARIA».

---

## Prompt A — IA de CÓDIGO (recomendado para piezas de marca)

> Úsalo con Claude, Cursor u otra IA que pueda leer archivos y escribir HTML/CSS.

```
Actúa como diseñador de marca de Actuaria. Vas a generar [PIEZA] como HTML/CSS autocontenido,
listo para exportar a PNG/PDF.

Fuentes obligatorias (léelas y respétalas):
- Tokens: https://raw.githubusercontent.com/renatopuente-ux/actuaria-brandbook-ai/main/tokens/tokens.json
- Logo (insértalo como <img> o SVG embebido, NO lo redibujes):
  https://raw.githubusercontent.com/renatopuente-ux/actuaria-brandbook-ai/main/assets/actuaria-logo-color.svg
  (sobre fondo oscuro usa actuaria-logo-negative.svg)
- Fuente Nunito vía @import de Google Fonts.

Reglas: usa SOLO los colores de tokens.json; tipografía Nunito; proporción 60/30/10; naranja sobre
navy = #FFBBA1; respeta el área de seguridad del logo (½ de la altura de la "A"). No inventes
colores, fuentes ni un logo alternativo.

Contenido: [describe textos/datos de la pieza].
Al final, lista cómo verificaste que cumple la identidad.
```

## Prompt B — IA de IMAGEN (solo fondos/concepto; adjunta el logo)

> Úsalo con ChatGPT-imágenes / DALL·E / Midjourney. **Adjunta el archivo del logo** (PNG) al chat.

```
Genera SOLO el fondo/composición de [PIEZA] con estética Actuaria: minimalista, corporativa,
neumorfismo suave sobre superficie #E8ECF4. Paleta EXACTA (no uses otros colores):
navy #151F47, azul #3061AA, naranja #DF5E2D (acento, ~10%). Tipografía Nunito.
NO dibujes ningún logo ni el texto "ACTUARIA": deja un espacio limpio arriba-izquierda para
colocar el logo después. No inventes marcas, taglines ni íconos de barco.
```
Luego **coloca el logo tú** (el PNG adjunto) sobre el espacio reservado, en Figma/Canva/editor.

> Si el modelo permite *image edit* con referencia, adjunta `actuaria-logo-color.png` y pide
> «coloca este logo exacto en la esquina, sin modificarlo».

---

## Checklist de homologación (antes de dar por buena una pieza)
- [ ] ¿El logo es el archivo oficial de `assets/` (velero tricolor + ACTUARIA), no uno inventado?
- [ ] ¿Colores solo de la paleta (`#151F47`, `#3061AA`, `#DF5E2D`, neutros)? ¿60/30/10?
- [ ] ¿Tipografía Nunito (no una genérica)?
- [ ] ¿Sin taglines/íconos inventados (p. ej. «Transformamos datos en decisiones» NO es de marca)?
- [ ] ¿Naranja sobre navy usa `#FFBBA1`?
- [ ] ¿Área de seguridad del logo respetada?

Si algo no está en este repo, **no es de marca**.

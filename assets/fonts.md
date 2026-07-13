# Fuentes de marca

## Nunito — sistema y cuerpo (obligatoria)
Toda la tipografía de UI, documentos y piezas usa **Nunito** (Google Fonts).

- Google Fonts: https://fonts.google.com/specimen/Nunito
- Pesos: 400 / 600 / 700 / 800 / 900

**Web (CSS):**
```css
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&display=swap');
body { font-family: 'Nunito', sans-serif; }
```

**Descarga (para editores gráficos / instalar en el sistema):**
https://fonts.google.com/download?family=Nunito

## Lemon Milk — wordmark del logo (display)
El wordmark «ACTUARIA» está trazado en **Lemon Milk**. No es de uso libre y **no la necesitas para
usar el logo**: los archivos de `assets/` ya traen el wordmark **vectorizado** (outlined), así que el
logo se ve idéntico sin instalar la fuente.

- Si necesitas un título display sin usar el logo, usa **Nunito 900** o, como aproximación al estilo
  geométrico del wordmark, **Jost 600** (https://fonts.google.com/specimen/Jost).
- No escribas «ACTUARIA» a mano con otra fuente para simular el logo: usa el archivo del logo.

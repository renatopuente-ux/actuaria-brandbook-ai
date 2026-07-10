# 3. Color

> Fuente canónica de valores: [`/tokens/tokens.json`](../tokens/tokens.json). Esta página explica el
> **uso**; los valores exactos también están aquí para lectura directa.

## Paleta núcleo (marca)

| Rol | HEX | Pantone | CMYK | RGB |
|-----|-----|---------|------|-----|
| **Navy** (institucional) | `#151F47` | 2766 C | 100/92/40/44 | 21, 31, 71 |
| **Azul** (secundario) | `#3061AA` | 7455 C | 87/66/1/0 | 48, 97, 170 |
| **Naranja** (acento) | `#DF5E2D` | 7579 C | 8/77/94/1 | 223, 94, 45 |

## Neutros

| Rol | HEX | Uso |
|-----|-----|-----|
| Superficie base | `#E8ECF4` | Fondo de piezas, cards neumórficas. |
| Neutro claro | `#D9DEEB` | Fondos alternos, separadores suaves. |
| Blanco | `#FFFFFF` | Negativos, contraste. |
| Naranja claro | `#FFBBA1` | **Texto naranja sobre fondo navy** (contraste AA). |

## Reglas de uso
- **Proporción 60/30/10:** ~60% navy/neutro, ~30% azul, ~10% naranja (acento).
- El **naranja es acento**, no color de fondo dominante ni de bloques de texto largos.
- **Naranja sobre navy:** usar `#FFBBA1` (naranja claro) para cumplir contraste AA; nunca `#DF5E2D`
  puro como texto sobre navy.
- Navy + naranja son complementarios (armónicos); respetar la proporción evita saturación.

## Color en producto digital (UI / ActuaFast)
Sistema semántico para interfaces (no reemplaza la paleta de marca; convive en pantallas):

| Rol | 500 | 100 (soft) | texto |
|-----|-----|-----------|-------|
| Éxito | `#00C781` | `#66DDB3` | `#00B374` |
| Aviso | `#FFBB38` | `#FFD688` | `#E6A832` |
| Error | `#FF4040` | `#FF8C8C` | `#CC3333` |
| Info / Primario | `#3C76F1` | `#ECF1FE` | `#366AD9` |

> Ratios de contraste verificados WCAG 2.1 contra la superficie `#E8ECF4`.

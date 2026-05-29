# Texture assets

Texturas y patrones del sistema visual.

## Archivos

| Archivo | Uso | Dimensiones | Notas |
|---|---|---|---|
| `paper-grain.svg` | Textura de papel sobre toda la página | 220 × 220 | Tile que se repite. `mix-blend-mode: multiply` aplicado |
| `topographic.svg` | Líneas topográficas en sección Laboratorio | 720 × 340 | Curvas tipo elevación |
| `pattern-band.svg` | Franja arquitectónica (6 tiles) entre secciones | 720 × 140 | Se repite horizontalmente |

## Reemplazar paper-grain por papel real

Para usar una textura fotográfica de papel:

1. Coloca `paper-grain.jpg` o `paper-grain.png` en esta carpeta
2. En `index_atlas.html`, busca esta línea en el `<style>`:
   ```
   body::before{...background-image:url("assets/textures/paper-grain.svg")...}
   ```
3. Cambia `.svg` por `.jpg` o `.png`
4. Opcionalmente ajusta `opacity` (.42 por defecto) y `mix-blend-mode`

Recomendado: PNG 800 × 800 con transparencia, o JPG 800 × 800 si solo
quieres aplicar como background.

## Reemplazar pattern-band

El patrón actual tiene 6 tiles geométricos en tu paleta (arco, escaleras,
columnas, puerta, luna, doble-arco). Si tienes una versión real de tu
patrón arquitectónico (como la imagen del moodboard):

1. Exporta en proporción 720 × 140 (o múltiplo) para tile horizontal
2. Guarda como `pattern-band.svg` o `pattern-band.png`
3. Si cambias extensión, ajusta en el CSS:
   ```
   .pattern-band{...background-image:url("assets/textures/pattern-band.png")...}
   ```

## Reemplazar topographic

Si quieres usar líneas topográficas reales (de un mapa GIS, contornos
exportados de QGIS):

1. Reemplaza `topographic.svg` manteniendo proporción 720 × 340
2. Usa stroke fino (0.4-0.6 px) en color oscuro
3. Mantén opacity baja para que no compita con el texto

## Sobre los SVG actuales

Los archivos actuales son placeholders generados procedural-mente
que mimic el look del brief. Funcionan perfectamente pero puedes
sustituir cualquiera por tu versión real cuando la tengas.

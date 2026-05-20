# Assets · CHUCHE Arquitectura Atlas

Estructura de assets del portafolio web. Cualquier archivo en estas
carpetas puede reemplazarse por la versión real sin tocar el HTML.

## Estructura

```
assets/
├── brand/        Logos e iconos de marca
├── textures/     Texturas y patrones del sistema visual
└── img/          Imágenes de proyectos (12 piezas del folio + cover)
```

## Cómo reemplazar cualquier asset

1. Mantén el mismo nombre de archivo (ej. `logo.svg`)
2. Mismas proporciones recomendadas (ver README de cada carpeta)
3. Refresca el navegador

El HTML solo apunta a las rutas de archivo. No hay nada inline que
modificar a menos que cambies el nombre del archivo.

## Formato preferido

- **SVG** para logos, iconos y texturas vectoriales (limpio, escalable, editable)
- **PNG con transparencia** para texturas con grano real / fotos de papel
- **JPG** para fotografías de proyectos (compresión 80-85%)

## Si reemplazas con archivos de otro formato

Si por ejemplo quieres usar `logo.png` en lugar de `logo.svg`, busca
la línea correspondiente en `index_atlas.html` y cambia la extensión.
Son referencias simples a `src="assets/brand/logo.svg"`.

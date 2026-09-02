# Memoria y Reglas del Proyecto

## 1. Reglas Estrictas de Tipografía (INMUTABLES)

En este proyecto está **terminantemente prohibido cambiar las familias tipográficas** o alterar sus pesos fuera de las especificaciones definidas por el usuario:

1. **Urbanist (Tipografía Principal)**:
   - **Uso exclusivo**: Títulos, subtítulos, textos generales, párrafos, valores numéricos, tarjetas, etiquetas de canvas y descripciones.
   - **Pesos admitidos**: 400, 500, 600, 700, 800, 900.
   - **Variables CSS asociadas**: `--font-display`, `--font-body`, `--font-main`.

2. **Syne (Tipografía de Énfasis y Botones)**:
   - **Uso exclusivo**: Botones interactivos (ej. `.mode-btn`, `.main-cta-button`), elementos de énfasis y llamados a la acción destacados.
   - **RESTRICCIÓN DE PESO ESTRICTA**: Syne **SOLO se puede usar con un peso MÁXIMO de 600** (`font-weight: 600` o inferior, ej. 500 o 600).
   - **Prohibición**: NUNCA usar pesos 700, 800, 900, `bold`, `bolder` ni `extra-bold` con la tipografía Syne.
   - **Variables CSS asociadas**: `--font-emphasis`, `--font-button`.

3. **Prohibición de sustitución de fuentes**:
   - No cambiar estas tipografías por Plus Jakarta Sans, Inter, Roboto, Montserrat ni ninguna otra fuente genérica bajo ninguna circunstancia.

## 2. Arquitectura de Archivos del Componente

- `embudo-interactivo.html`: Versión widget autocontenida para incrustar en WordPress / Elementor.
- `ayo-embudo.html`: Copia sincronizada del widget.
- `index.html`: Versión completa / standalone para visualización y pruebas locales.

Cualquier cambio de diseño o lógica debe mantenerse sincronizado entre estos archivos respetando siempre las reglas tipográficas.

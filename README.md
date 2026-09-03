# Embudo interactivo

Simulador visual de conversión que compara la capacidad operativa de un equipo humano con la de un agente de IA. Los leads se representan como partículas dentro de un embudo físico y las métricas se actualizan durante la simulación.

## Funcionalidades

- Cambio entre los escenarios **Equipo Humano** y **Agente IA**.
- Simulación física 2D de los leads mediante Matter.js.
- Métricas y etapas del embudo actualizadas en tiempo real.
- Diseño responsive para escritorio y móvil.
- Integración preparada para WordPress y Elementor.
- CTA final enlazable desde la configuración del documento.

## Ejecutar localmente

No se necesita instalación ni proceso de compilación. Abre [`index.html`](index.html) directamente en el navegador o sirve la carpeta con cualquier servidor HTTP estático:

```bash
python3 -m http.server 8000
```

Después visita <http://localhost:8000>.

La versión standalone carga Matter.js desde CDN, por lo que la previsualización necesita conexión a Internet.

## Archivos principales

| Archivo | Uso |
| --- | --- |
| [`index.html`](index.html) | Versión standalone para pruebas y visualización local. |
| [`embudo-interactivo.html`](embudo-interactivo.html) | Widget autocontenido para WordPress / Elementor. |
| [`ayo-embudo.html`](ayo-embudo.html) | Copia sincronizada del widget. |
| [`ai_lead_conversion_comparison.png`](ai_lead_conversion_comparison.png) | Recurso visual de referencia del proyecto. |

## Integración con WordPress / Elementor

1. Inserta el contenido de `embudo-interactivo.html` en un widget HTML de Elementor o en el método de código personalizado que utilice el sitio.
2. Comprueba que el sitio permita cargar recursos externos desde `cdnjs.cloudflare.com` y `fonts.googleapis.com`.
3. Publica y prueba ambos escenarios en escritorio y móvil.

El widget detecta el ciclo de renderizado de Elementor y evita inicializarse dos veces. Si el sitio bloquea scripts externos, carga Matter.js globalmente desde WordPress antes de insertar el widget.

## Dependencias externas

- [Matter.js 0.19.0](https://cdnjs.cloudflare.com/ajax/libs/matter-js/0.19.0/matter.min.js) para la simulación física.
- [Google Fonts](https://fonts.google.com/) para Urbanist y Syne.

## Convenciones de diseño

- **Urbanist** es la fuente principal para títulos, textos, métricas y etiquetas.
- **Syne** se reserva para botones y elementos de énfasis, con pesos de 500 o 600 como máximo.
- Los cambios de diseño o lógica deben mantenerse sincronizados entre `embudo-interactivo.html`, `ayo-embudo.html` e `index.html` cuando afecten a las tres variantes.

## Desarrollo

El proyecto es HTML, CSS y JavaScript autocontenido. No requiere Node.js, npm ni un paso de build. Para validar cambios, prueba la carga inicial, el cambio de escenario, la interacción del CTA y el comportamiento responsive en los tres archivos cuando corresponda.
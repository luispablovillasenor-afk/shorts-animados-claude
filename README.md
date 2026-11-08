# Shorts animados 3D con Claude

## Empieza aquí: elige tu estilo

**Un solo paquete, dos formas de crear videos:**

1. **Realista con Blender:** animaciones con modelos y materiales 3D, como una explicación visual de anatomía. [Mira el ejemplo](ejemplos/animacion-realista.png).
2. **Caricatura animada:** personajes de caricatura en un mundo 3D de colores, como el video de Alejandro. [Mira el ejemplo](ejemplos/animacion-caricatura.jpg).

No necesitas descargar carpetas por separado. En Claude Code, después de descargar y abrir esta carpeta, pega:

> Lee el archivo SKILL.md de esta carpeta. Soy principiante: muéstrame los dos ejemplos y explícame las dos opciones con palabras sencillas. Ayúdame a escoger y después guíame paso a paso, una pregunta a la vez.

La skill ayuda a preparar el guion, la voz, las escenas y el render, pero requiere herramientas y recursos que dependen del estilo, además de revisar y ajustar los avances. Descargarla no genera un video por sí solo. Algunas opciones de voz pueden tener costo.

La skill gratuita del video **«Cómo hacer shorts animados virales con Claude»** de Crea con LuisPa. En español.

Hace shorts verticales de historia en el estilo «personajes 2D en un mundo 3D de colores»: personajes planos con
contorno, mundo 3D pintado con líneas de tinta, fondo desenfocado, cámara que se desliza y nunca se queda quieta,
voz narrando y efectos de sonido. Todo se hace con código (three.js dentro de Remotion) en tu propia computadora,
sin generadores de video con IA.

Probada en **Alejandro Magno en Gaugamela** (47 mil contra 100 mil, con 100,000 soldados dibujados uno por uno) y en
**El puente que se cayó por una canción**.

**Nuevo (noviembre 2026): shorts 3D realistas en Blender**, del video «Cómo hacer shorts 3D ultra realistas con Claude»:
puntadas en el brazo y en la pierna, con piel, herida, hilo y vello que se ven reales. Todo en `realista/`.

## Qué trae
| Carpeta | Qué es |
|---|---|
| `SKILL.md` | La skill: el proceso completo, cada regla, cada arreglo y los valores finales del look |
| `plantillas/alejandro/` | El código completo del short de Alejandro: mundo de batalla, multitudes, cámara lenta, brasas, guion y mezcla de ejemplo |
| `plantillas/puente/` | El código completo del short del puente (de Mr omi): pueblo, personajes, tinta, desenfoque, color |
| `plantillas/audio/` | Sonido sintetizado: efectos, música, mezcla con la voz y volumen final |
| `plantillas/scripts/` | Fotos sueltas, hojas lado a lado, unir el trabajo de los agentes y revisión cuadro por cuadro |
| `realista/` | Shorts 3D realistas en Blender: guía (`REALISTA.md`), dos escenas completas (brazo y pierna con puntadas), medición de cámara y recursos con su licencia |
| `herramientas/medir_30fps.py` | Mide cualquier short a 30 cuadros por segundo: hojas, cortes, movimiento de cámara, color |
| `referencias/BIBLIA_DE_ESTILO.md` | La fórmula del guion y de la imagen medida en 20 shorts de referencia |
| `referencias/reportes_en/` | Siete reportes con medidas: movimiento, profundidad, texturas, personajes, luz, contornos, color (en inglés) |
| `referencias/hojas/` y `referencias/cuadros/` | 20 hojas de 60 cuadros (1,200 cuadros) y 38 cuadros completos para comparar |

## Cómo instalarla
1. Copia esta carpeta a `~/.claude/skills/shorts-animados-3d/` (clónala ahí o baja el ZIP).
2. Necesitas [Remotion](https://www.remotion.dev/) con `@remotion/three`, Node, Python 3 y ffmpeg
   (las versiones probadas están en `plantillas/alejandro/package_ejemplo.json`).
   Para lo realista: Blender 5.x y los recursos de `realista/recursos/FUENTES.md`.
3. En Claude Code dile: *«Usa la skill de shorts animados y hazme un short de…»*.

Claude sigue `SKILL.md`: tema y datos, guion, voz, plan de tomas en `story.ts`, fotos de prueba, medición y render.

## Notas
- Pon `TEMP`/`TMP` en un disco grande: cada render de Remotion copia la carpeta `public/` a la carpeta temporal.
- La historia, los personajes y la voz siempre deben ser tuyos. Las referencias son para el look, no para el contenido.
- La mezcla de Alejandro usa efectos de una biblioteca con licencia que no vienen aquí: usa los tuyos o la
  opción sintetizada de `plantillas/audio/`.

## Créditos y licencia
Basada en [claude-animated-shorts](https://github.com/mromidev/claude-animated-shorts) de Mr omi.
El código y los documentos son MIT (ver `LICENSE`). Los cuadros de referencia vienen solo para estudiar el estilo.

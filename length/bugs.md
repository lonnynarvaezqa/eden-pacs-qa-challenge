# Bug Report – Superposición de elementos creados desde el menú circular

**Área:** MPR Viewer  
**Componente:** Menú circular (Length / Annotations)  
**Tipo:** Comportamiento / UX  
**Severidad:** Media  
**Prioridad:** Media  

---

## Descripción

Al utilizar el menú circular para crear múltiples mediciones y anotaciones de forma consecutiva, el sistema permite que los elementos generados se superpongan con información contextual fija del visor (por ejemplo, datos de zoom, posición o valores mostrados en pantalla).

Aunque las anotaciones pueden moverse manualmente, el comportamiento inicial del menú circular no considera colisiones visuales con estos overlays, lo que puede provocar que información relevante quede oculta de forma temporal hasta que el usuario interviene.

---

## Pasos para reproducir

1. Abrir un estudio en el visor MPR.
2. Utilizar el menú circular para crear varias mediciones Length (medición básica, Bidirectional, Curve measurement o Deviation).
3. Agregar anotaciones adicionales desde el mismo menú.
4. Observar la esquina inferior izquierda del visor u otras áreas donde se muestra información contextual fija.

---

## Resultado observado

- Las etiquetas y líneas de medición pueden superponerse entre sí.
- Parte de la información contextual del visor queda cubierta.
- El usuario debe mover manualmente las anotaciones para recuperar visibilidad.

---

## Resultado esperado

- El menú circular debería prevenir o minimizar la superposición inicial de elementos con información contextual fija.
- La información contextual del visor debería mantenerse visible sin requerir acciones inmediatas por parte del usuario.

---

## Impacto para el usuario

- Dificulta la lectura simultánea de la imagen clínica y sus datos asociados.
- Incrementa la carga cognitiva durante flujos de trabajo continuos.
- Puede generar confusión en estudios con múltiples mediciones.

---

## Evidencia

Se incluye evidencia visual del comportamiento observado en la carpeta `/assets`.

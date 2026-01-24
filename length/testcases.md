# Casos de prueba funcionales – Herramienta Length

Los siguientes casos de prueba se diseñaron considerando el uso real de la herramienta por parte de personal clínico, priorizando la claridad de la interacción, la prevención de errores y la coherencia espacial dentro del visor MPR.

No se busca cubrir exhaustivamente todas las combinaciones posibles, sino validar los flujos más representativos y críticos para el usuario final.

---

## Prioridad Alta

### TC-LEN-01 – Creación de medición Length básica (lineal)

**Objetivo**  
Validar que la medición lineal por defecto sea clara y predecible para el usuario.

**Pasos**
1. Abrir un estudio en el visor MPR.
2. Seleccionar Length (sin elegir sub-opción).
3. Colocar los puntos inicial y final.

**Resultado esperado**
- Se crea una medición lineal simple.
- El valor se muestra de forma legible.
- El comportamiento es consistente con la expectativa básica del usuario.

---

### TC-LEN-02 – Creación de medición Length (Bidirectional)

**Objetivo**  
Validar que el usuario pueda medir distancias bidireccionales de forma clara y predecible.

**Pasos**
1. Abrir un estudio en el visor MPR.
2. Identificar visualmente el plano activo.
3. Click derecho → Length → Bidirectional.
4. Colocar los puntos requeridos para completar la medición.

**Resultado esperado**
- La medición se crea únicamente en el plano activo.
- El valor bidireccional se muestra de forma clara y legible.
- No se generan mediciones en otros planos.

---

### TC-LEN-03 – Creación de medición Length (Curve measurement)

**Objetivo**  
Verificar que el usuario pueda realizar una medición curva sin perder referencia espacial.

**Pasos**
1. Seleccionar Length → Curve measurement.
2. Colocar múltiples puntos siguiendo una estructura anatómica curva.

**Resultado esperado**
- La medición sigue la trayectoria definida por el usuario.
- El trazo se mantiene estable y coherente.
- El resultado numérico refleja la suma de la trayectoria.

---

### TC-LEN-04 – Creación de medición Length (Deviation)

**Objetivo**  
Validar la medición de desviaciones de forma comprensible para el usuario.

**Pasos**
1. Seleccionar Length → Deviation.
2. Definir los puntos necesarios para la medición.

**Resultado esperado**
- La desviación se representa visualmente de forma clara.
- El usuario puede identificar fácilmente el sentido y magnitud de la desviación.

---

### TC-LEN-05 – Claridad del plano activo durante cualquier tipo de medición Length

**Objetivo**  
Asegurar que el usuario tenga claridad sobre dónde se está aplicando la herramienta.

**Pasos**
1. Iniciar una medición Length (cualquiera de sus sub-opciones).
2. Cambiar visualmente el foco a otro plano antes de finalizar.

**Resultado esperado**
- El sistema indica claramente si la medición sigue asociada al plano original.
- No se permite continuar la medición en un plano distinto sin confirmación explícita.

---

### TC-LEN-06 – Persistencia de mediciones Length al navegar entre slices

**Objetivo**  
Verificar la coherencia de las mediciones al desplazarse por el estudio.

**Pasos**
1. Crear una medición usando cualquiera de las sub-opciones de Length.
2. Navegar entre distintos slices.

**Resultado esperado**
- Las mediciones solo son visibles cuando corresponde espacialmente.
- No se desalinean ni se distorsionan los puntos.

---

## Prioridad Media

### TC-LEN-07 – Cancelación de una medición incompleta (todas las sub-opciones)

**Objetivo**  
Evaluar cómo el sistema maneja interrupciones comunes del usuario.

**Pasos**
1. Iniciar una medición Bidirectional, Curve o Deviation.
2. Abandonar la acción antes de completarla.

**Resultado esperado**
- No quedan elementos incompletos visibles.
- El usuario puede reiniciar la acción sin confusión.

---

### TC-LEN-08 – Uso consecutivo de distintas sub-opciones de Length

**Objetivo**  
Validar que el cambio entre sub-opciones sea claro para el usuario.

**Pasos**
1. Crear una medición Bidirectional.
2. Seleccionar inmediatamente Curve measurement.

**Resultado esperado**
- El sistema cambia correctamente el modo de medición.
- No se mezclan comportamientos entre sub-opciones.

---

## Prioridad Baja

### TC-LEN-09 – Legibilidad visual de mediciones complejas

**Objetivo**  
Validar que múltiples tipos de medición no saturen visualmente la imagen.

**Resultado esperado**
- Las mediciones siguen siendo legibles.
- La imagen clínica no se ve comprometida.

# Eden PACS – QA Challenge

![Eden PACS – QA Challenge](assets/eden-pacs-qa-challenge.png)

## Propósito

Este repositorio contiene la resolución del **QA Challenge de Eden Medical**, enfocado en evaluar una funcionalidad clínica crítica dentro del **visor MPR de Eden PACS**.

El objetivo no es únicamente validar el correcto funcionamiento de la herramienta, sino analizarla desde una perspectiva de **calidad, seguridad clínica y claridad para el usuario**, considerando el contexto real en el que es utilizada.

---

## Enfoque de Calidad

En un entorno de diagnóstico médico, la calidad del software tiene implicaciones directas en la toma de decisiones clínicas. Por ello, este challenge se aborda considerando que:

* Los errores pueden impactar la interpretación de un estudio
* La ambigüedad en la interfaz incrementa el riesgo de uso incorrecto
* La claridad del estado de las herramientas es clave bajo presión operativa

El rol de QA, en este contexto, es reducir riesgos y asegurar que el sistema sea confiable y predecible para el usuario final.

---

## Alcance del Challenge

### Herramienta seleccionada del menú circular

**Length**, incluyendo sus sub-opciones:

* Deviation
* Bidirectional
* Curve measurement

Esta herramienta se eligió por su relevancia clínica, su complejidad geométrica y su alta sensibilidad a errores de interacción. Las acciones de **Delete** y **Restore** se consideran como parte natural del flujo de corrección de errores del usuario, sin ampliar el alcance más allá de la opción seleccionada.

---

## Contexto de Pruebas

* **Aplicación:** Eden PACS – Visor MPR
* **Funcionalidad:** Multiplanar Reconstruction (MPR)
* **Planos evaluados:** Axial, Coronal, Sagital

Aspectos clave considerados:

* Coherencia espacial entre planos
* Identificación clara del plano activo
* Estados explícitos de las herramientas
* Capacidad de recuperación ante errores del usuario

---

## Estructura del Repositorio

```
eden-pacs-qa-challenge/
│
├── README.md
│
├── length/
│   ├── overview.md          # Descripción funcional y clínica de Length
│   ├── test-cases.md        # Casos de prueba funcionales priorizados
│   ├── bugs.md              # Reporte de bug(s)
│   └── feedback.md          # Observaciones y oportunidades de mejora
│
├── jira/
│   ├── test-cases.csv       # Casos de prueba en formato Jira/XRay
│   └── bug-report.md        # Bug documentado como issue de Jira
│
└── bonus/
    ├── edge-cases.md        # Escenarios límite y de mayor riesgo
    └── automation-strategy.md # Estrategia de automatización
```

---

## Enfoque de Diseño de Pruebas

Los casos de prueba se priorizan considerando:

1. Impacto potencial en la interpretación clínica
2. Frecuencia de uso de la funcionalidad
3. Riesgo asociado a errores humanos
4. Claridad de la interacción bajo carga cognitiva

Prioridades:

* **Alta:** Riesgo funcional o clínico
* **Media:** Claridad de uso y prevención de errores
* **Baja:** Comportamientos visuales o cosméticos

---

## Consideración de Error Humano

Se asume que los usuarios pueden cometer errores durante la interacción con la herramienta. Por ello, se pone especial atención en escenarios como:

* Mediciones incompletas o accidentales
* Cambio de plano o slice durante una medición
* Activación simultánea de herramientas
* Eliminación involuntaria de mediciones

El sistema debe facilitar la detección y corrección de estos errores sin comprometer el flujo de trabajo.

---

## Perspectiva de Automatización

La automatización se considera como un complemento al análisis manual.

* **Apta para automatizar:**

  * Activación y desactivación de herramientas
  * Persistencia de estados
  * Comportamiento del menú circular

* **No prioritaria para automatizar:**

  * Validaciones visuales finas
  * Precisión clínica de mediciones

El detalle se documenta en `bonus/automation-strategy.md`.

---

## Nota Final

Este challenge se aborda como un ejercicio de QA aplicado a un entorno real de diagnóstico médico. El objetivo es evaluar la herramienta desde un punto de vista funcional, de usabilidad y de reducción de riesgos, manteniendo siempre el foco en la confiabilidad del sistema.

---

**Candidato:** Lonny Narváez
**Rol:** QA Engineer

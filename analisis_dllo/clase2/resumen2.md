# Ingeniería de Requerimientos de Software: Resumen Ejecutivo

---

## 1. Conceptos Fundamentales

> **Definición Formal (IEEE 830):** Un requerimiento es una propiedad documentada que un sistema debe poseer para resolver un problema o lograr un objetivo. Es una declaración verificable de una funcionalidad, restricción o característica de calidad.

Para que una necesidad sea considerada un requerimiento profesional, debe cumplir de manera estricta con dos condiciones: ser **documentada** (escrita) y **verificable** (medible/comprobable).

### Niveles de Abstracción
El proceso de ingeniería consiste en traducir el lenguaje informal del usuario a especificaciones técnicas:
1. **Necesidad del Usuario:** Expresión informal y emocional (*"Quiero saber qué hay de comida para no perder la ida"*).
2. **Requerimiento del Sistema:** Traducción formal y estructurada (*"El sistema debe mostrar el menú del día actualizado a los usuarios"*).
3. **Especificación Técnica:** Detalle de bajo nivel para desarrollo (*"La API /menu/dia debe retornar un JSON en menos de 300 ms usando HTTPS"*).

### Fuentes de Requerimientos (Stakeholders)
* **Usuarios finales:** Conocen el día a día operativo.
* **Clientes / Patrocinadores:** Definen los objetivos de negocio y financian el proyecto.
* **Leyes y Normas:** Regulaciones de obligatorio cumplimiento (ej. protección de datos).
* **Sistemas Externos:** Plataformas de terceros con las que se debe integrar (ej. pasarelas de pago).

### Cualidades de un Buen Requerimiento
* **Necesario:** Esencial para el propósito del sistema.
* **No ambiguo:** Tiene una única interpretación posible.
* **Verificable:** Se puede diseñar una prueba para comprobar si se cumple.
* **Consistente:** No entra en conflicto con ningún otro requerimiento.
* **Completo:** Contiene toda la información y contexto necesario.
* **Atómico:** Contiene una sola idea/función. Evita mezclar conceptos.
* **Trazable:** Se puede rastrear su origen y su impacto en el sistema.

---

## 2. Requerimientos Funcionales (RF) vs. No Funcionales (RNF)

| Criterio | Requerimientos Funcionales (RF) | Requerimientos No Funcionales (RNF) |
| :--- | :--- | :--- |
| **Definición** | Describen **QUÉ** acciones concretas realiza el sistema. | Describen **CÓMO** se comporta el sistema bajo restricciones de calidad. |
| **Enfoque** | Tareas, cálculos, flujos de datos e interacciones. | Rendimiento, seguridad, disponibilidad y experiencia. |
| **Estructura Estándar**| *"El sistema deberá + [acción] + [objeto] + [condición]"* | Debe incluir una **métrica** y un **umbral** medible. |

### Categorías de Requerimientos Funcionales
* **Autenticación:** Gestión de accesos, roles y contraseñas.
* **Cálculo:** Operaciones matemáticas, estadísticas y algoritmos.
* **Persistencia (CRUD):** Almacenamiento, modificación y eliminación de datos.
* **Comunicación:** Notificaciones por correo, SMS, o APIs externas.
* **Reporte:** Generación e impresión de archivos (PDF, Excel, etc.).
* **Validación:** Control de formatos, reglas de negocio y restricciones de campos.

### Categorías de Requerimientos No Funcionales
* **Rendimiento:** Tiempos de respuesta y velocidad de carga.
* **Seguridad:** Cifrado de datos, políticas de intentos de login y protección de identidad.
* **Usabilidad:** Facilidad de uso, curvas de aprendizaje y accesibilidad.
* **Confiabilidad:** Porcentaje de disponibilidad (Uptime) y tolerancia a fallos.
* **Escalabilidad:** Capacidad para soportar usuarios concurrentes sin degradarse.
* **Mantenibilidad:** Cobertura de pruebas unitarias y modularidad del código.
* **Portabilidad:** Compatibilidad con diferentes navegadores y sistemas operativos.

---

## 3. Atributos de Calidad (Norma ISO/IEC 25010)

Los atributos de calidad son los conceptos abstractos y teóricos. Los **RNF** son la materialización medible de estos atributos en un proyecto específico.

1. **Adecuación Funcional:** Idoneidad, completitud y corrección del software.
2. **Eficiencia de Desempeño:** Comportamiento temporal y uso optimizado de recursos.
3. **Compatibilidad:** Capacidad de coexistir e interactuar (interoperabilidad).
4. **Usabilidad:** Estética, facilidad de aprendizaje, accesibilidad y operabilidad.
5. **Confiabilidad:** Madurez, disponibilidad, resiliencia y recuperación ante errores.
6. **Seguridad:** Confidencialidad, integridad, no repudio y autenticidad.
7. **Mantenibilidad:** Modularidad, reusabilidad, facilidad de prueba y modificación.
8. **Portabilidad:** Facilidad de instalación, adaptación y reemplazo en nuevos entornos.

---

## 4. Historias de Usuario (Enfoque Ágil)

Representan una alternativa conversacional a los requerimientos tradicionales, enfocada en el **valor real** que recibe el usuario.

### Estructura Estándar
```text
Como [Tipo de Usuario],
Quiero [Acción / Funcionalidad],
Para [Beneficio / Objetivo].
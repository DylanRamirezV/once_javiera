# Fundamentos Esenciales de la Ingeniería de Software

## 1. El Rol Crítico de la Planificación: Análisis y Diseño
La construcción exitosa de software depende de una planeación estratégica previa. Escribir código sin una comprensión profunda del problema conduce al caos operativo, retrasos en las entregas y productos deficientes.

* **Fase de Análisis:** Determina el **QUÉ**. Define la problemática, el público objetivo, las necesidades reales y los límites operativos.
* **Fase de Diseño:** Determina el **CÓMO**. Establece la estructura técnica, la arquitectura del sistema, el stack tecnológico y la interfaz de usuario.
* **Programación:** Representa únicamente la etapa final de manufactura del proceso.

> **Indicador de Alerta:** De acuerdo con estudios del Standish Group, el **66%** de los proyectos de software fracasan o sufren desviaciones críticas. La raíz del problema no está en la codificación, sino en la **especificación imprecisa de requerimientos**.

### La Curva del Costo del Error (Regla 1-10-100)
Este principio demuestra que el impacto financiero para mitigar un fallo crece de forma exponencial según la etapa en la que se descubra:

* **Identificación en Análisis:** Gasto mínimo (1)
* **Identificación en Diseño:** Costo moderado (10)
* **Identificación en Programación:** Costo elevado (100)
* **Identificación en Producción (En vivo):** Impacto crítico (1000+)

---

## 2. Las Etapas del Ciclo de Vida del Software
Representa el mapa de ruta que recorre una aplicación desde su idea inicial hasta su retiro definitivo. En los entornos actuales, estas fases se ejecutan de manera **cíclica e iterativa**:

1. **Levantamiento de Requerimientos:** Sesiones de trabajo con los usuarios para documentar las necesidades del negocio. *Entregable: Especificación Técnica de Requisitos.*
2. **Modelado de la Solución:** Estructuración de componentes, bases de datos, diagramas y pantallas conceptuales. *Entregable: Planos arquitectónicos y prototipos.*
3. **Construcción (Codificación):** Traducción de los diseños a código fuente funcional. *Entregable: Módulos de software listos para evaluación.*
4. **Aseguramiento de Calidad (QA):** Ejecución de pruebas para detectar vulnerabilidades, fallos y validar el cumplimiento del plan original. *Entregable: Matriz de errores corregidos.*
5. **Despliegue (Puesta en Marcha):** Instalación y liberación de la plataforma en el entorno operativo real. *Entregable: Sistema activo para el usuario final.*
6. **Soporte y Evolución:** Corrección de incidencias en vivo e implementación de nuevas características. *Entregable: Actualizaciones y versiones mejoradas.*

---

## 3. Marcos de Trabajo y Metodologías

### A. Modelos Tradicionales (Estructurados)
Se caracterizan por una planificación exhaustiva e inamovible desde el primer día. Son idóneos para entornos con necesidades estables y regulaciones estrictas.

* **Esquema en Cascada (Waterfall):** Flujo estrictamente lineal. Cada etapa debe concluirse por completo para dar paso a la siguiente, impidiendo retroceder en el proceso.
* **Esquema en V:** Extensión del modelo en cascada que asocia directamente cada etapa de desarrollo con una fase de validación específica (por ejemplo, emparejar el Diseño de Componentes con las Pruebas Unitarias).
* **Esquema en Espiral:** Enfoque evolutivo y cíclico enfocado prioritariamente en la evaluación, control y mitigación de riesgos en cada vuelta del ciclo.

### B. Enfoques Flexibles (Ágiles)
Inspirados en el *Manifiesto Ágil*, priorizan la entrega continua de valor, la interacción humana y la adaptabilidad inmediata sobre la burocracia documental. Estructuran el trabajo en **bloques de tiempo cortos** (de 1 a 4 semanas).

* **Scrum:** Marco de gestión basado en ciclos cerrados (*Sprints*), revisiones periódicas y responsabilidades claras distribuidas en tres roles primarios: *Dueño de Producto (Product Owner)*, *Facilitador (Scrum Master)* y el *Equipo Técnico*.
* **Kanban:** Gestión visual del flujo de tareas mediante un tablero dividido en estados operativos (Pendiente, En Proceso, En Validación, Terminado). Su regla fundamental es restringir el Trabajo en Progreso (WIP) para evitar cuellos de botella.
* **XP (Programación Extrema):** Práctica netamente técnica centrada en la excelencia del código. Promueve el desarrollo guiado por pruebas (TDD), la creación de código por parejas (*Pair Programming*) y la limpieza constante del software.

### Análisis Comparativo de Enfoques


| Dimensión de Análisis | Modelos Tradicionales 📏 | Marcos Ágiles ⚡ |
| :--- | :--- | :--- |
| **Planificación** | Integral y estática al inicio | Progresiva, adaptada a cada ciclo |
| **Gestión del Cambio** | Rígida, costosa y desalentada | Flexible, integrada de forma natural |
| **Entregables Documentales** | Exhaustivos, formales y densos | Compactos, enfocados en lo útil |
| **Interacción con el Cliente** | Exclusiva al inicio y al cierre | Colaboración activa y constante |
| **Estructura del Equipo** | Grupos grandes y especializados | Células pequeñas y multidisciplinarias |
| **Nivel de Riesgo** | Alto (los fallos se ven al final) | Mitigado (se valida a corto plazo) |
| **Ámbito de Aplicación** | Sistemas críticos y entornos regulados | Proyectos innovadores, apps y startups |

---

## 4. Ingeniería de Requisitos
Un requerimiento representa una funcionalidad obligatoria o una condición limitante que el sistema debe cumplir satisfactoriamente.

### Clasificación Fundamental
* **Requisitos Funcionales (El QUÉ):** Acciones, servicios y comportamientos explícitos del sistema. *Ejemplo: "El portal debe procesar pagos con tarjeta de crédito".*
* **Requisitos No Funcionales (El CÓMO):** Parámetros de calidad, rendimiento, seguridad y restricciones. *Ejemplo: "La base de datos debe encriptar la información en reposo".*

### Criterios de Calidad SMART
Para garantizar que un requerimiento sea viable y libre de ambigüedades, debe cumplir con las siguientes siglas:
* **S**pecific (Específico): Claro y bien definido.
* **M**easurable (Medible): Que se pueda cuantificar o comprobar objetivamente.
* **A**chievable (Alcanzable): Realista bajo las restricciones del proyecto.
* **R**elevant (Relevante): Que aporte valor real al negocio.
* **T**ime-bound (Acotado en el tiempo): Con un límite temporal de ejecución.

### Métodos de Elicitación (Descubrimiento)
Para extraer y comprender las necesidades del cliente se emplean diversas herramientas:
* Cuestionarios masivos y entrevistas estructuradas.
* Monitoreo y observación de la operación diaria del cliente.
* Mesas de trabajo dinámicas con los actores clave del proyecto (*stakeholders*).
* Auditoría de normativas vigentes, leyes y manuales internos.
* Construcción experimental de maquetas y prototipos rápidos.

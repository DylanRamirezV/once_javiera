# Directrices Estratégicas para la Ingeniería de Software
## Manual de Principios, Arquitectura y Ciclo de Vida del Desarrollo

---

# 1. Perspectiva Estratégica del Análisis y Diseño de Software

El éxito de cualquier solución tecnológica depende en gran medida de una etapa inicial sólida de planificación, análisis y diseño. Comenzar a programar sin una comprensión clara del problema y sin una arquitectura definida suele generar retrasos, sobrecostos y problemas estructurales difíciles de corregir posteriormente.

## Fase de Análisis (Definición de Requerimientos)

Esta etapa tiene como propósito comprender con precisión el problema que se desea resolver. Su enfoque principal es determinar **qué debe construir el sistema**, identificando necesidades de negocio, expectativas de los usuarios y limitaciones técnicas.

## Fase de Diseño (Arquitectura de la Solución)

Una vez definidos los requerimientos, se establece la estructura que permitirá materializar la solución. Aquí se define **cómo se construirá el sistema**, incluyendo tecnologías, patrones de diseño, modelos de datos, arquitectura de software y experiencia de usuario.

## Fase de Implementación (Desarrollo)

Consiste en convertir las especificaciones y diseños previamente definidos en código ejecutable. La programación representa la materialización técnica de las decisiones tomadas durante las fases anteriores.

> ⚠️ **Indicador de Riesgo en Proyectos de Software**
>
> Diversos estudios de consultoría tecnológica, entre ellos los realizados por Standish Group, muestran que aproximadamente el **66 % de los proyectos de software** presentan retrasos significativos, sobrecostos o incumplen los objetivos planteados inicialmente.
>
> La causa principal no suele ser la calidad de la programación, sino una definición inadecuada o incompleta de los requerimientos.

## Evolución del Costo de los Errores (Regla 1-10-100)

Corregir un error se vuelve progresivamente más costoso conforme avanza el proyecto. Un problema detectado durante la etapa de análisis tiene un impacto mínimo comparado con uno encontrado en producción.

| Etapa de Detección | Costo Relativo | Nivel de Riesgo |
|--------------------|---------------:|----------------|
| **Análisis** | $1 | Bajo |
| **Diseño** | $10 | Medio |
| **Desarrollo** | $100 | Alto |
| **Producción** | $1000+ | Crítico |

---

# 2. Ciclo de Vida del Desarrollo de Software (SDLC)

El **Software Development Life Cycle (SDLC)** es el conjunto de procesos que guían un sistema desde su concepción inicial hasta su retiro definitivo. En la actualidad, estas fases suelen ejecutarse de manera iterativa para favorecer la mejora continua.

## 1. Ingeniería de Requerimientos

Se recopilan, documentan y validan las necesidades del negocio y de los usuarios.

**Entregable:** Documento de Especificación de Requisitos de Software (SRS).

## 2. Diseño Arquitectónico

Se define la estructura técnica del sistema, incluyendo componentes, bases de datos, interfaces y comunicaciones.

**Entregable:** Diagramas arquitectónicos, modelos de datos y prototipos.

## 3. Desarrollo e Implementación

Se construyen los componentes de software siguiendo las especificaciones definidas durante el diseño.

**Entregable:** Código fuente y aplicaciones funcionales.

## 4. Aseguramiento de la Calidad (QA)

Se realizan pruebas para verificar el cumplimiento de requisitos, detectar defectos y evaluar aspectos de seguridad y rendimiento.

**Entregable:** Informes de pruebas y registros de incidencias.

## 5. Despliegue

El software es instalado y configurado en los entornos operativos donde será utilizado por los usuarios finales.

**Entregable:** Sistema disponible en producción.

## 6. Mantenimiento y Evolución

Incluye la corrección de errores, optimización del rendimiento y la incorporación de nuevas funcionalidades.

**Entregable:** Actualizaciones, mejoras y parches de mantenimiento.

---

# 3. Clasificación de las Metodologías de Desarrollo

Las metodologías de desarrollo establecen la forma en que se organizan y ejecutan las actividades de un proyecto de software.

## A. Metodologías Tradicionales o Predictivas

Se caracterizan por definir detalladamente el alcance y la planificación desde el inicio, manteniendo un control estricto sobre los cambios.

### Modelo Cascada (Waterfall)

Las actividades se ejecutan de forma secuencial. Cada fase debe finalizar completamente antes de comenzar la siguiente.

### Modelo en V

Amplía el modelo cascada incorporando actividades de validación y pruebas asociadas a cada etapa del desarrollo.

### Modelo Espiral

Combina iteración y análisis de riesgos, permitiendo refinar progresivamente la solución mientras se controlan incertidumbres técnicas y de negocio.

## B. Metodologías Ágiles y Adaptativas

Se basan en la capacidad de adaptación continua y en la entrega frecuente de valor mediante ciclos cortos de trabajo.

### Scrum

Marco de trabajo basado en equipos autoorganizados que trabajan en iteraciones llamadas *Sprints*. Define roles específicos y reuniones periódicas para garantizar la coordinación y el seguimiento.

### Kanban

Método orientado a la gestión visual del flujo de trabajo mediante tableros que permiten controlar y optimizar la carga operativa.

### Extreme Programming (XP)

Metodología enfocada en la excelencia técnica mediante prácticas como desarrollo guiado por pruebas (TDD), programación en parejas y refactorización continua.

## Comparación entre Enfoques Tradicionales y Ágiles

| Aspecto | Enfoques Tradicionales | Enfoques Ágiles |
|----------|----------------------|----------------|
| **Planificación** | Completa desde el inicio | Evolutiva e incremental |
| **Adaptación al cambio** | Limitada | Alta |
| **Documentación** | Extensa y formal | Ligera y enfocada al valor |
| **Participación del cliente** | Puntual | Continua |
| **Estructura del equipo** | Jerárquica y especializada | Colaborativa y multidisciplinaria |
| **Gestión de riesgos** | Tardía | Continua |
| **Aplicaciones típicas** | Sistemas regulados y críticos | Productos digitales y startups |

---

# 4. Ingeniería de Requerimientos

La ingeniería de requerimientos es la disciplina encargada de identificar, analizar, documentar y validar las necesidades que deberá satisfacer el sistema.

## Tipos de Requerimientos

### Requerimientos Funcionales

Describen las funciones y comportamientos que el sistema debe proporcionar.

**Ejemplo:**

> El sistema debe validar tokens JWT antes de permitir el acceso a los servicios protegidos.

### Requerimientos No Funcionales

Definen atributos de calidad y restricciones relacionadas con rendimiento, seguridad, disponibilidad y escalabilidad.

**Ejemplo:**

> El sistema debe responder en menos de 250 milisegundos bajo una carga de 10.000 solicitudes concurrentes.

---

## Validación de Requerimientos con el Modelo SMART

Para evitar ambigüedades y mejorar la calidad de las especificaciones, cada requerimiento debería cumplir con los siguientes criterios:

- **S (Specific):** Debe ser claro y específico.
- **M (Measurable):** Debe poder medirse objetivamente.
- **A (Achievable):** Debe ser técnicamente viable.
- **R (Relevant):** Debe aportar valor al negocio.
- **T (Time-bound):** Debe contar con plazos definidos.

---

## Técnicas de Elicitación de Requerimientos

La recopilación de información puede realizarse mediante diferentes estrategias:

- Entrevistas estructuradas con usuarios y responsables del negocio.
- Encuestas y cuestionarios especializados.
- Revisión de documentación existente y normativas aplicables.
- Talleres colaborativos con los interesados del proyecto.
- Observación directa de procesos operativos.
- Construcción de prototipos y wireframes para validar expectativas tempranamente.

Estas técnicas permiten comprender de manera integral las necesidades reales del negocio y reducir el riesgo de construir soluciones que no satisfagan las expectativas de los usuarios.
# Resumen Ejecutivo: El Arte de Elicitar y Analisis de Viabilidad

## 1. El Arte de Elicitar: Concepto y Mentalidad

### Definicion
Elicitar significa "sacar, extraer, hacer salir". En ingenieria de software, es el proceso activo de descubrir las necesidades reales de los clientes y usuarios para traducirlas en requerimientos formales.
* No es "recolectar": El cliente rara vez sabe con exactitud lo que necesita. El analista no es un transcriptor pasivo, es un detective.
* El dilema de la innovacion: "Si hubiera preguntado a la gente que queria, me habrian dicho: caballos mas rapidos." — Henry Ford. Los usuarios suelen describir soluciones basadas en lo que conocen, no el problema de raiz.

### Habilidades Blandas del Analista
* Escucha activa: Concentracion total en el emisor, sin preparar la respuesta de antemano.
* Curiosidad genuina: Preguntar el porquede las cosas de forma iterativa.
* Saber callar: Tolerar los silencios; a menudo preceden a las revelaciones mas importantes.
* Empatia: Comprender la posicion y frustraciones del cliente sin juzgar.
* No asumir: Evitar dar por sentado "lo obvio". Todo debe ser validado.

### El Problema del Iceberg
* La Punta (Lo que dice): "Quiero una app rapida y bonita."
* El Medio (Lo que piensa pero no dice): "Mi competencia directa tiene una y me estoy quedando atras."
* La Base (Lo que NO sabe que piensa): Rutinas automatizadas, miedos al cambio tecnologico, procesos culturales implicitos.

---

## 2. La Tecnica Reina: Entrevistas

Es una conversacion guiada con un proposito claro. No es un interrogatorio ni un checklist.

### Tipos de Entrevistas
* Estructurada: Lista cerrada de preguntas en orden fijo. Util para comparar respuestas de grupos grandes (Rigida).
* No estructurada: Conversacion libre sin guion. Ideal en etapas muy tempranas para explorar el panorama (Dificil de analizar).
* Semi-estructurada: Balance ideal. Cuenta con una guia de preguntas pero permite desviaciones si surge un dato de valor.

### Las 3 Etapas Criticas
* ANTES (Preparacion): Investigar al stakeholder, definir objetivos y estructurar de 5 a 10 preguntas guia.
* DURANTE (Ejecucion): Romper el hielo, usar preguntas abiertas, repreguntar sobre las pausas, documentar o grabar (con autorizacion).
* DESPUES (Consolidacion): Pasar notas a limpio en menos de 24 horas, extraer requerimientos y enviar correo de agradecimiento.

### Tipos de Preguntas
* Abiertas: Exploran contexto ("¿Como es un dia tipico en su trabajo?").
* Cerradas: Confirman datos especificos ("¿Cuantos empleados nocturnos hay?").
* De sondeo: Profundizan en respuestas previas ("¿Me podria dar un ejemplo de ese fallo?").

---

## 3. Encuestas: Elicitacion Masiva

Cuestionarios asincronicos disenados para recopilar informacion cuantitativa de grandes volumenes de personas.
* ¿Cuando usar?: Grupos masivos (cientos/miles), usuarios dispersos, busqueda de metricas/porcentajes o validacion anonima de hipotesis.
* ¿Cuando NO usar?: Temas complejos que requieran explicacion tecnica o cuando se busca profundidad y matices.

### Reglas de Oro en el Diseno
* Brevedad: Maximo 10-15 preguntas para evitar el abandono.
* Foco: Una sola idea por pregunta (Evitar: "¿Es rapido y facil?").
* Lenguaje neutro: Cero jerga tecnica (API, JWT, Database).
* Escala Likert: Herramienta estrella para medir actitudes de 1 a 5 (Muy en desacuerdo a Muy de acuerdo).

---

## 4. Observacion: Descubrir lo Invisible

Consiste en acudir al entorno real de trabajo para registrar la ejecucion de los procesos sin interrumpir el flujo. Revela los atajos, trucos y errores que el usuario omite en las entrevistas porque los considera "normales".

### Variantes de Observacion
* Directa (Pasiva): El analista actua como una "mosca en la pared" sin intervenir.
* Participante: El analista se integra al equipo y ejecuta las tareas operativas para vivir los dolores del usuario.
* Etnografica / Shadowing: Estudio prolongado y profundo del entorno o seguimiento estricto a un rol especifico.

Nota: Efecto Hawthorne. Fenomeno psicologico donde las personas modifican o mejoran su comportamiento habitual por el simple hecho de saber que estan siendo observadas. Para mitigar esto, se recomienda extender las jornadas de observacion hasta que la presencia del analista se vuelva cotidiana.

---

## 5. Caso Practico: "Biblioteca del Colegio" (Triangulacion de Tecnicas)

El exito del levantamiento radica en alternar y complementar las herramientas segun el volumen y criticidad de los actores:
* Entrevistas (3 Bibliotecarios): Revelan la saturacion de los cuadernos fisicos y el desconocimiento de la demanda de libros.
* Observacion (Hora Pico de Prestamos): Permite medir que cada registro manual tarda de 4 a 5 minutos y que el 30% de los estudiantes desiste por las largas filas.
* Encuestas (800 Estudiantes / 40 Profesores): Cuantifican la necesidad (82% exige acceso movil, 91% quiere catalogo online antes de asistir).

### Traduccion de Hallazgos a Requerimientos Formales
* De Encuesta: El 82% quiere pedir desde el celular -> RF: El sistema debera permitir a los estudiantes solicitar prestamos desde una aplicacion movil.
* De Observacion: El registro a mano toma 5 minutos -> RNF: El tiempo total de registro de un prestamo no debera superar los 60 segundos.

---

## 6. Analisis de Viabilidad del Requerimiento

Filtro profesional y etico donde el analista evalua si lo solicitado puede implementarse de manera realista en el mundo real.

### Las 5 Dimensiones de Viabilidad
* Tecnica: ¿Existe la tecnologia y el equipo cuenta con el conocimiento tecnico para desarrollarlo?
* Economica: ¿El presupuesto asignado cubre el costo de las herramientas, infraestructura y licencias?
* Operativa: ¿La solucion se adapta a la cultura organizacional y las capacidades del usuario final?
* Legal: ¿El requerimiento infringe normativas de derechos de autor, accesibilidad o leyes de proteccion de datos personales?
* Temporal: ¿El cronograma propuesto es realista para el nivel de complejidad del software?
# Roles de la IA en la conversación de trabajo
Luisa Rincón Marzo 8  2026

## Introducción

En documentos de este repositorio se propuso que la inteligencia artificial puede participar en el trabajo intelectual a través de distintos [**patrones de colaboración**](https://github.com/lufe089/gen-ai-reflexiones/blob/main/patrones_colaboracion_ia.md), por ejemplo como generadora de respuestas, asistente de estructuración, interlocutora reflexiva o co-constructora de procesos. Esa clasificación ayuda a entender **qué función cumple la IA dentro del proceso de trabajo**.

Sin embargo, para diseñar buenos prompts hace falta una segunda distinción. Además de preguntarse para qué se usa la IA, conviene preguntarse **desde qué papel se le invita a participar en la conversación**. Esa segunda dimensión es la que aquí se denomina **roles de la IA**.

Esta idea es importante porque una misma función puede ejecutarse de maneras muy distintas según el rol asignado. Por ejemplo, una IA puede ayudar a revisar un documento como correctora de estilo, como analista crítico, como usuaria final simulada o como evaluadora metodológica. En todos los casos participa en una revisión, pero la conversación cambia porque cambia el lugar desde el cual interpreta la tarea.

Este texto presenta un marco para entender qué son los roles, por qué resultan útiles al diseñar prompts y cómo se relacionan con los patrones de colaboración. La intención es ofrecer una estructura que ayude a pasar de prompts vagos, del tipo “ayúdame con esto”, a lo que en este repositorio se denomina **prompts intencionados**.

La expresión *prompts intencionados* se utiliza aquí para referirse a prompts diseñados de manera deliberada para orientar el tipo de interacción que se quiere establecer con la inteligencia artificial. En lugar de formular una instrucción abierta y poco estructurada, el usuario define con mayor claridad qué tipo de ayuda necesita, desde qué perspectiva debe analizarse el problema y qué tipo de resultado se espera obtener.

Este uso del término no corresponde a una categoría formal establecida en la literatura sobre inteligencia artificial. La denominación se introduce en este repositorio como una forma de hacer explícita una práctica que aparece con frecuencia en el diseño de prompts más avanzados. En estos casos, el prompt no se limita a pedir un resultado, también busca **estimular procesos de análisis, organización de ideas y revisión crítica**.

La idea se relaciona con discusiones presentes en la literatura sobre *prompt engineering* y diseño de instrucciones para sistemas de IA generativa (Liu et al., 2023; White et al., 2023). En estos trabajos se observa que la calidad de la interacción mejora cuando el prompt incluye elementos que orientan el razonamiento del sistema, por ejemplo roles, pasos de análisis o criterios de evaluación.

---

## Qué se entiende aquí por rol

En este contexto, un **rol** es la posición conversacional desde la cual se invita a la inteligencia artificial a participar en una tarea.

La palabra posición es importante. No se trata de fingir que la IA “es” realmente una profesora, un analista o un revisor jurídico. Lo que se hace es delimitar **qué tipo de mirada debe adoptar**, qué aspectos debe priorizar y qué criterios debe usar para orientar su respuesta.

Cuando alguien escribe un prompt como:

> Actúa como analista de procesos y revisa este flujo de trabajo.

está definiendo un rol. La herramienta seguirá siendo un sistema de IA, pero su respuesta tenderá a organizarse alrededor de operaciones propias de un analista, por ejemplo identificar pasos, dependencias, cuellos de botella o ambigüedades.

Desde el punto de vista práctico, asignar un rol ayuda a reducir la ambigüedad de la interacción. Desde el punto de vista cognitivo, ayuda a **dar forma al tipo de ayuda que se espera recibir**.

---

## Por qué los roles mejoran la interacción con IA

Muchas interacciones pobres con inteligencia artificial no fallan porque la herramienta sea incapaz de responder, sino porque el usuario no ha delimitado bien el tipo de respuesta que necesita. Cuando un prompt queda demasiado abierto, la IA suele producir una salida genérica, correcta en apariencia, pero poco útil para el trabajo real.

La definición de un rol ayuda en al menos cuatro sentidos.

### 1. Delimita la perspectiva

Cada rol organiza la atención de la IA hacia ciertos aspectos del problema. Un revisor se fija en vacíos o inconsistencias. Un tutor se concentra en explicar. Un analista busca estructura. Un diseñador propone alternativas.

### 2. Hace más visible el tipo de ayuda que se espera

Muchas veces el usuario no necesita contenido nuevo, necesita una forma de mirar lo que ya tiene. Asignar un rol permite pedir con mayor precisión ese tipo de apoyo.

### 3. Facilita la evaluación de la respuesta

Si el rol está claro, también resulta más fácil juzgar si la respuesta fue útil. La pregunta deja de ser “¿respondió algo razonable?” y pasa a ser “¿respondió bien desde el rol que se le pidió?”.

### 4. Mejora la calidad del prompt

Diseñar prompts con roles obliga a formular mejor el problema. Ese esfuerzo ya constituye, en sí mismo, una forma de pensamiento más estructurado.

---

## Relación entre roles y patrones

Los **patrones** y los **roles** describen dos dimensiones distintas del uso de la inteligencia artificial.

Los patrones ayudan a responder la pregunta:

> ¿Para qué estoy usando la IA en este momento del trabajo?

Los roles ayudan a responder la pregunta:

> ¿Desde qué lugar quiero que la IA participe en esta conversación?

La diferencia puede verse mejor con un ejemplo.

Supongamos que una persona está trabajando con la transcripción de una reunión.

Si utiliza la IA para organizar la conversación e identificar temas, está siguiendo el patrón de **asistente de estructuración**.

Ahora bien, esa misma tarea puede pedirse desde roles distintos:

- como **analista temático**, si quiere categorías y patrones;
- como **facilitador de reuniones**, si quiere acuerdos, decisiones y pendientes;
- como **revisor de claridad**, si quiere identificar partes ambiguas o mal definidas.

El patrón sigue siendo parecido, organizar información, pero el rol cambia la manera en que la IA interpreta la tarea.

Por eso conviene distinguir entre ambas capas:

| Dimensión | Pregunta que responde |
|---|---|
| Patrón | ¿Qué función cumple la IA en el proceso? |
| Rol | ¿Desde qué posición interpreta la tarea? |
| Prompt | ¿Cómo se formula operativamente la interacción? |

Esta distinción permite diseñar interacciones más finas. También ayuda a enseñar mejor el uso de IA, porque muestra que una buena conversación con estas herramientas no depende solo del tema, depende de cómo se estructura el tipo de ayuda que se espera.

---

## Roles frecuentes en el trabajo con IA

A continuación se presentan algunos roles que aparecen con frecuencia en procesos de estudio, diseño, análisis y producción. La lista no pretende ser exhaustiva. Su propósito es ofrecer un vocabulario útil para pensar mejor la interacción.

---

## 1. IA como analista

### Descripción

En este rol la IA examina información para identificar estructura, categorías, relaciones o patrones. Resulta útil cuando el usuario necesita comprender mejor un conjunto de insumos antes de producir un resultado final.

### Qué tipo de tareas apoya

- analizar documentos extensos
- encontrar temas recurrentes
- organizar información dispersa
- identificar dependencias en un proceso
- comparar varias fuentes de información

### Ejemplo de prompt

> Actúa como analista de procesos. Revisa esta transcripción de reunión e identifica los pasos principales del proceso, los actores involucrados, las decisiones que aparecen y los puntos donde el flujo no está completamente claro.

### Qué aporta este rol

Este rol ayuda a **ver mejor el material de entrada**. En muchos casos el valor de la IA no está en escribir rápido, está en ayudar a leer mejor algo complejo.

---

## 2. IA como tutor

### Descripción

En este rol la IA explica, aclara y guía el aprendizaje. Resulta útil cuando la tarea requiere comprensión progresiva y no solo producción de un resultado.

### Qué tipo de tareas apoya

- explicar conceptos
- aclarar relaciones entre ideas
- proponer ejemplos
- guiar ejercicios paso a paso
- adaptar explicaciones al nivel del usuario

### Ejemplo de prompt

> Actúa como tutor. Explícame qué diferencia hay entre una épica, una feature y una historia de usuario, usando ejemplos simples de desarrollo de software. Después hazme dos preguntas para comprobar si lo entendí.

### Qué aporta este rol

Este rol convierte a la IA en una herramienta de **mediación pedagógica**. No produce simplemente una respuesta, organiza una secuencia de comprensión.

---

## 3. IA como crítico o revisor

### Descripción

En este rol la IA examina un artefacto ya producido, un texto, un diagrama, un flujo, una propuesta, y señala vacíos, debilidades, ambigüedades o puntos que conviene revisar antes de validarlo con otras personas.

### Qué tipo de tareas apoya

- revisar documentos antes de enviarlos
- identificar supuestos implícitos
- detectar pasos faltantes
- señalar ambigüedades en diagramas o procesos
- examinar la solidez de una argumentación

### Ejemplo de prompt

> Actúa como revisor preliminar de procesos. Observa este diagrama y señala qué pasos podrían estar incompletos, qué decisiones no están representadas y qué partes podrían generar interpretaciones distintas entre los expertos que lo revisarán.

### Qué aporta este rol

Este rol ayuda a **elevar la calidad antes de la validación final**. En contextos profesionales resulta especialmente valioso, porque permite hacer una revisión previa antes de involucrar a expertos humanos.

---

## 4. IA como diseñador o arquitecto de proceso

### Descripción

En este rol la IA participa en la estructuración de un método de trabajo. Puede sugerir secuencias, checkpoints, preguntas de verificación o formas de organizar la tarea.

### Qué tipo de tareas apoya

- diseñar flujos de trabajo
- construir prompts maestros
- definir pasos de análisis
- proponer mecanismos de validación
- ordenar procesos complejos

### Ejemplo de prompt

> Actúa como diseñador de procesos de trabajo con IA. Ayúdame a construir una secuencia reutilizable para transformar una reunión grabada en un diagrama de proceso validable por expertos. Incluye transcripción, análisis temático, extracción de decisiones, revisión preliminar del diagrama y validación final.

### Qué aporta este rol

Este rol mueve la interacción hacia un nivel más alto de madurez. La IA deja de participar solo en la ejecución de tareas y empieza a colaborar en la **ingeniería del propio proceso**.

---

## 5. IA como editor

### Descripción

En este rol la IA mejora un material existente, cuidando forma, claridad, coherencia, tono o estructura. Resulta útil cuando ya existe un borrador y lo que se necesita es refinarlo.

### Qué tipo de tareas apoya

- mejorar redacción
- ajustar tono
- clarificar ideas
- reorganizar secciones
- adaptar un texto a un formato específico

### Ejemplo de prompt

> Actúa como editor académico. Revisa este texto y ayúdame a mejorar su claridad, mantener un tono riguroso y hacer más visible la relación entre las ideas, sin cambiar el contenido central.

### Qué aporta este rol

Este rol es muy útil, pero conviene distinguirlo del rol de crítico. El editor mejora la forma y la estructura del texto. El crítico cuestiona la solidez del contenido o la lógica del argumento.

---

## 6. IA como generador de alternativas

### Descripción

En este rol la IA se utiliza para ampliar el espacio de posibilidades. Resulta útil en momentos de exploración, cuando el usuario todavía no quiere cerrar una respuesta.

### Qué tipo de tareas apoya

- generar opciones de solución
- proponer enfoques distintos
- sugerir interpretaciones alternativas
- ampliar posibilidades de diseño
- explorar escenarios

### Ejemplo de prompt

> Actúa como generador de alternativas. Propón tres formas distintas de representar este proceso de transferencia de conocimiento, una centrada en tareas, otra en decisiones y otra en roles involucrados.

### Qué aporta este rol

Este rol es especialmente valioso en fases de divergencia, porque evita que la primera idea disponible se convierta automáticamente en la única opción considerada.

---

## 7. IA como simulador de audiencia o usuario final

### Descripción

En este rol la IA revisa un material desde la perspectiva de quien lo recibirá o utilizará. Puede servir para anticipar dudas, malentendidos o necesidades de aclaración.

### Qué tipo de tareas apoya

- revisar si un documento es entendible
- anticipar preguntas de una audiencia
- probar claridad de instrucciones
- examinar si un flujo sería comprensible para otra área

### Ejemplo de prompt

> Actúa como usuario nuevo del proceso. Revisa este diagrama y dime qué partes te generarían dudas si tuvieras que ejecutarlo por primera vez.

### Qué aporta este rol

Este rol ayuda a poner a prueba la **legibilidad práctica** del material, algo muy importante cuando se trabaja con diagramas, instructivos o documentos de transferencia de conocimiento.

---

## Cómo elegir el rol adecuado

Elegir un rol útil depende de la naturaleza de la tarea. Una forma sencilla de decidir consiste en preguntarse qué tipo de ayuda se necesita en ese momento.

- Si necesitas entender mejor los insumos, el rol de **analista** puede ser adecuado.
- Si necesitas aprender o aclarar conceptos, el rol de **tutor** puede ser más útil.
- Si ya tienes un borrador y quieres mejorarlo, conviene pensar en **editor** o **revisor**.
- Si estás diseñando un flujo completo, puede resultar más adecuado el rol de **arquitecto o diseñador de proceso**.
- Si quieres explorar varias posibilidades antes de decidir, conviene usar el rol de **generador de alternativas**.

En la práctica, los roles pueden combinarse. Una misma tarea puede pasar por varios de ellos. Por ejemplo, en un proyecto de documentación de conocimiento se podría usar la IA primero como analista de transcripciones, luego como diseñadora de diagrama y después como revisora preliminar antes de enviar el material a expertos.

---

## Ejemplo completo de combinación entre patrón y rol

Supongamos un caso de transferencia de conocimiento, en el que una persona quiere transformar una reunión técnica en un diagrama de proceso.

### Paso 1, análisis del insumo

**Patrón:** asistente de estructuración  
**Rol:** analista

Prompt:

> Actúa como analista de procesos. Lee esta transcripción e identifica actores, pasos, decisiones, excepciones y posibles ambigüedades.

### Paso 2, exploración de representación

**Patrón:** colaborador de pensamiento  
**Rol:** generador de alternativas

Prompt:

> Actúa como diseñador de alternativas. Propón tres maneras distintas de representar este proceso, una orientada a flujo operativo, otra a decisiones y otra a roles.

### Paso 3, construcción del artefacto

**Patrón:** asistente de producción  
**Rol:** diseñador de proceso

Prompt:

> Actúa como diseñador de procesos. Con base en la alternativa elegida, ayúdame a redactar una descripción clara del flujo que luego llevaré a Miro.

### Paso 4, revisión previa

**Patrón:** revisor preliminar  
**Rol:** crítico

Prompt:

> Actúa como revisor preliminar. Examina este diagrama y señala qué partes podrían estar incompletas, qué condicionales faltan y qué puntos conviene validar con expertos antes de aprobarlo.

Este ejemplo muestra por qué conviene distinguir entre patrones y roles. El patrón ayuda a ubicar la función que cumple la IA en cada momento del proceso. El rol ayuda a precisar desde qué perspectiva debe operar la herramienta.

---

## Relación con el diseño de prompts

Los roles tienen implicaciones directas sobre la calidad de los prompts. Un prompt mejora cuando el usuario no se limita a decir qué quiere obtener, también explicita desde qué tipo de ayuda quiere construirlo.

Por eso un prompt como:

> Ayúdame con este texto.

suele ser menos útil que un prompt como:

> Actúa como revisor académico. Lee este texto, identifica partes ambiguas, señala supuestos no explicados y luego sugiere mejoras concretas en la organización de las ideas.

En el segundo caso, el rol organiza la interacción y orienta el tipo de respuesta.

Diseñar prompts con roles explícitos no garantiza automáticamente un mejor resultado, pero sí mejora la probabilidad de obtener una ayuda más pertinente y evaluable.

---

## Fundamento conceptual de la idea de rol

La noción de rol conversacional se relaciona con varias discusiones teóricas sobre herramientas cognitivas, mediación y reflexión profesional.

La teoría de la **mente extendida**, propuesta por Clark y Chalmers (1998), ayuda a entender por qué una herramienta externa puede participar en procesos de razonamiento, memoria y representación.

La idea de **mediación**, desarrollada por Vygotsky (1978), permite interpretar la interacción con IA como una actividad guiada por herramientas culturales que ayudan a organizar la comprensión.

La noción de **reflexión en la acción**, formulada por Schön (1983), aporta un marco especialmente útil para entender por qué la IA puede funcionar como interlocutora en procesos de revisión, reformulación y mejora del trabajo mientras este se está realizando.

Desde esta perspectiva, asignar roles a la IA no constituye un simple truco de redacción de prompts. Constituye una forma de hacer explícito qué tipo de mediación cognitiva se espera de la herramienta en un momento dado.

---

## Cierre

Incorporar la noción de roles en el trabajo con inteligencia artificial permite pasar de una interacción genérica a una interacción más estructurada. La pregunta deja de ser únicamente “qué quiero que me entregue la IA” y empieza a incluir otra pregunta más precisa, “desde qué lugar quiero que me ayude a pensar esto”.

Esta distinción tiene valor pedagógico y práctico. Pedagógico, porque ayuda a enseñar a estudiantes y profesionales que el trabajo con IA implica diseñar conversaciones. Práctico, porque mejora la calidad de los prompts y hace más visible el tipo de ayuda que se está buscando.

Cuando los roles se articulan con los patrones de colaboración, el uso de la IA se vuelve más legible, más transferible y más fácil de mejorar. Ese paso es importante para cualquier persona que quiera trabajar con estas herramientas de una manera más consciente y más rigurosa.

## Referencias

Clark, A., & Chalmers, D. (1998). *The extended mind*. Analysis, 58(1), 7–19.
Liu, P., Yuan, W., Fu, J., Jiang, Z., Hayashi, H., & Neubig, G. (2023). Pre-train, prompt, and predict: A systematic survey of prompting methods in natural language processing. ACM Computing Surveys.
Schön, D. A. (1983). *The reflective practitioner: How professionals think in action*. Basic Books.

Vygotsky, L. S. (1978). *Mind in society: The development of higher psychological processes*. Harvard University Press.

White, J., Fu, Q., Hays, S., Sandborn, M., Oleynik, V., Gilbert, H., Elnashar, A., Spencer-Smith, J., & Schmidt, D. (2023). A prompt pattern catalog to enhance prompt engineering with ChatGPT. arXiv.

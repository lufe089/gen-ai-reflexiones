# Prompts 
El uso de modelos de lenguaje de gran escala (Large Language Models, LLM) en educación, investigación y organizaciones ha crecido de manera acelerada. Sin embargo, la calidad de las respuestas generadas por estos sistemas depende en gran medida de cómo se formulan las instrucciones que guían su comportamiento. A este proceso se le conoce como **ingeniería de prompts**.

Un *prompt* suele definirse como el texto que se introduce en un sistema de inteligencia artificial para solicitar una respuesta. Sin embargo, en aplicaciones complejas esta definición resulta insuficiente. En muchos casos, el prompt no es simplemente una pregunta, sino una **estructura que organiza la interacción entre el usuario y el sistema**.

## Prompts intencionados: partes sugeridas y buenas prácticas de diseño

Los ejemplos de prompts incluidos en este repositorio muestran que un
prompt puede diseñarse como algo más que una instrucción breve dirigida
a un sistema de inteligencia artificial. En muchos casos, el prompt
organiza una interacción completa entre el usuario y la herramienta,
estructurando el proceso de análisis, generación de resultados y
revisión posterior.

En este repositorio se utiliza la expresión **prompt intencionado** para
referirse a prompts diseñados deliberadamente para orientar el proceso
de pensamiento que ocurre durante la interacción con la inteligencia
artificial. Estos prompts no buscan únicamente producir una respuesta.
Su objetivo es estructurar una conversación que permita analizar
información, identificar supuestos, explorar alternativas y mejorar
progresivamente la calidad de los resultados.

Un **prompt intencionado** es un prompt diseñado deliberadamente para orientar el proceso de pensamiento que ocurre durante la interacción con la inteligencia artificial. Su objetivo no es únicamente producir una respuesta automática, sino **estructurar un proceso de análisis, reflexión y mejora progresiva de los resultados**.

Este enfoque resulta especialmente útil cuando la inteligencia artificial se utiliza en contextos donde existe un propósito claro que debe guiar la interacción, como:

- aprendizaje y formación
- diseño de proyectos
- análisis de información
- toma de decisiones
- diseño de políticas
- innovación en organizaciones

Desde esta perspectiva, los prompts pueden entenderse como **estructuras de mediación cognitiva** que organizan el diálogo entre humanos y sistemas inteligentes.

Los ejemplos disponibles en el repositorio muestran prompts
relativamente largos y estructurados, porque reflejan **procesos de
trabajo reales**, no solo preguntas aisladas. Por esta razón suelen
dividirse en **secciones claramente identificables**, lo cual facilita
su comprensión por parte del humano que los utiliza y también permite
mantenerlos y modificarlos con el tiempo.

A continuación se presentan algunas **partes sugeridas que suelen
aparecer en prompts intencionados**, indicando cómo se denominan
prácticas similares en ingeniería de prompts.

Aquí se encuentran otros ejemplos:
* [Prompts para aprender](https://github.com/lufe089/gen-ai-reflexiones/blob/main/prompts_aprender.md)
* [Ejemplos](https://github.com/lufe089/gen-ai-reflexiones/blob/main/ejemplo_prompts_intencionados.md)
------------------------------------------------------------------------

## 1. Definición del rol de la IA

*(Role prompting)*

Una de las primeras decisiones al diseñar un prompt consiste en definir
**qué rol debe asumir la inteligencia artificial** al analizar la tarea.

En ingeniería de prompts esta técnica se conoce como **role prompting**.
Consiste en indicar explícitamente desde qué perspectiva debe
interpretarse el problema.

### Ejemplo inspirado en los prompts del repositorio

    Actúa como profesor universitario con experiencia en inteligencia artificial aplicada a la productividad laboral.
    Tu tarea es analizar el proyecto presentado por un estudiante y redactar una retroalimentación que le ayude a mejorar su forma de trabajar con IA.

La definición del rol cumple varias funciones:

-   establece el marco interpretativo de la tarea
-   orienta el tipo de criterios que debe usar la IA
-   ayuda a ajustar el tono y el nivel de profundidad de la respuesta

Los modelos de lenguaje tienden a producir respuestas más coherentes cuando se les asigna un rol explícito.

Desde la pedagogía, este enfoque se relaciona con el concepto de **andamiaje educativo** (*scaffolding*) propuesto por Wood, Bruner y Ross (1976), donde el tutor proporciona apoyo estructurado que facilita el proceso de razonamiento del aprendiz.

------------------------------------------------------------------------

## 2. Contexto y propósito de la interacción

*(Task framing / context setting)*

Otra parte importante consiste en explicar **por qué se está realizando
la tarea** y qué se espera lograr con la interacción.

En ingeniería de prompts esta práctica suele denominarse **task
framing** o **context setting**.

### Ejemplo

    Los estudiantes están finalizando un diplomado cuyo objetivo es aprender a utilizar la inteligencia artificial
    no solo para producir resultados, sino también para estructurar problemas, organizar criterios
    y diseñar procesos de validación.

Este tipo de contexto ayuda al modelo a comprender:

- el propósito de la interacción  
- el tipo de análisis requerido  
- el nivel de profundidad esperado  

Desde la teoría del **aprendizaje situado** (Lave & Wenger, 1991), el conocimiento se construye dentro de prácticas sociales concretas. Por ello, proporcionar contexto permite que la inteligencia artificial participe de manera más adecuada en ese entorno.


------------------------------------------------------------------------

## 3. Restricciones y límites de la tarea

*(Constraint specification)*

Los prompts intencionados suelen incluir instrucciones explícitas sobre
**lo que la inteligencia artificial debe evitar hacer**.

En ingeniería de prompts esta práctica se conoce como **constraint
specification**.

### Ejemplo

    No debes inventar información que no esté presente en el documento.
    Si una sección no tiene suficiente evidencia para evaluarla, debes indicarlo explícitamente.

Estas restricciones ayudan a:

-   reducir desviaciones del objetivo
-   disminuir alucinaciones
-   mantener coherencia con el propósito del trabajo

La investigación sobre LLM identifica las **alucinaciones** como uno de los principales desafíos de estos sistemas (Ji et al., 2023). Establecer límites explícitos en el prompt es una estrategia práctica para mitigarlas.

------------------------------------------------------------------------

## 4. Descomposición del proceso en etapas

*(Task decomposition / step‑by‑step prompting)*

Organizar la tarea en **etapas o bloques de
trabajo**. En la literatura sobre prompting esto se conoce como **task
decomposition**.

### Ejemplo

    Antes de redactar la retroalimentación debes realizar el siguiente proceso:

    1. Leer el documento completo.
    2. Evaluar si el proyecto cumple con los elementos esperados.
    3. Explicar brevemente tu valoración general.
    4. Preguntar al profesor si está de acuerdo antes de continuar.

Dividir el proceso en etapas permite:

-   mejorar la calidad del razonamiento
-   hacer visible el proceso de análisis
-   facilitar la supervisión humana

Desde la psicología cognitiva, esta estrategia se relaciona con la **teoría de la carga cognitiva** (Sweller, 1988). Dividir una tarea compleja en etapas reduce la carga mental y facilita el aprendizaje.

------------------------------------------------------------------------

## 5. Interacción explícita con el usuario

*(Human‑in‑the‑loop prompting)*
Instrucciones para **detener el proceso y solicitar información adicional al usuario**.

Esto introduce un enfoque conocido como **human‑in‑the‑loop**, en el
cual la IA colabora con el humano pero no reemplaza su criterio. En lugar de reemplazar al usuario, la inteligencia artificial se convierte en un **colaborador que apoya el proceso de análisis**.

### Ejemplo

    Después de este análisis debes preguntar:

    "¿Estás de acuerdo con esta valoración general antes de redactar el feedback?"

    Debes esperar confirmación antes de continuar.

Este tipo de instrucciones es muy importante porque convierte el prompt
en una **interacción colaborativa**, no en una simple generación
automática de texto.
Desde la teoría sociocultural del aprendizaje (Vygotsky, 1978), este tipo de interacción puede interpretarse como una forma de **mediación cognitiva** donde el conocimiento se construye mediante diálogo.

------------------------------------------------------------------------

## 6. Especificación del formato de salida

*(Output specification)*

Otra práctica común consiste en indicar claramente **cómo debe
estructurarse la respuesta final**.

Esto se conoce como **output specification**.

### Ejemplo

Escribe la respuesta en tres secciones:

1. análisis general  
2. recomendaciones  
3. riesgos o limitaciones  

Definir el formato permite:

- mejorar la consistencia de las respuestas  
- facilitar su integración en documentos  
- simplificar procesos organizacionales  

En entornos empresariales o institucionales, esta práctica resulta especialmente importante porque las respuestas generadas por IA suelen integrarse en informes o procesos de toma de decisiones.


------------------------------------------------------------------------

## 7. Revisión final del resultado

*(Self‑critique / reflection prompting)*

Instrucciones para que el sistema **revise su
propia respuesta antes de entregarla**.

Este patrón se conoce como **self‑critique** o **reflection prompting**.

### Ejemplo

    Antes de entregar la respuesta relee el texto como si fueras el estudiante
    y verifica que el tono sea natural y respetuoso.

Las etapas de revisión ayudan a mejorar la calidad de los resultados y a
reducir errores.
------------------------------------------------------------------------

## 8. Diseñar prompts reutilizables

Una característica importante es que pueden **reutilizarse en distintos contextos**. A diferencia de una simple plantilla donde se reemplazan palabras, un prompt intencionado funciona como una **estructura de interacción adaptable**.

Por ejemplo, un prompt diseñado para evaluar proyectos estudiantiles puede adaptarse para:

- evaluar propuestas de investigación
- analizar estrategias empresariales
- revisar informes técnicos

La clave es que el prompt **organiza el proceso de análisis**, no solo el contenido de la respuesta.

------------------------------------------------------------------------

Una práctica muy útil al diseñar prompts consiste en utilizar **separadores visuales y marcadores estructurales** dentro del texto del prompt.

Estos elementos ayudan a dividir la instrucción en partes claras y facilitan que el modelo interprete cada bloque como una unidad conceptual.

Entre los recursos posibles se encuentran:
- usar separadores para dividir secciones  
- escribir encabezados claros
- bloques delimitados por líneas horizontales 
- usar numeración para procesos  
- usar viñetas para criterios o listas  
- evitar párrafos demasiado largos  

Separar estas partes tiene varias ventajas.

Primero, facilita la **comprensión del prompt por parte del propio
humano que lo utiliza**. Cuando un prompt tiene secciones visibles es
más fácil entender qué hace cada parte.

Segundo, facilita el **mantenimiento del prompt con el tiempo**. Cuando
una parte necesita ajustarse, por ejemplo las restricciones o el formato
de salida, el cambio puede realizarse sin modificar todo el prompt.

Tercero, hace posible **reutilizar el prompt en otros contextos**. Un
prompt que incluye instrucciones para pedir aclaraciones al usuario
puede utilizarse en distintas tareas sin necesidad de convertirlo en una
simple plantilla de texto.

Esta diferencia es importante. Un prompt intencionado no se limita a ser
una **plantilla en la cual se reemplazan palabras**. En cambio, se
comporta como una **estructura de interacción reutilizable**, capaz de
solicitar información adicional al usuario cuando sea necesario y de
guiar el proceso de análisis paso a paso.

## 9. Errores comunes al diseñar prompts

A continuación se describen algunos de los problemas más frecuentes.

------------------------------------------------------------------------

### 9.1 Falta de estructura

Uno de los errores más comunes consiste en escribir prompts largos que
mezclan múltiples instrucciones sin una organización clara.

Ejemplo de prompt poco estructurado:

    Analiza este documento y dime qué piensas, revisa si tiene errores,
    sugiere mejoras y también explica si los argumentos son coherentes.
    Además revisa el tono del texto.

En este tipo de instrucciones no es evidente:

-   cuál es el objetivo principal\
-   qué criterios deben aplicarse\
-   en qué orden debe realizarse el análisis

Como resultado, el modelo puede responder de manera superficial o
ignorar algunos aspectos de la tarea.

Una práctica más efectiva consiste en **separar las instrucciones en
secciones claras**, por ejemplo:

    OBJETIVO
    Analizar el documento y evaluar su calidad argumentativa.

    CRITERIOS DE ANÁLISIS
    - coherencia de los argumentos
    - claridad del texto
    - consistencia del tono

    PROCESO
    1. Analizar el documento completo
    2. Identificar fortalezas
    3. Identificar oportunidades de mejora

La estructura facilita tanto la interpretación del prompt por parte del
modelo como la comprensión por parte del usuario.

------------------------------------------------------------------------

### 9.2 Mezclar contexto con instrucciones

Otro error frecuente consiste en **mezclar información de contexto con
instrucciones operativas**.

Ejemplo:

    Los estudiantes están terminando un diplomado y el objetivo es que aprendan
    a usar la inteligencia artificial para estructurar problemas, analiza el
    documento y escribe una retroalimentación pero también revisa los prompts.

En este caso el modelo recibe información relevante, pero las
instrucciones no están claramente delimitadas.

Una mejor práctica consiste en separar explícitamente:

-   el contexto\
-   el objetivo\
-   el proceso

Esto permite que el modelo identifique con mayor claridad qué parte del
texto describe la situación y cuál define las acciones que debe
realizar.

------------------------------------------------------------------------

### 9.3 Ausencia de proceso paso a paso

Muchos prompts piden directamente un resultado final sin orientar el
proceso de razonamiento.

Ejemplo:

    Evalúa este proyecto y escribe una retroalimentación.

Aunque esta instrucción es comprensible, no orienta el análisis.

En tareas complejas suele ser más efectivo especificar **un proceso de
análisis**.

    Antes de escribir la retroalimentación debes:

    1. Analizar el documento completo
    2. Identificar la idea principal
    3. Evaluar la coherencia entre problema y solución
    4. Proponer recomendaciones

Esta práctica se relaciona con técnicas conocidas como **step‑by‑step
prompting** o **chain‑of‑thought prompting** (Wei et al., 2022).

------------------------------------------------------------------------

### 9.4 Falta de delimitación del rol

Cuando el prompt no define qué tipo de asistente debe simular la
inteligencia artificial, las respuestas pueden variar mucho en estilo y
profundidad.

Ejemplo:

    Analiza este texto y comenta qué piensas.

Un prompt más claro podría definir el rol:

    Actúa como profesor universitario con experiencia en evaluación de proyectos académicos.

La definición del rol ayuda a establecer el **marco interpretativo**
desde el cual el modelo debe analizar la información.

------------------------------------------------------------------------

### 9.5 Repetición innecesaria de instrucciones

Otro problema frecuente en prompts largos es la **repetición excesiva de
las mismas instrucciones**.

Ejemplo:

    Analiza el documento cuidadosamente.
    Recuerda analizar el documento antes de responder.
    Antes de responder debes analizar el documento.

Aunque puede parecer que repetir instrucciones refuerza su importancia,
en muchos casos introduce **ruido innecesario** en el prompt.

La repetición excesiva puede provocar:

-   prompts innecesariamente largos\
-   pérdida de claridad en las instrucciones\
-   mayor dificultad para mantener o actualizar el prompt

Una alternativa más clara es organizar el prompt en secciones:

    PROCESO

    1. Analizar el documento completo.
    2. Identificar los elementos clave.
    3. Elaborar la retroalimentación final.

------------------------------------------------------------------------

### 9.6 Falta de delimitación entre secciones

Cuando un prompt contiene múltiples ideas sin separadores o encabezados,
resulta difícil identificar sus partes.

Ejemplo poco claro:

    Actúa como analista experto analiza el documento revisa coherencia
    y luego escribe recomendaciones teniendo en cuenta el contexto
    del diplomado.

Versión estructurada:

    ROL
    Actúa como analista experto en evaluación de proyectos.

    CONTEXTO
    El análisis se realiza en el contexto de un diplomado.

    TAREA
    Analizar el documento y proponer recomendaciones.

El uso de separadores, encabezados y listas facilita la lectura y mejora
la claridad de la interacción.

------------------------------------------------------------------------

### 9.7 Prompts demasiado vagos

Finalmente, muchos prompts fallan simplemente porque **no especifican lo
que se espera obtener**.

Ejemplo:

    Dame ideas sobre este tema.

Un prompt más claro podría indicar:

    Genera tres propuestas de mejora para este proyecto
    teniendo en cuenta criterios de viabilidad técnica
    y claridad conceptual.

Cuanto más claro sea el propósito del prompt, mayor será la probabilidad
de obtener respuestas útiles.

------------------------------------------------------------------------

### 9.8 Diseñar prompts es diseñar interacción

Estos errores muestran que diseñar prompts no consiste únicamente en
escribir preguntas.

En contextos profesionales, educativos o de investigación, diseñar
prompts implica **diseñar la interacción entre el humano y el sistema de
inteligencia artificial**.

Por esta razón, los prompts intencionados suelen adoptar estructuras
similares a:

-   documentos técnicos\
-   guías de trabajo\
-   protocolos de análisis

Cuando se diseñan con claridad, los prompts pueden convertirse en
**herramientas reutilizables que ayudan a organizar procesos de
pensamiento y de trabajo con inteligencia artificial**.


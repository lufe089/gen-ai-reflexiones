# Prompts intencionados: partes sugeridas y buenas prácticas de diseño

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

Este tipo de contexto permite que el modelo interprete mejor la tarea y
comprenda qué tipo de análisis resulta pertinente.

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

------------------------------------------------------------------------

## 4. Descomposición del proceso en etapas

*(Task decomposition / step‑by‑step prompting)*

Muchos prompts intencionados organizan la tarea en **etapas o bloques de
trabajo**.

En la literatura sobre prompting esto se conoce como **task
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

------------------------------------------------------------------------

## 5. Interacción explícita con el usuario

*(Human‑in‑the‑loop prompting)*

Muchos prompts intencionados incluyen instrucciones para **detener el
proceso y solicitar información adicional al usuario**.

Esto introduce un enfoque conocido como **human‑in‑the‑loop**, en el
cual la IA colabora con el humano pero no reemplaza su criterio.

### Ejemplo

    Después de este análisis debes preguntar:

    "¿Estás de acuerdo con esta valoración general antes de redactar el feedback?"

    Debes esperar confirmación antes de continuar.

Este tipo de instrucciones es muy importante porque convierte el prompt
en una **interacción colaborativa**, no en una simple generación
automática de texto.

------------------------------------------------------------------------

## 6. Especificación del formato de salida

*(Output specification)*

Otra práctica común consiste en indicar claramente **cómo debe
estructurarse la respuesta final**.

Esto se conoce como **output specification**.

### Ejemplo

    Escribe la retroalimentación en cuatro párrafos narrativos.
    No utilices listas ni viñetas.
    Utiliza un tono académico cercano.

Definir el formato permite que la salida generada sea más consistente y
más fácil de integrar en documentos o procesos institucionales.

------------------------------------------------------------------------

## 7. Revisión final del resultado

*(Self‑critique / reflection prompting)*

Algunos prompts incluyen instrucciones para que el sistema **revise su
propia respuesta antes de entregarla**.

Este patrón se conoce como **self‑critique** o **reflection prompting**.

### Ejemplo

    Antes de entregar la respuesta relee el texto como si fueras el estudiante
    y verifica que el tono sea natural y respetuoso.

Las etapas de revisión ayudan a mejorar la calidad de los resultados y a
reducir errores.

------------------------------------------------------------------------

## La importancia de la estructura en prompts más largos

Muchos ejemplos de prompting que circulan en internet utilizan prompts
muy cortos. Estos ejemplos son útiles para ilustrar ideas básicas, pero
resultan limitados cuando se intenta estructurar tareas complejas.

Los **prompts intencionados suelen ser más largos**, porque representan
procesos de trabajo más elaborados.

Por esta razón es útil **dividir el prompt en secciones claramente
identificables**, por ejemplo:

-   Rol del asistente
-   Contexto
-   Objetivo de la tarea
-   Proceso paso a paso
-   Formato de salida
-   Revisión final

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

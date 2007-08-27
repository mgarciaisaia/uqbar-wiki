El paradigma lógico se basa en la definición de reglas lógicas y es un paradigma declarativo así que si no lo leíste todavía te recomiendo leer antes sobre [Declaratividad](declaratividad.html). En este artículo hablamos principalmente de la teoría del paradigma lógico, pero para los ejemplos tomamos como base el lenguaje [Prolog](prolog.html)

Introducción: Silogismos
------------------------

¿Cómo describir un problema usando la lógica? ¿Qué tipo de problema podemos describir?

Comencemos con un ejemplo simple, seguramente muchos de ustedes lo habrán escuchado alguna vez:

  
*Sócrates es hombre*

*Todos los hombres son mortales*

Luego... ¿qué podemos deducir de esto? Claro adivinaste, que Sócrates es mortal. De eso se trata la programación lógica, vamos a describir nuestro conocimiento en formas de reglas y vamos a permitir que otra cosa (el [motor](motor.html)) se ocupe de procesar ese conocimiento y sacar conclusiones al respecto.

¿Y solito se da cuenta de las cosas? Más o menos, en realidad no podemos pedirle al motor que solamente se ponga a deducir y que nos diga a qué conclusión llega, hay que hacerle preguntas más concretas. Por ejemplo podemos preguntarle

  
si socrates es mortal, y nos va a decir que sí

qué mortales conoce, y nos va a decir que socrates es mortal

Esos son los dos tipos de preguntas básicas que el motor va a saber contestar, después vamos a bajar en detalle sobre esto.

¿Cómo lo bajamos a código?
--------------------------

Programemos este mismo ejemplo en Prolog, en realidad es bastante simple: <code>

    hombre(socrates).
    mortal(X):-hombre(X).

</code>

¿Qué quiere decir esto?

-   `hombre(socrates)` afirma que Sócrates es un hombre, o dicho de otra manera que *socrates* tiene la característica *hombre*. Es una afirmación que afecta únicamente a Sócrates y la llamamos un [hecho](hecho.html).
-   `mortal(X):-hombre(X)` es lo que llamamos una [regla](regla.html). La regla es una implicación, el antecedente es `hombre(X)` y el consecuente es `mortal(X)`. Esto quiere decir que para todo X que tenga la característica *hombre* se da que ese X también tiene la característica *mortal* (o más corto: todos los hombres son mortales).

Fijate que *socrates* está en minúscula, mientras que la *X* aparece en mayúscula, ¿por qué? Los términos en minúscula se refieren a cosas particulares y las palabras en mayúscula son [incógnitas](incognita.html) (o variables).

Eso se relaciona también con que la primera línea sea un hecho (porque habla de un individuo particular) y la segunda sea una regla (porque habla de todos los hombres).

Pero la principal diferencia entre el hecho y la regla es que la regla tiene un antecedente (que se debe cumplir para que se cumpla la regla) y el hecho no, el hecho es verdadero siempre. En programas más complejos, a veces pasa que tenemos hechos que usan variables o reglas sobre individuos particulares.

Los hechos me permiten definir **por extensión** el conjunto de individuos que tienen una característica. Las reglas me permiten hacer esa misma definición **por comprensión**.

Más detallado
-------------

Si entendiste todo hasta acá, es momento de formalizar algunas cositas acerca del programa que hicimos. Antes que nada, la base de conocimientos se compone de predicados e individuos.

[individuos](individuo.html) : Los individuos son aquellas cosas sobre las que versa el conocimiento que queremos expresar. En este ejemplo el único individuo que aparece es **socrates**.
[predicados](predicado.html) : Los predicados son las cosas que queremos decir (o predicar, je) acerca de los invividuos. En este ejemplo los predicados son **mortal** y **hombre**.  

Ojo que cuando decimos que Sócrates es un individuo no tiene que ver con que sea una persona, no pasa por ahí. Si hicieramos por ejemplo un sistema para controlar correlatividades entre las materias de la facultad, las materias serían individuos. Y podríamos tener un predicado que cuente qué materias cursaste y otro que refleje las correlatividades de la carrera, a partir de esa información el motor te podría decir qué materias podés cursar (traten de hacer este sistema en prolog y luego en C y vean la diferencia).
---
layout: article
title: Entradas al proceso de diseno
---

Ralph & Wand definen que el diseño clasifica las entradas o influencias al proceso de diseño en requerimientos, objetivos, componentes primitivas, restricciones y entorno.

Requerimientos
--------------

Los requerimientos o *requirements* son la entrada más obvia y tal vez la más importante. La fuente de los requerimientos es el proceso de análisis, el análisis también es una especificación: de lo que el sistema debe ser, de sus características externas. El diseño especifica cómo el sistema debe construirse.

La clasificación más común de los requerimientos es dividirlos entre funcionales y no funcionales. Una buena especificación de requerimientos debe contemplar tanto las cuestiones funcionales como las no funcionales, y el diseño deberá proponer ideas.

### Requerimientos funcionales

Los requerimientos funcionales son las capacidades o funcionalidades de un sistema de software. Detallan el comportamiento del sistema. En otras palabras, lo que el sistema debe proveer. Hay distintos tipos de requerimientos no funcionales:

Procesos de Negocio  
Los procesos de negocios permiten especificar como un proceso se lleva a cabo a través de la organización, ya que requiere intervención de diferentes actores y áreas, en diferentes lugares y tiempos.

<!-- -->

Casos de Uso  
Los caso de uso definen una interacción entre un actor y el sistema, para lograr un objetivo de negocio especifico en un lugar y momento especifico.

### Requerimientos no funcionales

Son los que especifican la forma en que el sistema debe llevar a cabo esas capacidades, determinan la calidad con la que el sistema brinda los servicios o bien la calidad con la que está construido.

### Objetivos (*goals*)

Ralph y Wand diferencian un subconjunto de los requerimientos denominados objetivos (goals). Los objetivos resumen el impacto esperado del sistema en el ambiente.

Componentes primitivas (*primitive components*)
-----------------------------------------------

Son los bloques de construcción provistos por la tecnología subyacente. En los niveles más bajos de abstracción del sistema, las abstracciones utilizadas tienden a coincidir con las herramientas provistas por la tecnología, tanto en cuanto a sus bloques primitivos de construcción, como en la forma de combinarlos entre sí.

Restricciones
-------------

Las restricciones o *constraints* pueden tener diferentes orígenes:

-   **Tecnológicas**, tenemos que tener en cuenta qué cosas permite o no permite la tecnología en la que vamos a construir el sistema.
-   **Leyes y otros reglamentos**, incluyendo a los reglamentos internos de la empresa o licencias de las herramientas que usamos.
-   **Negocio**, el negocio puede imponer restricciones de tiempo de llegada al mercado, costos y beneficios, tiempo de vida del sistema, entre otras.
-   **De arquitectura**, la arquitectura puede imponer restricciones de integridad, correctitud, completitud, constructibilidad o robustez, entre otras.

Entorno (*Environment*)
-----------------------

Nos interesa tanto el entorno tecnológico (con qué tecnología contamos) como social (características de las personas que intervienen). Podemos diferenciar dos entornos:

Entorno de desarrollo  
Es el ambiente en el que se diseña, construye y/o prueba el sistema.

-   Desde el punto de vista social debemos tener en cuenta sus conocimientos previos en cuanto a herramientas tecnológicas, conceptuales y metodológicas. Por ejemplo, antes de introducir una tecnología nueva puede ser una buena idea analizar la capacidad del equipo para aprenderla.
-   Desde el punto de vista tecnológico debemos tener en cuenta por ejemplo los equipos con los que contamos para trabajar, si están todos en un mismo lugar o separados, si la comunicación (redes) entre esos lugares es buena o mala, si tenemos licencias de los programas que queremos usar, etc.

Entorno de uso  
El entorno en el que se usa el sistema.

-   Desde el punto de vista social debemos considerar al usuario que esperamos, por ejemplo al diseñar la interfaz de usuario, o para instalarse el sistema en caso de ser necesario, sus costumbres previas, otros sistemas que usa.

:\*Desde el punto de vista tecnológico podemos considerar el hardware del que puede disponer el usuario, su conección a Internet, etc.

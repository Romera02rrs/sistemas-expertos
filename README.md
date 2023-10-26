# Sistemas-expertos

## Lenguajes imperativos
Este tipo de lenguaje de programación se centra en dar ***instrucciones específicas y precisas sobre como ha de realizarse una tarea***.
Se basa en dar una serie de ***instrucciones que el ordenador debe de seguir paso a paso***.
Gracias a esto se tiene un ***control preciso del resultado*** que se desea y ***también sobre el hardware***.

## Lenguajes declarativos
Este lenguaje se centra en ***obtener el resultado*** que se desea ***sin detallar la forma en la que se consigue*** este resultado.
La forma de programar sería especificar unas ***reglas y declaraciones que describen el resultado*** deseado. 

## Sistemas expertos
Un sistema experto es un tipo de software diseñado para emular el razonamiento y la toma de decisiones de un experto humano en un campo específico. Está basado en un conjunto de reglas y conocimientos expertos previamente definidos y almacenados en una base de datos. Los sistemas expertos utilizan esta base de conocimientos para analizar información nueva y ofrecer recomendaciones o soluciones en función de las reglas y hechos que contienen.

## CLIPS
CLIPS es un sistema experto y un lenguaje de programación desarrollado por la NASA. Fue creado por Charles L. Forgy en 1985. Este sistema experto es una herramienta de inteligencia artificial que se utiliza para construir sistemas expertos y aplicaciones basadas en reglas.
### Datos curiosos
- CLIPS ha sido utilizado por varias empresas e instituciones en todo el mundo, incluyendo NASA, Boeing y la Agencia de Seguridad Nacional de EE. UU.
- En 2009, el software CLIPS fue seleccionado por la NASA para su uso en el Sistema de soporte de ingeniería en vuelo para el Rover Mars Science Laboratory (Curiosity).
- Ha sido empleado en proyectos de robótica, como el desarrollo de robots autónomos para explorar entornos desconocidos.

## Futuro de los sistemas expertos
Con el auge de la inteligencia artificial (IA), los sistemas expertos (SE) evolucionarán para ser más precisos, automatizados y colaborativos. La IA mejorará la toma de decisiones de los SE, permitirá interacciones más naturales y los especializará aún más en áreas específicas. 

## Codigo ecrito en CLIPS devuelve "Es una jirafa"
~~~
(deffacts hechos-iniciales
(tiene-pelos)
(tiene-pezugnas)
(es-ungulado)
(tiene-cuello-largo))

(defrule mamifero-1
(tiene-pelos)
=>
(assert (es-mamifero)))

(defrule mamifero-2
(da-leche)
=>
(assert (es-mamifero)))

(defrule ungulado-1
(es-mamifero)
(tiene-pezugnas)
=>
(assert (es-ungulado)))

(defrule ungulado-2
(es-mamifero)
(rumia)
=>
(assert (es-ungulado)))

(defrule jirafa
(es-ungulado)
(tiene-cuello-largo)
=>
(printout t "Es una jirafa" crlf))
 
(defrule cebra
(es-ungulado)
(tiene-rayas-negras)
=>
(printout t "Es una cebra" crlf))
~~~

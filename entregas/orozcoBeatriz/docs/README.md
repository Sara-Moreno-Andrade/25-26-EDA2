# Reto 002
 
El problema consiste en resolver algunas operaciones como:
 
```
  S E N D
+ M O R E
---------
M O N E Y
```
 
Cada letra representa un dígito del 0 al 9 sin repetirse, y hay que encontrar qué número le toca a cada una para que la suma cuadre. El reto pide resolverlo mediante recursividad.
 
---
 
## Cómo lo he planteado
 
Mi idea fue ir asignándole números a las letras una a una de forma recursiva. Primero recojo todas las letras únicas de cada operación, y luego el método `asignar()` va probando dígitos del 0 al 9 para cada una. Cuando ya están todas asignadas compruebo si la suma se cumple, y si no, deshago la asignación y pruebo con otro número.
 
Hay un par de restricciones que hay que tener en cuenta: no se puede repetir un dígito que ya esté usado por otra letra, y ninguna palabra puede empezar por 0.
 
Lo bueno es que el código es completamente genérico, funciona para cualquier acertijo de este estilo solo cambiando las palabras en el `main`. Lo he probado con los tres puzzles del reto y los resuelve todos sin problema.
 
---
 
## Resultados
 
```
SEND + MORE = MONEY        →   9567 + 1085 = 10652
FORTY + TEN + TEN = SIXTY  →   29786 + 850 + 850 = 31486
ODD + ODD = EVEN           →   dos soluciones: 655+655 y 855+855
```
 
El tercero tiene dos soluciones porque las restricciones son menos estrictas al haber menos letras distintas.

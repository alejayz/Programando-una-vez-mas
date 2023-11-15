# Programando-una-vez-mas
En este repo se pretende dar solución al reto número 3 de la clase de programación:

**1.** Plantear el algoritmo para obtener los números primos hasta n, usando pseudocódigo y diagramas de flujo.

**Algoritmo**
1. Crear una lista de números naturales desde 3 hasta n.

2. Repetir para cada i de la lista.

2.1 Dividir i sobre todos los números x (<i y <(i/2)+1).

2.2 Si el residuo de una división es 0, x es divisor.

2.3 Sino x no es divisor.

3. Si i tiene como divisores a x, i no es un número primo

3.1 Sino i es número primo.

**Pseudocódigo**

```pseudocode
  [variables]
  n: entero
  i: entero
  x: entero <=[i**0,5]
  inicio
   i:=3
   Mientras (i<n) hacer
    Si modulo(i/x) == 0 entonces
     escribir("x es divisor de i")
    sino
     escribir("x no es divisor de i")
    Si x es divisor de i entonces
     escribir("i no es número primo)
    sino
     escribir("i es número primo)
    i:= i + i
   Fin mientras
  Fin
```
**Diagrama de flujo**

![Diagrama primos ](https://user-images.githubusercontent.com/124609988/224497094-c4354e66-a041-43ba-8d57-76278e9a09f9.png)

**2.** Revise el procedimiento matemático para hallar raíces cuadradas, plantee el algoritmo en pseudocódigo y en diagrama de flujo.

**Algoritmo**

1. Separar el radicando en pares de derecha a izquierda.

1.1 Si el radicando es un solo dígito agregar 6 ceros.

1.2 Sino dejar igual.

2. Buscar un número (raíz) que al cuadrado se aproxime al primer par de izquierda a derecha.

2.1 Su resultado restarlo al primer par.

2.2 Al residuo de esa resta agregarle el siguiente par.

3. Duplicar la raíz en un siguiente renglón.

3.1 Agregarle a la raíz duplicada un número entre 1 y 9, y multiplicar por el mismo número. Este resultado debe aproximarse a la cifra en cuestión.

3.2 Este mismo número agregarlo a la raíz.

4. El resultado debe restarse a la cifra en cuestión.

5. Elevar al cuadrado la raíz.

5.1 Sumarle al cuadrado de la raíz el residuo anterior.

**Pseudocódigo**

```pseudocode
  [variables]
  n: entero_radicando
  (p1, p2, p3...): pares
  x: entero_raíz
  z: entero_auxiliar
  (m1, m2...): entero_residuo
  r: real_resultado
  inicio
   Para (n<0) hacer
    escribir("la traíz de n no existe")
   Mientras (n>0) hacer
    Si (n = un dígito) entonces
     agregar 6 ceros y despúes una coma a la raíz
    sino
     dejar igual
     // separar n en pares de derecha a izquierda//
     // buscar un x que al cuadrado se aproxime al primer par de izquierda a drecha//
    Si (x**2) <= p1 entonces
     p1 - (x**2) == m1 y m1 agrego p2 
    sino
     buscar otro x
     // duplicar la raíz x y multiplicar por un número z//
    Si (2x agrego z) * z <= m1 agrego p2 entonces
     (m agrego p2) - ((2x agrego z)*z) == m2 y x agrego z
    sino 
     buscar otro z
     // elevar la raíz al cuadrado y sumar el residuo//
       Para m2 residuo de n + 6 ceros hacer
        agregar a m2 por izquierda ceros hasta completar siete dígitos
       Fin para
    Si (x agrego z)**2 + m2 == n**0,5 entonces
      escribir("x agrego z es la raíz cuadrada de n")
    sino
      escribir("x agrego z no es la raíz cuadrada de n")
       //el proceso continúa hasta que ya no hayan más pares en el radicando//
     m + p == (total de dígitos de n)
   Fin mientras
  Fin
```

**Diagrama de flujo**

![image](https://user-images.githubusercontent.com/124609988/224517722-2058eee9-2bb6-4b2d-804d-a639c24c3d50.png)
![image](https://user-images.githubusercontent.com/124609988/224517842-cc310b71-fc2b-4dd5-bb57-540ae4a1b2a2.png)
![image](https://user-images.githubusercontent.com/124609988/224518040-2de9a907-aaf1-4a7a-ab68-c61b9cf13845.png)

¡Yeah! Al fin completamos el reto


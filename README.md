# Entrgable7
IIP
trabajo de clase iip
Enunciado
La clase Cadena del proyecto entregableT7 representa cadenas de caracteres, en las que se considera que parte de la información relevante la constituyen los caracteres diferentes de los espacios en blanco. Por ello, alguno de los métodos sirve para obtener dicha información. Los caracteres vienen numerados de 0 en adelante.
Un objeto de la clase se construye a partir de un String. Su estructura viene dada por los siguientes atributos de instancia:
char[] a: array en donde se disponen, por orden, los caracteres de la cadena. Su longitud coincide con la longitud o número de caracteres de la cadena.
int prim, ult: posición en donde se encuentra el primer y el último carácter no blanco de la cadena, respectivamente. Así, el rango de índices prim..ult acota la zona del array en donde se encuentran los caracteres no blancos.
int cont: número de caracteres no blancos de la cadena.
       1
Los atributos prim, ult y cont son variables que mantienen información acerca del estado de la cadena, información que resulta útil para la implementación de los métodos que se aplican a la cadena.
El primer método que se encuentra en el código, el método constructor de la clase, es:
     /** Crea una Cadena con la misma secuencia de caracteres que s. */
     public Cadena(String s)
El método crea el objeto con un array de longitud s.length(), en el que dispone los consecutivos caracteres de s. Al crear el objeto se aprovecha que hay que volcar los caracteres del String en el array para contar el número de caracteres no blancos que aparecen, y se guarda en el atributo cont; con ello ya no es preciso contarlos, recorriendo el array a, cada vez que se requiera conocer ese dato. También registra en los atributos prim y ult en qué posición aparece el primer y el último carácter diferente de ’ ’, respectivamente.
Por ejemplo, en la figura 1 se muestra el objeto resultante de crear una Cadena a partir del String" Ja v a ".
Notar que la creación de una Cadena a partir de un String "" o cuyos caracteres son todos iguales a ’ ’, deja el atributo cont a 0 y los atributos ult < prim (rango prim .. ult vacío).
Figura 1: Objeto de la clase Cadena.
La clase posee además métodos para consultar la longitud total de una cadena, consultar el número de caracteres no blancos, consultar el carácter que ocupa una determinada posición, de 0 en adelante, y comprobar la coincidencia entre dos cadenas. También posee métodos para modificar la cadena: cambiar las apariciones de un determinado carácter por blancos, y recortarla para eliminar todos sus caracteres blancos.
Algunos de estos métodos ya se encuentran implementados en la clase que se deja como material, pero para tres ellos hay que completar su implementación en este entregable.
Trabajo a realizar
1. (15 puntos) Completar el código del siguiente método:
/** Cambia los caracteres de this iguales a c por blancos. */
         public void filtrar(char c)
El método deberá cambiar por ’ ’ las componentes del array this.a que sean iguales a c. Deberá actualizar el resto de atributos de this. En la figura 2 de la última página se muestra un ejemplo del resultado del método.
 2

2. (25 puntos) Completar el código del siguiente método:
    /** Elimina de this los espacios en blanco.
     */
     public void recortar()
El método deberá cambiar this.a por un nuevo array, del tamaño justo y necesario, en el que se hayan copiado los caracteres diferentes de ’ ’ de la cadena, en el mismo orden, y actualizar los otros atributos de this.
Se deberá recorrer únicamente la parte del array this.a que contiene los caracteres que no son blancos.
En la figura 3 se muestra un ejemplo del resultado del método. 3. (25 puntos) Completar el código del siguiente método:
     /** Comprueba que this y c coinciden carácter a carácter, salvo blancos.
      *  Devuelve true si coinciden, y false en caso contrario.
      */
     public boolean coinciden(Cadena c)
El método deberá seguir el siguiente análisis por casos. Si el número de caracteres no blancos de this y de c es diferente, entonces el método debe devolver false. En caso contrario, deberá buscar en this.a y en c.a, una pareja de caracteres diferentes que ocupen la misma posición, salvo blancos, en ambas secuencias de caracteres. El método devolverá false o true según se encuentre o no dicha discrepancia.
La búsqueda en this.a y en c.a se deberá restringir al rango de índices prim..ult de cada cadena.
En la figura 4 se muestran algunos ejemplos.
3

 Figura 2: Estado de la Cadena de la figura 1 después de aplicarle el método filtrar, con c = ’a’.
Figura 3: Estado de la Cadena de la figura 2 después de aplicarle del método recortar.
Figura 4: La Cadena a) coincide con la Cadena de la figura 1; la b) no coincide con ninguna de las anteriores.
  4

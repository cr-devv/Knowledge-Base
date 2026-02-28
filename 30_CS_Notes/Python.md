
## 1. Entrada y Salida de Datos
* `print()`: Imprime información o mensajes en la consola.
* `input()`: Pide al usuario que ingrese datos por consola.
* `+` (en strings): Concatena o une cadenas de texto directamente dentro de un print o variable.

## 2. Tipos de Datos y Conversiones (Casting)
* `type(variable)`: Devuelve el tipo de dato que contiene una variable (por ejemplo, `<class 'int'>`).
* `int()`: Convierte un valor a un número entero; si es un número decimal, simplemente elimina la parte decimal.
* `float()`: Convierte un valor a un número con decimales.
* *Nota importante*: Python arrojará un error si intentas concatenar texto (`strings`) directamente con números (`integers`) sin convertirlos previamente.

## 3. Operaciones Matemáticas
* `+`, `-`, `*`, `/`: Realizan suma, resta, multiplicación y división básica.
* `//` (División al piso): Realiza la división y devuelve únicamente el número entero resultante.
* `%` (Módulo): Devuelve el resto de una división.
* `**` (Exponente): Eleva un número a la potencia indicada.
* `**0.5`: Calcula la raíz cuadrada de un número.
* `round(numero, decimales)`: Redondea un número a la cantidad de posiciones decimales que se le especifique.

## 4. Strings (Cadenas de Texto)
* `f"{variable}"` (F-Strings): Permite insertar variables directamente dentro de un texto anteponiendo una `f` a las comillas.
* `"""texto"""`: Crea strings de múltiples líneas.
* `[inicio:fin:paso]` (Slicing): Extrae fragmentos específicos de un texto. Usar `[::-1]` invierte el texto completo.
* `.upper()`: Transforma todo el texto a mayúsculas.
* `.lower()`: Transforma todo el texto a minúsculas.
* `.split("separador")`: Divide el string basándose en el separador indicado y devuelve una lista con las partes.
* `"separador".join(lista)`: Une los distintos elementos de una lista utilizando el separador definido.
* `.replace("viejo", "nuevo")`: Busca un fragmento (substring) y lo reemplaza por otro.
* `.index()`: Encuentra la posición de un carácter, pero lanza un error (`ValueError`) si no lo encuentra.
* `.rindex()`: Funciona igual que index, pero busca la última aparición de la palabra o carácter (desde la derecha).
* `.find()`: Busca un substring, pero si no lo encuentra devuelve `-1` en lugar de romper el programa con un error.

## 5. Listas
* `[ ]`: Define una lista agrupando elementos.
* `len(lista)`: Devuelve la cantidad total de elementos que posee la lista (también sirve para contar caracteres en strings).
* `+` (en listas): Concatena o une dos listas en una sola.
* `lista[índice] = "nuevo"`: Modifica un elemento específico accediendo a su posición.
* `.append(elemento)`: Añade un nuevo elemento al final de la lista existente.
* `.pop(índice)`: Elimina el elemento ubicado en el índice especificado y devuelve ese valor.
* `.sort()`: Reordena los elementos de la lista, por ejemplo, en orden alfabético.

## 6. Operadores de Pertenencia
* `in`: Comprueba si un elemento existe dentro de una colección o string y devuelve `True` si lo encuentra.
* `not in`: Realiza la comprobación inversa, devolviendo `True` únicamente si el elemento NO está presente.

## 7. Comandos Básicos de Git
* `git status`: Muestra en rojo o verde qué archivos han sido modificados (ideal para revisar antes de guardar).
* `git add .`: Prepara todos los archivos nuevos o modificados en tu carpeta actual para ser guardados.
* `git commit -m "mensaje"`: Toma una "foto" de los cambios preparados y los guarda en tu historial local con una descripción.
* `git commit --amend --no-edit`: Agrega archivos olvidados al último commit sin cambiar el mensaje original (solo usar antes del push).
* `git push`: Sube tus commits locales hacia tu repositorio remoto en GitHub para respaldarlos.
## 8. Diccionarios
* `{}`: Define un diccionario agrupando elementos en pares de `"clave": valor`. 
* `diccionario["clave"]`: Accede directamente al valor asociado a esa clave específica.
* `diccionario["nueva_clave"] = valor`: Agrega un nuevo par clave-valor al diccionario, o sobreescribe el valor si la clave ya existe.
* `.get("clave")`: Busca el valor de una clave de forma segura. Si la clave no existe, devuelve `None` en lugar de romper el programa con un error.
* `.update({"clave": valor})`: Modifica valores existentes y/o agrega nuevos pares clave-valor todos de golpe.
* `.keys()`: Devuelve una vista con todas las claves (los nombres) que existen en el diccionario.
* `.values()`: Devuelve una vista con todos los valores (los datos) que contiene el diccionario.
* `.items()`: Devuelve todos los pares de clave-valor agrupados (muy útil para recorrerlos más adelante).
* `.pop("clave")`: Elimina la clave especificada del diccionario y te devuelve el valor que contenía.
* `in` (en diccionarios): Comprueba si una **clave** específica existe dentro del diccionario (ojo: busca en las claves, no en los valores).
## 9. Tuples 
* `()`: Se definen agrupando elementos entre paréntesis. 
* **Inmutables:** A diferencia de las listas, una vez creada una tupla, **no puedes** modificar, añadir ni eliminar sus elementos.
* Ocupan menos espacio en memoria y son más rápidas de procesar que las listas (ideales para datos que no deben cambiar, como coordenadas o configuraciones).
* Puedes extraer sus valores a variables individuales rápidamente: `a, b = (1, 2)`.
* **Métodos principales (solo tiene dos):**
    * `.count(elemento)`: Cuenta cuántas veces aparece un elemento específico en la tupla.
    * `.index(elemento)`: Devuelve la posición (índice) de la primera aparición del elemento.

## 10. Sets (Conjuntos)
* `set()` o `{}`: Se definen usando la función `set()` (si está vacío) o agrupando elementos entre llaves (ojo: si tiene formato `"clave": valor`, es un diccionario; si solo son valores, es un set).
* **Elementos únicos:** Los sets eliminan automáticamente cualquier elemento duplicado.
* **Desordenados:** No tienen un orden fijo. No puedes acceder a sus elementos usando índices (`mi_set[0]` arrojará error).
* **Métodos principales:**
    * `.add(elemento)`: Agrega un elemento al set.
    * `.remove(elemento)`: Elimina un elemento (arroja error si el elemento no existe).
    * `.discard(elemento)`: Elimina un elemento (pero si no existe, simplemente no hace nada y el programa sigue).
    * `.clear()`: Vacía el set por completo.
    * `.union(otro_set)` o `|`: Une dos sets (recordando que ignorará los repetidos).
    * `.intersection(otro_set)` o `&`: Devuelve un nuevo set solo con los elementos que ambos conjuntos tienen en común.

## 11. Booleanos y Comparaciones
* `True` / `False`: Los dos valores booleanos de Python (siempre deben escribirse con la primera letra en mayúscula).
* **Operadores de Comparación (Devuelven un booleano):**
	* `"=="` ¿Es igual a? 
    * `!=`: Diferente de.
    * `>`, `<`: Mayor que, Menor que.
    * `>=`, `<=`: Mayor o igual que, Menor o igual que.
* **Operadores Lógicos:**
    * `and`: Devuelve `True` solo si **todas** las condiciones son verdaderas.
    * `or`: Devuelve `True` si **al menos una** condición es verdadera.
    * `not`: Invierte el valor booleano (si es `True` lo vuelve `False`, y viceversa).
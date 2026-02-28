## Nivel 0

**Objetivo: Conectarse al servidor mediante ssh

Host: bandit.labs.overthewire.org

Puerto: 2220

Usuario: bandit0

Contraseña: bandit 0 

```ssh bandit0@bandit.labs.overthewire.org -p 2220```

### ¿Qué es SSH?
**SSH (Secure Shell)** es un protocolo criptográfico para operar servicios de red de forma segura sobre una red insegura.

**Sintaxis básica:**
`ssh usuario@host -p puerto`

* **Encriptación:** A diferencia de su predecesor (Telnet), SSH encripta la conexión, evitando que atacantes vean contraseñas o datos ("Man-in-the-Middle").
* **Cliente/Servidor:** Tu PC actúa como cliente y se conecta al servidor remoto.
* **Flags comunes:**
    * `-p`: Especifica un puerto (si no es el estándar 22).
    * `-i`: Especifica un archivo de llave privada (para no usar contraseña).

## Nivel 1

**Objetivo: La contraseña para el siguiente nivel está guardada en un archivo Readme

``ls``
``cat``

Aprendizaje:
* ls: lista los archivos en el directorio actual
* cat: Imprime el contenido de un archivo en la terminal

<details>
  <summary>Contraseña</summary>
  
  `bandit1: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
</details>

## Nivel 2
**Objetivo:** La contraseña está en un archivo llamado `-` (guion).

`ls`  `cat ./- `

aprendizaje: 
- El guion `-` es un carácter especial en Linux (a veces significa "entrada estándar").
- Para leer un archivo que se llama así, debemos especificar la ruta completa `./` (directorio actual) para que el comando no se confunda.

<details>
  <summary>Contraseña</summary>
  
  `bandit2: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
</details>

## Nivel 3

**Objetivo: la contraseña está en un archivo llamado "--spaces in this filename--"

`ls` `cat "./-- spaces in this filename--"`

aprendizaje: Si un archivo tiene espacios, la terminal piensa que son comandos distintos, usamos "" para decirle que es solo un archivo completo

<details>
  <summary>Contraseña</summary>
  
  `bandit3: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
</details>

## Nivel 4

**Objetivo: Encontrar la contraseña en un dotfile (archivo oculto)

`ls` `cd inhere` `ls -a` `cat Hiding-From-You` 

aprendizaje: El flag "-a" muestra los archivos ocultos, (los que empiezan con un **.** ), además, el flag "-l" Muestra una lista detallada, pudiendo ejecutarse
**ls -la** 

<details>
  <summary>Contraseña</summary>
  
  `bandit4: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
</details>



## Nivel 5

**Objetivo**: Buscar la contraseña en un único directorio "Human readable"

`ls` `cd inhere` `file ./*` `cat ./-file07` 

Aprendizaje: el comando **file** escanea el interior de un archivo y me dice exactamente que tipo de datos contiene, ya sea imagen, archivo comprimido, datos ilegibles o texto normal 

<details>
  <summary>Contraseña</summary>
  
  `bandit5: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
</details>

## Nivel 6

**Objetivo**: Encontrar la contraseña en un archivo con las propiedades: Human readable, 1033 bytes de peso, not executable

`ls` `cd inhere` `find . -type f -size 1033c ! -executable` `cd maybehere07` `ls -a` `cat ./.file2` 

Aprendizaje:  
`find`: Llama al programa de búsqueda.    

`.` **(Punto):** Le indica a `find` _dónde_ empezar a buscar. El punto significa "en el directorio actual y todo lo que haya dentro de él".

`-type f`: Filtra por tipo. La `f` significa _file_ (archivo normal). (Nota: si usaras `d`, buscaría _directories_ o carpetas).

`-size 1033c`: Filtra por el tamaño exacto del archivo. El número es el tamaño, y la `c` significa _bytes_ (viene de la palabra _character_, ya que en ASCII un carácter ocupa exactamente 1 byte).

`! -executable`: El signo de exclamación `!` es un operador lógico que en programación significa "NO" (negación). Por sí solo, `-executable` busca archivos que sean programas o scripts. Al ponerle el `!`, le decimos al sistema que busque archivos que **no** se puedan ejecutar (como un simple archivo de texto).

<details>
  <summary>Contraseña</summary>
  
  `bandit5: WasnPhtq9AVKe0dmk45nxy20cvUa6EG
</details>
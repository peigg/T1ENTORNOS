# Ejecuta el programa "Hola mundo" en los siguientes lenguajes:

## bash
1. Creamos un fichero llamado script.sh en la terminal bash:
~~~~
cat > script.sh
~~~~
2. Con el siguiente contenido
~~~~
#!/bin/bash
echo Hola Mundo!
~~~~
3. Después, ejecutamos bash script.sh, y ya tenemos el print Hola Mundo!
 
---  

## Python

1. Ejecutamos el intérprete.  
~~~
python
~~~

2. Escribimos las sentencias y luego pulsamos INTRO.
~~~
python
print "Hola Mundo"
~~~

3. Para salir del intérprete pulsamos CTRL+D.  


### Script ejecutable

1. Creamos archivo __hola.py__

~~~
python
#!/usr/bin/env python
print "Hola mundo"
~~~


2. Damos permisos de ejecución

~~~
bash
chmod  +x  hola.py
~~~

3. Ejecutamos

```bash
./hola.py
```

--- 

## PHP

1. Ejecutamos el intérprete.  

~~~
php -a
~~~

2. Escribimos las sentencias.

~~~
echo "Hola mundo\n";
~~~

3. Para salir del intérprete pulsamos CTRL+D.   


### Script ejecutable

1. Editamos archivo __hola.php__

```php
#!/usr/bin/env php

<?php 
  echo "Hola mundo\n" 
?>
```

2. Damos permisos de ejecución

```bash
chmod  +x  hola.php
```

3. Ejecutamos

```bash
./hola.php
```

--- 

## Javascript (nodejs)

### Pasos

1. Ejecutamos el intérprete.  

```bash
node
```

2. Escribimos las sentencias y luego pulsamos INTRO.

```javascript
console.log('Hola mundo');
```

3. Para salir del intérprete pulsamos CTRL+D.  


### Script ejecutable

1. Editamos archivo __hola.js__

```javascript
#!/usr/bin/env node

console.log('Hola mundo');
```


2. Damos permisos de ejecución

```bash
chmod  +x  hola.js
```

3. Ejecutamos

```bash
./hola.js
```

---

## C

### Pasos 

1. Editamos archivo __hola.c__

```c 
#include <stdio.h>

int main()
{
    printf("¡Hola, mundo!");
    return 0;
}
```

2. Compilamos y enlazamos

```bash
gcc  -o  hola  hola.c      # Compilamos y enlazamos
```

3. Ejecutamos

```bash
./hola                     # Ejecutamos
```
--- 

## C++

### Pasos 

1. Editamos archivo __hola.cpp__

```cpp
#include <iostream>

using namespace std;

int main()
{
   cout << "¡Hola, mundo!" << endl;
   return 0;
}
```

2. Compilamos y enlazamos

```bash
g++  -o  hola  hola.cpp    # Compilamos y enlazamos
```

3. Ejecutamos

```bash
./hola                     # Ejecutamos
```

--- 

## Java

### Pasos

1. Editamos archivo __Hola.java__

```java
class Hola
{
    public static void main(String[] args)
    {
        System.out.println("Hola Mundo");
    }
}
```

2. Compilamos

```bash
javac  Hola.java      # Compilamos
```

3. Interpretamos y ejecutamos

```bash
java  Hola            # Interpretamos y ejecutamos
```

### _Script ejecutable_

> Realmente no es un script, sino __bytecode empaquetado en JAR__ e interpretado por la JVM (Java Virtual Machine).

1. Empaquetamos

```bash
jar  cvfe  hola.jar  Hola  Hola.class  # Empaquetamos  
```

> NOTA: 
>
> Las opciones utilizadas en el comando jar son:
> 
> ```
> c: Create      (Crear archivo jar)
> v: Verbose     (Mostrar información)
> f: File        (Nombre de archivo jar, en este caso hola.jar)
> e: Entry point (Punto de entrada, en este caso la clase Hola)
> ```
> 
> Los argumentos utilizados son:
> 
> ```
> hola.jar:    (opción f anterior) Archivo .jar resultante.
> Hola:        (opción e anterior) Clase que contiene el método main (es decir el punto de entrada)
> Hola.class:  Archivos de bytecode a incluir en hola.jar. Pueden ser varios archivos.
> ```
>
> Los argumentos deben seguir el mismo orden que las opciones. En este caso indicamos primero el nombre del archivo .jar y luego la clase que contiene el método main.


> **NOTA IMPORTANTE: La FORMA HABITUAL de ejecutar un archivo .jar es invocando al intéprete java, es decir la siguiente:**
>
> ```bash
> java  -jar   hola.jar
>```
>
> **Los pasos 2 y 3 siguientes no es la forma habitual de ejecutar un archivo .jar, 
> pero se indican para mostrar su similitud respecto al método usado para otros lenguajes interpretados**.


2. Damos permiso de ejecución

```bash
chmod  +x  hola.jar                    # Damos permiso de ejecución
```

3. Ejecutamos

```bash
./hola.jar                             # Ejecutamos
```

## Ensamblador (nasm)

1. Creamos archivo __hola.asm__

```nasm
 section .data
 
 msg     db "¡Hola Mundo!", 0Ah
 len     equ     $ - msg  
 
 section .text
 
 global _start
 
 _start:
        mov     eax, 04h
        mov     ebx, 01h
        mov     ecx, msg
        mov     edx, len
        int     80h
        mov     eax, 01h
        mov     ebx, 00h
        int     80h
```

2. Ensamblamos y enlazamos

```bash
nasm  -f  elf64  hola.asm        # Ensamblado para ELF64
ld  hola.o  -o  hola             # Enlazado y generación de ejecutable
```

3. Ejecutamos

```bash
./hola                           # Ejecución
```
--- 

## Ruby

### Pasos

1. Ejecutamos el intérprete.  

```bash
ruby
```

2. Escribimos las sentencias y luego pulsamos INTRO.

```ruby
puts "Hola Mundo"
```

3. Para salir del intérprete pulsamos CTRL+D.  


### Script ejecutable

1. Editamos archivo __hola.rb__

```ruby
#!/usr/bin/env ruby

puts "Hola Mundo"
```


2. Damos permisos de ejecución

```bash
chmod  +x  hola.rb
```

3. Ejecutamos

```bash
./hola.rb
```

--- 

## Go

### Pasos

1. Editamos archivo __hola.go__ 

```go
package main

import "fmt"

func main() {
        fmt.Println("Hola mundo desde Go")
}
```

2. Compilamos y enlazamos

```bash
go  build  hola.go   # Compilamos y enlazamos
```

3. Ejecutamos

```bash
./ hola              # Ejecutamos
```

4. Si lo deseamos,en Go también es posible interpretar el código

```bash
go  run  hola.go     # Interpretamos y ejecutamos
```

--- 

## Rust

### Pasos

1. Editamos archivo __hola.rs__

```rust
fn main() {
    println!("¡Hola, mundo! Desde RUST ");
}
```

2. Compilamos y enlazamos

```bash
rustc  hola.rs              # Compilamos y enlazamos
```

3. Ejecutamos

```bash
./hola                      # Ejecutamos
```

---

## Lisp

### Pasos

1. Ejecutamos el intérprete.  

```bash
clisp
```

2. Escribimos las sentencias y luego pulsamos INTRO.

```lisp
(format t "¡Hola, mundo!")
```

3. Para salir del intérprete pulsamos CTRL+D.  


### Script ejecutable

1. creamos archivo __hola.lisp__

~~~
lisp
#!/usr/bin/env clisp
(format t "¡Hola, mundo!")
~~~


2. Damos permisos de ejecución

~~~
bash
chmod  +x  hola.lisp
~~~

3. Ejecutamos

~~~~
bash
./hola.lisp

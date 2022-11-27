# Bibliotecas. Define qué se entiende por biblioteca o librería y los tipos que existen.
## Una librería de programación es un conjunto de implementaciones codificadas (Archivos o ficheros) por medio de un lenguaje de programación (Phyton, Java Script) que ofrece una interfaz bien definida según la funcionalidad para la que fue diseñada. Para entenderlo bien, puede decirse que se trata de un conjunto de instrucciones que pueden ser utilizadas por diferentes programas. La misma librería, en teoría, es usada en varios programas, dándole el mismo uso o uno diferente.
## Existen diferentes tipos de bibliotecas, a continuación, te explico algunas.
~~~
Bibliotecas estáticas: es un fichero que contiene varios archivos de código objeto en su interior que se utilizan en los ficheros ejecutables, copiándolos y relocalizando según la necesidad. En este caso la biblioteca actúa como recipiente de archivos.

Se graban en programas como los ejecutables y sirven exclusivamente para esto, posteriormente se pueden borrar sin ningún problema porque el programa está funcionando con la función adecuada.

En pocas palabras, una biblioteca estática es aquella que está conformada por archivos de código objeto y su utilizan en los programas por medio de un proceso de enlazado, donde se pasan los archivos para que este se ejecute y posteriormente se puedan borrar. 
~~~~
~~~

Bibliotecas dinámicas: son archivos que tienen código objeto que se construyeron de manera independiente a su ubicación. Esto nos indica que este tipo de bibliotecas se utilizan cargando los archivos en el tiempo de ejecución y no se enlazan en el tiempo de compilación; de forma que aqui radica su diferencia respecto a las estáticas, que se enlazan.

Son aquellas que guardan archivos que se construyeron independientes a su ubicación y cargamos los archivos cuando el programa se esté ejecutando.
~~~~
~~~

Bibliotecas remotas: Esta es una biblioteca que utiliza ejecutables separados y por medio de un procedimiento remoto, llevado a cabo por otra computadora. Estas bibliotecas trabajan con un enfoque que maximiza la reutilización del sistema operativo; el código que soporta la biblioteca es el que le da a la aplicación el soporte y seguridad para otro programa.

Si bien este tipo de bibliotecas no requieren información grabada en la máquina, son más caras que los dos tipos anteriores.
~~~

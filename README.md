# Laboratorio-Segundo-Parcial- Creaccion de archivos .txt
    Integrantes: Quilumbaquín Lenin
                 Robalino Johanna
                 Jiménez Iván
                 Vallejo Keily
                 Mosquera William 
    NRC: 3725
    Carrera: Electrónica y Automatización
    Asignatura: Programación Orientada a Objetos 
    Docente: Ing. Cesar Osorio
    Tema: Persistencia de Datos en JAVA
    
   **OBJETIVOS.-**
   
* Analizar el significado de creación y lectura de archivos planos en JAVA para con ello desarrollar el programa propuesto, mediante la aplicación de conocimientos previos sobre el tema.
* Desarrollar un programa que permite grabar un archivo de texto, el cálculo de la edad que tiene cada empleado de una empresa a partir de su fecha de
nacimiento.
* Realizar el trabajo de una forma colaborativa compartiendo nuestros conocimientos para el adecuado desarrollo del programa propuesto..

**MARCO TEÓRICO.-**

**Definición**

Un fichero de texto o archivo es aquel que está formado por una secuencia de caracteres los cuales están organizados en líneas de igual o diferente longitud. Cada uno de los datos, que se encuentran en estos ficheros, están formados por caracteres.

**Manejo de archivos en Java**

En el momento en que creamos cada uno de los programas todos los datos solamente existían durante la ejecución de los mismos, es decir, cada vez que salíamos del programa todo aquello que habíamos desarrollado se perdía. También cada programador en sus inicios no se preocupa en tratar de guardar los datos que se hayan generado en algún lugar que permitiera recuperarlos u observarlos desde otros programas. Es por esto que saber como realizar la creación, lectura y escritura de ficheros de texto en Java es tan útil al momento de programar.

**Tratamiento de errores: las excepciones**

Las excepciones no son más que errores los cuales impiden el correcto funcionamiento del programa. Muchas excepciones que existen en Java son son excepciones en tiempo de ejecución un ejemplo de ello es la división para cero.
Otro tipo de excepciones que existe en Java son las comprobadas, estas hacen que el programador dentro del código de algún método invoque una instrucción que pueda lanzar a dos opciones las cuales son:
 Atrapar dicha excepción, usando un bloque try catch o declarar en la cabecera el método que dicho método puede lanzar excepción usando una declaración throws.
 
**Tratamiento simplificado de excepciones**

Una forma simplificada de las excepciones es la siguiente estructura:

	try { 
	"Codigo"que"abre"y"trata"el"fichero 
	} catch (IOExcepction ex) { 
	 "Código"que"trata"el"error 
	}

Como podemos observar esta estructura intenta (try) ejecutar las instrucciones desarrolladas, pero en caso de producirse un error en el tratamiento de los ficheros se lanza una IOExcepction, la cual atrapa (catch) ese error y ejecuta el código de corrección. 

**Operaciones con ficheros de texto en Java**

	Apertura: El programa abre el fichero y se prepara para leerlo o escribirlo. Suele “reservar” el fichero para sí. 

	Cierre: Indica que se ha finalizado con las operaciones sobre el fichero. Libera el fichero.

	Lectura: Lee el fichero o una de sus partes.

	Escritura: Permite escribir en el fichero, ya sea añadiendo datos o sobrescribiendo los ya existentes. 

	Ejecución: Similar a la lectura, pero utiliza los datos del fichero para ejecutar un software. 

	Creación: Crea un nuevo fichero con un nombre, extensión y ruta determinados.

	Eliminación: Elimina un fichero determinado

**Creación y cierre de ficheros de texto en Java**

Cuando se realiza la apertura de un fichero en Java, se reserva el fichero para operar con él, además se establece un flujo de datos desde el fichero a una variable en Java que representa al fichero. A partir de esa variable se pueden realizar todas las operaciones sobre el fichero que se desee y cuando se quiera dejar de usar el fichero se debe cerrar el mismo cortando el flujo de datos y liberando la variable

**Lectura de Ficheros de texto en Java**

Para leer un fichero de texto se pueden utilizar dos clases las cuales son:

     FileReader y BufferedReader.
 
La clase FileReader permite tener acceso al fichero en modo lectura y para crear objetos FileReader podemos utilizar los constructores siguientes:

    FileReader(String ruta)

    FileReader(File objetoFile);

En ambos casos se lanza una excepción FileNotFoundException en el caso de que el fichero no exista. 

La clase FileReader proporciona el método read( ) para la lectura de caracteres del fichero. Además, tiene una serie de métodos para leer carácter a carácter, donde el constructor del FileReader recibe el objeto File.

    FileReader reader = new FileReader(fichero);

Para leer utilizando la clase BufferedReader se debe crear un objeto BufferedReader a partir de un objeto FileReader. Esta clase crea un búfer a través del FileReader, lo cual permite Leer más de un carácter donde el constructor recibe el FileReader como parámetro.

    BufferedReader buffer = new BufferedReader (reader);

**Escritura de ficheros de texto en Java**

Para escribir en un fichero de texto se utilizan dos clases las cuales son FileWriter y PrintWriter. Mediante la clase FileWriter se puede tener acceso al fichero en modo de escritura.

Para la creación de objetos FileWriter podemos utilizar los constructores:

    FileWriter(String path)

    FileWriter(File objetoFile);

Mediante esto el fichero se crea y, si ya existe, su contenido se pierde. Para evitar que se pierda su contenido y abrir un fichero de texto podemos utilizar los siguientes constructores: 

    FileWriter(String path, boolean append)

    FileWriter(File objetoFile, boolean append) 

Así podemos observar que, si el parámetro append es True los datos se van a añadir a los existentes, por el contrario, si el parámetro append es False los datos existentes se pierden.

La clase PrintWriter permite escribir caracteres en el fichero de la misma forma que en la pantalla. Un objeto PrintWriter se crea a partir de un objeto FileWriter.
Ejemplo:

    FileWriter fw = new FileWriter("c:/ficheros/datos.txt");

    PrintWriter salida = new PrintWriter(fw);


Para crear un objeto PrintWriter directamente de un objeto FileWriter se lo hace mediante la siguiente manera:

	salida = new PrintWriter("c:/ficheros/datos.txt");

De esta manera, si el fichero no existe, se crea. una vez creado el objeto podemos utilizar print( ), println( ) y printf( )  para escribir en el fichero como si fuese a escribirse lo que se muestra en pantalla.
El método flush( ) hace que se escriban en el fichero los datos que puedan haber en el buffer de salida y el método close( ) cierra la conexión con el fichero y libera los recursos que está usando la conexión.


#### Capturas de pantalla de compilacion del programa y creacion de archivos .txt

* Creacion del programa principal 

Programa que permita grabar en un archivo de texto el cálculo de la edad que tiene cada empleado de una empresa a partir de su fecha de
nacimiento.

![image](https://user-images.githubusercontent.com/84789076/124529697-be441100-ddd0-11eb-9fda-97dd77e91482.png)

![image](https://user-images.githubusercontent.com/84789076/124529732-cbf99680-ddd0-11eb-98b6-f8e7567e1a59.png)

* Compilaciones 

![image](https://user-images.githubusercontent.com/84789076/124529765-d87def00-ddd0-11eb-99b8-f8db422126c2.png)

![image](https://user-images.githubusercontent.com/84789076/124529834-ee8baf80-ddd0-11eb-8d1d-b1d220094819.png)

* Carpeta donde se guardo la creacion del archivo .txt

![image](https://user-images.githubusercontent.com/84789076/124529900-19760380-ddd1-11eb-8d3a-3b5b8b685dd1.png)

* Muestra de datos ya en documento .txt guardados y compilados

![image](https://user-images.githubusercontent.com/84789076/124529954-36aad200-ddd1-11eb-8c81-c7bda2e60cce.png)

**CONCLUSIONES.-**

* En conclusión podemos decir que la entrada/salida de archivos de caracteres pueden crearse y visualizarse haciendo uso de un editor de texto. Las clases que se usaron en el tratamiento del archivo fue java.io. y el tratamiento de excepciones las cuales permiten atrapar las diferentes situaciones irregulares. 

* Según la ejecución del programa, lee por teclado el año y nombre de los n empleados utilizando el método BufferedReader y BufferedWriter guarda el String de caracteres  en un archivo llamado empleados.txt. 

* La implementación de los métodos se la debe tratar como excepciones de tipo IOException ya que al ingresar por error un tipo de dato diferente se genera una excepción.

**RECOMENDACIONES.-**

* Una de las recomendaciones más indispensables para poder crear y manejar los archivos (.txt) en java es tener el conocimiento necesario de cada uno de las clases como lo son file, filewriter, etc., para de esta manera poder aplicarlos de una manera correcta sin que se nos presente un error de sintaxis o un error al ejecutar el programa.

* Conocer y poner en práctica todo lo aprendido en clases para poder crear un programa que contenga archivos tx, y si de ser necesario consultar en lugares de internet recomendados para tener  mayor conocimiento y capacidad al ejecutar estos archivos.

**REFERENCIAS**

* Creacion de txt con scanner en Java. (17 de Octubre de 2017). Obtenido de https://es.stackoverflow.com/questions/97144/creaci%c3%b3n-de-txt-con-scanner-en-java

* JAVA-Crear archivos de texto. (1 de Agosto de 2019). Obtenido de https://decodigo.com/java-crear-archivos-de-texto#:~:text=Crear%20archivos%20de%20texto%20usando.%20FileWriter.%20y.%20BufferWriter.,segunda%20forma%20es%20usando%20PrintWriter%20que%20te%20









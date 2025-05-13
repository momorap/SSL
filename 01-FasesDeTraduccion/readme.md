# Trabajo 1 (Solo para Practica PERSONAL)
- PUNTO 1
    - 1A
    > se utiliza el comando de la siguiente manera ```gcc -E hello2.c -o hello2.i```
    - 1B
    > Las conclusiones que se pueden sacar es que el preprocesador pego el archivo header del include con los prototipos en el archivo. Rempazo el comentario por un solo espacio. No reemplazo los escaper no se porque
    - 1D
    > int printf(const char * restrict s, ...);
    >int main(void){
    >int i=42;
    >prontf("La respuesta es %d\n");
    > ```int printf(const char * restrict s, ...);``` semanticamente se declara una funcion llamada print que devuelve un numero entero y recibe una cantidad de parametros variable por ```...```. ```const``` significa que no se puede modificar, ```char``` es que va a ser algo del tipo caracter ```*``` va a ser un puntero
    - 1E
    > La unica diferencia que pude encontrar es que tiene los siguientes # el .i 
- PUNTO 2
    - 2A 
    > se utiliza el siguiente comando para compilar ``` gcc -S hello3.i -o hello3.s```
    - 2b
    > arrojó un error sintactico 
    ``` bash
 
    hello3.c:4:32: error: expected '}' 
    4 | prontf("La respuesta es %d\n"); 

    ```
    
   > y uno semantico 
   ``` bash
   hello3.c:4:1: error: call to undeclared function 'prontf'; ISO C99 and later do not support implicit function declarations [-Wimplicit-function-declaration] 
   4 | prontf("La respuesta es %d\n"); 
   ```
    - 2C
    > El objetivo del codigo es llamar a printf; primero guarda espacio en memoria, luego inicializa las variable, llama a la funcion printf y luego realiza el retorno
    - 2D
    > Se utiliza el comando ``` gcc -c hello4.s -o hello4.o ```
- PUNTO 3 
    - 3A
    > Se utiliza el comando ```gcc hello4.o -o hello4```
    - 3B
    > No fue necesario corregir nada ya que dejo vincular
    - 3C
    > en vez de arrojar el i , el programa mostro un numero negativo;
- PUNTO 6
    - 6B
        - I) Al compilar arroja el siguiente error 
         ```bash
          error: call to undeclared library function 'printf' with type 'int (const char *, ...)'; ISO C99 and later do not support implicit function declarations [-Wimplicit-function-declaration] 
          3 |     printf("La respuesta es %d\n", i); 
        ```
        - II) Un prototipo de una funcion es  una declaracion que especifica la interfaz de una funcion, incluyendo su nombre, tipo de retorno y parametros. El prototipo de una funcion se utiliza para informal al compilador sobre la existencia de la funcion y su firma, lo que permite al compilador realizar comprobaciones de tipo y sintaxis.
            Las formas de generarlos son por declaracion explicita, encabezados, declaracion implicita y herramientas
        - III) La declaracion implicita es cuando el compilador asume la existencia de una funcion  sin que se haya proporcionaso un prototipo explicito
        - IV) Segun el estandar C11 la declaracion implicita esta obsoleta y no se recomienda su uso
        - V) Dependiendo la version de gcc emite un warning o un error y en clang emite un error
        - VI) Las funciones buitlt-in son funciones proporcionadas por el compilador que pueden mejorar el rendimiento y simplificar el enlace del cogigo. Sin embargo, tiene limitacones y posibles problemas de portabilidad

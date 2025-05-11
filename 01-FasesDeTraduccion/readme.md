#Trabajo 1 (Solo para Practica PERSONAL)
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
Al principio del código fuente se ha implementado un lector de ficheros de texto que sirve para facilitar la creación de nuevos circuitos digitales.
Para poder ser leído correctamente el fichero de texto tiene que encontrarse en la misma ubicación que el código fuente y tiene seguir un determinado formato. En cada fila del fichero se debe escribir los datos relevantes de una puerta del circuito a crear. En concreto, se debe especificar el tipo de la puerta (NOT, AND, NAND, OR, NOR, XOR o XNOR) y los dos índices que referencian los elementos del circuito (otras puertas lógicas o bits de entrada) con los que la puerta está conectada mediante sus dos entradas. Si se desea que una determinada entrada esté desconectada, se debe poner -1. Los tres datos de cada puerta deben ir separados por coma.

Ejemplos:

AND,0,1
OR,0,1
OR,1,2
AND,3,4
NOT,4,-1
AND,4,5
OR,6,7
NAND,6,8
XOR,7,8 


A continuación se implementan los métodos: salida_Puerta(TipoPuerta, entrada1, entrada2) y salida_Circuito(Circuito, Entrada, Puertas_defectuosas, Conexiones_defectuosas). Después se ha proporcionado una plantilla para hacer pruebas sobre el circuito. Se hacen llamadas al método salida_Circuito y como parámetros de entrada se especifican el circuito, un vector de n bits (la entrada) y  si se desea, se pueden marcar ciertas puertas y/o conexiones como "defectuosas". Para marcar una puerta como "defectuosa" se debe introducir su índice en la lista Puertas_defectuosas. Para marcar una conexión como defectuosa" se debe introducir en la lista Conexiones_defectuosas el par de índices que referencian los elementos conectadados a sus dos extremos. El método salida_Circuito debe devolver la salida correspondiente a la entrada especificada.


En la siguiente parte del código fuente se implementan los métodos: construir_pares_referencia() y autodiagnostico(Circuito, Puertas_defectuosas, Conexiones_defectuosas). A continuación se han proporcionado dos plantillas para comprobar los dos métodos. El método construir_pares_referencia() no recibe ningún parámetro de entrada y debe devolver todas las posibles combinaciones de n bits y sus respectivas salidas. Estos pares entrada-salida representan el comportamiento correcto del circuito. En la siguiente plantilla se prueba el método autodiagnostico(Circuito, Puertas_defectuosas, Conexiones_defectuosas). Se hace llamada a dicho método y se especifican las listas de puertas dañadas y conexiones dañadas. El método calculará el impacto de los daños, es decir, cuántas discrepancias ocurren entre salida esperada y salida devuelta (para cada una de las posibles entradas).

La última parte del código fuente corresponde al algoritmo genético. Se implementan todas los métodos necesarios para que el algortimo funcione como se espera. Al final del código, aparece otra plantilla donde, una vez que ha terminado la ejecución del algoritmo genético, se muestran el circuito alternativo devuelto por el algoritmo y el porsentaje del rendimiento (si se ha podido realizar una reparación completa o no). 


Los ficheros de texto con los dos circuitos que se han usado para llevar a cabo los 4 experimentos se encuentran en la carpeta del código fuente (Circuito1.txt y Circuito2.txt). 

Para llevar a cabo más experimentos, es necesario definir el circuito que se va a usar. Para ello, se crea un fichero de texto especificando la estructura del circuito y se utiliza el lector implementado al principio del código para leerlo. A continuación se puede proceder directamente a la parte correspondiente al apartado 4. En este apartado se deben introducir las puertas y conexiones dañadas y después de debe ejecutar cada una de las partes del código en el mismo orden en el que aparecen. Al final se obtendrán los resultados. 

 
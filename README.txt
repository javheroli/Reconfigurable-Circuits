Al principio del c�digo fuente se ha implementado un lector de ficheros de texto que sirve para facilitar la creaci�n de nuevos circuitos digitales.
Para poder ser le�do correctamente el fichero de texto tiene que encontrarse en la misma ubicaci�n que el c�digo fuente y tiene seguir un determinado formato. En cada fila del fichero se debe escribir los datos relevantes de una puerta del circuito a crear. En concreto, se debe especificar el tipo de la puerta (NOT, AND, NAND, OR, NOR, XOR o XNOR) y los dos �ndices que referencian los elementos del circuito (otras puertas l�gicas o bits de entrada) con los que la puerta est� conectada mediante sus dos entradas. Si se desea que una determinada entrada est� desconectada, se debe poner -1. Los tres datos de cada puerta deben ir separados por coma.

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


A continuaci�n se implementan los m�todos: salida_Puerta(TipoPuerta, entrada1, entrada2) y salida_Circuito(Circuito, Entrada, Puertas_defectuosas, Conexiones_defectuosas). Despu�s se ha proporcionado una plantilla para hacer pruebas sobre el circuito. Se hacen llamadas al m�todo salida_Circuito y como par�metros de entrada se especifican el circuito, un vector de n bits (la entrada) y  si se desea, se pueden marcar ciertas puertas y/o conexiones como "defectuosas". Para marcar una puerta como "defectuosa" se debe introducir su �ndice en la lista Puertas_defectuosas. Para marcar una conexi�n como defectuosa" se debe introducir en la lista Conexiones_defectuosas el par de �ndices que referencian los elementos conectadados a sus dos extremos. El m�todo salida_Circuito debe devolver la salida correspondiente a la entrada especificada.


En la siguiente parte del c�digo fuente se implementan los m�todos: construir_pares_referencia() y autodiagnostico(Circuito, Puertas_defectuosas, Conexiones_defectuosas). A continuaci�n se han proporcionado dos plantillas para comprobar los dos m�todos. El m�todo construir_pares_referencia() no recibe ning�n par�metro de entrada y debe devolver todas las posibles combinaciones de n bits y sus respectivas salidas. Estos pares entrada-salida representan el comportamiento correcto del circuito. En la siguiente plantilla se prueba el m�todo autodiagnostico(Circuito, Puertas_defectuosas, Conexiones_defectuosas). Se hace llamada a dicho m�todo y se especifican las listas de puertas da�adas y conexiones da�adas. El m�todo calcular� el impacto de los da�os, es decir, cu�ntas discrepancias ocurren entre salida esperada y salida devuelta (para cada una de las posibles entradas).

La �ltima parte del c�digo fuente corresponde al algoritmo gen�tico. Se implementan todas los m�todos necesarios para que el algortimo funcione como se espera. Al final del c�digo, aparece otra plantilla donde, una vez que ha terminado la ejecuci�n del algoritmo gen�tico, se muestran el circuito alternativo devuelto por el algoritmo y el porsentaje del rendimiento (si se ha podido realizar una reparaci�n completa o no). 


Los ficheros de texto con los dos circuitos que se han usado para llevar a cabo los 4 experimentos se encuentran en la carpeta del c�digo fuente (Circuito1.txt y Circuito2.txt). 

Para llevar a cabo m�s experimentos, es necesario definir el circuito que se va a usar. Para ello, se crea un fichero de texto especificando la estructura del circuito y se utiliza el lector implementado al principio del c�digo para leerlo. A continuaci�n se puede proceder directamente a la parte correspondiente al apartado 4. En este apartado se deben introducir las puertas y conexiones da�adas y despu�s de debe ejecutar cada una de las partes del c�digo en el mismo orden en el que aparecen. Al final se obtendr�n los resultados. 

 
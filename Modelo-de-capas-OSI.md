
# MODELO DE CAPAS OSI



Tenemos varios **problemas** a la hora de la comunicación en red, tales como:

- Reodenar paquetes.
- Control de diálogo.
- Sintáxis.
- Semántica.
......

y para llevar a cabo la comunicación necesitamos transparencia + eficacia + seguridad.

**SOLUCIÓN** --> Open System Interconection (OSI): Hizo el conjunto de soluciones a los problemas que hemos visto, el Modelo de Capas OSI.

MODELO DE REFERENCIA = CAPAS + FUNCIONALIDADES

*La capa superior siempre encapsula a la inferior.

    ______________________________
    Unidad              Capa                Comunicación
    ------          -------------           ------------
    APDU            Aplicación              |   Extremo
    PPDU            Presentación            |      a
    SPDU            Sesión                  |   extremo  
    TPDU            Transporte              |   
    ---------------------------------------------------------->     
    Paquetes        Red                     |   Salto
    Tramas          Enlace                  |     a  
    Bits            Física                  |   salto
    _______________________________


## DESCRIPCIÓN DE LAS CAPAS:

### --------------------> Comunicación salto a salto:
- ***CAPA FÍSICA*** Es la que se encarga de la tranmisión de la señal en la comunicación. Resuelve los problemas relacionados con la transmisión de la información y cómo se representa. Existen una serie de acuerdos entre los dos puntos de la comucicación. Su unidad de comunicación es el bit.
- ***CAPA DE ENLACE:*** delimita la información en tramas (conjuntos de bits), que es su unidad de comunicación. En la capa de enlace tenemos:
    - **Control de errores:** para conseguir que la información recibida se corresponda con la enviada, existe un temporizador, checksum, ...

                          _____________________
                     _   |                     | 
                     |  --                     v
                temp | |  |                   ---
                     |  --                   | F |
                     -   ^                    ---
                         |_____________________|

    - **Control de flujo:** para evitar que el emisor sature el buffer  de recepción del destino debido a una velocidad u ocupación diferente de las dos partes. El receptor frena al origen para que el destino vaya a una velocidad adecuada. También controla si la conexión se ha parado.
    - **Delimitación de tramas:** para conocer el principio y el fin de un bloque de datos y sincronizar al emisor y al receptor, así sabe lo que son cabeceras y lo que son datos.
- ***CAPA DE RED:*** se encarga del encaminamiento. Garantiza que un paquete que sale de un origen llega a un destino, resolviendo el camino que tienen que elegir los paquetes. Procesa paquetes que es su unidad de datos. 
### --------------------> Comunicación extremo a extremo:
- ***CAPA DE TRANSPORTE:*** controla lo mismo que la capa de enlace de datos pero, a diferencia de ésta, sólo lo controla de host (extremo) a host (extremo), no salto a salto como la capa de enlace que están directamente conectados. Es decir, controla que la transmisión de datos entre los dos hosts se haga correctamente. Ejemplo: corregir la información en vez de reenviar. Otra función de esta capa es la de multiplexar aplicaciones sobre una misma conexión de red.
    - **Control de errores:**
    - **Control de flujo:**
- ***CAPA DE SESIÓN:*** se encarga del **diálogo** entre dos entidades gestionando su "turno de palabra", mantiene las sesiones.
- ***CAPA DE PRESENTACIÓN:*** se encarga de la **sintaxis** transformando un lenguaje común al lenguaje específico de la máquina que interpreta. Ejemplos: codificaciones de compresión, encriptado https, transformación de los datos,... Un ejemplo de sintaxis es cómo representamos los enteros.
- ***CAPA DE APLICACIÓN:*** se encarga de la **semántica**. Es la capa donde interactúan los usuarios, los programadores también programan en esta capa.
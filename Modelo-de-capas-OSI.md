
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
    Unidad              Capa
    ------          -------------
    APDU            Aplicación
    PPDU            Presentación
    SPDU            Sesión
    TPDU            Transporte
    ---------------------------------->
    Paquetes        Red
    Tramas          Enlace
    Bits            Física          
    _______________________________


## DESCRIPCIÓN DE LAS CAPAS:

- _CAPA FÍSICA_: Es la que se encarga de la tranmisión de la señal en la comunicación. Resuelve los problemas relacionados con la transmisión de la información y cómo se representa. Existen una serie de acuerdos entre los dos puntos de la comucicación. Su unidad de comunicación es el bit.
- _CAPA DE ENLACE_: delimita la información en tramas (conjuntos de bits), que es su unidad de comunicación. En la capa de enlace tenemos:
    - **Control de errores:**
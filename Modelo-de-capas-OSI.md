
# MODELO DE CAPAS OSI



Tenemos varios **problemas** a la hora de la comunicación en red, tales como:

- Reodenar paquetes.
- Control de diálogo.
- Sintáxis.
- Semántica.
......

y para llevar a cabo la comunicación necesitamos transparencia + eficacia + seguridad.

SOLUCIÓN --> Open System Interconection (OSI): Hizo el conjunto de soluciones a los problemas que hemos visto, el Modelo de Capas OSI.

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


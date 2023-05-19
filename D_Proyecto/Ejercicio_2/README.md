**Ejercicio #2, lógica secuencial: 15/05 al 21/05**

    Diseñar y programar un autómata secuencial (Moore o Mealy) para
    implementar el control de una línea de carga de paquetes de harina. El
    proceso de carga de paquetes debe iniciarse cuando la tolva tiene harina, las
    condiciones de seguridad están aseguradas y el operador pulsa el botón
    "start". Se deben definir al menos 6 estados para el automatismo.
----------------------------------------------------------------------------------------------------------------------------------------------

## **Descripcion de los 6 estados del autómata secuencial modelo de Moore**

**S1:** En este estado se verifica que la tolva tenga harina y se cumplan las condiciones de seguridad. En caso positivo se avanza al siguiente estado, en caso negativo permanece en el mismo estado.

*Transición: S1 -> Condiciones de seguridad cumplidas ->S2*

**S2:**  En este estado el autómata espera que se presione el botón “start”. En caso de ser positivo se avanza al siguiente estado y en caso negativo regresa al punto anterior S1.

*Transición: S2 -> Se presiona el botón “Start” ->S3*

**S3:** enciende el motor y avanza hasta detectar el punto donde se encuentra la boquilla de carga. En caso positivo se avanza al siguiente estado. En caso negativo continua en el mismo estado (S3).

*Transición: S3 -> Se detecta el punto de ubicación de la boquilla de carga ->S4*

**S4:** Se detiene el motor y se carga el paquete. Al finalizar se avanza al siguiente estado. En caso negativo continua en el estado en que se encuentra (S4).

*Transición: S4 -> Finalizada la carga. Se enciende el motor->S5*

**S5:** Una vez lleno el paquete de harina en este proceso se enciende el motor para avanzar hasta llegar al final de la cinta transportadora. En caso positivo se avanza al siguiente estado en caso negativo continua en el estado en el que se encuentra (S5)

*Transición: S5 ->Se enciende el motor ->S6*

**S6:** Se enciende el motor para hacer avanzar el paquete al final de la línea de carga y finaliza el proceso.  En caso positivo termina el proceso y regresa al comienzo (S1). En caso negativo continua en el estado en que se encuentra (S6).

*Transición: S6 -> Paquete en final de la línea finaliza el proceso y regresa el estado 1 ->S1*

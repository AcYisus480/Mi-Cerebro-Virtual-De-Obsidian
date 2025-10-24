# Transmisión de Datos

La transmisión de datos es el proceso de enviar información de un punto a otro. La información puede ser representada por señales analógicas o digitales.

## Señales Analógicas y Digitales

*   **Señal Analógica**: Una señal continua que puede tomar cualquier valor dentro de un rango. Se caracteriza por su **amplitud**, **fase** y **frecuencia**.
*   **Señal Digital**: Una señal discreta que solo puede tomar un número finito de valores. Se representa como una secuencia de bits (0 y 1).

## Modulación: de Digital a Analógica

La modulación es el proceso de convertir una señal digital en una señal analógica para que pueda ser transmitida a través de un medio analógico. Algunos ejemplos de técnicas de modulación son:

*   **Modulación por desplazamiento de amplitud (ASK - Amplitude Shift Keying)**: La amplitud de la señal portadora se varía para representar los datos digitales.
*   **Modulación por desplazamiento de frecuencia (FSK - Frequency Shift Keying)**: La frecuencia de la señal portadora se varía para representar los datos digitales.
*   **Modulación por desplazamiento de fase (PSK - Phase Shift Keying)**: La fase de la señal portadora se varía para representar los datos digitales.
*   **Quadrature PSK (QPSK)**: Una forma de PSK que permite transmitir dos bits por símbolo.

## Codificación: de Digital a Digital

La codificación es el proceso de convertir datos digitales en una señal digital. El objetivo es asegurar que la señal pueda ser transmitida y recibida de manera fiable. Algunas técnicas de codificación son:

*   **No retorno a cero (NRZ - Non Return to Zero)**: Un nivel de voltaje representa un 1 y otro nivel de voltaje representa un 0.
*   **No retorno a cero invertido (NRZI)**: Una transición en el nivel de voltaje representa un 1, mientras que la ausencia de transición representa un 0.
*   **Bipolar AMI (Alternate Mark Inversion)**: Los 0 se representan por un nivel de voltaje cero, y los 1 se representan por niveles de voltaje alternos positivos y negativos.
*   **Manchester**: Cada bit se representa por una transición en el nivel de voltaje. Una transición de bajo a alto representa un 1, y una transición de alto a bajo representa un 0. Esto ayuda a la [[sincronización]].
*   **Manchester diferencial**: Una transición al principio del intervalo de bit representa un 0, y la ausencia de una transición representa un 1.

## Problemas en la Transmisión

La transmisión de datos puede verse afectada por varios problemas:

*   **Atenuación**: La pérdida de la fuerza de la señal a medida que viaja a través del medio.
*   **Distorsión**: El cambio en la forma de la señal.
*   **Ruido**: Señales no deseadas que se mezclan con la señal original.

Estos problemas pueden causar errores en los datos recibidos. La [[Capa de Enlace de Datos]] se encarga de la [[detección y corrección de errores]].

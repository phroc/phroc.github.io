
Evohome es un sistema de calefacci�n multizona de Honeywell.

Es posible controlar Evohome desde eedomus a trav�s de IFTTT.

De esta forma podr� cambiar en cualquier momento la temperatura de consigna en cualquier zona desde eedomus (por ejemplo cuando sale de casa, cuando activa la alarma, etc.).

En cambio, la integraci�n de Evohome a trav�s de IFTTT no permite obtener un retorno de informaci�n. No se puede, por ejemplo, obtener en eedomus la temperatura ambiente en cada zona.


## Configuraci�n necesaria en IFTTT

- Debe tener una cuenta de IFTTT.

- Debe dar de alta en IFTTT el servicio Webhooks y apuntar la la �key� que le ha proporcionado IFTTT.

- Debe dar de alta en IFTTT el servicio Evohome.

- Debe crear en IFTTT un Applet por cada zona de calefacci�n de Evohome. Por consiguiente, si tiene 6 zonas de calefacci�n deber� crear 6 Applets.

- El �THIS� de cada uno de los Applets a crear debe ser el servicio Webhooks. El �EVENT� debe ser necesariamente Evohome-zone1 para el primer Applet. Si crea un segundo Applet para una segunda zona de calefacci�n, el �EVENT� deber� ser Evohome-zone2, y as� sucesivamente.

- El �THAT� de cada uno de los Applets a crear debe ser el  servicio Evohome, configurado como se indica a continuaci�n: Which zone -> Zona de calefacci�n elegida; Target temperature -> Value1; Temperature in -> Celsius; Hours-> Value2 (para introducir Value1 y Value 2 debe hace clic en  Ingredient)


## Creaci�n del perif�rico Evohome via IFTTT en eedomus

Los datos que debe introducir al crear el perif�rico son los siguientes:

- Key Webhooks IFTTT

- Zona de calefacci�n. Debe elegirla en el men� desplegable.

- Duraci�n de la consigna en horas: Valor predefinido y recomendado: 2.

 

Evohome es un sistema de calefacción multizona de Honeywell.

Es posible controlar Evohome desde eedomus a través de IFTTT.

De esta forma podrá cambiar en cualquier momento la temperatura de consigna en cualquier zona desde eedomus (por ejemplo cuando sale de casa, cuando activa la alarma, etc.).

En cambio, la integración de Evohome a través de IFTTT no permite obtener un retorno de información. No se puede, por ejemplo, obtener en eedomus la temperatura ambiente en cada zona.


## Configuración necesaria en IFTTT

- Debe tener una cuenta de IFTTT.

- Debe dar de alta en IFTTT el servicio Webhooks y apuntar la la “key” que le ha proporcionado IFTTT.

- Debe dar de alta en IFTTT el servicio Evohome.

- Debe crear en IFTTT un Applet por cada zona de calefacción de Evohome. Por consiguiente, si tiene 6 zonas de calefacción deberá crear 6 Applets.

- El “THIS” de cada uno de los Applets a crear debe ser el servicio Webhooks. El ”EVENT” debe ser necesariamente Evohome-zone1 para el primer Applet. Si crea un segundo Applet para una segunda zona de calefacción, el ”EVENT” deberá ser Evohome-zone2, y así sucesivamente.

- El “THAT” de cada uno de los Applets a crear debe ser el  servicio Evohome, configurado como se indica a continuación: Which zone -> Zona de calefacción elegida; Target temperature -> Value1; Temperature in -> Celsius; Hours-> Value2 (para introducir Value1 y Value 2 debe hace clic en  Ingredient)


## Creación del periférico Evohome via IFTTT en eedomus

Los datos que debe introducir al crear el periférico son los siguientes:

- Key Webhooks IFTTT

- Zona de calefacción. Debe elegirla en el menú desplegable.

- Duración de la consigna en horas: Valor predefinido y recomendado: 2.

 
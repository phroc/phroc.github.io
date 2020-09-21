
## �Para qu� sirve?

Para controlar con eedomus un objeto conectado no compatible con la plataforma eedomus pero compatible con IFTTT (https://ifttt.com/), se necesita lo siguiente:

- Un controlador eedomus o eedomus+

- Una cuenta de IFTTT

- El servicio Webhooks dado de alta en la cuenta de IFTTT

- El servicio correspondiente al objeto conectado que queramos controlar, dado de alta en la cuenta de IFTTT.

Adem�s, para interactuar entre eedomus e IFTTT:

- Hay que crear un perif�rico actuador http en eedomus.

- Hay que crear en IFTTT Applets basados en el servicio Webhooks (es el 'THIS') y el servicio correspondiente al objeto conectado que queramos controlar (es el 'THAT').

El perif�rico Webhooks IFTTT de la store eedomus sirve para crear de forma sencilla el actuador http necesario en eedomus, para poder interactuar con el servicio Webhooks f�cilmente.

Por tanto, el usuario s�lo deber� crear los Applets necesarios en IFTTT.


## �Para qu� no sirve?

El perif�rico Webhooks IFTTT de la store eedomus no permite controlar eedomus desde IFTTT, sino precisamente lo contrario (controlar un objeto conectado compatible con IFTTT desde eedomus).


## �Qu� datos hay que introducir para crear el perif�rico Webhooks IFTTT en eedomus?

Tres tipos de datos son necesarios:

- El 'Key' del servicio Webhooks: Es el c�digo que IFTTT le proporciona cuando da de alta el servicio Webhooks en su cuenta de IFTTT.

- Event n� 1: Cuando se crea en IFTTT un Applet basado en el servicio Webhooks, hay que proporcionar un nombre de evento  ('event' en ingl�s). Ejemplo: Apagar_Sonoff. El nombre de este evento es de libre elecci�n.

- Event n� 2: Idem event n� 1 pero para crear un segundo Applet basado en el servicio Webhooks, que permita configurar otra acci�n. Ejemplo: Encender_Sonoff.

Una vez creado el perif�rico Webhooks IFTTT en eedomus (con la 'key' y los dos 'events'), se obtiene un actuador HTTP con dos valores: OFF y ON, que se corresponden respectivamente con los 'events' creados.

Despu�s, el usuario deber� crear en su cuenta de IFTTT dos Applets basados en el servicio Webhooks y en los 'events' creados previamente en el controlador eedomus.

## Versiones

- Versi�n 1.1: Ahora es posible a�adir hasta 3 valores (opcional).

## ¿Para qué sirve?

Para controlar con eedomus un objeto conectado no compatible con la plataforma eedomus pero compatible con IFTTT (https://ifttt.com/), se necesita lo siguiente:

- Un controlador eedomus o eedomus+

- Una cuenta de IFTTT

- El servicio Webhooks dado de alta en la cuenta de IFTTT

- El servicio correspondiente al objeto conectado que queramos controlar, dado de alta en la cuenta de IFTTT.

Además, para interactuar entre eedomus e IFTTT:

- Hay que crear un periférico actuador http en eedomus.

- Hay que crear en IFTTT Applets basados en el servicio Webhooks (es el 'THIS') y el servicio correspondiente al objeto conectado que queramos controlar (es el 'THAT').

El periférico Webhooks IFTTT de la store eedomus sirve para crear de forma sencilla el actuador http necesario en eedomus, para poder interactuar con el servicio Webhooks fácilmente.

Por tanto, el usuario sólo deberá crear los Applets necesarios en IFTTT.


## ¿Para qué no sirve?

El periférico Webhooks IFTTT de la store eedomus no permite controlar eedomus desde IFTTT, sino precisamente lo contrario (controlar un objeto conectado compatible con IFTTT desde eedomus).


## ¿Qué datos hay que introducir para crear el periférico Webhooks IFTTT en eedomus?

Tres tipos de datos son necesarios:

- El 'Key' del servicio Webhooks: Es el código que IFTTT le proporciona cuando da de alta el servicio Webhooks en su cuenta de IFTTT.

- Event nº 1: Cuando se crea en IFTTT un Applet basado en el servicio Webhooks, hay que proporcionar un nombre de evento  ('event' en inglés). Ejemplo: Apagar_Sonoff. El nombre de este evento es de libre elección.

- Event nº 2: Idem event nº 1 pero para crear un segundo Applet basado en el servicio Webhooks, que permita configurar otra acción. Ejemplo: Encender_Sonoff.

Una vez creado el periférico Webhooks IFTTT en eedomus (con la 'key' y los dos 'events'), se obtiene un actuador HTTP con dos valores: OFF y ON, que se corresponden respectivamente con los 'events' creados.

Después, el usuario deberá crear en su cuenta de IFTTT dos Applets basados en el servicio Webhooks y en los 'events' creados previamente en el controlador eedomus.

## Versiones

- Versión 1.1: Ahora es posible añadir hasta 3 valores (opcional).
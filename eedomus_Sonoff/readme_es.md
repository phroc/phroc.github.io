Este plugin sirve para controlar el módulo domótico Sonoff Basic (el único modelo compatible de momento) desde eedomus.

Funciona conjuntamente con el firmware alternativo ESPeedomus. Por consiguiente, es necesario flashear el módulo Sonoff con el firmware antes citado.

ESPeeomus está disponible para su descarga en la siguiente URL: http://www.domoticadomestica.com/foro/index.php?topic=3326 


<br>

# ¿Cómo instalar el plugin Sonoff para eedomus?

- En el portal eedomus (secure.eedomus.com), identifíquese con su usuario y contraseña, vaya a Configuración/Añadir o eliminar un periférico/Store eedomus/Sonoff y haga clic en “Crear”.

- En la ventana que se abre al instalar el plugin, asigne el nuevo periférico a una de las habitaciones disponibles, introduzca la dirección IP de su módulo Sonoff y haga clic en “Crear”.


<br>

# ¿Qué periférico se crea en eedomus al instalar el plugin?

Después de instalar el plugin Sonoff en su controlador eedomus, le parecerá 1 nuevo periférico llamado "SONOFF CONTROL", con 4 valores, 2 ellos ocultos y 2 visibles.

Los valores ocultos sirven para obtener el retorno de estado del módulo Sonoff. Los valores visibles (ON/OFF) sirven para controlar el encendido y apagado del módulo desde eedomus.


<br>

# Observaciones

Debe instalar primero el plugin y flashear después el módulo Sonoff con el firmware ESPeedomus (ya que en este firmware debe introducir algunos datos, como el código API del periférico SONOFF CONTROL creado con el plugin).

Es posible controlar el encendido y apagado del módulo no sólo desde eedomus, sino también desde el pulsador físico del módulo Sonoff. 

El estado se reporta a eedomus en todo momento, incluso si se controla el módulo con el pulsador.

En caso de querer usar el módulo para controlar luces de techo, basta con soldar en la placa un hilo en cada uno de los bornes del pulsador y conectar a esos hilos un pulsador mural (libre de carga).

Se pueden hacer conmutadas conectando distintos pulsadores murales en paralelo.

<br>

# Licencia de uso del plugin

El presente plugin es un desarrollo de Philippe Rochette (http://pr-domotica.es) para la Store eedomus.

Se proporciona sin ningún tipo de garantía, expresa o implícita, sobre su funcionamiento y uso.

Tanto el plugin como el firmware ESPeedomus con el que funciona, pueden usarse, copiarse, distribuirse y modificarse libremente, siempre y cuando se mencionen su origen y su autor.
<br>
<br>
<br>
<br>
<br>
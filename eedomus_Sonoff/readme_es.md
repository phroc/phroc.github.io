Este plugin sirve para controlar el m�dulo dom�tico Sonoff Basic (el �nico modelo compatible de momento) desde eedomus.

Funciona conjuntamente con el firmware alternativo ESPeedomus. Por consiguiente, es necesario flashear el m�dulo Sonoff con el firmware antes citado.

ESPeeomus est� disponible para su descarga en la siguiente URL: http://www.domoticadomestica.com/foro/index.php?topic=3326 


<br>

# �C�mo instalar el plugin Sonoff para eedomus?

- En el portal eedomus (secure.eedomus.com), identif�quese con su usuario y contrase�a, vaya a Configuraci�n/A�adir o eliminar un perif�rico/Store eedomus/Sonoff y haga clic en �Crear�.

- En la ventana que se abre al instalar el plugin, asigne el nuevo perif�rico a una de las habitaciones disponibles, introduzca la direcci�n IP de su m�dulo Sonoff y haga clic en �Crear�.


<br>

# �Qu� perif�rico se crea en eedomus al instalar el plugin?

Despu�s de instalar el plugin Sonoff en su controlador eedomus, le parecer� 1 nuevo perif�rico llamado "SONOFF CONTROL", con 4 valores, 2 ellos ocultos y 2 visibles.

Los valores ocultos sirven para obtener el retorno de estado del m�dulo Sonoff. Los valores visibles (ON/OFF) sirven para controlar el encendido y apagado del m�dulo desde eedomus.


<br>

# Observaciones

Debe instalar primero el plugin y flashear despu�s el m�dulo Sonoff con el firmware ESPeedomus (ya que en este firmware debe introducir algunos datos, como el c�digo API del perif�rico SONOFF CONTROL creado con el plugin).

Es posible controlar el encendido y apagado del m�dulo no s�lo desde eedomus, sino tambi�n desde el pulsador f�sico del m�dulo Sonoff. 

El estado se reporta a eedomus en todo momento, incluso si se controla el m�dulo con el pulsador.

En caso de querer usar el m�dulo para controlar luces de techo, basta con soldar en la placa un hilo en cada uno de los bornes del pulsador y conectar a esos hilos un pulsador mural (libre de carga).

Se pueden hacer conmutadas conectando distintos pulsadores murales en paralelo.

<br>

# Licencia de uso del plugin

El presente plugin es un desarrollo de Philippe Rochette (http://pr-domotica.es) para la Store eedomus.

Se proporciona sin ning�n tipo de garant�a, expresa o impl�cita, sobre su funcionamiento y uso.

Tanto el plugin como el firmware ESPeedomus con el que funciona, pueden usarse, copiarse, distribuirse y modificarse libremente, siempre y cuando se mencionen su origen y su autor.
<br>
<br>
<br>
<br>
<br>
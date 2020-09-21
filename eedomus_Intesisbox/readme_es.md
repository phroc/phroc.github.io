IntesisBox son unos gateways wifi que permiten domotizar m�quinas de aire acondicionado por conductos o splits (https://www.intesisbox.com/en/wifi/gateways/).

Existen dos tipos de gateways IntesisBox: unos que son espec�ficos para una marca y unos modelos determinados de m�quinas de aire acondicionado por conductos, y uno que es universal y que permite controlar cualquier m�quina de aire acondicionado que tenga un mando a distancia por IR.

Con este plugin, es posible integrar en eedomus todos los modelos de gateway wifi IntesisBox que existen en la actualidad (basados en el protocolo WMP).

<br>

# �C�mo instalar el plugin IntesisBox para eedomus?

- En el portal eedomus (secure.eedomus.com), identif�quese con su usuario y contrase�a, vaya a Configuraci�n/A�adir o eliminar un perif�rico/Store eedomus/IntesisBox y haga clic en "Crear".

![STEP1](https://i.imgur.com/tg5QxoF.png)

- En la ventana que se abre al instalar el plugin, asigne el nuevo perif�rico a una de las habitaciones disponibles, introduzca la direcci�n IP o la direcci�n MAC de su gateway IntesisBox y haga clic en "Crear".

![STEP2](https://i.imgur.com/8VM29HQ.png)

<br>

# �Qu� perif�ricos se crean en eedomus al instalar el plugin?

Despu�s de instalar el plugin IntesisBox en su controlador eedomus, le parecer�n 7 nuevos perif�ricos y 1 widget HTML:

-	CLIM CONTROL - POWER: Sirve para controlar el encendido y apagado de la m�quina de aire acondicionado y obtener el retorno de estado.

-	CLIM CONTROL - FAN: Sirve para controlar el ventilador de la m�quina de aire acondicionado y obtener el retorno de estado. Las opciones disponibles son AUTO y niveles del 1 al 9.

-	CLIM CONTROL - TEMPERATURE (SETPOINT): Sirve para establecer la temperatura de consigna entre 16 y 32�C, con pasos de 1 grado, y obtener el retorno de estado.

-	CLIM CONTROL - MODE: Sirve para controlar el modo de funcionamiento de la m�quina de aire acondicionado y obtener el retorno de estado. Las opciones disponibles son AUTO, COOL, DRY, FAN Y HEAT.

-	CLIM CONTROL - VANE UP/DOWN: Sirve para controlar las paletas de orientaci�n vertical del chorro de aire y obtener el retorno de estado. Las opciones disponibles son AUTO, SWING y niveles del 1 al 3.

-	CLIM CONTROL - VANE LEFT/RIGHT: Sirve para controlar las paletas de orientaci�n horizontal del chorro de aire y obtener el retorno de estado. Las opciones disponibles son AUTO, SWING y niveles del 1 al 3.

-	TEMPERATURE (SENSOR): Sirve para conocer la temperatura ambiente (comprendida entre 16 y 34,5�C, con pasos de 0,5 grados. Consultar el apartado "Configuraciones avanzadas" para m�s detalles) medida por el sensor  de temperatura integrado en la m�quina de aire acondicionado. Este retorno de estado no es instant�neo sino que se hace por polling con una frecuencia de 5 minutos (el usuario puede modificar esta frecuencia de polling en la ventana de configuraci�n del perif�rico, en el apartado "Par�metros experto").


-	WIDGET INTESISBOX: Es un widget HTML que agrupa los 7 perifericos anteriormente descritos.

<br>

# Configuraciones avanzadas para usuarios expertos de eedomus (opcional).

## I - Posibilidad de prescrindir de algunos perif�ricos: usuarios con m�quina de A/A sin paletas de orientaci�n del chorro de aire

Los usuarios de aparatos de aire acondicionado por conductos, sin paletas de orientaci�n del chorro de aire, pueden borrar, si as� lo dedesan (opcional), los perif�ricos asociados, denominados "CLIM CONTROL - VANE UP/DOWN" y "CLIM CONTROL - VANE LEFT/RIGHT". 

Pero antes de borrar dichos perif�ricos, el usuario DEBE DESVINCULARLOS de los otros perif�ricos actuadores, ya que de lo contrario borrar� no s�lo los dos perif�ricos de control de paletas, sino otros.

Para desvincular el perif�rico "CLIM CONTROL - VANE UP/DOWN", el usuario debe ir a la ventana de configuraci�n del perif�rico en cuesti�n y, en el apartado "Param�tros experto", abrir el menu desplegable denominado "Adjuntar a", como se puede ver en la siguiente imagen.

![STEP7](https://i.imgur.com/dYhjwBt.png)

Por defecto, el perif�rico "CLIM CONTROL - VANE UP/DOWN" est� vinculado con el perif�rico "CLIM CONTROL - POWER", como se puede ver en la imagen anterior. Por consiguiente, el usuario debe seleccionar la opci�n "Ning�n perif�rico".

Una vez seleccionado "Ning�n perif�rico", el usuario debe hacer clic en "Guardar y seguir editando" y a continuaci�n en "Eliminar", como se puede ver en la siguiente imagen.

![STEP 8](https://i.imgur.com/sKRzXjz.png)

A continuaci�n se abrir� una ventana de confirmaci�n en la que el usuario debe confirmar que quiere suprimir el perif�rico.

El usuario deber� repetir la misma operaci�n con el perif�rico "CLIM  CONTROL - VANE LEFT/RIGHT" (es decir, antes de eliminarlo, deber� desvincularlo como hemos indicado anteriormente).

Despu�s de borrar los perif�ricos no �tiles, adicionalmente el usuario debe eliminar los valores correspondientes a los perif�ricos eliminados en dos sitios concretos:

- En la ventana de configuraci�n del perif�rico "CLIM CONTROL - POWER", en la casilla VAR2.

- En la ventana de configuraci�n del widget HTLML, en la casilla VAR1.

Si el usuario ha eliminado el perif�rico "CLIM CONTROL - VANE UP/DOWN", deber� eliminar en VAR1 del widget y en VAR2 del perif�rico "CLIM CONTROL - POWER" la cadena VUD:xxxxxxx (donde xxxxxxx corresponde al c�digo API del perif�rico eliminado).

Si el usuario ha eliminado el perif�rico "CLIM CONTROL - VANE LEFT/RIGHT", deber� eliminar en VAR1 del widget y en VAR2 del perif�rico "CLIM CONTROL - POWER" la cadena VLR:xxxxxxx (donde xxxxxxx corresponde al c�digo API del perif�rico eliminado).

INFORMACI�N SOBRE VAR2: La cadena de caracteres VAR2 incluye los 6 c�digos API de los perif�ricos actuadores creados por el plugin Intesisbox, as� como separadores (�:� y �,�) y el nombre abreviado de cada perif�rico actuador (POW para POWER, FAN para FAN, MOD para MODE, TEM para TEMPERATURE, VUD para VAN UP/DOWN y VLR para VANE LEFT/RIGHT).

Ejemplo de cadena VAR2 con c�digos API ficticios: POW:123451,FAN:123452,MOD:1243453,TEM:123454,VUD:123455,VLR:123456


<br>
## II - Usuarios cuya m�quina de A/A no tiene todos los valores previstos en el plugin

El plugin IntesisBox est� dise�ado para fucionar con todas las pasarelas intesisBox Wifi WMP compatibles con distintas marcas y modelos de m�quinas de aire acondicionado.

Por ello, es posible que algunos de los valores disponibles en los distintos perif�ricos "CLIM CONTROL" no sean de utilidad para una marca y/o un modelo concreto de m�quina de A/A.

Si lo desea, el usuario puede eliminar los valores que no sean �tiles en su caso particular (es opcional, se pueden dejar si se prefiere).

Ejemplo: el perif�rico "CLIM CONTROL - FAN" tiene 10 valores por defecto: AUTO y niveles del 1 al 9.

Es posible que en su m�quina de aire acondicionado, el usuario tenga disponible tan s�lo 4 configuraciones posibles: AUTO y niveles 1, 2 y 3. En ese caso, si lo desea puede borrar los valores del perif�rico que van del 4 al 9.

Para ello, en este ejemplo, el usuario debe ir a la ventana de configuraci�n del perif�rico "CLIM CONTROL - FAN" y luego a la pesta�a "Valores" y suprimir los valores que no le sean de utilidad (haciendo clic en el valor a suprimir y pulsando a continuaci�n en el bot�n "Eliminar" situado debajo de los valores).

<br>
## III - Temperature (Sensor)

Tal y como se menciona anteriormente, este perif�rico indica la temperatura medida por el sensor de la m�quina de aire acondicionado. Los valores presentados en eedomus est�n comprendido entre 16� y 34,5�. Este rango de temperaturas es arbitrario y se podr�a dar un rang mayor en la pr�ctica. Por ello, si el usuario lo desea, puede a�adir valores inferiores a 16� y/o superiores a 34,5� (en la pesta�a "Valores" de la ventana de configuraci�n del perif�rico, pulsando en "A�adir").


<br>
## IV - Widget HTML 

Si el usuario no desea usar el Widget HTML, puede ocultarlo (para ello basta con no asignarlo a ninguna habitacion) o, si lo prefiere, puede eliminarlo (pulsando en "WIDGET INTESISBOX" y una vez en la ventana de configuraci�n del widget, en "Eliminar").

Al contrario, el usuario puede querer conservar el widget HTML pero ocultar los otros 7 perif�ricos creados (NO DEBE ELIMINAR ESTOS PERIF�RICOS EN NING�N CASO). Para ocultar los perif�ricos, basta con entrar en la ventana de configuraci�n de cualquiera de ellos, no asignarlo a ninguna habitaci�n y elegir la opci�n "Salvar (Todos los canales)". De esta forma los 7 perif�ricos seguir�n instalados en eedomus pero no ser�n visibles, el �nico visible en este caso siendo el widget HTML.

<br>

# Licencia de uso del plugin

El presente plugin es un desarrollo de Jos� Miguel Go�i Menoyo y Philippe Rochette (http://pr-domotica.es) para la Store eedomus.

Se proporciona sin ning�n tipo de garant�a, expresa o impl�cita, sobre su funcionamiento y uso.

Tanto el plugin como el script que contiene pueden usarse, copiarse, distribuirse y modificarse libremente, siempre y cuando se mencionen su origen y sus autores.
<br>
<br>
<br>
<br>
<br>
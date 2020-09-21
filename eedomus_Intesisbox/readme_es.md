IntesisBox son unos gateways wifi que permiten domotizar máquinas de aire acondicionado por conductos o splits (https://www.intesisbox.com/en/wifi/gateways/).

Existen dos tipos de gateways IntesisBox: unos que son específicos para una marca y unos modelos determinados de máquinas de aire acondicionado por conductos, y uno que es universal y que permite controlar cualquier máquina de aire acondicionado que tenga un mando a distancia por IR.

Con este plugin, es posible integrar en eedomus todos los modelos de gateway wifi IntesisBox que existen en la actualidad (basados en el protocolo WMP).

<br>

# ¿Cómo instalar el plugin IntesisBox para eedomus?

- En el portal eedomus (secure.eedomus.com), identifíquese con su usuario y contraseña, vaya a Configuración/Añadir o eliminar un periférico/Store eedomus/IntesisBox y haga clic en "Crear".

![STEP1](https://i.imgur.com/tg5QxoF.png)

- En la ventana que se abre al instalar el plugin, asigne el nuevo periférico a una de las habitaciones disponibles, introduzca la dirección IP o la dirección MAC de su gateway IntesisBox y haga clic en "Crear".

![STEP2](https://i.imgur.com/8VM29HQ.png)

<br>

# ¿Qué periféricos se crean en eedomus al instalar el plugin?

Después de instalar el plugin IntesisBox en su controlador eedomus, le parecerán 7 nuevos periféricos y 1 widget HTML:

-	CLIM CONTROL - POWER: Sirve para controlar el encendido y apagado de la máquina de aire acondicionado y obtener el retorno de estado.

-	CLIM CONTROL - FAN: Sirve para controlar el ventilador de la máquina de aire acondicionado y obtener el retorno de estado. Las opciones disponibles son AUTO y niveles del 1 al 9.

-	CLIM CONTROL - TEMPERATURE (SETPOINT): Sirve para establecer la temperatura de consigna entre 16 y 32ºC, con pasos de 1 grado, y obtener el retorno de estado.

-	CLIM CONTROL - MODE: Sirve para controlar el modo de funcionamiento de la máquina de aire acondicionado y obtener el retorno de estado. Las opciones disponibles son AUTO, COOL, DRY, FAN Y HEAT.

-	CLIM CONTROL - VANE UP/DOWN: Sirve para controlar las paletas de orientación vertical del chorro de aire y obtener el retorno de estado. Las opciones disponibles son AUTO, SWING y niveles del 1 al 3.

-	CLIM CONTROL - VANE LEFT/RIGHT: Sirve para controlar las paletas de orientación horizontal del chorro de aire y obtener el retorno de estado. Las opciones disponibles son AUTO, SWING y niveles del 1 al 3.

-	TEMPERATURE (SENSOR): Sirve para conocer la temperatura ambiente (comprendida entre 16 y 34,5ºC, con pasos de 0,5 grados. Consultar el apartado "Configuraciones avanzadas" para más detalles) medida por el sensor  de temperatura integrado en la máquina de aire acondicionado. Este retorno de estado no es instantáneo sino que se hace por polling con una frecuencia de 5 minutos (el usuario puede modificar esta frecuencia de polling en la ventana de configuración del periférico, en el apartado "Parámetros experto").


-	WIDGET INTESISBOX: Es un widget HTML que agrupa los 7 perifericos anteriormente descritos.

<br>

# Configuraciones avanzadas para usuarios expertos de eedomus (opcional).

## I - Posibilidad de prescrindir de algunos periféricos: usuarios con máquina de A/A sin paletas de orientación del chorro de aire

Los usuarios de aparatos de aire acondicionado por conductos, sin paletas de orientación del chorro de aire, pueden borrar, si así lo dedesan (opcional), los periféricos asociados, denominados "CLIM CONTROL - VANE UP/DOWN" y "CLIM CONTROL - VANE LEFT/RIGHT". 

Pero antes de borrar dichos periféricos, el usuario DEBE DESVINCULARLOS de los otros periféricos actuadores, ya que de lo contrario borrará no sólo los dos periféricos de control de paletas, sino otros.

Para desvincular el periférico "CLIM CONTROL - VANE UP/DOWN", el usuario debe ir a la ventana de configuración del periférico en cuestión y, en el apartado "Paramétros experto", abrir el menu desplegable denominado "Adjuntar a", como se puede ver en la siguiente imagen.

![STEP7](https://i.imgur.com/dYhjwBt.png)

Por defecto, el periférico "CLIM CONTROL - VANE UP/DOWN" está vinculado con el periférico "CLIM CONTROL - POWER", como se puede ver en la imagen anterior. Por consiguiente, el usuario debe seleccionar la opción "Ningún periférico".

Una vez seleccionado "Ningún periférico", el usuario debe hacer clic en "Guardar y seguir editando" y a continuación en "Eliminar", como se puede ver en la siguiente imagen.

![STEP 8](https://i.imgur.com/sKRzXjz.png)

A continuación se abrirá una ventana de confirmación en la que el usuario debe confirmar que quiere suprimir el periférico.

El usuario deberá repetir la misma operación con el periférico "CLIM  CONTROL - VANE LEFT/RIGHT" (es decir, antes de eliminarlo, deberá desvincularlo como hemos indicado anteriormente).

Después de borrar los periféricos no útiles, adicionalmente el usuario debe eliminar los valores correspondientes a los periféricos eliminados en dos sitios concretos:

- En la ventana de configuración del periférico "CLIM CONTROL - POWER", en la casilla VAR2.

- En la ventana de configuración del widget HTLML, en la casilla VAR1.

Si el usuario ha eliminado el periférico "CLIM CONTROL - VANE UP/DOWN", deberá eliminar en VAR1 del widget y en VAR2 del periférico "CLIM CONTROL - POWER" la cadena VUD:xxxxxxx (donde xxxxxxx corresponde al código API del periférico eliminado).

Si el usuario ha eliminado el periférico "CLIM CONTROL - VANE LEFT/RIGHT", deberá eliminar en VAR1 del widget y en VAR2 del periférico "CLIM CONTROL - POWER" la cadena VLR:xxxxxxx (donde xxxxxxx corresponde al código API del periférico eliminado).

INFORMACIÓN SOBRE VAR2: La cadena de caracteres VAR2 incluye los 6 códigos API de los periféricos actuadores creados por el plugin Intesisbox, así como separadores (“:” y “,”) y el nombre abreviado de cada periférico actuador (POW para POWER, FAN para FAN, MOD para MODE, TEM para TEMPERATURE, VUD para VAN UP/DOWN y VLR para VANE LEFT/RIGHT).

Ejemplo de cadena VAR2 con códigos API ficticios: POW:123451,FAN:123452,MOD:1243453,TEM:123454,VUD:123455,VLR:123456


<br>
## II - Usuarios cuya máquina de A/A no tiene todos los valores previstos en el plugin

El plugin IntesisBox está diseñado para fucionar con todas las pasarelas intesisBox Wifi WMP compatibles con distintas marcas y modelos de máquinas de aire acondicionado.

Por ello, es posible que algunos de los valores disponibles en los distintos periféricos "CLIM CONTROL" no sean de utilidad para una marca y/o un modelo concreto de máquina de A/A.

Si lo desea, el usuario puede eliminar los valores que no sean útiles en su caso particular (es opcional, se pueden dejar si se prefiere).

Ejemplo: el periférico "CLIM CONTROL - FAN" tiene 10 valores por defecto: AUTO y niveles del 1 al 9.

Es posible que en su máquina de aire acondicionado, el usuario tenga disponible tan sólo 4 configuraciones posibles: AUTO y niveles 1, 2 y 3. En ese caso, si lo desea puede borrar los valores del periférico que van del 4 al 9.

Para ello, en este ejemplo, el usuario debe ir a la ventana de configuración del periférico "CLIM CONTROL - FAN" y luego a la pestaña "Valores" y suprimir los valores que no le sean de utilidad (haciendo clic en el valor a suprimir y pulsando a continuación en el botón "Eliminar" situado debajo de los valores).

<br>
## III - Temperature (Sensor)

Tal y como se menciona anteriormente, este periférico indica la temperatura medida por el sensor de la máquina de aire acondicionado. Los valores presentados en eedomus están comprendido entre 16º y 34,5º. Este rango de temperaturas es arbitrario y se podría dar un rang mayor en la práctica. Por ello, si el usuario lo desea, puede añadir valores inferiores a 16º y/o superiores a 34,5º (en la pestaña "Valores" de la ventana de configuración del periférico, pulsando en "Añadir").


<br>
## IV - Widget HTML 

Si el usuario no desea usar el Widget HTML, puede ocultarlo (para ello basta con no asignarlo a ninguna habitacion) o, si lo prefiere, puede eliminarlo (pulsando en "WIDGET INTESISBOX" y una vez en la ventana de configuración del widget, en "Eliminar").

Al contrario, el usuario puede querer conservar el widget HTML pero ocultar los otros 7 periféricos creados (NO DEBE ELIMINAR ESTOS PERIFÉRICOS EN NINGÚN CASO). Para ocultar los periféricos, basta con entrar en la ventana de configuración de cualquiera de ellos, no asignarlo a ninguna habitación y elegir la opción "Salvar (Todos los canales)". De esta forma los 7 periféricos seguirán instalados en eedomus pero no serán visibles, el único visible en este caso siendo el widget HTML.

<br>

# Licencia de uso del plugin

El presente plugin es un desarrollo de José Miguel Goñi Menoyo y Philippe Rochette (http://pr-domotica.es) para la Store eedomus.

Se proporciona sin ningún tipo de garantía, expresa o implícita, sobre su funcionamiento y uso.

Tanto el plugin como el script que contiene pueden usarse, copiarse, distribuirse y modificarse libremente, siempre y cuando se mencionen su origen y sus autores.
<br>
<br>
<br>
<br>
<br>
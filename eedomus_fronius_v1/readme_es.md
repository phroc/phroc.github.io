Este plugin permite integrar en eedomus los inversores solares fotovoltaicos de la marca Fronius a trav�s de la API Fronius (V1). Por tanto, se trata de una integraci�n en local, no dependiente de la nube.

<br>

# �C�mo instalar el plugin Fronius en eedomus?

- En el portal eedomus (secure.eedomus.com), identif�quese con su usuario y contrase�a, vaya a Configuraci�n/A�adir o eliminar un perif�rico/Store eedomus/Fronius y haga clic en "Crear".

- En la ventana que se abre al instalar el plugin, asigne el nuevo perif�rico a una de las habitaciones disponibles, introduzca la direcci�n IP local o la direcci�n MAC de su inversor Fronius, as� como el ID del inversor (el ID es 1 si se trata del inversor principal/primario, y 2,3... etc. para los dem�s). Despu�s, haga clic en "Crear".

<br>

# �Qu� perif�ricos se crean en eedomus al instalar el plugin?

Despu�s de instalar el plugin Solax Cloud en su controlador eedomus, le aparecer�n 13 nuevos perif�ricos que le van a permitir obtener en eedomus la informaci�n esencial referente a su inversor Fronius proporcionada por la API de Fronius (V1).

Si alguno de esos perif�ricos/canales no es de utilidad para usted, puede desactivarlo en la ventana de configuraci�n del perif�rico, y m�s concretamente en el apartado "Par�metros Experto". Es mejor no eliminarlo porque est� asociado a los dem�s perif�ricos y deber�a desvincularlo de los dem�s antes de eliminarlo para no suprimirlos todos.

El polling de cada uno de estos 13 perif�ricos est� establecido en 1 minuto. Por consiguiente, los datos se refrescan cada minuto.

<br>

# Licencia de uso del plugin

El presente plugin es un desarrollo de Philippe Rochette (http://pr-domotica.es) para la Store eedomus.

Se proporciona sin ning�n tipo de garant�a, expresa o impl�cita, sobre su funcionamiento y uso.

Tanto el plugin como los scripts que contiene pueden usarse, copiarse, distribuirse y modificarse libremente, siempre y cuando se mencionen su origen y su autor.
<br>
<br>
<br>
<br>
<br>
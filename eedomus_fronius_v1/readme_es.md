Este plugin permite integrar en eedomus los inversores solares fotovoltaicos de la marca Fronius a través de la API Fronius (V1). Por tanto, se trata de una integración en local, no dependiente de la nube.

<br>

# ¿Cómo instalar el plugin Fronius en eedomus?

- En el portal eedomus (secure.eedomus.com), identifíquese con su usuario y contraseña, vaya a Configuración/Añadir o eliminar un periférico/Store eedomus/Fronius y haga clic en "Crear".

- En la ventana que se abre al instalar el plugin, asigne el nuevo periférico a una de las habitaciones disponibles, introduzca la dirección IP local o la dirección MAC de su inversor Fronius, así como el ID del inversor (el ID es 1 si se trata del inversor principal/primario, y 2,3... etc. para los demás). Después, haga clic en "Crear".

<br>

# ¿Qué periféricos se crean en eedomus al instalar el plugin?

Después de instalar el plugin Solax Cloud en su controlador eedomus, le aparecerán 13 nuevos periféricos que le van a permitir obtener en eedomus la información esencial referente a su inversor Fronius proporcionada por la API de Fronius (V1).

Si alguno de esos periféricos/canales no es de utilidad para usted, puede desactivarlo en la ventana de configuración del periférico, y más concretamente en el apartado "Parámetros Experto". Es mejor no eliminarlo porque está asociado a los demás periféricos y debería desvincularlo de los demás antes de eliminarlo para no suprimirlos todos.

El polling de cada uno de estos 13 periféricos está establecido en 1 minuto. Por consiguiente, los datos se refrescan cada minuto.

<br>

# Licencia de uso del plugin

El presente plugin es un desarrollo de Philippe Rochette (http://pr-domotica.es) para la Store eedomus.

Se proporciona sin ningún tipo de garantía, expresa o implícita, sobre su funcionamiento y uso.

Tanto el plugin como los scripts que contiene pueden usarse, copiarse, distribuirse y modificarse libremente, siempre y cuando se mencionen su origen y su autor.
<br>
<br>
<br>
<br>
<br>
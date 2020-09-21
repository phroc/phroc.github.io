El plugin Widget Universal permite crear en el controlador eedomus widgets HTML que incluyan hasta 8 periféricos a elegir por el usuario entre los existentes.

Un widget HTML es la representación en la interfaz de eedomus (portal web o aplicaciones móviles) de varios periféricos.

<br>

# ¿Cómo instalar el plugin Widget Universal para eedomus?

- En el portal eedomus (secure.eedomus.com), identifíquese con su usuario y contraseña, vaya a Configuración/Añadir o eliminar un periférico/Store eedomus/Widget Universal y haga clic en "Crear".

- En la ventana que se abre al instalar el plugin, asigne el nuevo periférico a una de las habitaciones disponibles, indique el número de periféricos que quiere incluir en el widget (2 mínimo, 8 máximo), y en los campos "Choose device nº1", "Choose device nº2"... elija en cada caso el periférico que quiera incluir en el widget.

-  En los campos denominados "Check the box if device nºX is a sensor", marque la casilla si el periférico seleccionado es de tipo sensor (en caso contrario, no marque la casilla).

-   A continuación haga clic en "Crear".

<br>

# Observaciones sobre los widgets HTML

A día de hoy, los widgets HTML son una funcionalidad experimental de la plataforma eedomus. Por ello, su comportamiento podría no ser totalmente satisfactorio en algunos casos.

Por ejemplo, al instalar el plugin puede que el widget no aparezca inicialmente en la habitación correspondiente en las aplicaciones móviles (ya sea en iOS o Android). En ese caso, asociando el periférico del widget a otra habitación suele aparecer en la aplicación y ya se puede volver a asociar a la habitación que desee el usuario.

Otras anomalias posibles: en aplicaciones móviles para iOS y Android, el comportamiento del widget HTML puede verse afectado por el rendimiento del smartphone. Por consiguiente, no se recomienda el uso de más de un widget HTML en una misma pantalla en dispositivos móviles con recursos limitados.

<br>

# Modificación de los periféricos incluidos en el widget


En caso de querer modificar los periféricos incluidos en el widget, el usuario puede simplemente eliminar el widget existente y crear uno nuevo con los periféricos deseados, o puede seguir las instrucciones detalladas a continuación para modificar el widget existente.


Se puede modificar en cualquier momento el widget existente, cambiando tanto los periféricos que se desea incluir como el número de éstos.


Para ello, en la página de configuración del periférico debe cambiarse la cadena [VAR1], del apartado "Variables de usuario". La cadena debe mostrar una lista de los códigos API de los periféricos a incluir, separados por comas. Por ejemplo, para mostrar los periféricos que tienen códigos 1234, 1243 y 1324 la cadena [VAR1] debería ser "1234,1243,1324" y el widget los mostraría	en el orden en que se han escrito.


En algunos casos, el widget no es capaz de detectar si el periférico es -o se quiere que sea- un sensor, presentándose al usuario un menú desplegable que permitiría cambiar su valor. Para evitar la aparición de este menú, puede prefijarse el código API del periférico, en la cadena [VAR1], con una de las cadenas siguientes: "1:", "X:" o "SEN:". En el ejemplo anterior, si se quiere que del periférico 1243 muestre su valor actual y no un menú que permitiera modificar su valor, la cadena [VAR1] debería ser "1234,1:1243,1324” (o “1234,X:1243,1324”).

Aunque el número de periféricos que se puede incluir en esa cadena no está limitado, se recomienda que no supere 8, puesto que eedomus no reservaría espacio suficiente para mostrarlos en caso contrario. El espacio reservado por eedomus para la presentación de los periféricos del widget puede cambiarse en la página de configuración del periférico, cambiando el valor del desplegable "Hauteur d'affichage" por el deseado.

Cualquier otra cadena que preceda al código API de un periférico y que esté separada de este con “:” (similares a “0:”, “ZZ:” o “1X:”) no tienen ningún efecto. Así “1234,1:1243,1324” es equivalente a “0:1234,1:1243,AFX:1324”.

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
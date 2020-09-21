El plugin Widget Universal permite crear en el controlador eedomus widgets HTML que incluyan hasta 8 perif�ricos a elegir por el usuario entre los existentes.

Un widget HTML es la representaci�n en la interfaz de eedomus (portal web o aplicaciones m�viles) de varios perif�ricos.

<br>

# �C�mo instalar el plugin Widget Universal para eedomus?

- En el portal eedomus (secure.eedomus.com), identif�quese con su usuario y contrase�a, vaya a Configuraci�n/A�adir o eliminar un perif�rico/Store eedomus/Widget Universal y haga clic en "Crear".

- En la ventana que se abre al instalar el plugin, asigne el nuevo perif�rico a una de las habitaciones disponibles, indique el n�mero de perif�ricos que quiere incluir en el widget (2 m�nimo, 8 m�ximo), y en los campos "Choose device n�1", "Choose device n�2"... elija en cada caso el perif�rico que quiera incluir en el widget.

-  En los campos denominados "Check the box if device n�X is a sensor", marque la casilla si el perif�rico seleccionado es de tipo sensor (en caso contrario, no marque la casilla).

-   A continuaci�n haga clic en "Crear".

<br>

# Observaciones sobre los widgets HTML

A d�a de hoy, los widgets HTML son una funcionalidad experimental de la plataforma eedomus. Por ello, su comportamiento podr�a no ser totalmente satisfactorio en algunos casos.

Por ejemplo, al instalar el plugin puede que el widget no aparezca inicialmente en la habitaci�n correspondiente en las aplicaciones m�viles (ya sea en iOS o Android). En ese caso, asociando el perif�rico del widget a otra habitaci�n suele aparecer en la aplicaci�n y ya se puede volver a asociar a la habitaci�n que desee el usuario.

Otras anomalias posibles: en aplicaciones m�viles para iOS y Android, el comportamiento del widget HTML puede verse afectado por el rendimiento del smartphone. Por consiguiente, no se recomienda el uso de m�s de un widget HTML en una misma pantalla en dispositivos m�viles con recursos limitados.

<br>

# Modificaci�n de los perif�ricos incluidos en el widget


En caso de querer modificar los perif�ricos incluidos en el widget, el usuario puede simplemente eliminar el widget existente y crear uno nuevo con los perif�ricos deseados, o puede seguir las instrucciones detalladas a continuaci�n para modificar el widget existente.


Se puede modificar en cualquier momento el widget existente, cambiando tanto los perif�ricos que se desea incluir como el n�mero de �stos.


Para ello, en la p�gina de configuraci�n del perif�rico debe cambiarse la cadena [VAR1], del apartado "Variables de usuario". La cadena debe mostrar una lista de los c�digos API de los perif�ricos a incluir, separados por comas. Por ejemplo, para mostrar los perif�ricos que tienen c�digos 1234, 1243 y 1324 la cadena [VAR1] deber�a ser "1234,1243,1324" y el widget los mostrar�a	en el orden en que se han escrito.


En algunos casos, el widget no es capaz de detectar si el perif�rico es -o se quiere que sea- un sensor, present�ndose al usuario un men� desplegable que permitir�a cambiar su valor. Para evitar la aparici�n de este men�, puede prefijarse el c�digo API del perif�rico, en la cadena [VAR1], con una de las cadenas siguientes: "1:", "X:" o "SEN:". En el ejemplo anterior, si se quiere que del perif�rico 1243 muestre su valor actual y no un men� que permitiera modificar su valor, la cadena [VAR1] deber�a ser "1234,1:1243,1324� (o �1234,X:1243,1324�).

Aunque el n�mero de perif�ricos que se puede incluir en esa cadena no est� limitado, se recomienda que no supere 8, puesto que eedomus no reservar�a espacio suficiente para mostrarlos en caso contrario. El espacio reservado por eedomus para la presentaci�n de los perif�ricos del widget puede cambiarse en la p�gina de configuraci�n del perif�rico, cambiando el valor del desplegable "Hauteur d'affichage" por el deseado.

Cualquier otra cadena que preceda al c�digo API de un perif�rico y que est� separada de este con �:� (similares a �0:�, �ZZ:� o �1X:�) no tienen ning�n efecto. As� �1234,1:1243,1324� es equivalente a �0:1234,1:1243,AFX:1324�.

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

## � quoi �a sert ?

Pour commander depuis eedomus un objet connect� non compatible avec la plate-forme eedomus mais compatible avec IFTTT (https://ifttt.com/), il faut disposer des �l�ments suivants :

- Une box eedomus ou eedomus+

- Un compte IFTTT

- Le service Webhooks sur le compte IFTTT

- Le service correspondant � l'objet connect� que l'on souhaite commander, sur le compte IFTTT.

Par ailleurs, pour interagir entre eedomus et IFTTT, il faut :

- cr�er un actionneur http sur eedomus.

- cr�er sur IFTTT des Applets bas�s sur le service Webhooks (c'est le 'THIS') et le service correspondant � l'objet connect� � commander (c'est le 'THAT').

Le p�riph�rique Webhooks IFTTT du store eedomus a pour objet de simplifier la cr�ation de l�actionneur http sur eedomus, afin de pouvoir interagir avec le service Webhooks plus facilement.

L'utilisateur doit donc uniquement cr�er les Applets n�cessaires sur IFTTT.


## � quoi �a ne sert pas ?

Le p�riph�rique Webhooks IFTTT du store eedomus ne permet pas de commander la box eedomus depuis IFTTT, mais justement le contraire (commander un objet connect� compatible avec IFTTT depuis eedomus).


## Quelles sont les informations � renseigner lors de la cr�ation du p�riph�rique Webhooks IFTTT sur la box eedomus ?

Trois types de donn�es sont requises lors de la cr�ation du p�riph�rique :

- La 'Key' du service Webhooks : C'est le code que IFTTT vous fournit lorsque vous activez le service Webhooks sur votre compte IFTTT.

- Event n� 1 : Lors de la cr�ation sur IFTTT d'un Applet bas� sur le service Webhooks, il faut fournir un nom d��v�nement ('event' en anglais). Exemple : Eteindre_Sonoff. Le nom de cet �v�nement peut �tre choisi librement.

- Event n� 2 : Idem event n� 1 mais pour cr�er un second Applet bas� sur le service Webhooks, qui permet de configurer une autre action. Exemple : Allumer_Sonoff.

Une fois le p�riph�rique Webhooks IFTTT cr�� sur la box eedomus (avec la 'key' et les deux 'events'), on obtient un actionneur HTTP avec deux valeurs : OFF et ON correspondant respectivement aux 'events' d�clar�s.

A posteriori, il reste donc � l'utilisateur de cr�er sur son compte IFFFT deux Applets bas�s sur le service Webhooks et sur les 'events' d�clar�s auparavant sur la box eedomus.

## Versions

- Version 1.1: Il est d�sormais possible d�ajouter jusqu�� 3 valeurs (facultatif).
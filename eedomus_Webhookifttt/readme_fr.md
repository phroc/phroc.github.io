
## À quoi ça sert ?

Pour commander depuis eedomus un objet connecté non compatible avec la plate-forme eedomus mais compatible avec IFTTT (https://ifttt.com/), il faut disposer des éléments suivants :

- Une box eedomus ou eedomus+

- Un compte IFTTT

- Le service Webhooks sur le compte IFTTT

- Le service correspondant à l'objet connecté que l'on souhaite commander, sur le compte IFTTT.

Par ailleurs, pour interagir entre eedomus et IFTTT, il faut :

- créer un actionneur http sur eedomus.

- créer sur IFTTT des Applets basés sur le service Webhooks (c'est le 'THIS') et le service correspondant à l'objet connecté à commander (c'est le 'THAT').

Le périphérique Webhooks IFTTT du store eedomus a pour objet de simplifier la création de l’actionneur http sur eedomus, afin de pouvoir interagir avec le service Webhooks plus facilement.

L'utilisateur doit donc uniquement créer les Applets nécessaires sur IFTTT.


## À quoi ça ne sert pas ?

Le périphérique Webhooks IFTTT du store eedomus ne permet pas de commander la box eedomus depuis IFTTT, mais justement le contraire (commander un objet connecté compatible avec IFTTT depuis eedomus).


## Quelles sont les informations à renseigner lors de la création du périphérique Webhooks IFTTT sur la box eedomus ?

Trois types de données sont requises lors de la création du périphérique :

- La 'Key' du service Webhooks : C'est le code que IFTTT vous fournit lorsque vous activez le service Webhooks sur votre compte IFTTT.

- Event nº 1 : Lors de la création sur IFTTT d'un Applet basé sur le service Webhooks, il faut fournir un nom d’événement ('event' en anglais). Exemple : Eteindre_Sonoff. Le nom de cet événement peut être choisi librement.

- Event nº 2 : Idem event nº 1 mais pour créer un second Applet basé sur le service Webhooks, qui permet de configurer une autre action. Exemple : Allumer_Sonoff.

Une fois le périphérique Webhooks IFTTT créé sur la box eedomus (avec la 'key' et les deux 'events'), on obtient un actionneur HTTP avec deux valeurs : OFF et ON correspondant respectivement aux 'events' déclarés.

A posteriori, il reste donc à l'utilisateur de créer sur son compte IFFFT deux Applets basés sur le service Webhooks et sur les 'events' déclarés auparavant sur la box eedomus.

## Versions

- Version 1.1: Il est désormais possible d’ajouter jusqu’à 3 valeurs (facultatif).
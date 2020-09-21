
Evohome est un système de chauffage multizone de Honeywell.

Il est possible de piloter Evohome depuis la box eedomus via IFTTT.

On peut ainsi modifier à tout moment la consigne de température dans n’importe quelle zone depuis eedomus (par exemple lorsqu’on quitte la maison, lorsqu’on active l’alarme, etc.).

En revanche, l’intégration de Evohome via IFTTT me permet pas d’obtenir un retour d’information. Il n’’est donc pas possible, notamment, de faire remonter sur eedomus la température ambiante de chaque zone.


## Configuration requise côté IFTTT

- Il faut bien entendu disposer d’un compte IFTTT.

- Il faut activer sur le compte IFTTT le service Webhooks et noter la “key” que vous fournit IFTTT.

- Il faut activer sur le compte IFTTT le service Evohome.

- Il faut créer sur IFTTT un Applet par zone de chauffage Evohome. Par conséquent, si vous avez 6 zones de chauffage, vous devrez créer 6 Applets.

- Le “THIS” de chacun des Applets à créer doit être le service Webhooks. L’”EVENT” doit impérativement être Evohome-zone1 pour le premier Applet. Si vous créez un second Applet pour une deuxième zone de chauffage, l’”EVENT” devra être Evohome-zone2, et ainsi de suite.

- Le THAT de chacun des Applets à créer doit être le service Evohome, lequel doit être configuré comme suit: Which zone -> Zone de chauffage à choisir; Target temperature -> Value1; Temperature in -> Celsius; Hours-> Value2 (pour saisir Value1 et Value 2 vous devez cliquer sur Ingredient)


## Création du périphérique Evohome via IFTTT sur eedomus

Les informations à renseigner lors de la création du périphérique, sont les suivantes:

- Key Webhooks IFTTT

- Zone de chauffage à choisir dans le menu déroulant.

- Durée de la consigne en heures: Valeur prédéfinie et conseillée: 2.

 
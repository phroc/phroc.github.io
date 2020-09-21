
Evohome est un syst�me de chauffage multizone de Honeywell.

Il est possible de piloter Evohome depuis la box eedomus via IFTTT.

On peut ainsi modifier � tout moment la consigne de temp�rature dans n�importe quelle zone depuis eedomus (par exemple lorsqu�on quitte la maison, lorsqu�on active l�alarme, etc.).

En revanche, l�int�gration de Evohome via IFTTT me permet pas d�obtenir un retour d�information. Il n��est donc pas possible, notamment, de faire remonter sur eedomus la temp�rature ambiante de chaque zone.


## Configuration requise c�t� IFTTT

- Il faut bien entendu disposer d�un compte IFTTT.

- Il faut activer sur le compte IFTTT le service Webhooks et noter la �key� que vous fournit IFTTT.

- Il faut activer sur le compte IFTTT le service Evohome.

- Il faut cr�er sur IFTTT un Applet par zone de chauffage Evohome. Par cons�quent, si vous avez 6 zones de chauffage, vous devrez cr�er 6 Applets.

- Le �THIS� de chacun des Applets � cr�er doit �tre le service Webhooks. L��EVENT� doit imp�rativement �tre Evohome-zone1 pour le premier Applet. Si vous cr�ez un second Applet pour une deuxi�me zone de chauffage, l��EVENT� devra �tre Evohome-zone2, et ainsi de suite.

- Le THAT de chacun des Applets � cr�er doit �tre le service Evohome, lequel doit �tre configur� comme suit: Which zone -> Zone de chauffage � choisir; Target temperature -> Value1; Temperature in -> Celsius; Hours-> Value2 (pour saisir Value1 et Value 2 vous devez cliquer sur Ingredient)


## Cr�ation du p�riph�rique Evohome via IFTTT sur eedomus

Les informations � renseigner lors de la cr�ation du p�riph�rique, sont les suivantes:

- Key Webhooks IFTTT

- Zone de chauffage � choisir dans le menu d�roulant.

- Dur�e de la consigne en heures: Valeur pr�d�finie et conseill�e: 2.

 
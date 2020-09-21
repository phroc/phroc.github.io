Les passerelles Wifi IntesisBox permettent de domotiser des systèmes de climatisation gainables ou par split (https://www.intesisbox.com/en/wifi/gateways/).

Il existe deux types de passerelles wifi IntesisBox: des passerelles spécifiques pour domotiser des marques/modèles bien précis de systèmes de climatisation gainables, et une passerelle dite universelle, qui permet de piloter n'importe quel climatiseur équipé d'une télécommande à infrarouge.

Ce plugin permet d'intégrer dans la box eedomus tous les modèles de passerelles Wifi IntesisBox disponibles à ce jour (basés sur le protocole WMP).

<br>

# Comment installer le plugin IntesisBox sur votre box eedomus ?

- Sur le portail eedomus (secure.eedomus.com), saisissez votre identifiant et votre mot-de-passe puis rendez-vous à Configuration / Ajouter ou supprimer un périphérique / Store eedomus / IntesisBox et cliquez sur "Créer".

![STEP1](https://i.imgur.com/tg5QxoF.png)

- Dans la fenêtre qui s'ouvre après l'installation du plugin, associez le nouveau périphérique à l'une des pièces disponibles puis saisissez l'adresse IP ou l'adresse MAC de votre passerelle IntesisBox et cliquez sur "Créer".

![STEP2](https://i.imgur.com/8VM29HQ.png)

<br>

# Périphériques créés sur la box eedomus après l'installation du plugin

Suite à l'installation du plugin IntesisBox sur votre box eedomus, vous aurez 7 nouveaux périphériques et 1 widget HTML :

-	CLIM CONTROL - POWER : Périphérique permettant de contrôler les fonctions marche/arrêt du système de climatisation et d'obtenir un retour d'état.

-	CLIM CONTROL - FAN : Périphérique permettant de contrôler le ventilateur du système de climatisation et d'obtenir un retour d'état. Les réglages disponibles sont les suivants : AUTO et niveaux de 1 à 9.

-	CLIM CONTROL - TEMPERATURE (SETPOINT) : Périphérique permettant de régler la consigne de température entre 16 et 32ºC, par paliers de 1 degré, et d'obtenir un retour d'état.

-	CLIM CONTROL - MODE : Périphérique permettant de contrôler le mode de fonctionnement du système de climatisation et d'obtenir un retour d'état. Les réglages disponibles sont les suivants : AUTO, COOL, DRY, FAN et HEAT.

-	CLIM CONTROL - VANE UP/DOWN : Périphérique permettant de contrôler les lames verticales d'orientation du flux d'air et d'obtenir un retour d'état. Les réglages disponibles sont les suivants : AUTO, SWING et niveaux de 1 à 3.

-	CLIM CONTROL - VANE LEFT/RIGHT : Périphérique permettant de contrôler les lames horizontales d'orientation du flux d'air et d'obtenir un retour d'état. Les réglages disponibles sont les suivants: AUTO, SWING et niveaux de 1 à 3.

-	TEMPERATURE (SENSOR) : Périphérique permettant de connaître la température ambiante (comprise entre 16 et 34,5ºC, par paliers de 0,5 degrés. Veuillez consulter la section "Configurations avancées" pour plus de détails) relevée par le capteur de température du climatiseur. La remontée de la tempÈrature ambiante n'est pas instantanée. Elle s'effectue par polling, toutes les 5 minutes (l'utilisateur peut modifier la fréquence de polling dans la fenêtre de configuration du périphérique, section "Paramètres expert").

-	WIDGET INTESISBOX: Widget HTML qui regroupe les 7 periphériques décrits ci-dessus.

<br>

# Configurations avancées pour les utilisateurs chevronnés de la box eedomus (facultatif).

## I - Possibilité de supprimer certains périphéiques : utilisateurs possédant un climatiseur sans lames d'orientation du flux d'air

Si vous possédez un système de climatisation gainable, sans lames d'orientation du flux d'air, vous pouvez supprimer, si vous le souhaitez (facultatif), les périphériques correspondants, dénommés "CLIM CONTROL - VANE UP/DOWN" et "CLIM CONTROL - VANE LEFT/RIGHT".

Mais avant de supprimer ces périphériques, vous devez LES DISSOCIER des autres périphériques actionneurs, sans quoi ils seront tous supprimés et pas seulement les deux périphériques de contrôle des lames d'orientation du flux d'air.

Pour dissocier le périphérique "CLIM CONTROL - VANE UP/DOWN" des autres actionneurs, vous devez ouvrir la fenêtre de configuration du périphérique en question puis, dans la section "Paramètres expert", vous devez ouvrir le menu déroulant dénommé "Associer à", comme vous pouvez le voir sur l'image suivante.

![STEP7](https://i.imgur.com/dYhjwBt.png)

Par défaut, le périphérique "CLIM CONTROL - VANE UP/DOWN" est associé au périphérique "CLIM CONTROL - POWER", comme vous pouvez le voir sur l'image précédente. Vous devez donc sélectionner l'option "Aucun périphérique".

Après avoir sélectionné "Aucun périphérique, vous devez cliquer  sur "Sauvegarder et poursuivre l'édition", puis sur "Supprimer", comme vous pouvez le voir sur l'image suivante.

![STEP 8](https://i.imgur.com/sKRzXjz.png)

À ce moment-là s'ouvre une fenêtre de confirmation dans laquelle vous devez confirmer que vous souhaitez supprimer le périphérique.

Vous devrez ensuite recommencer la même opération avec le périphérique "CLIM  CONTROL - VANE LEFT/RIGHT" (avant de le supprimer, vous devrez donc le dissocier comme nous l'avons expliqué auparavant).

Après avoir éliminé les périphériques qui ne vous sont pas utiles, vous devez également éliminer les valeurs correspondant aux périphériques éliminés à deux endroits différents :

- Dans la fenêtre de configuration du périphérique "CLIM CONTROL - POWER", et plus précisément dans le champ VAR2.

- Dans la fenêre de configuration du widget HTLML, et plus précisément dans le champ VAR1.

Si vous avez éliminé le périphérique "CLIM CONTROL - VANE UP/DOWN", vous devrez alors éliminer dans la variable VAR1 du widget et dans la vaiable VAR2 du périphérique "CLIM CONTROL - POWER" la chaîne de caractères VUD:xxxxxxx (où xxxxxxx correspond au code API du périphérique éliminé).

Si vous avez éliminé le périphérique "CLIM CONTROL - VANE LEFT/RIGHT", vous devrez alors éliminer dans la variable  VAR1 du widget et dans la variable VAR2 du périphérique "CLIM CONTROL - POWER" la chaîne de caractères VLR:xxxxxxx (où xxxxxxx correspond au code API du périphérique éliminé).

EXPLICATION CONCERNANT LA VARIABLE VAR2: La chaîne de caractères contenue dans la variable VAR2 comprend les 6 codes API des périphériques actionneurs créés par le plugin Intesisbox, ainsi que des caractères de séparation (“:” et “,”) et le nom abrégé de chaque périphérique actionneur (POW pour POWER, FAN pour FAN, MOD pour MODE, TEM pour TEMPERATURE, VUD pour VAN UP/DOWN et VLR pour VANE LEFT/RIGHT).

Exemple de chaîne de caractères de la variable VAR2 avec des codes API fictifs: POW:123451,FAN:123452,MOD:1243453,TEM:123454,VUD:123455,VLR:123456

<br>
## II - Utilisateurs possédant un climatiseur ne permettant pas de configurer toutes les valeurs prévues dans le plugin

Le plugin IntesisBox est conçu pour fonctionner avec toutes les passerelles intesisBox Wifi WMP compatibles avec différentes marques et modèles de climatiseurs.

De ce fait, il est possible que certains des réglages proposés par les différents périphériques "CLIM CONTROL" ne soient pas utiles pour une marque et/ou pour un modèle bien précis de climatiseur.

Si vous le souhaitez, vous pouvez supprimer les valeurs qui se sont pas utiles dans votre cas particulier (cela est facultatif, vous pouvez tout simplement conserver ces valeurs si vous le préférez).

Exemple : le périphérique "CLIM CONTROL - FAN" a 10 valeurs par défaut : AUTO et les niveaux de 1 à 9.

Il est possible que votre climatiseur ne propose que 4 réglages : AUTO et niveaux 1, 2 et 3. Dans ce cas, si vous le souhaitez, vous pouvez supprimer les valeurs comprises entre 4 et 9.

Pour ce faire, dans cet exemple, vous devez ouvrir la fenêtre de configuration du périphérique "CLIM CONTROL - FAN" puis, dans l'onglet "Valeurs", vous devez supprimer les valeurs qui ne vous sont pas utiles (en cliquant sur la valeur à supprimer puis sur le bouton "Supprimer" situé juste en-dessous des valeurs).

<br>
## III - Temperature (Sensor)

Comme nous l'avons expliqué auparavant, ce périphérique remonte la température relevée par le capteur de température du climatiseur. Les valeurs remontées sur la box eedomus sont comprises entre 16º et 34,5º. Cette plage de températures est arbitraire et pourrait être plus large dans la pratique. Si vous le souhaitez, vous pouvez ajouter des valeurs inférieures à 16º et/ou supérieures à 34,5º (dans l'onglet "Valeurs" de la fenêtre de configuration du périphérique, en cliquant sur "Ajouter").

<br>
## IV - Widget HTML 

Si vous ne souhaitez pas utiliser le Widget HTML, vous pouvez le masquer (pour ce faire, il suffit de ne l'associer à aucune pièce) ou, si vous le préférez, vous pouvez l'éliminer (cliquez sur "WIDGET INTESISBOX" puis, dans la fenêtre de configuration du widget, sur "Supprimer").

À l'inverse, vous pourriez vouloir conserver le widget HTML et masquer les 7 autres périphériques créés (VOUS NE DEVEZ EN AUCUN CAS SUPPRIMER CES PÉRIPHÉRIQUES). Pour masquer les périphériques, il vous suffit de vous rendre dans la fenêtre de configuration de l'un des 7 périphériques, de ne l'associer à aucune pièce puis de cliquer sur "Sauvegarder (Tous les canaux)". Les 7 périphériques resteront ainsi présents sur votre box eedomus, mais seront masqués et seul le widget HTML sera visible.

<br>
# Licence d'utilisation du plugin

Ce plugin a été développé par José Miguel Goñi Menoyo et Philippe Rochette (http://pr-domotica.es) pour le Store eedomus.

Il est fourni sans garantie d'aucune sorte, expresse ou implicite, quant à son fonctionnement et son utilisation.

Ce plugin comme le script qu'il contient peuvent être utilisés, copiés, distribués et modifiés librement, sous réserve d'en mentionner l'origine et les auteurs.

<br>
<br>
<br>
<br>
<br>
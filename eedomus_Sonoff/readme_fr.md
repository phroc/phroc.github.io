Ce plugin permet de contrôler via la box eedomus le module domotique Sonoff Basic (le seul compatible à ce jour).

Il fonctionne conjointement avec le firmware non officiel ESPeedomus. Par conséquent, il faut flasher el module Sonoff avec le firmware précité.

ESPeeomus est disponible au téléchargement à l'adresse suivante: http://www.domoticadomestica.com/foro/index.php?topic=3326 


<br>

# Comment installer le plugin Sonoff pour eedomus ?

- Sur le portail eedomus (secure.eedomus.com), saisissez votre identifiant et votre mot-de-passe puis rendez-vous à Configuration/Ajouter ou supprimer un périphérique/Store eedomus/Sonoff et cliquez sur “Créer”.

- Dans la fenêtre qui s'ouvre après l'installation du plugin, associez le nouveau périphérique à l'une des pièces disponibles puis saisissez l'adresse IP de votre module Sonoff et cliquez sur “Créer”.


<br>

# Périphérique créé sur eedomus après l'installation du plugin

Suite à l'installation du plugin Sonoff sur votre box eedomus, vous aurez 1 nouveau périphérique dénommé "SONOFF CONTROL", avec 4 valeurs, dont 2 valeurs masquées et 2 valeurs visibles.

Les valeurs masquées permettent d'obtenir la remontée de l'état (ON/OFF) du module Sonoff. Les valeurs visibles (ON/OFF) permettent de contrôler le module via la box eedomus.


<br>

# Remarques

Vous devez installer en premier lieu le plugin, avant de flasher le module Sonoff avec le firmware ESPeedomus (il faut en effet renseigner certaines données dans ce firmware, comme par exemple le code API du périphérique SONOFF CONTROL créé lors de l'installation du plugin).

Il est possible de contrôler le module non seulement via la box eedomus, mais aussi en appuyant sur le bouton poussoir présent sur le module Sonoff. 

La remontée de l'état du module sur la box eedomus se fait à tout moment, même si vous contrôlez le module en appuyant sur le bouton poussoir.

Si vous souhaitez utiliser le module Sonoff pour domotiser des plafonniers, il suffit de souder sur la plaque un fil à chacune des deux bornes du bouton poussoir et de relier ces fils à un bouton poussoir mural (libre de potentiel).

Il est possible de domotiser un circuit commuté (va-et-vient)avec un module Sonoff. Il suffit de connecter différents boutons poussoirs en parallèle.

<br>

# Licence d'utilisation du plugin

Ce plugin a été développé par Philippe Rochette (http://pr-domotica.es) pour le Store eedomus.

Il est fourni sans garantie d'aucune sorte, expresse ou implicite, quant à son fonctionnement et son utilisation.

Ce plugin comme le firmware ESPeedomus avec lequel il fonctionne, peuvent être utilisés, copiés, distribués et modifiés librement, sous réserve d'en mentionner l'origine et l'auteur.
<br>
<br>
<br>
<br>
<br>
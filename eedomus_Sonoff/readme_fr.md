Ce plugin permet de contr�ler via la box eedomus le module domotique Sonoff Basic (le seul compatible � ce jour).

Il fonctionne conjointement avec le firmware non officiel ESPeedomus. Par cons�quent, il faut flasher el module Sonoff avec le firmware pr�cit�.

ESPeeomus est disponible au t�l�chargement � l'adresse suivante: http://www.domoticadomestica.com/foro/index.php?topic=3326 


<br>

# Comment installer le plugin Sonoff pour eedomus ?

- Sur le portail eedomus (secure.eedomus.com), saisissez votre identifiant et votre mot-de-passe puis rendez-vous � Configuration/Ajouter ou supprimer un p�riph�rique/Store eedomus/Sonoff et cliquez sur �Cr�er�.

- Dans la fen�tre qui s'ouvre apr�s l'installation du plugin, associez le nouveau p�riph�rique � l'une des pi�ces disponibles puis saisissez l'adresse IP de votre module Sonoff et cliquez sur �Cr�er�.


<br>

# P�riph�rique cr�� sur eedomus apr�s l'installation du plugin

Suite � l'installation du plugin Sonoff sur votre box eedomus, vous aurez 1 nouveau p�riph�rique d�nomm� "SONOFF CONTROL", avec 4 valeurs, dont 2 valeurs masqu�es et 2 valeurs visibles.

Les valeurs masqu�es permettent d'obtenir la remont�e de l'�tat (ON/OFF) du module Sonoff. Les valeurs visibles (ON/OFF) permettent de contr�ler le module via la box eedomus.


<br>

# Remarques

Vous devez installer en premier lieu le plugin, avant de flasher le module Sonoff avec le firmware ESPeedomus (il faut en effet renseigner certaines donn�es dans ce firmware, comme par exemple le code API du p�riph�rique SONOFF CONTROL cr�� lors de l'installation du plugin).

Il est possible de contr�ler le module non seulement via la box eedomus, mais aussi en appuyant sur le bouton poussoir pr�sent sur le module Sonoff. 

La remont�e de l'�tat du module sur la box eedomus se fait � tout moment, m�me si vous contr�lez le module en appuyant sur le bouton poussoir.

Si vous souhaitez utiliser le module Sonoff pour domotiser des plafonniers, il suffit de souder sur la plaque un fil � chacune des deux bornes du bouton poussoir et de relier ces fils � un bouton poussoir mural (libre de potentiel).

Il est possible de domotiser un circuit commut� (va-et-vient)avec un module Sonoff. Il suffit de connecter diff�rents boutons poussoirs en parall�le.

<br>

# Licence d'utilisation du plugin

Ce plugin a �t� d�velopp� par Philippe Rochette (http://pr-domotica.es) pour le Store eedomus.

Il est fourni sans garantie d'aucune sorte, expresse ou implicite, quant � son fonctionnement et son utilisation.

Ce plugin comme le firmware ESPeedomus avec lequel il fonctionne, peuvent �tre utilis�s, copi�s, distribu�s et modifi�s librement, sous r�serve d'en mentionner l'origine et l'auteur.
<br>
<br>
<br>
<br>
<br>
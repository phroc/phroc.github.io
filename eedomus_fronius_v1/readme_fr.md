Plugin permettant d'intégrer sur la box eedomus les onduleurs solaires photovoltaïques de la marque Fronius via l'API Fronius (V1). Il s'agit donc d'une intégration en local, non dépendante du cloud.

<br>

# Comment installer le plugin Fronius sur votre box eedomus ?

- Sur le portail eedomus (secure.eedomus.com), saisissez votre identifiant et votre mot-de-passe puis rendez-vous à Configuration / Ajouter ou supprimer un périphérique / Store eedomus / Fronius et cliquez sur "Créer".

- Dans la fenêtre qui s'ouvre après l'installation du plugin, associez le nouveau périphérique à l'une des pièces disponibles, puis saisissez l'adresse IP locale ou l'adresse MAC de votre onduleur Fronius, ainsi que l'ID du onduleur (l'ID est 1 pour l'onduleur principal/primaire et 2,3, ... etc. pour les autres). Enfin, cliquez sur "Créer".

<br>

# Périphériques créés sur la box eedomus après l'installation du plugin

Suite à l'installation du plugin Fronius sur votre box eedomus, vous aurez 13 nouveaux périphériques qui vont vous permettre d'obtenir les informations essentielles relatives à votre onduleur Fronius fournies par l'API Fronius (V1).

Si l'un de ces périphériques/canaux ne vous est pas utile, vous pouvez le désactiver depuis l'écran de configuration du périphérique (dans Paramètres Expert). Il vaut mieux ne pas le supprimer car il est associé aux autres périphériques et il vous faudrait le dissocier avant de l'éliminer pour ne pas supprimer tous les périphériques/canaux.

Le polling de chacun de ces 13 périphériques est fixé à 1 minute. Par conséquent, le rafraîchissement s'effectue toutes les minutes.

<br>
# Licence d'utilisation du plugin

Ce plugin a été développé par Philippe Rochette (http://pr-domotica.es) pour le Store eedomus.

Il est fourni sans garantie d'aucune sorte, expresse ou implicite, quant à son fonctionnement et son utilisation.

Ce plugin comme les scripts qu'il contient peuvent être utilisés, copiés, distribués et modifiés librement, sous réserve d'en mentionner l'origine et l'auteur.
<br>
<br>
<br>
<br>
<br>
Le plugin Widget Universel permet de créer sur la box eedomus des widgets HTML comprenant jusqu'à 8 périphériques différents choisis par l'utilisateur parmi les périphériques existants.

Un widget HTML est la représentation de plusieurs périphériques dans l'interface eedomus (portail web ou apps pour smartphones).

<br>

# Comment installer le plugin Widget Universel sur votre box eedomus ?

- Sur le portail eedomus (secure.eedomus.com), saisissez votre identifiant et votre mot-de-passe puis rendez-vous à Configuration / Ajouter ou supprimer un périphérique / Store eedomus / Widget Universel, puis cliquez sur "Créer".

- Dans la fenêtre qui s'ouvre après l'installation du plugin, associez le nouveau périphérique à l'une des pièces disponibles, indiquez le nombre de périphériques que vous souhaitez inclure dans le widget (2 minimum, 8 maximum), puis, dans les champs "Choose device nº1", "Choose device nº2"... sélectionnez dans chaque cas le périphérique que vous souhaitez inclure dans le widget.

- Dans les champs "Check the box if device nºX is a sensor", cochez la case si le périphérique sélectionné est un capteur (dans le cas contraire, ne cochez pas la case).

- Pour finir, cliquez sur "Créer".

<br>

# Remarques concernant les widgets HTML

À ce jour, les widget HTML sont une fonctionnalité expérimentale de la box eedomus. De ce fait, il se pourrait que le comportement du widget ne soit pas totalement satisfaisant dans certaines circonstances.

Par exemple, suite à l'installation du plugin, il est possible que le widget n'apparaisse pas dans la pièce correspondante si vous utilisez l'application eedomus pour iOS ou Android. Dans ce cas, il suffit d'associer le périphérique du widget à une autre pièce pour qu'il apparaisse dans l'application, après quoi l'utilisateur peut l'associer à nouveau à la pièce de son choix.

Autres anomalies constatées: dans les apps pour iOS et Android, le comportement du widget HTML peut être conditionné par les performances du smartphone. Il n'est donc pas conseillé d'utiliser plus d'un widget HTML dans un même écran de visualisation sur des smartphones aux ressources limitées.

<br>

# Modification des périphériques présents dans le widget


Si vous souhaitez modifier les périphériques présents dans le widget, vous pouvez tout simplement éliminer le widget existant et en créer un nouveau contenant les périphériques souhaités, ou vous pouvez suivre les indications ci-dessous pour modifier le widget existant.


Il est possible de modifier à tout moment le widget existant, que ce soit pour remplacer les périphériques présents dans le widget par d'autres périphériques, ou pour en modifier le nombre.


Pour ce faire, dans la fenêtre de configuration du widget, vous devez modifier la chaîne [VAR1] de la section "Variables utilisateur". Cette chaîne de caractères doit contenir les codes API des différents périphériques que vous souhaitez inclure dans le widget, séparés par une virgule. Exemple: pour inclure dans le widget les périphériques dont les codes API seraient 1234, 1243 et 1324, la chaîne [VAR1] devrait être la suivante: "1234,1243,1324". Dans ce cas, le widget présenterait les périphériques en question dans l'ordre où ont été saisi leurs codes API.


Dans certains cas, le widget n'est pas capable de détecter si le périphérique est un capteur ou un actionneur (il se peut également que vous souhaitiez qu'il soit traité comme un capteur). Dans ce cas de figure, le widget vous présente un menu dépliant qui permet de modifier la valeur du capteur. Pour éviter que ce menu dépliant n'apparaisse dans le widget, il suffit d'utiliser un préfixe devant le code API du capteur, dans la chaîne [VAR1]. Les préfixes qui peuvent être utilisés sont les suivants : "1:", "X:" ou "SEN:". Dans l'exemple précédent, si vous souhaitez que le périphérique dont le code API est 1243 soit traité comme un capteur et montre donc sa valeur actuelle sans que celle-ci ne puisse être modifiée via un menu dépliant, la chaîne [VAR1] devrait être la suivante : "1234,1:1243,1324” (ou “1234,X:1243,1324”).

Bien que le nombre de périphériques pouvant être inclus dans cette chaîne ne soit pas limité, il est conseillé de ne pas dépasser 8 périphériques étant donné que l'espace maximum réservé dans l'interface par la box eedomus ne permet pas de présenter plus de 8 périphériques. Cet espace peut être modifié (1 périphérique minimum, 8 maximum) dans la fenêtre de configuration du widget, en modifiant la valeur indiquée dans le menu dépliant "Hauteur d'affichage".

En cas d'utilisation d'un préfixe autre que ceux qui sont indiqués précédemment devant le code API d'un périphérique, avec le caractère de séparation “:” (exemples: “0:”, “ZZ:” ou “1X:”), la chaîne de caractères n'a aucun effet. Par exemple, la chaîne “1234,1:1243,1324” équivaut à “0:1234,1:1243,AFX:1324”.

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
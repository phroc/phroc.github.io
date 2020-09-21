Le plugin Widget Universel permet de cr�er sur la box eedomus des widgets HTML comprenant jusqu'� 8 p�riph�riques diff�rents choisis par l'utilisateur parmi les p�riph�riques existants.

Un widget HTML est la repr�sentation de plusieurs p�riph�riques dans l'interface eedomus (portail web ou apps pour smartphones).

<br>

# Comment installer le plugin Widget Universel sur votre box eedomus ?

- Sur le portail eedomus (secure.eedomus.com), saisissez votre identifiant et votre mot-de-passe puis rendez-vous � Configuration / Ajouter ou supprimer un p�riph�rique / Store eedomus / Widget Universel, puis cliquez sur "Cr�er".

- Dans la fen�tre qui s'ouvre apr�s l'installation du plugin, associez le nouveau p�riph�rique � l'une des pi�ces disponibles, indiquez le nombre de p�riph�riques que vous souhaitez inclure dans le widget (2 minimum, 8 maximum), puis, dans les champs "Choose device n�1", "Choose device n�2"... s�lectionnez dans chaque cas le p�riph�rique que vous souhaitez inclure dans le widget.

- Dans les champs "Check the box if device n�X is a sensor", cochez la case si le p�riph�rique s�lectionn� est un capteur (dans le cas contraire, ne cochez pas la case).

- Pour finir, cliquez sur "Cr�er".

<br>

# Remarques concernant les widgets HTML

� ce jour, les widget HTML sont une fonctionnalit� exp�rimentale de la box eedomus. De ce fait, il se pourrait que le comportement du widget ne soit pas totalement satisfaisant dans certaines circonstances.

Par exemple, suite � l'installation du plugin, il est possible que le widget n'apparaisse pas dans la pi�ce correspondante si vous utilisez l'application eedomus pour iOS ou Android. Dans ce cas, il suffit d'associer le p�riph�rique du widget � une autre pi�ce pour qu'il apparaisse dans l'application, apr�s quoi l'utilisateur peut l'associer � nouveau � la pi�ce de son choix.

Autres anomalies constat�es: dans les apps pour iOS et Android, le comportement du widget HTML peut �tre conditionn� par les performances du smartphone. Il n'est donc pas conseill� d'utiliser plus d'un widget HTML dans un m�me �cran de visualisation sur des smartphones aux ressources limit�es.

<br>

# Modification des p�riph�riques pr�sents dans le widget


Si vous souhaitez modifier les p�riph�riques pr�sents dans le widget, vous pouvez tout simplement �liminer le widget existant et en cr�er un nouveau contenant les p�riph�riques souhait�s, ou vous pouvez suivre les indications ci-dessous pour modifier le widget existant.


Il est possible de modifier � tout moment le widget existant, que ce soit pour remplacer les p�riph�riques pr�sents dans le widget par d'autres p�riph�riques, ou pour en modifier le nombre.


Pour ce faire, dans la fen�tre de configuration du widget, vous devez modifier la cha�ne [VAR1] de la section "Variables utilisateur". Cette cha�ne de caract�res doit contenir les codes API des diff�rents p�riph�riques que vous souhaitez inclure dans le widget, s�par�s par une virgule. Exemple: pour inclure dans le widget les p�riph�riques dont les codes API seraient 1234, 1243 et 1324, la cha�ne [VAR1] devrait �tre la suivante: "1234,1243,1324". Dans ce cas, le widget pr�senterait les p�riph�riques en question dans l'ordre o� ont �t� saisi leurs codes API.


Dans certains cas, le widget n'est pas capable de d�tecter si le p�riph�rique est un capteur ou un actionneur (il se peut �galement que vous souhaitiez qu'il soit trait� comme un capteur). Dans ce cas de figure, le widget vous pr�sente un menu d�pliant qui permet de modifier la valeur du capteur. Pour �viter que ce menu d�pliant n'apparaisse dans le widget, il suffit d'utiliser un pr�fixe devant le code API du capteur, dans la cha�ne [VAR1]. Les pr�fixes qui peuvent �tre utilis�s sont les suivants : "1:", "X:" ou "SEN:". Dans l'exemple pr�c�dent, si vous souhaitez que le p�riph�rique dont le code API est 1243 soit trait� comme un capteur et montre donc sa valeur actuelle sans que celle-ci ne puisse �tre modifi�e via un menu d�pliant, la cha�ne [VAR1] devrait �tre la suivante : "1234,1:1243,1324� (ou �1234,X:1243,1324�).

Bien que le nombre de p�riph�riques pouvant �tre inclus dans cette cha�ne ne soit pas limit�, il est conseill� de ne pas d�passer 8 p�riph�riques �tant donn� que l'espace maximum r�serv� dans l'interface par la box eedomus ne permet pas de pr�senter plus de 8 p�riph�riques. Cet espace peut �tre modifi� (1 p�riph�rique minimum, 8 maximum) dans la fen�tre de configuration du widget, en modifiant la valeur indiqu�e dans le menu d�pliant "Hauteur d'affichage".

En cas d'utilisation d'un pr�fixe autre que ceux qui sont indiqu�s pr�c�demment devant le code API d'un p�riph�rique, avec le caract�re de s�paration �:� (exemples: �0:�, �ZZ:� ou �1X:�), la cha�ne de caract�res n'a aucun effet. Par exemple, la cha�ne �1234,1:1243,1324� �quivaut � �0:1234,1:1243,AFX:1324�.

<br>

# Licence d'utilisation du plugin

Ce plugin a �t� d�velopp� par Jos� Miguel Go�i Menoyo et Philippe Rochette (http://pr-domotica.es) pour le Store eedomus.

Il est fourni sans garantie d'aucune sorte, expresse ou implicite, quant � son fonctionnement et son utilisation.

Ce plugin comme le script qu'il contient peuvent �tre utilis�s, copi�s, distribu�s et modifi�s librement, sous r�serve d'en mentionner l'origine et les auteurs.

<br>
<br>
<br>
<br>
<br>
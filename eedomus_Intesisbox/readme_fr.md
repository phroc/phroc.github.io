Les passerelles Wifi IntesisBox permettent de domotiser des syst�mes de climatisation gainables ou par split (https://www.intesisbox.com/en/wifi/gateways/).

Il existe deux types de passerelles wifi IntesisBox: des passerelles sp�cifiques pour domotiser des marques/mod�les bien pr�cis de syst�mes de climatisation gainables, et une passerelle dite universelle, qui permet de piloter n'importe quel climatiseur �quip� d'une t�l�commande � infrarouge.

Ce plugin permet d'int�grer dans la box eedomus tous les mod�les de passerelles Wifi IntesisBox disponibles � ce jour (bas�s sur le protocole WMP).

<br>

# Comment installer le plugin IntesisBox sur votre box eedomus ?

- Sur le portail eedomus (secure.eedomus.com), saisissez votre identifiant et votre mot-de-passe puis rendez-vous � Configuration / Ajouter ou supprimer un p�riph�rique / Store eedomus / IntesisBox et cliquez sur "Cr�er".

![STEP1](https://i.imgur.com/tg5QxoF.png)

- Dans la fen�tre qui s'ouvre apr�s l'installation du plugin, associez le nouveau p�riph�rique � l'une des pi�ces disponibles puis saisissez l'adresse IP ou l'adresse MAC de votre passerelle IntesisBox et cliquez sur "Cr�er".

![STEP2](https://i.imgur.com/8VM29HQ.png)

<br>

# P�riph�riques cr��s sur la box eedomus apr�s l'installation du plugin

Suite � l'installation du plugin IntesisBox sur votre box eedomus, vous aurez 7 nouveaux p�riph�riques et 1 widget HTML :

-	CLIM CONTROL - POWER : P�riph�rique permettant de contr�ler les fonctions marche/arr�t du syst�me de climatisation et d'obtenir un retour d'�tat.

-	CLIM CONTROL - FAN : P�riph�rique permettant de contr�ler le ventilateur du syst�me de climatisation et d'obtenir un retour d'�tat. Les r�glages disponibles sont les suivants : AUTO et niveaux de 1 � 9.

-	CLIM CONTROL - TEMPERATURE (SETPOINT) : P�riph�rique permettant de r�gler la consigne de temp�rature entre 16 et 32�C, par paliers de 1 degr�, et d'obtenir un retour d'�tat.

-	CLIM CONTROL - MODE : P�riph�rique permettant de contr�ler le mode de fonctionnement du syst�me de climatisation et d'obtenir un retour d'�tat. Les r�glages disponibles sont les suivants : AUTO, COOL, DRY, FAN et HEAT.

-	CLIM CONTROL - VANE UP/DOWN : P�riph�rique permettant de contr�ler les lames verticales d'orientation du flux d'air et d'obtenir un retour d'�tat. Les r�glages disponibles sont les suivants : AUTO, SWING et niveaux de 1 � 3.

-	CLIM CONTROL - VANE LEFT/RIGHT : P�riph�rique permettant de contr�ler les lames horizontales d'orientation du flux d'air et d'obtenir un retour d'�tat. Les r�glages disponibles sont les suivants: AUTO, SWING et niveaux de 1 � 3.

-	TEMPERATURE (SENSOR) : P�riph�rique permettant de conna�tre la temp�rature ambiante (comprise entre 16 et 34,5�C, par paliers de 0,5 degr�s. Veuillez consulter la section "Configurations avanc�es" pour plus de d�tails) relev�e par le capteur de temp�rature du climatiseur. La remont�e de la temp�rature ambiante n'est pas instantan�e. Elle s'effectue par polling, toutes les 5 minutes (l'utilisateur peut modifier la fr�quence de polling dans la fen�tre de configuration du p�riph�rique, section "Param�tres expert").

-	WIDGET INTESISBOX: Widget HTML qui regroupe les 7 periph�riques d�crits ci-dessus.

<br>

# Configurations avanc�es pour les utilisateurs chevronn�s de la box eedomus (facultatif).

## I - Possibilit� de supprimer certains p�riph�iques : utilisateurs poss�dant un climatiseur sans lames d'orientation du flux d'air

Si vous poss�dez un syst�me de climatisation gainable, sans lames d'orientation du flux d'air, vous pouvez supprimer, si vous le souhaitez (facultatif), les p�riph�riques correspondants, d�nomm�s "CLIM CONTROL - VANE UP/DOWN" et "CLIM CONTROL - VANE LEFT/RIGHT".

Mais avant de supprimer ces p�riph�riques, vous devez LES DISSOCIER des autres p�riph�riques actionneurs, sans quoi ils seront tous supprim�s et pas seulement les deux p�riph�riques de contr�le des lames d'orientation du flux d'air.

Pour dissocier le p�riph�rique "CLIM CONTROL - VANE UP/DOWN" des autres actionneurs, vous devez ouvrir la fen�tre de configuration du p�riph�rique en question puis, dans la section "Param�tres expert", vous devez ouvrir le menu d�roulant d�nomm� "Associer �", comme vous pouvez le voir sur l'image suivante.

![STEP7](https://i.imgur.com/dYhjwBt.png)

Par d�faut, le p�riph�rique "CLIM CONTROL - VANE UP/DOWN" est associ� au p�riph�rique "CLIM CONTROL - POWER", comme vous pouvez le voir sur l'image pr�c�dente. Vous devez donc s�lectionner l'option "Aucun p�riph�rique".

Apr�s avoir s�lectionn� "Aucun p�riph�rique, vous devez cliquer  sur "Sauvegarder et poursuivre l'�dition", puis sur "Supprimer", comme vous pouvez le voir sur l'image suivante.

![STEP 8](https://i.imgur.com/sKRzXjz.png)

� ce moment-l� s'ouvre une fen�tre de confirmation dans laquelle vous devez confirmer que vous souhaitez supprimer le p�riph�rique.

Vous devrez ensuite recommencer la m�me op�ration avec le p�riph�rique "CLIM  CONTROL - VANE LEFT/RIGHT" (avant de le supprimer, vous devrez donc le dissocier comme nous l'avons expliqu� auparavant).

Apr�s avoir �limin� les p�riph�riques qui ne vous sont pas utiles, vous devez �galement �liminer les valeurs correspondant aux p�riph�riques �limin�s � deux endroits diff�rents :

- Dans la fen�tre de configuration du p�riph�rique "CLIM CONTROL - POWER", et plus pr�cis�ment dans le champ VAR2.

- Dans la fen�re de configuration du widget HTLML, et plus pr�cis�ment dans le champ VAR1.

Si vous avez �limin� le p�riph�rique "CLIM CONTROL - VANE UP/DOWN", vous devrez alors �liminer dans la variable VAR1 du widget et dans la vaiable VAR2 du p�riph�rique "CLIM CONTROL - POWER" la cha�ne de caract�res VUD:xxxxxxx (o� xxxxxxx correspond au code API du p�riph�rique �limin�).

Si vous avez �limin� le p�riph�rique "CLIM CONTROL - VANE LEFT/RIGHT", vous devrez alors �liminer dans la variable  VAR1 du widget et dans la variable VAR2 du p�riph�rique "CLIM CONTROL - POWER" la cha�ne de caract�res VLR:xxxxxxx (o� xxxxxxx correspond au code API du p�riph�rique �limin�).

EXPLICATION CONCERNANT LA VARIABLE VAR2: La cha�ne de caract�res contenue dans la variable VAR2 comprend les 6 codes API des p�riph�riques actionneurs cr��s par le plugin Intesisbox, ainsi que des caract�res de s�paration (�:� et �,�) et le nom abr�g� de chaque p�riph�rique actionneur (POW pour POWER, FAN pour FAN, MOD pour MODE, TEM pour TEMPERATURE, VUD pour VAN UP/DOWN et VLR pour VANE LEFT/RIGHT).

Exemple de cha�ne de caract�res de la variable VAR2 avec des codes API fictifs: POW:123451,FAN:123452,MOD:1243453,TEM:123454,VUD:123455,VLR:123456

<br>
## II - Utilisateurs poss�dant un climatiseur ne permettant pas de configurer toutes les valeurs pr�vues dans le plugin

Le plugin IntesisBox est con�u pour fonctionner avec toutes les passerelles intesisBox Wifi WMP compatibles avec diff�rentes marques et mod�les de climatiseurs.

De ce fait, il est possible que certains des r�glages propos�s par les diff�rents p�riph�riques "CLIM CONTROL" ne soient pas utiles pour une marque et/ou pour un mod�le bien pr�cis de climatiseur.

Si vous le souhaitez, vous pouvez supprimer les valeurs qui se sont pas utiles dans votre cas particulier (cela est facultatif, vous pouvez tout simplement conserver ces valeurs si vous le pr�f�rez).

Exemple : le p�riph�rique "CLIM CONTROL - FAN" a 10 valeurs par d�faut : AUTO et les niveaux de 1 � 9.

Il est possible que votre climatiseur ne propose que 4 r�glages : AUTO et niveaux 1, 2 et 3. Dans ce cas, si vous le souhaitez, vous pouvez supprimer les valeurs comprises entre 4 et 9.

Pour ce faire, dans cet exemple, vous devez ouvrir la fen�tre de configuration du p�riph�rique "CLIM CONTROL - FAN" puis, dans l'onglet "Valeurs", vous devez supprimer les valeurs qui ne vous sont pas utiles (en cliquant sur la valeur � supprimer puis sur le bouton "Supprimer" situ� juste en-dessous des valeurs).

<br>
## III - Temperature (Sensor)

Comme nous l'avons expliqu� auparavant, ce p�riph�rique remonte la temp�rature relev�e par le capteur de temp�rature du climatiseur. Les valeurs remont�es sur la box eedomus sont comprises entre 16� et 34,5�. Cette plage de temp�ratures est arbitraire et pourrait �tre plus large dans la pratique. Si vous le souhaitez, vous pouvez ajouter des valeurs inf�rieures � 16� et/ou sup�rieures � 34,5� (dans l'onglet "Valeurs" de la fen�tre de configuration du p�riph�rique, en cliquant sur "Ajouter").

<br>
## IV - Widget HTML 

Si vous ne souhaitez pas utiliser le Widget HTML, vous pouvez le masquer (pour ce faire, il suffit de ne l'associer � aucune pi�ce) ou, si vous le pr�f�rez, vous pouvez l'�liminer (cliquez sur "WIDGET INTESISBOX" puis, dans la fen�tre de configuration du widget, sur "Supprimer").

� l'inverse, vous pourriez vouloir conserver le widget HTML et masquer les 7 autres p�riph�riques cr��s (VOUS NE DEVEZ EN AUCUN CAS SUPPRIMER CES P�RIPH�RIQUES). Pour masquer les p�riph�riques, il vous suffit de vous rendre dans la fen�tre de configuration de l'un des 7 p�riph�riques, de ne l'associer � aucune pi�ce puis de cliquer sur "Sauvegarder (Tous les canaux)". Les 7 p�riph�riques resteront ainsi pr�sents sur votre box eedomus, mais seront masqu�s et seul le widget HTML sera visible.

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
<span style="color: #67A4F2">Description du plugin Solax Cloud</span>
===

Le plugin Solax Cloud vous permet de récupérer les informations de vos **onduleurs Solax via Solax Cloud**.

Il ne s'agit donc pas d'une intégration en local, **mais via le cloud**.

Si vous souhaitez intégrer vos onduleurs Solax sur Jeedom sans dépendance du cloud, installez le plugin "Onduleur Solax", disponible gratuitement sur le market Jeedom.

L'avantage de ce plugin Solax Cloud est qu'il permet de récupérer les informations de onduleurs Solax non supportés par l'autre plugin.
<br>
<br>

<span style="color: #67A4F2">Configuration du plugin Solax Cloud</span>
===

Après avoir installé le plugin via le market Jeedom, il vous suffit de l'activer. **Il n'a ni dépendances, ni démon**. Par conséquent, il n'y a rien d'autre à faire à ce niveau-là.

Ensuite vous devez créer un équipement. Pour cela, rendez-vous à Plugin / Monitoring / Solax Cloud.

Cliquez sur "+" (Ajouter).

Saisissez un nom pour votre nouvel équipement.

Vous devez ensuite saisir le "Registration No" de votre onduleur Solax (indiqué sur celui-ci).

Vous devez également saisir le "token" préalablement obtenu sur votre compte Solax Cloud.

Pour finir, cliquez sur "Sauvegarder"

C'est tout!
<br>
<br>

<span style="color: #67A4F2">Commandes</span>
===

**Les commandes de l'équipement se créent automatiquement** dès que vous sauvegardez la configuration à l'étape précédente.

Vous obtenez **13 commandes de type "info"** que vous pouvez afficher et/ou historiser à votre convenance.
<br>
<br> 


<span style="color: #67A4F2">Widget</span>
===

Widget en forme de jauges, à l'état brut.

Vous pouvez personnaliser ce widget à votre guise.

**Le rafraîchissement des données s'effectue toutes les minutes**.

Si vous avez plusieurs onduleurs Solax, vous pouvez créér un équipement pour chacun d'entre eux. Dans ce cas, vous aurez un widget par onduleur.
<br>
<br> 


<span style="color: #67A4F2">Autres informations</span>
===

* changelog disponible [ici](https://github.com/phroc/jeedom_plugins_docs/blob/master/Solaxcloud/fr_FR/changelog.md)
* Documentación en español disponible [aquí](https://github.com/phroc/jeedom_plugins_docs/blob/master/Solaxcloud/es_ES/index.md)

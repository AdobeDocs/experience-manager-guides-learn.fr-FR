---
title: Notes de mise à jour | Adobe Experience Manager Guides as a Cloud Service, version de février 2023
description: Dernière version des guides Adobe Experience Manager as a Cloud Service
source-git-commit: d56855bf9078482ec1676b0eeb7a13df05475d5c
workflow-type: tm+mt
source-wordcount: '2178'
ht-degree: 2%

---

# Dernière version des guides Adobe Experience Manager as a Cloud Service

## Mise à niveau vers la dernière version

Mettez à niveau vos guides Adobe Experience Manager actuels as a Cloud Service (plus tard appelés *AEM Guides as a Cloud Service*) en procédant comme suit :
1. Extrayez le code Git des Cloud Services et passez à la branche configurée dans le pipeline Cloud Services correspondant à l’environnement que vous souhaitez mettre à niveau.
2. Mettre à jour `<dox.version>` dans `/dox/dox.installer/pom.xml` du code Git Cloud Services vers la version 2023.2.235.
3. Validez les modifications et exécutez le pipeline Cloud Services pour effectuer la mise à niveau vers la dernière version d’AEM Guides as a Cloud Service.

## Étapes d’indexation du contenu existant (uniquement si vous utilisez une version antérieure à la version de septembre des AEM Guides as a Cloud Service)

Effectuez les étapes suivantes pour indexer le contenu existant et utilisez le nouveau texte de recherche et de remplacement au niveau de la carte :

* Exécutez une requête de POST sur le serveur (avec l’authentification correcte) - `http://<server:port>/bin/guides/map-find/indexing`.
(Facultatif) Vous pouvez transmettre des chemins d’accès spécifiques des cartes pour les indexer ; par défaut, toutes les cartes seront indexées. || Exemple : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* L’API renvoie un jobId. Pour vérifier l’état de la tâche, vous pouvez envoyer une demande de GET avec l’ID de la tâche au même point de terminaison : `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Par exemple : http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Une fois la tâche terminée, la requête de GET ci-dessus répond avec succès et indique si une correspondance a échoué. Les mappages indexés avec succès peuvent être confirmés à partir des journaux du serveur.

## Matrice de compatibilité

Cette section répertorie le tableau de compatibilité des applications logicielles prises en charge par AEM Guides as a Cloud Service de février 2023.

### FrameMaker et FrameMaker Publishing Server

| AEM Guides as a Cloud | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.02.0 | Non compatible | 2022 ou version ultérieure |
|  |  |  |

*Les conditions de base et créées dans AEM sont prises en charge dans les versions FMPS à partir de 2020.2.

### Connecteur Oxygen

| AEM Guides as a Cloud | Fenêtres du connecteur Oxygen | Mac du connecteur Oxygen | Modifier sous Windows Oxygen | Modifier dans Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023.02.0 | 2.8-uuid-8 | 2.8-uuid-8 | 2.3 | 2.3 |
|  |  |  |  |


## Nouvelles fonctionnalités et améliorations

AEM Guides as a Cloud Service fournit des améliorations et de nouvelles fonctionnalités dans la dernière version :

### Génération de rapports à partir de l’éditeur Web

AEM Guides s’accompagne d’une fonctionnalité de l’éditeur web qui vous permet de vérifier l’exhaustivité globale de vos documents techniques et de générer des rapports à leur sujet.
Vous pouvez afficher la liste des rubriques, gérer les métadonnées et afficher le contenu multimédia utilisé dans toutes les références pour la carte actuelle à partir de la
**Rapports** dans l’éditeur Web.

**Génération de la vue Liste des rubriques**

Vous pouvez générer la liste des rubriques qui fournit des informations détaillées sur vos rubriques, telles que le type de référence, l’état du document et l’auteur. Vous pouvez également générer le fichier CSV pour télécharger l’instantané actuel des rubriques dans la carte DITA.

**Gestion des métadonnées et modification de l’état du document**

Vous pouvez appliquer des balises sur une rubrique individuelle ou utiliser la fonction de balisage en masse pour appliquer plusieurs balises sur plusieurs rubriques, un mappage DITA ou un sous-mappage. Vous pouvez également remplacer l’état du document de toutes les rubriques sélectionnées par l’état suivant du document commun.

<img src="assets/web-editor-metadata-panel.png" alt="gestion des métadonnées" width="600">

**Génération du rapport Multimédia**

Vous pouvez générer le rapport multimédia qui contient des informations détaillées sur le multimédia utilisé dans vos références dans la carte actuelle. Vous avez la possibilité de filtrer et de trier les fichiers multimédia répertoriés dans le rapport.
Vous pouvez également générer le fichier CSV pour télécharger l’instantané actuel du fichier multimédia utilisé dans la carte DITA.

<img src="assets/web-editor-reports-multimedia.png" alt="rapport multimédia" width="600">

### UX restructuré pour la fonctionnalité de révision

Désormais, AEM guides fournit un UX amélioré qui vous aide à passer en revue les rubriques partagées en vue de la révision. Dans la dernière expérience, la fonctionnalité de révision présente les améliorations suivantes :

* Interface utilisateur actualisée
* Panneau Conditions qui vous permet de mettre en surbrillance le contenu en fonction des conditions disponibles dans la rubrique.
* Chaque commentaire du panneau des commentaires est associé au texte correspondant dans la rubrique actuelle. Il permet d’identifier le texte commenté.
* Les commentaires sont affichés dans l’ordre du texte commenté dans le document.
* Le nom de la tâche de révision s’affiche dans le workflow de révision.
* Sélectionnez la feuille de route de la tâche de révision utilisée pour résoudre toutes les références clés et tous les termes du glossaire utilisés dans le contenu de la révision.
* Barre d’outils contextuelle qui permet de mettre rapidement le texte en surbrillance ou barré
* Menu Options pour modifier ou supprimer vos propres commentaires
* Pour les commentaires obsolètes, vous avez accès à une vue côte à côte qui vous aide à comparer la version précédente de la rubrique à la version de révision actuelle.
* Lorsque vous utilisez les filtres, les commentaires sur le panneau de droite sont filtrés en fonction de la sélection et le nombre de commentaires dans le panneau de gauche est mis à jour en conséquence.


   <img alt="tâche de révision" src="assets/comment-pop-up-panel.png" width="600">



### Améliorations de la traduction

Le tableau de bord Traduction contient désormais plus d’améliorations conviviales qui vous permettent de traduire facilement vos documents à partir de l’éditeur Web.

**Transmettre le libellé de la version à la version cible**

AEM Guides vous permet de transmettre le libellé du fichier source au fichier cible. Vous pouvez ainsi identifier facilement la version source du fichier traduit.

<img alt="libellés de traduction" src="assets/translation-pass-source-label.png" width="600">

Par exemple, si vous avez des fichiers source auxquels est appliqué le libellé de version Version 1.0, vous pouvez également transmettre le libellé source (Version 1.0) au fichier traduit.

**Forcer la synchronisation pour les ressources désynchronisées**

Si vous apportez des modifications à certaines ressources, AEM Guides les signale comme étant désynchronisés. Vous pouvez soit retraduire les ressources modifiées, soit choisir d’ignorer l’état Désynchronisé . Par exemple, si vous avez apporté des modifications mineures qui n’ont vraiment pas besoin de traduction, vous pouvez marquer leur état comme étant Synchronisé.

<img src="assets/translation-version-diff.png" alt="forum de traduction" width="600">

**Projets de traduction Afficher en cours pour une rubrique ou une carte**

Certaines des références de votre tableau de bord de traduction peuvent être en cours. Désormais, AEM Guides fournit une fonctionnalité qui vous aide à afficher la liste de tous les projets de traduction en cours (ainsi que la langue cible) qui contiennent la référence sélectionnée.


### Générer une sortie dans divers formats à partir de l’éditeur web

Vous pouvez désormais facilement générer la sortie pour vos rubriques ou mappage DITA à partir de l’éditeur web. Vous pouvez configurer divers paramètres prédéfinis de sortie tels qu’AEM Site, PDF, HTML5, JSON (format de sortie sans interface) et une sortie personnalisée. Vous pouvez ensuite les utiliser pour générer les sorties respectives.

Vous pouvez définir des attributs dans vos rubriques DITA, puis utiliser le paramètre prédéfini de condition pour appliquer une condition lors de la publication de la sortie. Vous pouvez également utiliser la fonction de publication de ligne de base pour publier sélectivement une version spécifique de votre mappage ou de votre rubrique DITA.


### Rechercher et remplacer le texte au niveau de la carte

AEM Guides vous permet de rechercher des fichiers dans une carte contenant du texte spécifique. Le texte recherché est mis en surbrillance dans les fichiers. Vous pouvez désormais également remplacer le mot ou l’expression recherché par un autre mot ou expression dans tous les fichiers. Vous pouvez sélectionner **Tout remplacer** à droite en haut de la liste pour remplacer toutes les occurrences du terme recherché dans tous les fichiers.

<img src="assets/map-find-replace.png" alt="map find replace" width="600">

### Suppression et duplication de fichiers à partir du panneau du référentiel

Vous pouvez désormais facilement créer un doublon ou une copie d’un fichier à partir du **Options** du fichier sélectionné dans le panneau du référentiel. Par défaut, le fichier est créé avec un suffixe (comme `filename_1.extension`).

<img src="assets/options-menu-repo-view-file-level.png" alt="menu des options de fichier " width="500">


### Autres améliorations apportées à l’éditeur web

* Dans AEM Guides, vous pouvez effectuer certaines opérations courantes pour les images et les fichiers multimédias à l’aide du menu contextuel. Vous pouvez désormais également localiser l’image ou le média sélectionné dans le référentiel ou afficher l’aperçu du fichier dans l’interface utilisateur d’Assets.

* Le nom du profil de dossier actif s’affiche sous forme de libellé pour l’icône Préférences utilisateur dans la barre d’outils principale. Vous pouvez ainsi identifier le profil de dossier sur lequel vous travaillez.

* Lorsque vous ouvrez une carte en mode Carte, le titre de la carte active s’affiche au centre de la barre d’outils principale. Ceci s’avère utile pour indiquer aux utilisateurs quelle carte est actuellement ouverte.


### Afficher le titre à la place de l’UUID dans l’éditeur Oxygen

Maintenant AEM Guides vous permet de choisir **Utilisation du titre dans l’éditeur et le gestionnaire de cartes** dans Paramètres. Si vous sélectionnez cette option, le titre du fichier s’affiche dans l’onglet du fichier lorsqu’il est ouvert dans l’éditeur ou dans le Gestionnaire de mappages DITA. Si vous ne sélectionnez pas cette option, l’UUID du fichier est affiché dans l’onglet du fichier.

### Publication basée sur un microservice pour AEM Guides as a Cloud Service

Le nouveau microservice de publication vous permet d’exécuter simultanément des charges de travail de publication volumineuses sur AEM Guides as a Cloud Service et d’exploiter la plate-forme Adobe I/O Runtime sans serveur de pointe.

Pour chaque demande de publication AEM Guides as a Cloud Service exécute un conteneur distinct qui se met à l’échelle horizontalement en fonction des demandes de l’utilisateur. Cela vous permet d’exécuter plusieurs requêtes de publication et d’obtenir des performances améliorées.

Pour plus d’informations, voir [Configuration de la nouvelle publication basée sur un microservice pour AEM Guides as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/knowledge-base/publishing/configure-microservices.md).

### PDF natif | Ajout d’un signet personnalisé dans la sortie PDF

Vous pouvez maintenant ajouter un signet personnalisé sur un contenu particulier dans la sortie finale du PDF pour une navigation facile. Cela sera ajouté à la table des matières qui est créée à partir des titres de rubrique ou de section dans votre mappage DITA.

### PDF natif | Application d’un style personnalisé aux entrées de la table des matières et au contenu de la rubrique

AEM Guides fournit la fonctionnalité permettant d’appliquer un style personnalisé aux entrées de la table des matières ou à une rubrique particulière dans la sortie du PDF. Par exemple, vous pouvez modifier la couleur du texte dans la table des matières et le titre de la rubrique. Vous pouvez également appliquer des styles à l’ensemble du contenu dans la rubrique.


### PDF natif | Style du marqueur de page dans le composant de note de bas de page

Vous pouvez maintenant mettre en forme le marqueur de la page dans les notes de pied. Par exemple, vous pouvez ajouter des crochets ou modifier leur couleur. Ces styles permettent aux utilisateurs d’identifier facilement les marqueurs de page dans le document.

### PDF natif | Barre de modification pour indiquer les rubriques modifiées dans la table des matières

AEM Guides vous permet désormais d’identifier rapidement les rubriques modifiées dans la table des matières de la sortie du PDF.  Une barre de modification s’affiche à gauche des rubriques modifiées dans la table des matières. Vous pouvez cliquer sur la rubrique dans la table des matières et afficher les modifications détaillées.

<img src="assets/change-marker-toc.png" alt="Changement de marqueur dans la table des matières " width="500">

## Problèmes résolus

Les bogues résolus dans différentes zones sont répertoriés ci-dessous :

### Création

* Les modifications dans le code HTML de l’éditeur Web entraînent des problèmes avec `<dl>` et `<dlentry>`. (11024)
* Certains attributs ne sont pas traités comme conditionnels et posent des problèmes. (10895)
* Trois niveaux ou plus imbriqués `<indexterm>` ne sont pas imbriqués dans l’exportation de PDF natif. (10799)
* Le contenu disparaît dans le corps d’une tâche lors du passage de la vue Auteur à la vue Source. (10735)
* Les commentaires de révision sont déplacés dans une tâche de révision. (10625)
* **Annuler** ou **Rétablir** ne fonctionne pas correctement sur certains fichiers. (10373)
* Les métadonnées personnalisées ne sont pas conservées lors de l’action copier-coller. (10367)
* L’option Annuler de l’éditeur XML permet à l’utilisateur d’accéder au haut de la page. (10091)
* Les propriétés de noeud sont supprimées après l’opération de copier-coller d’une ressource. (10053)
* mimeType est codé en dur pour la création et la mise à jour de ressources DITA. (8979)
* Le nom du créateur de versions dans l’historique de versions est &quot;fmdita-serviceuser&quot; pour les fichiers chargés via l’interface utilisateur d’Assets. (8910)
* Les fragments de contenu ne peuvent pas être copiés et collés lorsqu’AEM Guides est installé sur Cloud. (11315)
* Le navigateur (éditeur web) se bloque lors du chargement de contenu avec un schéma personnalisé. (11211)

### Gestion

* La copie d’une ressource de mappage DITA (à partir de l’interface utilisateur d’Asset ) entraîne des lignes de base erronées dans la ressource copiée. (11218)
* Le message d’avertissement ne s’affiche pas lors du téléchargement d’un fichier qui est supérieur à la limite autorisée dans AEM (2 Go par défaut). (10817)
* Ligne de base de l’éditeur web | Le comportement de la colonne Dernière colonne est différent dans le nouveau tableau de bord de ligne de base de l’éditeur web. (10808)
* Traduction | La tâche de traduction ne démarre pas en raison d’un /libs/fmdita/i18n/ja.json non valide. (10543)
* Traduction | Une erreur se produit dans un projet de traduction de portée créé à partir du tableau de bord de traduction (traduction humaine). (10526)
* Traduction | Le post-traitement est bloqué pour l’ensemble du dossier linguistique dont les ressources sont présentes dans un principal projet de traduction. (10332)
* Plusieurs fenêtres contextuelles s’affichent pour n’importe quelle ressource si la version est modifiée et enregistrée dans l’éditeur de ligne de base. (10399)
* La fuite de session se produit à l’adresse `com.day.cq.search.impl.builder.QueryBuilderImpl.createResourceResolver(QueryBuilderImpl.java:210)`. (10279)

### Publication

* La régénération de rubrique ne fonctionne pas dans certains scénarios. (10635)
* L’écouteur de publication n’affiche pas les données demandées dans les journaux d’informations et contient également des journaux indésirables.( 10567)
* PDF natif | Lors de la création d’un paramètre prédéfini de sortie avec l’option &quot;Ajouter au profil de dossier&quot;, la génération du PDF échoue avec une exception Null Pointer. (10950)
* PDF natif | Des problèmes se produisent lors de la rotation de l’en-tête du tableau. (10555)
* PDF natif | Imbriqué `<indexterm>` ne sont pas imbriqués dans l’exportation de PDF natif. (10521)
* PDF natif | La référence de topicref imbriquée dans les appendices est toutes transformée en h1 dans le HTML temporaire. (10454)
* La publication de ligne de base échoue pour le PDF généré à l’aide de FrameMaker Publishing Server 2020. (10551)
* PDF natif | Ajouter `xref` à une image n’effectue pas le rendu de l’image sur le PDF généré. (11346)
* PDF natif | La balise d’image ajoute un attribut display-inline à toutes les images. (10653)
* PDF natif | Les commentaires brouillons sont masqués par défaut dans la sortie générée. (10560)
* PDF natif | navtitle n’est pas honoré pour topichead. (10509)

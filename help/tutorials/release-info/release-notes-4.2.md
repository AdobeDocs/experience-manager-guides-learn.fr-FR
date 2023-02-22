---
title: Notes de mise à jour | Adobe Experience Manager Guides version 4.2
description: Dernière version des guides Adobe Experience Manager
source-git-commit: 2fb46bdfb7f42fd9b3ef19343700009818c5b4f2
workflow-type: tm+mt
source-wordcount: '3681'
ht-degree: 2%

---

# Version 4.2 des guides Adobe Experience Manager (février 2023)

Cette note de mise à jour décrit les instructions de mise à niveau, les nouvelles fonctionnalités et les améliorations de la version 4.2 des Guides Adobe Experience Manager (appelée ultérieurement *Guides d’AEM*).

## Mise à niveau vers la dernière version

Vous pouvez facilement mettre à niveau votre version actuelle des AEM Guides vers la version 4.2. Avant de procéder à la mise à niveau vers la version 4.2 des AEM Guides, vous devez tenir compte des points suivants :
* Si vous utilisez la version 4.0, 4.1 ou 4.1.x, vous pouvez directement effectuer la mise à niveau vers la version 4.2.
* Si vous utilisez la version 3.8.5, vous devez effectuer la mise à niveau vers la version 4.0 avant de passer à la version 4.2.
* Si vous utilisez une version antérieure à 3.8.5, reportez-vous à la section *Mise à niveau AEM guides* dans le guide d’installation spécifique au produit.

>[!NOTE]
>
>Vous devez installer AEM Service Pack avant de mettre à niveau AEM version de Guides.

Pour plus d’informations, voir [Instructions de mise à niveau](assets/Adobe-Experience-Manager-Guides-Upgrade-Instructions-EN.pdf).

## 4.2 | Notes de mise à jour

## Matrice de compatibilité

Cette section répertorie le tableau de compatibilité des applications logicielles prises en charge par AEM Guides 4.2.

### Adobe Experience Manager

**Non UUID**
Version 6.5 Service Pack 15, 14, 13 ou 12

**UUID**
Version 6.5 Service Pack 15, 14, 13 ou 12

Pour plus d’informations, voir *Exigences techniques* dans le guide d’installation et de configuration d’Adobe Experience Manager Guides.

### FrameMaker et FrameMaker Publishing Server

| Mise à jour | FMPS 2022 | FMPS 2020 | Fm 2022 | Fm 2020 |
| --- | --- | --- | --- | --- |
| 4.2 (non UUID) | 2022 ou version ultérieure | 2020.2 ou version ultérieure* | 2022 ou version ultérieure | 2020.3 ou version ultérieure |
| 4.2 (UUID) | 2022 ou version ultérieure | 2020.2 ou version ultérieure* | 2022 ou version ultérieure | 2020.4 ou version ultérieure |
|  |  |  |  |

*Les conditions de base et créées dans AEM sont prises en charge dans les versions FMPS à partir de 2020.2.

### Connecteur Oxygen

| Mise à jour | Fenêtres du connecteur Oxygen | Mac du connecteur Oxygen | Modifier sous Windows Oxygen | Modifier dans Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.2 (non UUID) | 2.1-normal-4 | 2.1-normal-4 | 1,6 | 1,6 |
| 4.2 (UUID) | 2.8-uuid-8 | 2.8-uuid-8 | 2.3 | 2.3 |
|  |  |  |


## Nouvelles fonctionnalités et améliorations

AEM Guides contient de nombreuses améliorations et nouvelles fonctionnalités de la version 4.2 :

### Génération de rapports à partir de l’éditeur Web

AEM Guides s’accompagne d’une fonctionnalité de l’éditeur web qui vous permet de vérifier l’exhaustivité globale de vos documents techniques et de générer des rapports à leur sujet.
Vous pouvez afficher la liste des rubriques et gérer les métadonnées de toutes les références pour la carte actuelle à partir de la
**Rapports** dans l’éditeur Web.

**Génération de la vue Liste des rubriques**

Vous pouvez générer la liste des rubriques qui fournit des informations détaillées sur vos rubriques, telles que le type de référence, l’état du document et l’auteur. Vous pouvez également générer le fichier CSV pour télécharger l’instantané actuel des rubriques dans la carte DITA.

**Gestion des métadonnées et modification de l’état du document**

Vous pouvez appliquer des balises sur une rubrique individuelle ou utiliser la fonction de balisage en masse pour appliquer plusieurs balises sur plusieurs rubriques, un mappage DITA ou un sous-mappage. Vous pouvez également remplacer l’état du document de toutes les rubriques sélectionnées par l’état suivant du document commun.

<img src="assets/web-editor-metadata-panel.png" alt="gestion des métadonnées" width="600">

### UX restructuré pour la fonctionnalité de révision

Désormais, AEM guides fournit un UX amélioré qui vous aide à passer en revue les rubriques partagées en vue de la révision. Dans la dernière expérience, la fonctionnalité de révision présente les améliorations suivantes :

* Interface utilisateur actualisée
* Panneau Conditions qui vous permet de mettre en surbrillance le contenu en fonction des conditions disponibles dans la rubrique.
* Chaque commentaire du panneau des commentaires est associé au texte correspondant dans la rubrique actuelle. Il permet d’identifier le texte commenté.
* Les commentaires sont affichés dans l’ordre du texte commenté dans le document.
* Le nom de la tâche de révision s’affiche dans le workflow de révision.
* Sélectionnez la feuille de route de la tâche de révision utilisée pour résoudre toutes les références clés et tous les termes du glossaire utilisés dans le contenu de la révision.
* Barre d’outils contextuelle qui permet de mettre rapidement le texte en surbrillance ou barré.
* Menu Options pour modifier ou supprimer vos propres commentaires.
* Pour les commentaires obsolètes, vous avez accès à une vue côte à côte qui vous aide à comparer la version précédente de la rubrique à la version de révision actuelle.
* Lorsque vous utilisez les filtres, les commentaires sur le panneau de droite sont filtrés en fonction de la sélection et le nombre de commentaires dans le panneau de gauche est mis à jour en conséquence.


<img alt="tâche de révision" src="assets/comment-pop-up-panel.png" width="600">


Pour plus d’informations, reportez-vous à la section *Révision de rubriques ou de mappages* dans le guide d’utilisation des guides Adobe Experience Manager.

### Améliorations de la traduction

Le tableau de bord Traduction contient désormais plus d’améliorations conviviales qui vous permettent de traduire facilement vos documents à partir de l’éditeur Web.


**Colonne Libellé de version ajoutée au tableau de bord de traduction**

Dans le tableau de bord de traduction, vous pouvez également voir la colonne Libellé de version . Le Libellé de la version sélectionnée du fichier source s’affiche. Vous pouvez ainsi sélectionner tous les fichiers avec un libellé spécifique et les traduire en une seule fois.

**Afficher la différence de version des fichiers désynchronisés depuis le tableau de bord de traduction**

Vous pouvez maintenant vérifier les différences entre la version sélectionnée et la dernière version source traduite des rubriques. Vous pouvez également choisir de traduire le **Désynchronisé** en fonction des modifications apportées entre les deux versions d’une rubrique.

<img src="assets/translation-version-diff.png" alt="forum de traduction" width="600">



**Transmettre le libellé de la version à la version cible**

AEM Guides vous permet de transmettre le libellé du fichier source au fichier cible. Vous pouvez ainsi identifier facilement la version source du fichier traduit.

<img alt="libellés de traduction" src="assets/translation-pass-source-label.png" width="600">

Par exemple, si vous avez des fichiers source auxquels est appliqué le libellé de version Version 1.0, vous pouvez également transmettre le libellé source (Version 1.0) au fichier traduit.

**Forcer la synchronisation pour les ressources désynchronisées**

Si vous apportez des modifications à certaines ressources, AEM Guides les signale comme étant désynchronisés. Vous pouvez soit retraduire les ressources modifiées, soit choisir d’ignorer l’état Désynchronisé . Par exemple, si vous avez apporté des modifications mineures qui n’ont vraiment pas besoin de traduction, vous pouvez marquer leur état comme étant Synchronisé.

**Projets de traduction Afficher en cours pour une rubrique ou une carte**

Certaines des références de votre tableau de bord de traduction peuvent être en cours. Désormais, AEM Guides fournit une fonctionnalité qui vous aide à afficher la liste de tous les projets de traduction en cours (ainsi que la langue cible) qui contiennent la référence sélectionnée.

Pour plus d’informations, reportez-vous à la section *Traduire des documents à partir de l’éditeur Web* dans le guide d’utilisation des guides Adobe Experience Manager.

### Générer une sortie dans divers formats à partir de l’éditeur web

Vous pouvez désormais facilement générer la sortie pour vos rubriques ou mappage DITA à partir de l’éditeur web. Vous pouvez configurer divers paramètres prédéfinis de sortie tels qu’AEM Site, PDF, HTML5, JSON (format de sortie sans interface) et une sortie personnalisée. Utilisez-les pour générer les sorties respectives. Vous pouvez définir des attributs dans vos rubriques DITA, puis utiliser le paramètre prédéfini de condition pour appliquer une condition lors de la publication de la sortie. Vous pouvez également utiliser la fonction de publication de ligne de base pour publier sélectivement une version spécifique de votre mappage ou de votre rubrique DITA.

**Gestion des paramètres prédéfinis de sortie de profil global et de dossier**

AEM Guides vous fournit la fonction permettant de créer et de gérer des paramètres prédéfinis de sortie pour les profils globaux et de dossiers. Vous pouvez ensuite facilement utiliser ces paramètres prédéfinis de sortie pour générer une sortie pour toutes les cartes liées à ce profil Global ou Dossier.

<img alt="ajouter un paramètre prédéfini" src="assets/add-global-output-preset.png" width="400">


Ces paramètres prédéfinis globaux apparaissent sous **Sortie** de toutes les cartes associées. Vous pouvez les utiliser pour générer la sortie pour toutes les cartes associées. Vous pouvez sélectionner le paramètre prédéfini comme paramètre prédéfini de PDF par défaut pour générer la sortie du PDF. Vous pouvez également **Modifier**, **Renommer**, **Dupliquer** ou **Supprimer** un paramètre prédéfini de sortie existant à partir de la fonction **Options** .

>[!NOTE]
>
>Seuls les utilisateurs administratifs de niveau dossier peuvent créer des paramètres prédéfinis de profil global et de dossier.

### Rechercher et remplacer le texte au niveau de la carte

Vous pouvez désormais rechercher des fichiers dans une carte qui contient du texte spécifique. Le texte recherché est mis en surbrillance dans les fichiers. Vous pouvez également remplacer le mot ou l’expression recherché par un autre mot ou expression dans les fichiers. Sélectionnez la **Remplacer une occurrence unique** pour remplacer l’occurrence actuelle et la variable **Remplacer tout dans le fichier** pour remplacer toutes les occurrences dans le fichier sélectionné. Vous pouvez sélectionner **Tout remplacer** pour remplacer toutes les occurrences du terme recherché dans tous les fichiers.

<img src="assets/map-find-replace.png" alt="map find replace" width="600">


Par défaut, les options **Extraction de fichier avant remplacement** et **Créer une version après remplacement** étant sélectionnés, un fichier est extrait avant de remplacer le texte et une nouvelle version est créée après le remplacement du texte. Vous pouvez également rechercher la chaîne dans les références indirectes dans le mappage DITA. Par défaut, cette option est désactivée. La recherche n’est donc effectuée que sur les références directes.

### Mode Mise en page dans l’éditeur de cartes


Vous pouvez désormais afficher la mise en page complète d’un mappage DITA dans l’éditeur de cartes. Lorsque vous ouvrez une carte en vue de la modifier, la vue Disposition de l’éditeur de cartes s’affiche. Dans cette vue, vous pouvez voir la hiérarchie des mappages dans une arborescence. Vous pouvez également modifier, organiser ou structurer les rubriques dans une carte.

<img src="assets/layout-view-map.png" alt=" vue de mise en page des cartes" width="600">

La vue Disposition contient une barre d’outils distincte qui vous permet d’effectuer de nombreuses tâches sur les rubriques présentes dans une carte.
Vous pouvez insérer des références de rubrique, un groupe de rubriques, des définitions de clés dans un mappage. Vous pouvez réorganiser les rubriques présentes dans une carte en les déplaçant vers le haut, le bas, la gauche ou la droite. Vous pouvez également faire glisser et déposer les rubriques pour les déplacer dans une carte. L’éditeur de mappage fournit également les icônes permettant de verrouiller ou de déverrouiller des fichiers, de vérifier l’historique des versions et d’effectuer une gestion des libellés de version.


La vue Disposition fournit également le **Options d’affichage** pour afficher ou masquer le numéro de ligne, afficher ou masquer une case à cocher ou afficher le nom ou le titre du fichier pour les rubriques dans une carte.
Vous pouvez également afficher les rubriques en fonction des filtres conditionnels qui leur sont appliqués.

Outre l’organisation des rubriques dans le fichier de mappage, vous pouvez également ajouter, déplacer, copier, coller ou supprimer des références à l’aide de la variable **Options** pour un élément en mode Mise en page.

<img src="assets/layout-inline-attributes.png" alt=" Attributs de mise en page du mappage" width="600">


Le panneau de droite affiche les propriétés du contenu et les propriétés de mappage dans la vue Disposition de l’éditeur de cartes. Vous pouvez désormais également définir les informations de métadonnées pour les rubriques ou la carte. Vous pouvez définir le titre de navigation, le texte du lien, la description courte et les mots-clés pour la rubrique ou le mappage sélectionné.

Pour plus d’informations, voir *Mode Disposition* dans le guide d’utilisation des guides Adobe Experience Manager.

### Panneau Génération rapide

Désormais, AEM Guides fournit le panneau de génération rapide qui vous permet de générer rapidement et d’afficher la sortie des paramètres prédéfinis créés pour votre mappage DITA.

<img src="assets/quick-generate-map-view.png" alt=" panneau de génération rapide" width="600">

Dans le **Génération rapide** vous pouvez voir la liste de tous les paramètres prédéfinis de sortie créés pour votre mappage DITA. Vous pouvez également afficher rapidement la sortie générée pour les paramètres prédéfinis. Un message de réussite ou d’échec s’affiche à la fin de la génération de sortie. Vous pouvez également afficher le journal des erreurs qui contient les détails de l’erreur survenue dans le processus de génération.

### Création d’une ligne de base dynamique basée sur des étiquettes

Désormais, AEM Guides vous offre la fonctionnalité de création de lignes de base dynamiques basées sur des libellés. Si vous générez une ligne de base, téléchargez une ligne de base ou créez un projet de traduction à l’aide d’une ligne de base, les fichiers sont sélectionnés dynamiquement en fonction des étiquettes mises à jour. Cette fonctionnalité est pratique, car vous n’avez pas à modifier la ligne de base lors de la mise à jour des libellés.

<img src="assets/dynamic-baseline.png" alt=" ligne de base dynamique" width="400">

### Suppression et duplication de fichiers à partir du panneau du référentiel

Vous pouvez désormais facilement supprimer des fichiers (un seul fichier à la fois) du **Options** du fichier sélectionné dans le panneau du référentiel. Une invite de confirmation s’affiche avant de supprimer le fichier. Si le fichier n’est référencé dans aucun autre fichier, il est supprimé et un message de réussite s’affiche.

<img src="assets/options-menu-repo-view-file-level.png" alt="menu des options de fichier " width="500">

Vous pouvez également créer un doublon ou une copie du fichier sélectionné. Par défaut, le fichier est créé avec un suffixe (comme filename_1.extension).


### Autres améliorations apportées à l’éditeur web

* Dans AEM Guides, vous pouvez effectuer certaines opérations courantes pour les images et les fichiers multimédias à l’aide du menu contextuel. Vous pouvez désormais également localiser l’image ou le média sélectionné dans le référentiel ou afficher l’aperçu du fichier dans l’interface utilisateur d’Assets.

* Le nom du profil de dossier actif s’affiche sous forme de libellé pour l’icône Préférences utilisateur dans la barre d’outils principale. Vous pouvez ainsi identifier le profil de dossier sur lequel vous travaillez.

* Lorsque vous ouvrez une carte en mode Carte, le titre de la carte active s’affiche au centre de la barre d’outils principale. Ceci s’avère utile pour indiquer aux utilisateurs quelle carte est actuellement ouverte.

### Purge des versions sélectionnées des fichiers

Lorsque vous créez et conservez votre contenu, de nombreuses versions peuvent être créées pour vos fichiers DITA dans votre référentiel. AEM Guides vous permet de purger les anciennes versions de vos fichiers DITA du référentiel et de libérer de l’espace disque.

<img src="assets/preview-purge-report.png" alt="Aperçu du rapport de purge" width="500">

AEM Guides ne supprime pas la première version du fichier ou une version incluse dans une ligne de base ou à laquelle un libellé est appliqué. L’opération de purge ne supprime même pas les fichiers inclus dans un processus de traduction ou de révision. Vous pouvez choisir le nombre de versions à conserver et choisir de supprimer les fichiers dont la date est antérieure au nombre de jours défini.

Avant de commencer l’opération de purge, vous pouvez prévisualiser le rapport afin d’afficher les versions qui seront purgées. Vous pouvez ensuite décider de lancer ou d’annuler l’opération de purge.

<img src="assets/download-purge-report.png" alt="Rapport Purge de téléchargement PDF" width="500">

Une fois l’opération de purge terminée, vous pouvez vérifier le rapport de purge pour afficher les fichiers purgés.

### Afficher le titre à la place de l’UUID dans l’éditeur Oxygen

Maintenant AEM Guides vous permet de choisir **Utilisation du titre dans l’éditeur et le gestionnaire de cartes** dans Paramètres. Si vous sélectionnez cette option, le titre du fichier s’affiche dans l’onglet du fichier lorsqu’il est ouvert dans l’éditeur ou dans le Gestionnaire de mappages DITA. Si vous ne sélectionnez pas cette option, l’UUID du fichier est affiché dans l’onglet du fichier.

### Interface utilisateur des métadonnées disponible pour les paramètres prédéfinis de PDF

Vous pouvez définir les métadonnées à partir du paramètre prédéfini de sortie d’un mappage DITA. Vous pouvez définir les métadonnées Titre, Auteur, Objet et Mots-clés. Ces métadonnées sont mappées aux métadonnées dans les propriétés de fichier de votre PDF de sortie. Ces métadonnées remplacent les métadonnées définies au niveau du livre. Vous pouvez définir les métadonnées spécifiquement dans chaque paramètre prédéfini de sortie et les transmettre au PDF de sortie.

### PDF natif | PDF avec barre de modification affichant la différence entre les versions de document

Vous pouvez maintenant créer un PDF qui affiche les différences de contenu entre deux versions à l’aide de la barre de modification. Vous pouvez choisir de comparer la version actuelle à une ligne de base de la version précédente ou de comparer les deux versions de ligne de base sélectionnées.

<img src="assets/pdf-change-version.png" alt="pdf-change-version" width="600">

Une barre de modification s’affiche dans le PDF pour indiquer le contenu modifié, inséré ou supprimé. Vous disposez également des options suivantes :
* Afficher le contenu inséré en vert et souligné
* Afficher le contenu supprimé en rouge et marqué d’une barre oblique

### PDF natif | Prise en charge des variables pour Output Path et PDF File Name

Vous pouvez désormais également utiliser les variables d’usine suivantes pour définir le Chemin de sortie et le Fichier de PDF. Vous pouvez utiliser une seule ou une combinaison de variables pour définir ces options :
* ${map_filename}
* ${map_title}
* ${preset_name}
* ${language_code}
* ${map_parentpath} (Uniquement pour le chemin de sortie)
* ${path_after_langfolder} (Uniquement pour le chemin de sortie)

### PDF natif | Générer la table des matières pour les mappages DITA et réorganiser les mises en page

Vous pouvez désormais également générer la table des matières dans les mappages DITA à l’aide d’un paramètre de PDF avancé du modèle. Vous pouvez choisir d’activer ou de désactiver l’affichage des différentes mises en page et de réorganiser leur position.

### PDF natif | Ajout d’un signet personnalisé dans la sortie PDF

Vous pouvez maintenant ajouter un signet personnalisé sur un contenu particulier dans la sortie finale du PDF pour une navigation facile. Cela sera ajouté à la table des matières qui est créée à partir des titres de rubrique ou de section dans votre mappage DITA.

### PDF natif | Application d’un style personnalisé aux entrées de la table des matières et au contenu de la rubrique

AEM Guides fournit la fonctionnalité permettant d’appliquer un style personnalisé aux entrées de la table des matières ou à une rubrique particulière dans la sortie du PDF. Par exemple, vous pouvez modifier la couleur du texte dans la table des matières et le titre de la rubrique. Vous pouvez également appliquer des styles à l’ensemble du contenu dans la rubrique.




## Problèmes résolus

Les bogues résolus dans différentes zones sont répertoriés ci-dessous :

### Création

* Le panneau de gauche se casse lors de l’ajout d’un onglet. (11126)
* Les modifications dans le code HTML de l’éditeur Web entraînent des problèmes avec `<dl>` et `<dlentry>`. (11024)
* Certains attributs ne sont pas traités comme conditionnels et posent des problèmes. (10895)
* Trois niveaux ou plus imbriqués `<indexterm>` ne sont pas imbriqués dans l’exportation de PDF natif. (10799)
* Le contenu disparaît dans le corps d’une tâche lors du passage de la vue Auteur à la vue Source. (10735)
* Les commentaires de révision sont déplacés dans une tâche de révision. (10625)
* `<conref>` remarque à l’intérieur d’une balise para ne s’affiche pas en mode aperçu. (10559)
* Lorsque vous appuyez sur Retour arrière à la fin d’un élément de liste, toute la liste est supprimée. (10540)
* L’écran s’affiche comme vide dans Chrome v106 lors du glisser-déposer d’un élément de l’interface utilisateur (par exemple, dans le panneau Conditions ). (10524)
* Le bouton Retrait automatique est manquant dans la barre d’outils de la **Source** vue. (10448)
* Le premier caractère d’un élément de liste est parfois perdu lorsque la liste est en cours de création dans l’éditeur.( 10447)
* **Annuler** ou **Rétablir** ne fonctionne pas correctement sur certains fichiers. (10373)
* Les métadonnées personnalisées ne sont pas conservées lors de l’action copier-coller. (10367)
* Une erreur se produit lors de la copie (ctrl+c) et du collage (ctrl+v) du contenu. (10304)
* Le panneau Plan n’affiche pas de contenu lorsqu’il est passé du mode Auteur au mode Source. (10296)
* Le sous-mappage n’est pas créé lorsqu’il fait référence à un mappage principal dans les modèles DITA. (10231)
* Les problèmes de navigation se produisent dans l’éditeur web après la mise à niveau vers la version 4.0. (10159)
* L’option Annuler de l’éditeur XML permet à l’utilisateur d’accéder au haut de la page. (10091)
* Les propriétés de noeud sont supprimées après l’opération de copier-coller d’une ressource. (10053)
* Les fichiers de SVG ajoutés aux rubriques DITA ne s’affichent pas en mode aperçu de l’éditeur. (10010)
* Les résultats de recherche pour rechercher et remplacer dans l’éditeur web ne sont pas lisibles en mode sombre. (9978)
* Il n’existe aucun chargeur lors de la création d’une carte à partir du modèle de carte. (9891)
* La référence dans le modèle de rubrique ne fonctionne pas et l’ID de hachage copié n’est pas mis à jour dans la copie de contenu. (9890)
* Aucune option n’est affichée pour parcourir les rubriques ou le modèle de mappage dans les sous-dossiers du dossier de rubrique ou de mappage. (9889)
* Aucune option pour créer un modèle sur les sous-dossiers de rubriques ou de mappages. (9888)
* XML Editor ne met pas à jour les images sur les rubriques. (9500)
* mimeType est codé en dur pour la création et la mise à jour de ressources DITA. (8979)
* Un trait d’union normal est inséré lors de la sélection d’un trait d’union insécable dans le **Insérer un caractère spécial** boîte de dialogue. (8919)
* Le nom du créateur de versions dans l’historique de versions est &quot;fmdita-serviceuser&quot; pour les fichiers chargés via l’interface utilisateur d’Assets. (8910)
* L’option Modifier ne fonctionne pas pour les images lorsque vous utilisez le mode Colonnes de l’interface utilisateur d’Assets. (8758)
* La rubrique DITA n’est pas mise à jour automatiquement avec les modifications effectuées sur **Propriétés** page. (8745)
* Lors du déplacement d’éléments dans la rubrique dans l’éditeur web, les identifiants attribués aux éléments sont remplacés par des identifiants attribués automatiquement. (7895)

### Gestion

* La copie d’une ressource de mappage DITA (à partir de l’interface utilisateur d’Asset ) entraîne des lignes de base erronées dans la ressource copiée. (11218)
* Le message d’avertissement ne s’affiche pas lors du téléchargement d’un fichier qui est supérieur à la limite autorisée dans AEM (2 Go par défaut). (10817)
* Ligne de base de l’éditeur web | Le comportement de la colonne Dernière colonne est différent dans le nouveau tableau de bord de ligne de base de l’éditeur web. (10808)
* Traduction | La tâche de traduction ne démarre pas en raison d’un /libs/fmdita/i18n/ja.json non valide. (10543)
* Traduction | Une erreur se produit dans un projet de traduction de portée créé à partir du tableau de bord de traduction (traduction humaine). (10526)
* Traduction | Le post-traitement est bloqué pour l’ensemble du dossier linguistique dont les ressources sont présentes dans un principal projet de traduction. (10332)
* Traduction| Les métadonnées et les balises ne sont pas propagées aux copies traduites. (4696)
* Plusieurs fenêtres contextuelles s’affichent pour n’importe quelle ressource si la version est modifiée et enregistrée dans l’éditeur de ligne de base. (10399)
* La fuite de session se produit à l’adresse com.day.cq.search.impl.builder.QueryBuilderImpl.createResourceResolver(QueryBuilderImpl.java:210). (10279)
* Le fichier vidéo est absent de la ligne de base si le dossier parent contient de l’espace dans le nom. (10031)

### Publication

* La régénération de rubrique ne fonctionne pas dans certains scénarios. (10635)
* La publication du PDF échoue lors de la génération de la sortie pour un paramètre prédéfini en double (d’un paramètre prédéfini existant). (10584)
* Le bouton Afficher le journal ne fonctionne pas si la génération du PDF échoue pour un paramètre prédéfini. (10576)
* L’écouteur de publication n’affiche pas les données demandées dans les journaux d’informations et contient également des journaux indésirables.( 10567)
* PDF natif | La génération du PDF échoue avec une exception Null Pointer . (10950)
* PDF natif | conkeyref n’est pas résolu dans la sortie générée. (10564)
* PDF natif | Des problèmes se produisent avec les métadonnées d’un mappage qui doit être référencé dans la sortie du PDF.( 10556)
* PDF natif | Des problèmes se produisent lors de la rotation de l’en-tête du tableau. (10555)
* PDF natif | Des problèmes se produisent lors de la suppression des rubriques qui ont un rôle de traitement=&#39;resource-only&#39;. (10554)
* PDF natif | Les clés vides s’affichent en sortie PDF. (10553)
* PDF natif | Imbriqué `<indexterm>` ne sont pas imbriqués dans l’exportation de PDF natif. (10521)
* PDF natif | Le PDF natif utilise le style intégré au lieu du nom de classe pour les balises générées. (10498)
* PDF natif | La référence de topicref imbriquée dans les appendices est toutes transformée en h1 dans le HTML temporaire.( 10454)
* PDF natif | Impossible de masquer les rubriques de première ligne de la table des matières. (10355)
* PDF natif | L’attribut de cadre de tableau n’est pas propagé au HTML temporaire (en tant que classe). (10353)
* PDF natif | Les fichiers de HTML temporaires ajoutent les classes colsep et rowsep à <td> et <th> même si leur valeur est 0 dans le DITA source. (10352)
* PDF natif | Le redémarrage des numéros de page dans la mise en page de chapitre commence aléatoirement la numérotation à partir de la fin du chapitre précédent. (10154)
* PDF natif | Les références clés des clés avec des liens d’image ou externes ne sont pas résolues. (10063)
* PDF natif | L’annexe s’affiche sous la forme d’un chapitre dans le PDF généré. (9829)
* L’onglet Modèle de l’éditeur xml n’est pas affiché pour les administrateurs de profil de dossier. (10266)
* La publication de ligne de base échoue pour le PDF généré à l’aide de FrameMaker Publishing Server 2020. (10551)
* Une erreur d’application se produit lorsque vous cliquez sur le bouton Modifier après avoir sélectionné tous les paramètres prédéfinis via la case Paramètres prédéfinis de sortie dans la fenêtre contextuelle Génération rapide . (10388)
* Si l’onglet Sortie de l’éditeur web comporte davantage de paramètres prédéfinis, la section Paramètres prédéfinis ne peut pas être défilée verticalement et n’affiche pas tous les paramètres prédéfinis disponibles. (9787)
* Impossible de supprimer les paramètres prédéfinis du workflow de sortie lors de la publication via l’éditeur. (9100)
* Le lien d’homologue est rendu sous forme de texte normal au lieu d’un lien sur la page générée. (7774)

### Problème connu

Adobe a identifié le problème connu suivant pour la version 4.2 d’AEM Guides :

* Les utilisateurs peuvent effectuer des opérations de révision même une fois la tâche de révision terminée.

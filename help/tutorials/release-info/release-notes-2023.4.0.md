---
title: Notes de mise à jour | Adobe Experience Manager Guides as a Cloud Service, version d’avril 2023
description: Dernière version des guides Adobe Experience Manager as a Cloud Service
source-git-commit: 77b118655ad8e37e00b0371497e4a2578ddd276e
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 2%

---

# Version d’avril des guides Adobe Experience Manager as a Cloud Service

## Mise à niveau vers la dernière version

Mettez à niveau vos guides Adobe Experience Manager actuels as a Cloud Service (plus tard appelés *AEM Guides as a Cloud Service*) en procédant comme suit :

1. Extrayez le code Git des Cloud Services et passez à la branche configurée dans le pipeline Cloud Services correspondant à l’environnement que vous souhaitez mettre à niveau.
2. Mettre à jour `<dox.version>` dans `/dox/dox.installer/pom.xml` du code Git Cloud Services vers la version 2023.4.249.
3. Validez les modifications et exécutez le pipeline Cloud Services pour effectuer la mise à niveau vers la dernière version d’AEM Guides as a Cloud Service.

## Étapes d’indexation du contenu existant (uniquement si vous utilisez une version antérieure à la version de septembre des AEM Guides as a Cloud Service)

Effectuez les étapes suivantes pour indexer le contenu existant et utiliser le nouveau texte de recherche et de remplacement au niveau de la carte :

* Exécutez une requête de POST sur le serveur (avec l’authentification correcte) - `http://<server:port>/bin/guides/map-find/indexing`.
(Facultatif) Vous pouvez transmettre des chemins d’accès spécifiques des cartes pour les indexer ; par défaut, toutes les cartes seront indexées. || Exemple : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* L’API renvoie un jobId. Pour vérifier l’état de la tâche, vous pouvez envoyer une demande de GET avec l’ID de la tâche au même point de terminaison : `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Par exemple : http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Une fois la tâche terminée, la requête de GET ci-dessus répond avec succès et indique si une correspondance a échoué. Les mappages indexés avec succès peuvent être confirmés à partir des journaux du serveur.

## Matrice de compatibilité

Cette section répertorie le tableau de compatibilité des applications logicielles prises en charge par AEM Guides as a Cloud Service d’avril 2023.

### FrameMaker et FrameMaker Publishing Server

| AEM Guides as a Cloud | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.04.0 | Non compatible | 2022 ou version ultérieure |
|  |  |  |


### Connecteur Oxygen

| AEM Guides as a Cloud | Fenêtres du connecteur Oxygen | Mac du connecteur Oxygen | Modifier sous Windows Oxygen | Modifier dans Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023.04.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


## Nouvelles fonctionnalités et améliorations

AEM Guides as a Cloud Service fournit des améliorations et de nouvelles fonctionnalités dans la dernière version :

### Prise en charge avancée des métadonnées dans la publication dans PDF

AEM Guides fournit désormais une prise en charge avancée des métadonnées mappées aux métadonnées dans la sortie de votre PDF. Les options de métadonnées incluent des informations sur le document et son contenu, telles que le nom de l’auteur, le titre du document, les mots-clés, les informations de copyright et d’autres champs de données.

<img src="assets/pdf-metadata.png" alt=" métadonnées pdf natives">

Vous pouvez importer un fichier XMP et AEM Guides peuvent sélectionner les informations du fichier. Vous avez également la possibilité de fournir les noms et valeurs des métadonnées à l’aide de la liste déroulante. Vous pouvez également ajouter des métadonnées personnalisées en saisissant directement dans le champ du nom.


### Panneau Aperçu amélioré

AEM Guides fournit un panneau d’aperçu improvisé dans lequel vous obtenez une vue hiérarchique des éléments utilisés dans le document.

<img src="assets/select-element-content-outline-view_cs.png" alt=" métadonnées pdf natives">

La vue Plan comprend les améliorations suivantes :

* La liste déroulante Options d’affichage s’affiche en haut du panneau Vue synchrone. Si un élément comporte un identifiant, un attribut et du texte, vous pouvez les sélectionner dans la liste déroulante pour les afficher avec l’élément . Les attributs qui peuvent s’afficher dans le panneau Vue synchrone sont déterminés par les paramètres Attributs d’affichage configurés par votre administrateur dans la variable **Paramètres de l’éditeur**.

* La fonction de recherche vous permet de rechercher un élément par son nom, son identifiant, son texte ou sa valeur d’attribut.


### Publication basée sur un microservice pour AEM Guides as a Cloud Service

AEM Guides as a Cloud Service permet d’exécuter des charges de travail de publication volumineuses simultanément avec la publication basée sur un microservice et d’exploiter la plate-forme sans serveur Adobe I/O Runtime de pointe.

Dans la version d’avril, vous pouvez désormais exécuter plusieurs demandes de publication simultanément et générer des sorties de PDF en masse très efficacement à l’aide de la publication de PDF natif basée sur un microservice.
Pour plus d’informations, voir [Configuration de la nouvelle publication basée sur un microservice pour AEM Guides as a Cloud Service](../knowledge-base/publishing/configure-microservices.md).


## Problèmes résolus

Les bogues résolus dans différentes zones sont répertoriés ci-dessous :

* PDF natif | La publication de contenu comportant une classe de sortie avec crochets () entraîne un gel de publication. (11596)
* Le problème survient lors du déplacement (par glisser-déposer) à la place d’un élément de liste existant sur lequel le suivi des modifications est activé. (11570)
* Le problème se produit lors du déplacement (par glisser-déposer) en tant que nouvel élément de liste avec le suivi des modifications activé. (11569)
* Les éléments de la liste de retrait ou de retrait ne fonctionnent pas comme prévu lorsque le suivi des modifications est activé. (11568)
* L’ajout de contenu sur une ligne avec le suivi des modifications activé, puis la désactivation du suivi des modifications ne la désactive pas. (11567)
* Difficulté à faire glisser et déposer un élément de liste, le texte est déplacé à la place de l’élément de liste. (11566)
* La révision terminée ne s’ouvre pas en mode lecture seule. (11387)
* Le problème se produit dans AEM recherche de site (ne fonctionne pas au-delà des noeuds de 2 à 3 niveaux). (11352)
* Lors de la création dans l’élément affiché en vert (Suivi des modifications), le nouveau contenu s’affiche comme suivi des modifications, même si le suivi des modifications est désactivé. (7021)

### Problème connu avec la solution de contournement

Adobe a identifié le problème connu suivant pour la version d’avril 2023 d’AEM Guides as a Cloud Service.

* PDF natif | Les anciennes métadonnées ne sont pas renseignées tant que le paramètre prédéfini de sortie n’est pas ouvert explicitement.


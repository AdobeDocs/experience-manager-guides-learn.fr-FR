---
title: Notes de mise à jour | Adobe Experience Manager Guides as a Cloud Service, version de mars 2023
description: Dernière version des guides Adobe Experience Manager as a Cloud Service
source-git-commit: 07709048f560a77b923436d990c831a5f8b907e3
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 2%

---

# Version de mars des guides Adobe Experience Manager as a Cloud Service

## Mise à niveau vers la dernière version

Mettez à niveau vos guides Adobe Experience Manager actuels as a Cloud Service (plus tard appelés *AEM Guides as a Cloud Service*) en procédant comme suit :
1. Extrayez le code Git des Cloud Services et passez à la branche configurée dans le pipeline Cloud Services correspondant à l’environnement que vous souhaitez mettre à niveau.
2. Mettre à jour `<dox.version>` dans `/dox/dox.installer/pom.xml` du code Git Cloud Services vers la version 2023.3.242.
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

Cette section répertorie le tableau de compatibilité des applications logicielles prises en charge par AEM Guides as a Cloud Service de mars 2023.

### FrameMaker et FrameMaker Publishing Server

| AEM Guides as a Cloud | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.03.0 | Non compatible | 2022 ou version ultérieure |
|  |  |  |


### Connecteur Oxygen

| AEM Guides as a Cloud | Fenêtres du connecteur Oxygen | Mac du connecteur Oxygen | Modifier sous Windows Oxygen | Modifier dans Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023.03.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


## Nouvelles fonctionnalités et améliorations

AEM Guides as a Cloud Service fournit des améliorations et de nouvelles fonctionnalités dans la dernière version :

### Ouverture et lecture de fichiers vidéo ou audio dans l’éditeur web

AEM Guides fournit désormais la fonctionnalité permettant d’ouvrir et de lire les fichiers audio ou vidéo dans l’éditeur web. Vous pouvez modifier le volume ou l’affichage de la vidéo. Dans le menu contextuel, vous avez également la possibilité de **Télécharger**, modifier **Lecture de la vitesse** ou afficher **Image dans l’image**.

<img src="assets/video-web-editor.png" alt="vidéo de lecture" width="600">


## Problèmes résolus

Les bogues résolus dans différentes zones sont répertoriés ci-dessous :

* Le processus du PDF de téléchargement ne fonctionne pas correctement dans l’éditeur web. (11496)
* Sortie JSON | Métadonnées de carte dont la valeur de propriété est `"value in spaces and double quotes"` génère une erreur de publication. (11438)
* L’insertion des fichiers multimédia audio et vidéo échoue au format YouTube sous le **Insérer du contenu multimédia** icône . (11320)
* Une erreur de validation se produit lorsqu’une map est créée à l’aide du modèle qui comporte un élément de titre spécialisé. (11212)
* PDF natif | La note de bas de page présente dans l’en-tête du tableau pour afficher le texte en gras aligné au centre dans le pied de page correspondant dans la sortie du PDF. (10610)
>[!NOTE]
>
>Pour refléter la modification du PDF natif, supprimez le dossier du PDF situé à l’emplacement /content/dam/dita-templates, puis effectuez la mise à niveau vers le dernier build. (10610)

### Problème connu avec la solution de contournement

Adobe a identifié le problème connu suivant pour AEM Guides version as a Cloud Service de mars 2023.

* Les utilisateurs ne peuvent pas enregistrer ni créer de version d’une ressource dupliquée.

**Solution**: Avant d’apporter des modifications à la ressource en double, retraitez-la à partir de l’interface utilisateur d’Assets.


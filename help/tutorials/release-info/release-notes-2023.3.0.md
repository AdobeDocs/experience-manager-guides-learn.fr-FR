---
title: Notes de mise à jour | Adobe Experience Manager Guides as a Cloud Service, version de mars 2023
description: Version de mars des guides Adobe Experience Manager as a Cloud Service
source-git-commit: 99ca14a816630f5f0ec1dc72ba77994ffa71dff6
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 1%

---


# Version de mars 2023 des Guides Adobe Experience Manager as a Cloud Service

Cette note de mise à jour traite des instructions de mise à niveau, de la matrice de compatibilité et des problèmes résolus dans la version de mars 2023 des Guides Adobe Experience Manager (appelée ultérieurement *AEM Guides as a Cloud Service*).

Pour plus d’informations sur les nouvelles fonctionnalités et améliorations, voir [Nouveautés de la version de mars 2023 d’AEM Guides as a Cloud Service](whats-new-2023.3.0.md).

## Mise à niveau vers la version de mars 2023

Mettez à niveau votre configuration as a Cloud Service actuelle AEM Guides en procédant comme suit :
1. Extrayez le code Git des Cloud Services et passez à la branche configurée dans le pipeline Cloud Services correspondant à l’environnement que vous souhaitez mettre à niveau.
2. Mettre à jour `<dox.version>` dans `/dox/dox.installer/pom.xml` du code Git Cloud Services vers la version 2023.3.242.
3. Validez les modifications et exécutez le pipeline Cloud Services pour effectuer la mise à niveau vers la version de mars 2023 d’AEM Guides as a Cloud Service.

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



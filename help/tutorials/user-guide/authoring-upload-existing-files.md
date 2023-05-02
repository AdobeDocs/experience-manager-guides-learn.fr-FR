---
title: Charger des fichiers
description: Découvrez comment télécharger des fichiers
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 4%

---


# Charger des fichiers {#id176FF000JUI}

Il est probable que vous disposiez d’un référentiel de contenu DITA existant que vous souhaitez utiliser avec AEM Guides. Pour ce contenu existant, vous pouvez utiliser l’une des méthodes suivantes pour charger en masse votre contenu dans AEM référentiel :

>[!IMPORTANT]
>
> Voir [Ajout de ressources numériques à Adobe Experience Manager as a Cloud Service Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html) pour plus d’informations, voir les méthodes de chargement de contenu prises en charge dans AEM.

## Interface utilisateur de la console de ressources

Vous pouvez sélectionner du contenu sur votre bureau et le faire glisser sur l’interface utilisateur d’AEM \(navigateur web\) vers le dossier de destination. Pour plus d’informations, voir [Chargement de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html#upload-assets) dans AEM documentation.

## Application de bureau AEM

Utilisez AEM’appli de bureau si vous êtes un professionnel de la création et souhaitez gérer les ressources sur votre ordinateur local. Vous pouvez ouvrir et modifier ces ressources à l’aide de vos applications de bureau. Vous pouvez également conserver des versions et partager vos fichiers avec d’autres utilisateurs. Pour plus d’informations, voir [Application de bureau AEM](https://experienceleague.adobe.com/docs/experience-manager-desktop-app/using/using.html?lang=fr).

## Outil d’ingestion en masse de ressources

Si vous disposez de migrations à grande échelle et d’assimilations en masse occasionnelles, utilisez l’outil d’ingestion en masse des ressources pour charger votre contenu. Grâce à cet outil, vous pouvez charger du contenu en masse à partir de banques de données prises en charge telles qu’Azure ou S3. Pour plus d’informations, voir [Ingestion en masse de ressources](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=en#asset-bulk-ingestor).

## Utilisation de FrameMaker pour le transfert en masse

Adobe FrameMaker est fourni avec un puissant connecteur d’AEM qui vous permet de télécharger facilement votre DITA existant et d’autres documents FrameMaker \(`.book` et `.fm`\) dans AEM. Vous pouvez utiliser différentes fonctionnalités de chargement de fichier, telles que le chargement d’un seul fichier, le chargement d’un dossier complet avec ou sans dépendances \(comme les références de contenu, les références croisées et les graphiques\).

Pour plus d’informations sur l’utilisation de la fonctionnalité de chargement en masse dans FrameMaker, reportez-vous à la section . *Création d’un dossier CRX et chargement de fichiers* dans le Guide de l’utilisateur de FrameMaker.

## Gestion des erreurs lors du chargement de contenu {#id201MI0I04Y4}

En cas d’échec du chargement d’un ou de plusieurs fichiers, une invite s’affiche à la fin du processus de chargement avec une liste des fichiers dont le chargement a échoué :

![](images/uuid-files-failed-to-upload_cs.png){width="650" align="center"}

Pour plus d’informations sur les différents scénarios de téléchargement de fichiers, voir [Chargement du contenu DITA](authoring-file-management.md#).

Si vous utilisez un outil tel que l’appli de bureau AEM ou l’outil d’assimilation en masse de ressources, l’action à effectuer sur un fichier en double est contrôlée par un paramètre du serveur AEM. Contactez votre administrateur système pour connaître cette configuration.

**Rubrique parente :**[ Gestion du contenu](authoring.md)

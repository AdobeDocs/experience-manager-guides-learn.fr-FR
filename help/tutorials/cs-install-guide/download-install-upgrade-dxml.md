---
title: Mise à niveau AEM guides
description: Découvrez comment mettre à niveau AEM guides
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# Mise à niveau AEM guides {#id213BD050YPH}

1. Accédez au référentiel Git de Cloud Manager.

1. Mettez à jour le fichier dox/dox.installer/pom.xml .

1. Mettez à jour la valeur de la variable dox.version vers les détails de version fournis par Adobe.

1. Validez les modifications et exécutez le pipeline Cloud Manager pour déployer le package mis à niveau.


>[!NOTE]
>
> Pour plus d’informations sur l’utilisation du pipeline CI/CD, voir [Utilisation du pipeline CI/CD dans Adobe Cloud Manager](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/cloud-manager/use-the-cicd-pipeline-in-cloud-manager-for-aem.html).

## Effacer le cache du navigateur

Une fois le processus de mise à niveau terminé, tous les utilisateurs doivent vider le cache du navigateur avant d’utiliser la version mise à niveau des AEM Guides.

**Rubrique parente :**[ Télécharger et installer](download-install.md)

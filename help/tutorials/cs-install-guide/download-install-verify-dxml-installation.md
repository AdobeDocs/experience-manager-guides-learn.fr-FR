---
title: Vérification de l’installation AEM Guides
description: Découvrez comment vérifier l’installation des AEM Guides
source-git-commit: 6051181e243cf71919901093c1b5590f21832545
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 5%

---


# Vérification de l’installation AEM Guides {#id213BD030FBE}

Une fois que vous avez installé AEM Guides, vous devez vérifier si l’installation a réussi ou non. Effectuez les étapes suivantes pour vérifier l’installation :

1. Accédez à Developer Console de votre Cloud Service.

   Pour plus d’informations sur l’accès à Developer Console, voir [Accès à Developer Console](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/developer-console.html?lang=fr) dans AEM documentation.

1. Accédez à la liste des lots OSGi dans AEM.

   Pour plus d’informations sur l’accès aux lots, voir [Lots](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/developer-console.html?lang=en#bundles) dans AEM documentation.

1. Recherchez fmdita dans la liste des lots et vérifiez son état.

   L’état doit s’afficher. *Principal* pour les lots déployés avec succès. Si l’un des lots ne dispose pas d’un état Principal, vérifiez les journaux d’AEM pour résoudre le problème d’installation.


**Rubrique parente :**[ Télécharger et installer](download-install.md)


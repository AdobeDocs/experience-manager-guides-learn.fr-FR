---
title: Configuration d’une invite pour l’enregistrement en tant que nouvelle version à la fermeture
description: Découvrez comment configurer une invite pour enregistrer en tant que nouvelle version à la fermeture.
source-git-commit: 801c306fa120e7889d4b9428fd5bee2849bf1956
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# Configuration d’une invite pour l’enregistrement en tant que nouvelle version à la fermeture {#id222HBI00XXA}

Lorsque l’utilisateur tente de fermer un fichier ouvert dans l’éditeur Web à l’aide de la fonction **Fermer** dans l’onglet du fichier ou dans la fonction **Fermer** dans le menu Options, une boîte de dialogue s’affiche si le fichier contient des données non enregistrées ou une version non enregistrée. L’utilisateur est invité à enregistrer le fichier en tant que nouvelle version si la version n’est pas enregistrée.

Le **Enregistrer comme nouvelle version** n’est pas activée par défaut et vous devez l’activer à partir de configMgr. Effectuez les étapes suivantes pour activer l’option par défaut dans l’éditeur web :

1. Ouvrez la page Configuration de la console web Adobe Experience Manager .

   L&#39;URL par défaut pour accéder à la page de configuration est :

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Recherchez et cliquez sur le bouton **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** du lot.

1. Sélectionnez la **Demander la nouvelle version à fermeture** .

1. Cliquez sur **Enregistrer**.


Lorsque cette option est sélectionnée, la variable **Enregistrer comme nouvelle version** est sélectionnée par défaut dans la boîte de dialogue.

Pour plus d’informations, voir *Fermeture du fichier et enregistrement des scénarios* dans le guide as a Cloud Service Utilisation des guides Adobe Experience Manager .

**Rubrique parente :**[ Personnalisation de l’éditeur web](conf-web-editor.md)

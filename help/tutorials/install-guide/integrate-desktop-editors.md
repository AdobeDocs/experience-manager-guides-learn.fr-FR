---
title: Intégration d’éditeurs XML de bureau
description: Découvrez comment intégrer des éditeurs XML de bureau
source-git-commit: 5ac066bb8db32944abd046f64da11eeb1bdbe467
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# Intégration d’éditeurs XML de bureau {#id181GB01G0HS}

Il y a beaucoup d&#39;éditeurs XML disponibles sur le marché, et vous pourriez déjà en utiliser un. Adobe FrameMaker est l’un des éditeurs XML les plus puissants, qui est fourni avec AEM connecteur. Grâce au connecteur d’AEM dans FrameMaker, vous pouvez facilement vous connecter au référentiel AEM, extraire et archiver des fichiers et modifier des fichiers directement dans FrameMaker. Vous pouvez également configurer AEM Guides pour lancer FrameMaker à partir de l’éditeur web. Une fois le fichier ouvert dans FrameMaker, vous pouvez le modifier et le réarchiver dans le référentiel AEM.

## Activation de l’édition de fichiers dans FrameMaker à partir de l’éditeur web

Vous pouvez utiliser FrameMaker ou tout autre éditeur DITA pour créer et mettre à jour du contenu DITA. Cependant, si votre entreprise utilise FrameMaker comme éditeur DITA, vous pouvez donner à vos utilisateurs la possibilité d’ouvrir des documents DITA directement dans FrameMaker depuis AEM.

Par défaut, vos utilisateurs ne voient pas le **Ouvrir dans FrameMaker** dans la barre d’outils AEM. Procédez comme suit pour ajouter ce bouton dans la barre d’outils AEM :

1. Ouvrez la page Configuration de la console web Adobe Experience Manager .

   L&#39;URL par défaut pour accéder à la page de configuration est :

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Recherchez et cliquez sur le bouton **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** du lot.

   ![](assets/open-in-fm-toolbar.png){width="550" align="left"}

1. Sélectionnez la **Afficher l’ouverture dans le bouton FrameMaker** .

1. Cliquez sur **Enregistrer**.


Lorsque vous activez la variable **Afficher l’ouverture dans le bouton FrameMaker** , puis la variable **Ouvrir dans FrameMaker** s’affiche lors de la sélection d’un fichier DITA dans le référentiel AEM. Lorsque cette option est *not enabled*, la variable **Ouvrir dans FrameMaker** s’affiche uniquement lorsque vous sélectionnez un fichier .fm ou .livre dans le référentiel.


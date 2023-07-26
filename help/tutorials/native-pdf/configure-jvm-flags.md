---
title: PDF natif | Configuration des indicateurs JVM pour la publication native de PDF
description: Configuration des indicateurs JVM pour la publication native de PDF
source-git-commit: cfb1197d0aad7ea3771bc6e1a73c02f540cef0c9
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---


# Configuration des indicateurs JVM pour la publication native de PDF

La publication d’un PDF natif lance un processus JVM distinct pour générer un PDF. Vous devrez peut-être ajuster les configurations de cette JVM pour prendre en charge différents scénarios. Par exemple, pour exécuter des charges de travail plus volumineuses, vous devez augmenter la taille maximale du tas disponible pour le processus JVM engendré.

Effectuez les étapes suivantes pour configurer AEM Guides Native PDF Publishing JVM indicateurs :

1. Ouvrez la page Configuration de la console web Adobe Experience Manager .

   L&#39;URL par défaut pour accéder à la page de configuration est :

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Recherchez et sélectionnez le *com.adobe.config.ConfigManager* du lot.

1. Mettre à jour la propriété **Options de ligne de commande Java pour le pdf natif** (*native.pdf.java.opts*) pour transmettre des indicateurs JVM standard.



1. Cliquez sur **Enregistrer**.
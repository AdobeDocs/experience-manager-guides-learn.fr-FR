---
title: Configuration du nombre de LimitReads pour une requête
description: Découvrez comment configurer le nombre de limites de lecture pour une requête
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---

# Configuration du nombre de LimitReads pour une requête {#id231RC0HL0ID}

Pour augmenter le nombre de noeuds qu’une requête peut lire à la fois, procédez comme suit :

1. Ouvrez la page JMX de la console web Adobe Experience Manager.

   L&#39;URL par défaut pour accéder à la page de configuration est :

   ```http
   http://<server name>:<port>/system/console/jmx
   ```

1. Recherchez et cliquez sur **QueryEngineSettings**.

1. Modifiez la valeur d’attribut pour la variable **LimitReads** attribut.

1. Cliquez sur **Enregistrer**.


Lorsque vous augmentez cette valeur d’attribut, vous pouvez générer le rapport pour les mappages DITA plus volumineux.

**Rubrique parente :**[ Personnalisation de l’éditeur web](conf-web-editor.md)

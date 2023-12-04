---
title: Remplacements de configuration
description: Découvrez comment remplacer les configurations
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# Remplacements de configuration {#id216IFC003XA}

Pour effectuer toute mise à jour de configuration, l’approche générique suivante doit être utilisée :

1. Accédez au référentiel Git de Cloud Manager.

1. Créez un fichier JSON à l’emplacement suivant :

   src/main/content/jcr\_root/apps/fmditaCustom/config/

1. Nommez le fichier au format suivant :

   $\{PID\}.cfg.json

   Ici, le PID est l’ID de processus de la configuration.

1. Ajoutez des propriétés dans le fichier JSON au format suivant :

   ```
   {
      "aem.adminuname": "updatedUserjson",
      "valid.characters": "[-a-zA-Z0-9_@$]",
      "dita.serialization": true
   }
   ```

1. Validez les modifications et exécutez le pipeline Cloud Manager pour déployer la configuration mise à jour.


**Rubrique parente :**[ Télécharger et installer](download-install.md)

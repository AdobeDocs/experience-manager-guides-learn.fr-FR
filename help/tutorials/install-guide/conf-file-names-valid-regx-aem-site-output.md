---
title: Configuration de noms de fichier valides pour AEM sortie Site
description: Découvrez comment configurer des noms de fichier valides pour AEM sortie Site
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Configuration de noms de fichier valides pour AEM sortie Site {#id214GK0X0KXA}

Tout comme la liste des caractères de nom de fichier valides autorisés pour les rubriques DITA, vous pouvez configurer une liste de caractères de nom de fichier valides pour AEM sortie Site. Voici quelques-uns des caractères connus qui ne sont pas autorisés dans une URL : ```'<>`@$```. Ces caractères sont configurés pour être automatiquement convertis en traits de soulignement &quot;_&quot; lorsqu’ils sont détectés lors de la génération AEM noms de fichiers de sortie de site. La configuration qui vous permet de définir des caractères valides dans AEM sortie Site est présente dans la variable `com.adobe.fmdita.common.SanitizeNodeNameImpl` du lot. **Définition du jeu de caractères non autorisé pour la publication sur AEM Sites** pour inclure les caractères que vous souhaitez remplacer par un trait de soulignement dans les noms de fichiers de sortie Site AEM.

**Rubrique parente :**[ Configuration des noms de fichier](conf-file-names.md)

---
title: Recommendations pour l’optimisation des performances
description: Découvrez Recommendations pour l’optimisation des performances
source-git-commit: 6051181e243cf71919901093c1b5590f21832545
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 3%

---


# Recommendations pour l’optimisation des performances {#id213BD0JG0XA}

Pour optimiser les performances, tenez compte des points suivants :

- Pour optimiser le contenu et l’indexation, voir [Optimisation de la recherche et de l’indexation de contenu](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=fr) dans AEM documentation.

- Correction de Xerces Jar lors de l’utilisation de DITA-OT personnalisé pour la publication. Cette configuration est obligatoire, selon votre cas d’utilisation. Cette modification n’est requise que si vous utilisez le code DITA-OT personnalisé pour la publication de la sortie.

  *Configuration requise*: Remplacez le fichier Xerces Jar dans votre package DITA-OT personnalisé par celui fourni en standard. Le fichier OOTB par défaut xercesImpl-2.11.0.jar est disponible dans le fichier /libs/fmdita/dita\_resources/DITA-OT.zip . Veillez à renommer le fichier xercesImpl-2.11.0.jar pour qu’il corresponde à l’ancien fichier Xerces Jar remplacé. Cela peut être effectué au moment de l’exécution.

  Cette modification réduit le temps de publication et l’utilisation de la mémoire lors de la publication de mappages DITA avec un grand nombre de rubriques.


**Rubrique parente :**[ Télécharger et installer](download-install.md)


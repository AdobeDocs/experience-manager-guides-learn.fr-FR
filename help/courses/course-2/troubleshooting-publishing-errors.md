---
title: Dépannage des erreurs de publication
description: Dépannage des erreurs de publication dans [!DNL Adobe Experience Manager Guides]
exl-id: b37ea3e7-59cf-4fc5-8fae-e1fadd26f8d8
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Dépannage des erreurs de publication

La publication d’une carte est généralement simple. Ouvrez la carte, sélectionnez un paramètre prédéfini de sortie et générez la sortie. Cependant, si une carte ou ses rubriques comportent des erreurs, la génération de sortie peut échouer. Dans ce cas, il est important de savoir comment résoudre les problèmes.

>[!VIDEO](https://video.tv.adobe.com/v/338990)

## Préparation de l’exercice

Vous pouvez télécharger des fichiers d’exemple pour l’exercice ici.

[Exercise-Download](assets/exercises/publishing-basic-to-advanced.zip)

## Causes courantes des erreurs de publication

Des erreurs peuvent être introduites dans le contenu source. Par exemple :

* Référence de chemin de fichier mal nommée

* Dossier mal nommé

* Graphique ou fichier manquant

* Référence de contenu mal configurée

* Référence croisée rompue

* Erreurs dans les valeurs d’un attribut (par exemple, une chaîne plutôt qu’un nombre)

* Configuration incorrecte des composants utilisés par [!DNL AEM Guides]

## Impact des erreurs

Une erreur peut être mineure et se traduire par une simple note vous informant qu’un fichier n’a pas été correctement empaqueté ou suffisamment grave pour entraîner l’échec complet de la génération de la sortie. L’onglet Sorties affiche des icônes codées par couleur afin d’afficher les performances, les erreurs ou les échecs liés à la génération de la sortie.

![error-impact](images/error-impact.png)

## Ouverture et révision des logs d’erreur

Le fichier journal généré peut être ouvert pour révision.

1. Dans le **Sorties** , cliquez sur l’onglet **date/heure sous Généré à.**

   ![error-log](images/error-log.png)

2. Faites défiler le journal des erreurs.

## Affichage et masquage des types d’erreur

Le journal des erreurs affiche chaque type d’erreur dans une couleur unique.

![navigate-errors](images/navigate-errors.png)

1. **Sélectionner** ou **désélectionner** tout type d’erreur pour afficher ou masquer la mise en surbrillance.

2. Parcourez les erreurs à l’aide de la variable **next** ou **previous** boutons (flèches).

## Résolution des erreurs

Selon le type d’erreur, la résolution peut être simple ou complexe. Il peut être terminé par un auteur dans l’éditeur XML ou demander à un administrateur de travailler avec [!DNL AEM Guides]. Les corrections spécifiques dépendent de l’erreur, de l’impact et des workflows de votre organisation.

* Référence de chemin de fichier mal nommée

       Les auteurs peuvent mettre à jour la référence au chemin dans le document source.
       
   
* Dossier mal nommé

       Les auteurs peuvent mettre à jour le nom du dossier ou déplacer les fichiers si nécessaire.
       
   
* Graphique ou fichier manquant

       Les auteurs peuvent charger un graphique/fichier manquant, renommer un fichier/graphique ou déplacer un fichier
       
   
* Référence de contenu mal configurée

       Les auteurs peuvent corriger l’emplacement du contenu référencé ou modifier le chemin d’accès à la référence du contenu.
       
   
* Référence croisée rompue

       Les auteurs peuvent corriger l’emplacement vers lequel pointe la référence croisée ou modifier le nom ou les propriétés du fichier de destination.
       
   
* Erreurs dans les valeurs d’un attribut (par exemple, une chaîne plutôt qu’un nombre)

       Les auteurs peuvent mettre à jour l’attribut vers une valeur correcte ou les administrateurs peuvent mettre à jour le système pour prendre en charge de nouvelles valeurs.
       
   
* Configuration incorrecte des composants utilisés par [!DNL AEM Guides]

       Les administrateurs peuvent mettre à jour l’installation du système, de ses composants ou des autorisations.
       
   
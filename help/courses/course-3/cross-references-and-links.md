---
title: Références croisées et liens
description: Création de références croisées et de liens dans AEM Guides
exl-id: bee7d50f-cbdd-4ac8-b15b-101febc4ae80
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Références croisées et liens

L’éditeur XML et le DITA offrent un moyen puissant de lier les différentes rubriques. Il est important de gérer efficacement vos références de contenu, notamment en utilisant des valeurs d’identifiant uniques.

Des exemples de fichiers que vous pouvez choisir d’utiliser pour cette leçon sont fournis dans le fichier .
[crossreferencesandlinks.zip](assets/crossreferencesandlinks.zip)

>[!VIDEO](https://video.tv.adobe.com/v/342764?quality=12&learn=on)

## Création d’une référence croisée à une rubrique externe

Il est possible de créer une référence croisée externe en faisant glisser une rubrique du référentiel vers un fichier ouvert. Cependant, pour éviter les références croisées rompues, un identifiant doit d’abord être défini sur une valeur liée à l’élément parent. Il s’agit d’un moyen simple de créer une référence croisée tout en s’assurant que les identifiants sont correctement attribués.

1. Ouvrez un fichier dans lequel vous souhaitez insérer une référence croisée externe.

1. Attribuez un identifiant à l’élément à référencer.

   a. Cliquez à l’intérieur de l’élément .

   b. Dans le panneau Propriétés du contenu, sélectionnez **ID** dans la liste déroulante Attribut.

   c. Saisissez un nom logique dans le champ Valeur .

   d. Affichez l’élément et sa valeur dans la **vue hiérarchique** si vous le souhaitez.

1. **Enregistrez** la rubrique pour vous assurer que le référentiel dispose de l’ID mis à jour.

1. Cliquez sur l’icône [!UICONTROL **Référence**] dans la barre d’outils supérieure.

   ![Barre d’outils](images/lesson-7/references-icon.png)

1. Dans l’onglet **Référence du contenu**, sélectionnez l’association de l’ID et de l’élément à insérer comme référence croisée.

1. Cliquez sur [!UICONTROL **Sélectionner**].

La référence croisée a été ajoutée à la rubrique.

## Lien vers un site web

Vous pouvez insérer un lien vers un site web dans n’importe quelle rubrique. Pour plus d’informations, visionnez la vidéo du cours AEM Guides 1 sur la liaison à des sites web .


## Afficher les liens rompus

Certaines modifications peuvent entraîner des références croisées rompues. Il s’agit notamment de supprimer une rubrique, de réorganiser une section contenant une référence croisée ou de modifier un identifiant une fois la référence croisée insérée. Notez qu’un exemple de rubrique _crossreferencesandlinks.zip_ est fourni avec cette leçon qui provoquera la rupture de plusieurs des références croisées à puces au contenu interne.

1. Accédez à la **vue Plan** dans le panneau de gauche.

1. Cliquez sur l&#39;icône [!UICONTROL **Filtre**] .

1. Sélectionnez **Liens rompus**.

   ![Liste déroulante de filtres](images/lesson-7/broken-links.png)

Les liens rompus s’affichent sous forme d’objets cliquables. Vous pouvez les identifier en rouge dans la rubrique.

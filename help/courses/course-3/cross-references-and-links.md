---
title: Références croisées et liens
description: Création de références croisées et de liens dans AEM Guides
exl-id: bee7d50f-cbdd-4ac8-b15b-101febc4ae80
source-git-commit: 1c4d278a05f2612bc55ce277efb5da2e6a0fa9a9
workflow-type: tm+mt
source-wordcount: '347'
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

2. Attribuez un identifiant à l’élément à référencer.

   a. Cliquez à l’intérieur de l’élément .

   b. Dans le panneau Propriétés du contenu, choisissez **ID** dans la liste déroulante Attribut .

   c. Saisissez un nom logique dans le champ Valeur .

   d. Afficher l’élément et sa valeur dans **Mode plan** si vous le souhaitez.

3. **Enregistrer** Consultez la rubrique pour vous assurer que le référentiel dispose de l’identifiant mis à jour.

4. Cliquez sur le bouton [!UICONTROL **Référence**] dans la barre d’outils supérieure.

   ![Barre d’outils](images/lesson-7/references-icon.png)

5. Dans la **Référence de contenu** , sélectionnez l’identifiant et l’association d’éléments à insérer comme référence croisée.

6. Cliquez sur [!UICONTROL **Sélectionner**].

La référence croisée a été ajoutée à la rubrique.

## Lien vers un site web

Vous pouvez insérer un lien vers un site web dans n’importe quelle rubrique. Pour plus d’informations, reportez-vous à la vidéo AEM Guides Course 1 sur la liaison aux sites web .


## Afficher les liens rompus

Certaines modifications peuvent entraîner des références croisées rompues. Il s’agit notamment de supprimer une rubrique, de réorganiser une section contenant une référence croisée ou de modifier un identifiant une fois la référence croisée insérée. Notez qu’un exemple de rubrique _crossreferencesandlinks.zip_ est fourni avec cette leçon qui provoquera l’arrêt de plusieurs références croisées à puces au contenu interne.

1. Accédez au **Mode plan** dans le panneau de gauche.

2. Cliquez sur le bouton [!UICONTROL **Filtrer**] icône .

3. Sélectionner **Liens rompus**.

   ![Liste déroulante Filtre](images/lesson-7/broken-links.png)

Les liens rompus s’affichent sous forme d’objets cliquables. Vous pouvez les identifier en rouge dans la rubrique.

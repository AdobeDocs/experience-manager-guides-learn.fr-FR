---
title: Cartes et bookmaps
description: Création et modification de cartes et de zones cliquables dans AEM Guides
exl-id: 9c717e4b-017b-4f2b-b93e-f2c0e7525c55
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 1%

---

# Cartes et cartes-livres

L’éditeur de cartes d’Adobe Experience Manager Guides vous permet de créer et de modifier des fichiers de carte. À l’aide de l’éditeur de cartes, vous pouvez modifier deux types de fichiers : le mappage DITA et le signet. À notre avis, ces concepts sont en grande partie interchangeables.
L’éditeur de cartes est disponible en deux modes : l’éditeur de cartes de base et l’éditeur de cartes avancé.

>[!VIDEO](https://video.tv.adobe.com/v/342766?quality=12&learn=on)

## Création d’une carte

AEM Guides fournit deux modèles de mappage prêts à l’emploi : carte DITA et carte d’applet. Vous pouvez également créer vos propres modèles de carte et les partager avec vos auteurs pour créer des fichiers de carte.

Effectuez les étapes suivantes pour créer un fichier map.

1. Dans l’interface utilisateur d’Assets, accédez à l’emplacement où vous souhaitez créer le fichier de mappage.

1. Cliquez sur [!UICONTROL **Créer > Carte DITA**].

1. Sur la page Plan directeur, sélectionnez le type de modèles de carte à utiliser, puis cliquez sur [!UICONTROL **Suivant**].

1. Sur la page Propriétés, saisissez une **Titre** et **Nom** pour la carte.

1. Cliquez sur [!UICONTROL **Créer**].

## Ouverture d’une carte à l’aide de l’éditeur de carte avancé

1. Dans le **Interface utilisateur des ressources**, sélectionnez la carte à modifier.

1. Cliquez sur [!UICONTROL **Modifier les rubriques**].

   ![Interface utilisateur de modification des rubriques](images/lesson-14/edit-topics.png)

OU

1. Passez la souris sur l’icône de carte.

1. Sélectionner **Modifier les rubriques** de la **Action** .


## Ajout de contenu à une carte ou à une carte d’utilisateur

1. Accédez au **Repository View**.

1. Faites glisser et déposez du contenu de la vue Repository vers des emplacements valides dans la carte ou la carte d’applet.

OU

1. Cliquez sur un emplacement valide dans la carte ou la carte d’utilisateur.

1. Cliquez sur la [!UICONTROL **Icône Barre d’outils**] pour ajouter des chapitres, des rubriques ou des rubriques.

   ![Icônes de la barre d’outils](images/lesson-14/toolbar-icons.png)

1. Sélectionnez une ou plusieurs ressources à ajouter.

1. Cliquez sur [!UICONTROL **Sélectionner**].

### Promouvoir ou rétrograder des éléments dans une carte

Utilisation **Flèches de la barre d’outils** pour promouvoir ou rétrograder des chapitres et des topicrefs dans une carte ou une carte des pages.

1. Sélectionnez un élément dans la carte.

1. Cliquez sur le bouton [!UICONTROL **Flèche gauche**] pour promouvoir une référence de rubrique vers un chapitre, ou la variable [!UICONTROL **Flèche vers la droite**] pour rétrograder un chapitre à une référence de rubrique.

   ![Icônes de la flèche](images/lesson-14/toolbar-arrows.png)

1. Enregistrez et modifiez la carte si nécessaire.

OU

1. Faites glisser et déposez les éléments pour les réorganiser.

## Ajout de métadonnées à une carte

1. Dans la **Barre d’outils Carte**, insérez un groupe de rubriques.

   ![Ajouter un attribut](images/lesson-14/add-topicgroup.png)

1. Cliquez sur le bouton [!UICONTROL **Icône Plus**] pour insérer des éléments.

1. Sélectionnez les éléments à insérer.

   ![Insérer des métadonnées](images/lesson-14/insert-metadata.png)

1. Cliquez sur [!UICONTROL **Fermer**].

## Ajout d’une table relationnelle à une carte

Il est possible d’ajouter un reltable après la structure d’une carte.

1. Cliquez dans la carte où vous souhaitez insérer la table de relation.

1. Utilisez la variable **Icône Barre d’outils** pour ajouter le reltable à la carte.

   ![Icône Reltable](images/lesson-14/reltable-icon.png)

1. Configurez la boîte de dialogue.

1. Cliquez sur [!UICONTROL **Insérer**].

1. Faites glisser les rubriques requises à partir du **Référentiel** dans le reltable.

1. Copiez et collez les éléments requis de la carte dans le tableau reltable à l’aide des raccourcis clavier standard.

## Attribution d’attributs aux topicrefs dans une carte

1. Mettez en surbrillance un topicref ou une collection imbriquée de topicrefs dans la carte.

1. Sous Autres attributs dans le panneau Propriétés du contenu , choisissez une **Attribut** et son **Valeur.**

   ![Ajout d’attributs](images/lesson-14/add-attribute.png)

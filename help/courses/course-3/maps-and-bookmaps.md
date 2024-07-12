---
title: Cartes et bookmaps
description: Création et modification de cartes et de bookmaps dans AEM Guides
exl-id: 9c717e4b-017b-4f2b-b93e-f2c0e7525c55
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 1%

---

# Cartes et cartes-livres

L’éditeur de cartes d’Adobe Experience Manager Guides vous permet de créer et de modifier des fichiers de mappage. À l’aide de l’éditeur de cartes, vous pouvez modifier deux types de fichiers : le mappage DITA et le signet. À notre avis, ces concepts sont en grande partie interchangeables.
L’éditeur de cartes est disponible en deux modes : l’éditeur de cartes de base et l’éditeur de cartes avancé.

>[!VIDEO](https://video.tv.adobe.com/v/342766?quality=12&learn=on)

## Création d’une carte

AEM Guides fournit deux modèles de mappage prêts à l’emploi : carte DITA et carte d’applet. Vous pouvez également créer vos propres modèles de carte et les partager avec vos auteurs pour créer des fichiers de carte.

Effectuez les étapes suivantes pour créer un fichier map.

1. Dans l’interface utilisateur d’Assets, accédez à l’emplacement où vous souhaitez créer le fichier de mappage.

1. Cliquez sur [!UICONTROL **Créer > Carte DITA**].

1. Sur la page Plan directeur, sélectionnez le type de modèles de carte à utiliser et cliquez sur [!UICONTROL **Suivant**].

1. Sur la page Propriétés, saisissez un **Titre** et un **Nom** pour la carte.

1. Cliquez sur [!UICONTROL **Créer**].

## Ouverture d’une carte à l’aide de l’éditeur de carte avancé

1. Dans l’ **interface utilisateur d’Assets**, sélectionnez la carte à modifier.

1. Cliquez sur [!UICONTROL **Modifier les rubriques**].

   ![Modifier l’interface utilisateur de la rubrique](images/lesson-14/edit-topics.png)

Ou

1. Passez la souris sur l’icône de carte.

1. Sélectionnez **Modifier les rubriques** dans le menu **Action**.


## Ajout de contenu à une carte ou à une carte d’utilisateur

1. Accédez à la **vue du référentiel**.

1. Faites glisser et déposez du contenu de la vue Repository vers des emplacements valides dans la carte ou la carte d’applet.

Ou

1. Cliquez sur un emplacement valide dans la carte ou la carte d’utilisateur.

1. Cliquez sur l’icône [!UICONTROL **Barre d’outils**] appropriée pour ajouter des chapitres, des rubriques ou des références de rubriques.

   ![Icônes de barre d’outils](images/lesson-14/toolbar-icons.png)

1. Sélectionnez une ou plusieurs Assets que vous souhaitez ajouter.

1. Cliquez sur [!UICONTROL **Sélectionner**].

### Promouvoir ou rétrograder des éléments dans une carte

Utilisez les **flèches de la barre d’outils** pour promouvoir ou rétrograder les chapitres et les topicrefs dans une carte ou une carte-livre.

1. Sélectionnez un élément dans la carte.

1. Cliquez sur la [!UICONTROL **flèche vers la gauche**] pour promouvoir une référence de rubrique vers un chapitre ou sur la [!UICONTROL **flèche vers la droite**] pour rétrograder un chapitre vers une référence de rubrique.

   ![Icônes de flèche](images/lesson-14/toolbar-arrows.png)

1. Enregistrez et modifiez la carte si nécessaire.

Ou

1. Faites glisser et déposez les éléments pour les réorganiser.

## Ajout de métadonnées à une carte

1. Dans la **barre d’outils de carte**, insérez un groupe de rubriques.

   ![Ajouter un attribut](images/lesson-14/add-topicgroup.png)

1. Cliquez sur l’icône [!UICONTROL **Plus**] pour insérer des éléments.

1. Sélectionnez les éléments à insérer.

   ![Insérer des métadonnées](images/lesson-14/insert-metadata.png)

1. Cliquez sur [!UICONTROL **Fermer**].

## Ajout d’une table relationnelle à une carte

Il est possible d’ajouter un reltable après la structure d’une carte.

1. Cliquez dans la carte où vous souhaitez insérer la table de relation.

1. Utilisez l’ **icône de barre d’outils** pour ajouter le reltable au mappage.

   ![Icône Relable](images/lesson-14/reltable-icon.png)

1. Configurez la boîte de dialogue.

1. Cliquez sur [!UICONTROL **Insérer**].

1. Faites glisser les rubriques requises du **Référentiel** vers le reltable.

1. Copiez et collez les éléments requis de la carte dans le tableau reltable à l’aide des raccourcis clavier standard.

## Attribution d’attributs aux topicrefs dans une carte

1. Mettez en surbrillance un topicref ou une collection imbriquée de topicrefs dans la carte.

1. Sous Autres attributs dans le panneau Propriétés du contenu, choisissez un **attribut** et sa **valeur.**

   ![Ajouter des attributs](images/lesson-14/add-attribute.png)

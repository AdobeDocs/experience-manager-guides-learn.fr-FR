---
title: Cartes et bookmaps
description: Création et modification de cartes et de signets dans AEM Guides
exl-id: 9c717e4b-017b-4f2b-b93e-f2c0e7525c55
TQID: https://experienceleague.adobe.com/Fg0DsG6-pi2TSKPrBpvbbTlBGtpzeoojTnMqk0f22mw
product_v2:
  - id: fae5e35a-80c9-4b94-9352-1a060a6aab1d
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 27ffc636d63300fb2e99903d92cab12f0cfcbb25
workflow-type: tm+mt
source-wordcount: 468
ht-degree: 1%

---

# Cartes et signets

L’éditeur de carte d’Adobe Experience Manager Guides vous permet de créer et de modifier des fichiers de carte. L&#39;éditeur de carte vous permet de modifier deux types de fichiers : DITA map et bookmap. Pour nos besoins, considérez qu’il s’agit de concepts largement interchangeables.
L’éditeur de carte se présente sous deux modes : l’éditeur de carte de base et l’éditeur de carte avancé.

>[!VIDEO](https://video.tv.adobe.com/v/342766?quality=12&learn=on)

## Créer un mappage

AEM Guides fournit deux modèles de mappage prêts à l’emploi : un mappage DITA et un mappage bookmap. Vous pouvez également créer vos propres modèles de carte et les partager avec vos auteurs pour créer des fichiers de carte.

Pour créer un fichier de mappage, procédez comme suit.

1. Dans l’interface utilisateur d’Assets, accédez à l’emplacement où vous souhaitez créer le fichier de mappage.

1. Cliquez sur [!UICONTROL **Créer > Plan DITA**].

1. Sur la page Plan directeur, sélectionnez le type de modèle de carte à utiliser, puis cliquez sur [!UICONTROL **Suivant**].

1. Sur la page Propriétés , saisissez un **Titre** et un **Nom** pour la carte.

1. Cliquez sur [!UICONTROL **Créer**].

## Ouverture d’une carte à l’aide de l’éditeur de cartes avancé

1. Dans l’**interface utilisateur d’**, sélectionnez le mappage à modifier.

1. Cliquez sur [!UICONTROL **Modifier les rubriques**].

   ![Modifier l’interface utilisateur des rubriques](images/lesson-14/edit-topics.png)

Ou

1. Pointez la souris sur l’icône de carte.

1. Sélectionnez **Modifier les rubriques** dans le menu **Action**.


## Ajout de contenu à une carte ou un bookmap

1. Accédez à la **Vue du référentiel**.

1. Effectuez un glisser-déposer du contenu de la Vue du référentiel vers des emplacements valides dans la carte ou la libellule.

Ou

1. Cliquez à un emplacement valide dans la carte ou la libellule.

1. Cliquez sur l’[!UICONTROL **icône de barre d’outils**] appropriée pour ajouter des chapitres, des rubriques ou des références de rubrique.

   ![Icônes de la barre d’outils](images/lesson-14/toolbar-icons.png)

1. Choisissez un ou plusieurs Assets à ajouter.

1. Cliquez sur [!UICONTROL **Sélectionner**].

### Promouvoir ou rétrograder des éléments dans un mappage

Utilisez **les flèches de la barre d’outils** pour convertir ou rétrograder des chapitres et des éléments contextuels dans une carte ou un bookmap.

1. Sélectionnez un élément dans le mappage.

1. Cliquez sur la [!UICONTROL **Flèche gauche**] pour convertir un objet topicref en chapitre, ou sur la [!UICONTROL **Flèche droite**] pour rétrograder un chapitre en objet topicref.

   ![Icônes fléchées](images/lesson-14/toolbar-arrows.png)

1. Enregistrez et gérez la version du mappage si nécessaire.

Ou

1. Faites glisser et déposez des éléments pour les réorganiser.

## Ajout de métadonnées à une carte

1. Dans la **barre d’outils Carte**, insérez un groupe de rubriques.

   ![Ajouter un attribut](images/lesson-14/add-topicgroup.png)

1. Cliquez sur l’icône [!UICONTROL **Plus**] pour insérer des éléments.

1. Choisissez les éléments à insérer.

   ![Insérer des métadonnées](images/lesson-14/insert-metadata.png)

1. Cliquez sur [!UICONTROL **Fermer**].

## Ajout d’un objet fiable à un mappage

Un objet fiable peut être ajouté après la structure d’un mappage.

1. Cliquez sur le mappage dans lequel vous souhaitez insérer le dossier fiable.

1. Utilisez l’icône **Icône de la barre d’outils** pour ajouter le fiable à la carte.

   ![&#x200B; Icône Fiable &#x200B;](images/lesson-14/reltable-icon.png)

1. Configurez la boîte de dialogue.

1. Cliquez sur [!UICONTROL **Insérer**].

1. Effectuez un glisser-déposer des rubriques requises du **Référentiel** dans le référentiel.

1. Copiez et collez les éléments requis du mappage dans le fichier à relier à l’aide des raccourcis clavier standard.

## Attribuer des attributs aux objets contextuels dans un mappage

1. Mettez en surbrillance une rubrique ou une collection imbriquée de rubriques dans la carte.

1. Sous Autres attributs dans le panneau Propriétés du contenu, choisissez un **Attribut** et sa **Valeur.**

   ![Ajouter des attributs](images/lesson-14/add-attribute.png)

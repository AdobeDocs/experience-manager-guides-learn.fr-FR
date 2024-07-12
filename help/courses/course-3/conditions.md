---
title: Conditions
description: Utilisation des conditions dans AEM Guids
exl-id: 2cb670d9-1a22-47c6-8409-52d1d526010a
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 1%

---

# Conditions

Dans DITA, les conditions sont souvent pilotées par des attributs tels que Produit, Plateforme et Audience. Des valeurs spécifiques peuvent également leur être affectées. Les utilisateurs peuvent contrôler tout cela via les profils de dossier.

Des exemples de fichiers que vous pouvez choisir d’utiliser pour cette leçon sont fournis dans le fichier [conditions.zip](assets/conditions.zip).

>[!VIDEO](https://video.tv.adobe.com/v/342755?quality=12&learn=on)

## Affectation de conditions à un profil de dossier

1. Sélectionnez la mosaïque **Profils de dossier** .

1. Cliquez sur [!UICONTROL **Attributs conditionnels**].

1. Cliquez sur [!UICONTROL **Modifier**] dans le coin supérieur gauche du profil.

1. Cliquez sur [!UICONTROL **Ajouter**].

   ![Conditions dans les profils de dossier](images/lesson-13/add-name.png)

1. Renseignez les champs requis.

   - Le Nom doit correspondre à un attribut utilisé pour le profilage.

   - La valeur est l’entrée exacte qui sera utilisée dans la source de code DITA.

   - Le libellé est le mot qui sera affiché par l’utilisateur qui saisit des attributs.

1. Cliquez sur [!UICONTROL **Enregistrer**].

>[!NOTE]
>
>REMARQUE : la configuration d’un profil global peut être un moyen rapide et efficace de contrôler l’utilisation des attributs et des valeurs afin de suivre un guide de style cohérent.

## Attribution d’attributs aux éléments

Si aucun profil de dossier personnalisé n’a été affecté à un concept, vous pouvez attribuer des attributs à des éléments spécifiques, tels que des paragraphes.

1. Dans la **vue du référentiel**, cliquez sur l’élément avec lequel vous souhaitez travailler pour le sélectionner.

1. Dans le panneau **Propriétés du contenu**, cliquez sur la liste déroulante [!UICONTROL **Attribut**] .

1. Sélectionnez l’attribut que vous souhaitez attribuer.

1. Ajoutez une **valeur**.

L’association d’attributs et de valeurs est désormais affectée à l’élément sélectionné.

## Attribuer des paires d’attributs et de valeurs à l’aide de conditions

Le panneau Conditions permet une affectation contrôlée des paires Attribut/Valeur.

1. Modifiez les **préférences utilisateur**.

   a. Cliquez sur l’icône Préférences utilisateur .

   ![Icône de préférences utilisateur](images/lesson-13/user-prefs-icon.png)

   b. Renseignez les champs requis dans la boîte de dialogue **Préférences utilisateur**. Par exemple :

   ![Préférences utilisateur](images/lesson-13/user-preferences.png)

   c. Cliquez sur [!UICONTROL **Enregistrer**].

1. Dans le panneau des conditions, développez les listes déroulantes pour Audience et Platform. Notez que les conditions disponibles sont spécifiques à Folder Profile.

1. Faites glisser et déposez une condition sur l’élément souhaité pour l’affecter.

## Attribution d’un schéma d’objet

Les mappages de schéma d’objet sont une forme spécialisée de mappage aléatoire et sont référencés par une carte. Les schémas d’objet sont utilisés pour définir des taxonomies. Elles permettent de contrôler les valeurs disponibles.

1. Accédez à la **vue du référentiel**.

1. Sélectionnez une carte qui référence le schéma d’objet ditamap. Cet exemple utilise la carte appelée _Design and Layout_.

   ![Préférences utilisateur](images/lesson-13/subject-scheme-map.png)

1. Configurez les préférences utilisateur.

   a. Cliquez sur l’icône [!UICONTROL **Préférences utilisateur**] .

   ![Préférences utilisateur](images/lesson-13/user-prefs-icon-2.png)

   b. Renseignez les champs de la boîte de dialogue **Préférences utilisateur**.

   c. Cliquez sur le symbole du dossier en regard du champ Chemin d’accès de base pour choisir le chemin d’accès au fichier souhaité.

   d. Cliquez sur [!UICONTROL **Sélectionner**].

   e. Cliquez sur le symbole de la clé en regard du champ **Root Map** pour saisir un chemin d’accès.

   >[!IMPORTANT]
   >
   >Important : la carte racine sélectionnée doit être la carte contenant le schéma d’objet.

   ![Préférences utilisateur](images/lesson-13/user-preferences-2.png)

   f. Limitez les ressources affichées en sélectionnant le ou les dossiers que vous souhaitez utiliser.

   g. Cliquez sur [!UICONTROL **Sélectionner**].

   h. Cliquez sur [!UICONTROL **Enregistrer**].

Le schéma d’objet a maintenant été attribué.

## Affichage du schéma d’objet à partir du panneau Conditions

1. Accédez à **Paramètres de l’éditeur**.

1. Sélectionnez l’onglet **Conditions** .

1. Cochez la case **Afficher le schéma d’objet dans le panneau Conditions**

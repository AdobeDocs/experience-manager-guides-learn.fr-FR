---
title: Clés
description: Les clés vous permettent d’inclure des informations sur les variables lors de l’utilisation de DITA dans AEM Guides.
exl-id: cb64e094-fe6d-4a5e-8f0e-25ae58aaa2c6
source-git-commit: 1c4d278a05f2612bc55ce277efb5da2e6a0fa9a9
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---

# Clés

Différents ensembles de matériaux peuvent contenir des informations similaires qui doivent être personnalisées dans des endroits choisis. Les clés vous permettent d’inclure des informations sur les variables lors de l’utilisation de DITA.

Des exemples de fichiers que vous pouvez choisir d’utiliser pour cette leçon sont fournis dans le fichier . [keys.zip](assets/keys.zip).

>[!VIDEO](https://video.tv.adobe.com/v/342756?quality=12&learn=on)

## Activer les clés

1. Chargez l’ensemble des fichiers d’exemple fournis.

   a. Chargez le fichier zip.

   b. Actualisez l’environnement AEM.

   c. Sélectionnez le fichier à extraire.

   ![Sélectionner une zone](images/lesson-9/select-zip.png)

   d. Cliquez sur [!UICONTROL **Extraction de l’archive**] dans la barre d’outils supérieure.

   ![Barre d’outils](images/lesson-9/extract-archive.png)

   e. Dans la boîte de dialogue, choisissez l’emplacement spécifique des fichiers à extraire, par exemple un dossier appelé Clés.

   f. Cliquez sur [!UICONTROL **Suivant**].

   g. Ignorez les conflits, car ils n’existeront pas pour le contenu qui n’a jamais été chargé auparavant.

   h. Sélectionner [!UICONTROL **Extract**] en haut à droite de l’écran.

2. Une fois l’extraction terminée, cliquez sur [!UICONTROL **Accédez au dossier cible**].

   ![Confirmation](images/lesson-9/go-to-target.png)

## Résoudre les clés des valeurs référencées

Pour utiliser correctement les clés, les préférences utilisateur doivent référencer une carte spécifique comme carte racine. A l&#39;intérieur de cette carte se trouve un ensemble de clés, regroupées au sein d&#39;un groupe de sujets. L’ouverture du mappage et des rubriques résout les clés sur les valeurs auxquelles ce mappage fait référence.

1. Spécifiez une carte racine.

   a. Dans l’écran Clés , ouvrez une carte.

   b. Configurez les préférences utilisateur.

   c. Cliquez sur le bouton [!UICONTROL **Préférences utilisateur**] dans la barre d’outils supérieure.

   ![Barre d’outils supérieure](images/lesson-9/author-view.png)

   d. Cliquez sur l’icône de clé pour spécifier une **Root Map** qui sera utilisé pour résoudre les clés.

   e. Cochez les cases correspondant aux ressources de votre choix.

   ![Liste déroulante Ressources](images/lesson-9/select-assets.png)

   f. Cliquez sur [!UICONTROL **Sélectionner**].

   g. **Enregistrer** Préférences utilisateur.

2. Accédez au **Vue Carte**.

3. Ouvrez la carte spécifiée.

Les clés sont résolues.

## Ajouter manuellement une nouvelle clé

1. Ouvrez une carte avec une carte racine spécifiée.

2. Sélectionnez une clé.

   ![Menu déroulant des clés](images/lesson-9/hybrid-key.png)

3. Insérez une nouvelle clé.

   a. Cliquez dans un emplacement valide de la carte.

   b. Sélectionnez la **Keydef** dans la barre d’outils supérieure.

   ![Barre d’outils Keydef](images/lesson-9/key-icon.png)

   c. Dans la boîte de dialogue Insérer une clé, saisissez une valeur unique pour les clés qui correspond à la définition que vous créez.

   d. Cliquez sur [!UICONTROL **Insérer**].

4. Ajoutez topicmeta dans le fichier keydef.

   a. Cliquez sur le bouton [!UICONTROL **Insérer un élément**] dans la barre d’outils supérieure.

   ![Barre d’outils Keydef](images/lesson-9/add-icon.png)

   b. Dans la boîte de dialogue Insérer un élément, recherchez et sélectionnez &quot;topicmeta&quot;.

5. Ajoutez des mots-clés dans la topicmeta.

   a. Cliquez sur le bouton [!UICONTROL **Insérer un élément**] dans la barre d’outils supérieure.

   ![Barre d’outils Keydef](images/lesson-9/add-icon.png)

   b. Dans la boîte de dialogue Insérer un élément, recherchez et sélectionnez &quot;mots-clés&quot;.

6. Ajoutez un mot-clé dans la rubrique .

   a. Cliquez sur le bouton [!UICONTROL **Insérer un élément**] dans la barre d’outils supérieure.

   ![Barre d’outils Keydef](images/lesson-9/add-icon.png)

   b. Dans le **Insérer un élément** boîte de dialogue, recherchez et sélectionnez &quot;mot-clé&quot;.

7. Saisissez la valeur de keydef dans le mot-clé.

Sur la carte, votre clé de sécurité devrait maintenant ressembler à ceci :

![Keydef terminé](images/lesson-9/keydef.png)

## Configuration d’une clé comme fragment de code

Les fragments de code sont de petits fragments de contenu qui peuvent être réutilisés dans diverses rubriques de votre projet de documentation. Au lieu de générer manuellement chaque clé, vous pouvez configurer une seule clé comme extrait de code.

1. Sélectionnez un élément keydef dans la carte.

2. Dans le menu contextuel, cliquez sur [!UICONTROL **Créer un fragment de code**].

3. Dans la boîte de dialogue Nouveau fragment de code, ajoutez un titre et une description.
Vous pouvez également supprimer des clés ou des définitions de mots-clés existantes du contenu.

4. Cliquez sur [!UICONTROL **Créer**].

5. Dans le panneau de gauche, sélectionnez **Fragments de code**.

6. Faites glisser le fragment que vous venez de créer du panneau Fragments de code vers la carte.

7. Mettez à jour la clé keydef selon les besoins à l’aide des propriétés du contenu.
Une fois enregistré et actualisé, cet ensemble de clés est disponible pour tous les utilisateurs qui ont défini une carte contenant la même carte racine.

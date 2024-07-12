---
title: Vérifier l’orthographe et rechercher/remplacer
description: Utilisation de la vérification orthographique et de la recherche/remplacement dans AEM Guides
exl-id: 5f39618d-a919-4d3c-a4de-2896f2d1bf20
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 1%

---

# Vérifier l’orthographe et rechercher/remplacer

L’éditeur AEM Guides dispose de puissantes fonctionnalités de vérification orthographique et de recherche et remplacement.

>[!VIDEO](https://video.tv.adobe.com/v/342768?quality=12&learn=on)

Corriger une erreur d’orthographe

1. Recherchez une erreur dans une rubrique ouverte, affichée avec un trait de soulignement rouge.

1. Maintenez la touche Ctrl enfoncée et cliquez sur le bouton secondaire de la souris dans le mot.

1. Choisissez l’orthographe correcte parmi les suggestions.

Si l’orthographe correcte n’est pas suggérée, vous pouvez toujours modifier le mot manuellement.

## Passer à la vérification orthographique AEM

Vous pouvez utiliser un outil de vérification orthographique autre que le dictionnaire par défaut du navigateur.

1. Accédez à **Paramètres de l’éditeur**.

1. Sélectionnez l’onglet des paramètres **Général** .

   ![Configuration de la vérification orthographique](images/lesson-11/configure-dictionary.png)

1. Deux options sont disponibles :

   - **Vérification orthographique du navigateur** : paramètre par défaut dans lequel la vérification orthographique utilise le dictionnaire intégré du navigateur.

   - **AEM Vérifier l’orthographe** : utilisez cette option pour créer une liste de mots personnalisée à l’aide AEM dictionnaire personnalisé.

1. Sélectionnez **AEM Orthographe**.

1. Cliquez sur [!UICONTROL **Enregistrer**].

Configuration d’un dictionnaire personnalisé

L’administrateur peut modifier les paramètres afin que le dictionnaire d’AEM reconnaisse les mots personnalisés tels que les noms d’entreprise.

1. Accédez au volet **Outils**.

1. Connectez-vous à **CRXDE Lite**.

   ![Icône du CRXDE Lite de l’interface utilisateur AEM](images/lesson-11/crxde-lite.png)

1. Accédez au noeud **_/apps/fmdita/config_**.

   ![Noeud de configuration du CRXDE Lite](images/lesson-11/config-node.png)

1. Créez un fichier.

   a. Cliquez avec le bouton droit sur le dossier config .

   b. Sélectionnez **Créer > Créer un fichier**.

   ![Création d’un fichier de dictionnaire](images/lesson-11/new-dictionary-file.png)

   c. Nommez le fichier _**user_dictionary.txt**_.

   ![Texte du dictionnaire utilisateur](images/lesson-11/user-dictionary.png)

   d. Cliquez sur [!UICONTROL **OK**].

1. Ouvrez le fichier .

1. Ajoutez une liste de mots à inclure dans votre dictionnaire personnalisé.

1. Cliquez sur [!UICONTROL **Enregistrer tout**].

1. Fermez le fichier.

Les auteurs peuvent avoir besoin de redémarrer leur session de l’éditeur web pour obtenir la liste de mots personnalisée mise à jour dans le dictionnaire d’AEM.

## Rechercher et remplacer dans un seul fichier

1. Cliquez sur l’icône Rechercher et remplacer dans la barre d’outils supérieure.

   ![Rechercher une icône de remplacement](images/lesson-11/find-replace-icon.png)

1. Dans la barre d’outils inférieure, saisissez un mot ou une expression.

1. Cliquez sur [!UICONTROL **Rechercher**].

1. Si nécessaire, saisissez un mot pour remplacer le mot trouvé.

1. Cliquez sur [!UICONTROL **Remplacer**].

## Recherche et remplacement dans le référentiel

1. Accédez au **référentiel**.

1. Cliquez sur l’icône [!UICONTROL **Rechercher et remplacer**] en bas à gauche de l’écran.

1. Cliquez sur l’icône [!UICONTROL **Afficher les paramètres**] .

1. Choisissez l’une

   - **Fichier d’extraction avant de remplacer** : s’il est activé par un administrateur, le fichier est extrait automatiquement avant de remplacer les termes de recherche.

   - **Mot entier uniquement** : limite la recherche pour renvoyer uniquement le mot ou l’expression exact saisi.

   ![Rechercher un remplacement dans le référentiel](images/lesson-11/repository-find-replace.png)

1. Cliquez sur l’icône [!UICONTROL **Appliquer le filtre**] pour sélectionner le chemin d’accès dans le référentiel où vous souhaitez effectuer la recherche.

1. Saisissez les termes à rechercher et à remplacer.

1. Si nécessaire, sélectionnez **Créer une version après remplacer**.

1. Cliquez sur [!UICONTROL **Rechercher**].

1. Ouvrez le fichier souhaité et utilisez les flèches pour naviguer d’un résultat trouvé à l’autre.

   ![Rechercher un remplacement de l’interface utilisateur de navigation](images/lesson-11/find-replace-navigation.png)

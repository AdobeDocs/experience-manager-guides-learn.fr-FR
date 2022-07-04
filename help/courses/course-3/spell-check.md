---
title: Vérifier l’orthographe et rechercher/remplacer
description: Utilisation de la vérification orthographique et de la recherche/remplacement dans AEM Guides
exl-id: 5f39618d-a919-4d3c-a4de-2896f2d1bf20
source-git-commit: 0b4326b02ef52f5de77c3f26c18feec84567cebb
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 3%

---

# Vérifier l’orthographe et rechercher/remplacer

L’éditeur de guides d’AEM dispose de puissantes fonctionnalités de vérification orthographique et de recherche et remplacement.

>[!VIDEO](https://video.tv.adobe.com/v/342768)

Correction d’une erreur d’orthographe

1. Recherchez une erreur dans une rubrique ouverte, affichée avec un trait de soulignement rouge.

2. Maintenez la touche Ctrl enfoncée et cliquez sur le bouton secondaire de la souris dans le mot.

3. Choisissez l’orthographe correcte parmi les suggestions.

Si l’orthographe correcte n’est pas suggérée, vous pouvez toujours modifier le mot manuellement.

## Passer à la vérification orthographique AEM

Vous pouvez utiliser un outil de vérification orthographique autre que le dictionnaire par défaut du navigateur.

1. Accédez à **Paramètres de l’éditeur**.

2. Sélectionnez la **Général** l’onglet paramètres .

   ![Configuration de la vérification orthographique](images/lesson-11/configure-dictionary.png)

3. Vous disposez de deux options :

   - **Vérifier l’orthographe du navigateur** — le paramètre par défaut où la vérification orthographique utilise le dictionnaire intégré du navigateur.

   - **Vérifier l’orthographe AEM** — utilisez cette option pour créer une liste de mots personnalisée à l’aide du dictionnaire personnalisé d’AEM.

4. Choisir **Vérifier l’orthographe AEM**.

5. Cliquez sur [!UICONTROL **Enregistrer**].

Configuration d’un dictionnaire personnalisé

L’administrateur peut modifier les paramètres afin que le dictionnaire d’AEM reconnaisse les mots personnalisés tels que les noms d’entreprise.

1. Accédez au **Outils** volet.

2. Connectez-vous à **CRXDE Lite**.

   ![Icône du CRXDE Lite de l’interface utilisateur AEM](images/lesson-11/crxde-lite.png)

3. Accédez au **_Noeud /apps/fmdita/config_**.

   ![Noeud de configuration du CRXDE Lite](images/lesson-11/config-node.png)

4. Créez un fichier.

   a. Cliquez avec le bouton droit sur le dossier de configuration.

   b. Choisir **Créer > Créer un fichier**.

   ![Création d’un fichier de dictionnaire](images/lesson-11/new-dictionary-file.png)

   c. Nommez le fichier _**user_dictionary.txt**_.

   ![Texte du dictionnaire d’utilisateur](images/lesson-11/user-dictionary.png)

   d. Cliquez sur [!UICONTROL **OK**].

5. Ouvrez le fichier.

6. Ajoutez une liste de mots à inclure dans votre dictionnaire personnalisé.

7. Cliquez sur [!UICONTROL **Enregistrer tout**].

8. Fermez le fichier.

Les auteurs peuvent avoir besoin de redémarrer leur session de l’éditeur web pour obtenir la liste de mots personnalisée mise à jour dans le dictionnaire d’AEM.

## Rechercher et remplacer dans un seul fichier

1. Cliquez sur l’icône Rechercher et remplacer dans la barre d’outils supérieure.

   ![Icône Rechercher un remplacement](images/lesson-11/find-replace-icon.png)

2. Dans la barre d’outils inférieure, saisissez un mot ou une expression.

3. Cliquez sur [!UICONTROL **Rechercher**].

4. Si nécessaire, saisissez un mot pour remplacer le mot trouvé.

5. Cliquez sur [!UICONTROL **Remplacer**].

## Recherche et remplacement dans le référentiel

1. Accédez au **Référentiel**.

2. Cliquez sur le bouton [!UICONTROL **Rechercher et remplacer**] en bas à gauche de l’écran.

3. Cliquez sur le bouton [!UICONTROL **Afficher les paramètres**] icône .

4. Choisissez l’une

   - **Extraction de fichier avant remplacement** — s’il est activé par un administrateur, le fichier est extrait automatiquement avant de remplacer les termes de recherche.

   - **Mot entier uniquement** — limite la recherche pour renvoyer uniquement le mot ou l’expression exact saisi.

   ![Rechercher un remplacement dans le référentiel](images/lesson-11/repository-find-replace.png)

5. Cliquez sur le bouton [!UICONTROL **Appliquer un filtre**] pour sélectionner le chemin d’accès dans le référentiel où vous souhaitez effectuer la recherche.

6. Saisissez les termes à rechercher et à remplacer.

7. Si nécessaire, sélectionnez **Créer une version après remplacement**.

8. Cliquez sur [!UICONTROL **Rechercher**].

9. Ouvrez le fichier souhaité et utilisez les flèches pour naviguer d’un résultat trouvé à l’autre.

   ![Rechercher un remplacement de l’interface de navigation](images/lesson-11/find-replace-navigation.png)

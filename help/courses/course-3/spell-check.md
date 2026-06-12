---
title: Vérification orthographique et recherche/remplacement
description: Utilisation de la vérification orthographique et de la fonction rechercher/remplacer dans AEM Guides
exl-id: 5f39618d-a919-4d3c-a4de-2896f2d1bf20
TQID: https://experienceleague.adobe.com/cSdhulSc30KrwsGh1ldB2yn-8eSLccHBpyD-0S1x1M0
product_v2: id: fae5e35a-80c9-4b94-9352-1a060a6aab1did: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 27ffc636d63300fb2e99903d92cab12f0cfcbb25
workflow-type: tm+mt
source-wordcount: 443
ht-degree: 2%

---

# Vérification orthographique et rechercher/remplacer

L’éditeur AEM Guides dispose de puissantes fonctionnalités de vérification orthographique et de recherche et remplacement.

>[!VIDEO](https://video.tv.adobe.com/v/342768?quality=12&learn=on)

Correction d’une faute d’orthographe

1. Recherchez une erreur dans une rubrique ouverte, soulignée en rouge.

1. Maintenez la touche Ctrl enfoncée tout en cliquant sur le bouton de souris secondaire à l’intérieur du mot.

1. Choisissez la bonne orthographe parmi les suggestions.

Si l’orthographe correcte n’est pas suggérée, vous pouvez toujours modifier manuellement le mot.

## Basculer vers la vérification orthographique AEM

Vous pouvez utiliser un outil de vérification orthographique autre que le dictionnaire par défaut du navigateur.

1. Accédez à **Paramètres de l’éditeur**.

1. Sélectionnez l’onglet Paramètres **généraux**.

   ![Configuration de la vérification orthographique](images/lesson-11/configure-dictionary.png)

1. Il existe deux options :

   - **Vérification orthographique du navigateur** : paramètre par défaut dans lequel la vérification orthographique utilise le dictionnaire intégré du navigateur.

   - **Vérification orthographique AEM** — utilisez-la pour créer une liste de mots personnalisée à l&#39;aide du dictionnaire personnalisé AEM.

1. Choisissez **Vérification Orthographique**.

1. Cliquez sur [!UICONTROL **Enregistrer**].

Configuration d’un dictionnaire personnalisé

L’administrateur peut modifier les paramètres afin que le dictionnaire AEM reconnaisse les mots personnalisés tels que les noms de société.

1. Accédez au volet **Outils**.

1. Connectez-vous à ****.

   ![Icône de CRXDE Lite de l’interface utilisateur d’AEM](images/lesson-11/crxde-lite.png)

1. Accédez au nœud **_/apps/fmdita/config_**.

   ![Nœud de configuration ](images/lesson-11/config-node.png)

1. Créez un fichier .

   a. Cliquez avec le bouton droit sur le dossier de configuration.

   b. Choisissez **Créer > Créer un fichier**.

   ![Création d’un fichier de dictionnaire](images/lesson-11/new-dictionary-file.png)

   c. Nommez le fichier _**user_dictionary.txt**_.

   ![Texte du dictionnaire utilisateur](images/lesson-11/user-dictionary.png)

   d. Cliquez sur [!UICONTROL **OK**].

1. Ouvrez le fichier .

1. Ajoutez une liste de mots à inclure dans votre dictionnaire personnalisé.

1. Cliquez sur [!UICONTROL **Enregistrer tout**].

1. Fermez le fichier .

Il se peut que les auteurs doivent redémarrer leur session d’éditeur web pour obtenir la liste de mots personnalisés mise à jour dans le dictionnaire AEM.

## Rechercher et remplacer dans un seul fichier

1. Cliquez sur l’icône Rechercher et remplacer dans la barre d’outils supérieure.

   ![Icône Rechercher et remplacer](images/lesson-11/find-replace-icon.png)

1. Dans la barre d’outils inférieure, saisissez un mot ou une expression.

1. Cliquez sur [!UICONTROL **Rechercher**].

1. Si nécessaire, saisissez un mot pour remplacer le mot trouvé.

1. Cliquez sur [!UICONTROL **Remplacer**].

## Rechercher et remplacer dans le référentiel

1. Accédez au **référentiel**.

1. Cliquez sur l’icône [!UICONTROL **Rechercher et remplacer**] en bas à gauche de l’écran.

1. Cliquez sur l’icône [!UICONTROL **Afficher les paramètres**].

1. Choisissez l’une des options suivantes :

   - **Extraction du fichier avant remplacement** — si un administrateur l&#39;active, le fichier sera extrait automatiquement avant de remplacer les termes de recherche.

   - **Mot entier uniquement** — limite la recherche pour renvoyer uniquement le mot ou l&#39;expression exact saisi.

   ![Rechercher un remplacement dans le référentiel](images/lesson-11/repository-find-replace.png)

1. Cliquez sur l’icône [!UICONTROL **Appliquer le filtre**] pour sélectionner le chemin d’accès dans le référentiel où vous souhaitez effectuer la recherche.

1. Saisissez les termes à rechercher et à remplacer.

1. Si nécessaire, sélectionnez **Créer une version après le remplacement**.

1. Cliquez sur [!UICONTROL **Rechercher**].

1. Ouvrez le fichier souhaité et utilisez les flèches pour passer d’un résultat trouvé au suivant.

   ![Rechercher l’interface utilisateur de navigation de remplacement](images/lesson-11/find-replace-navigation.png)

---
title: Profils de dossier
description: Création et utilisation de profils de dossier pour AEM Guides
exl-id: 5a0daa68-51ae-42d0-8320-6e8bdb1fe545
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 1%

---

# Profils de dossier

AEM permet d’accéder rapidement aux outils de configuration. En personnalisant Profils de dossier, différents services ou produits peuvent avoir des modèles, des environnements de création, des profils d’attributs conditionnels, des fragments de code ou même des configurations de l’éditeur web.

Des exemples de fichiers que vous pouvez choisir d’utiliser pour cette leçon sont fournis dans le fichier . [folderprofiles.zip](assets/folderprofiles.zip).

>[!VIDEO](https://video.tv.adobe.com/v/342758)

## Accès aux profils de dossier

Les configurations sont gérées via l’icône Profils de dossier .

1. Dans l’écran de navigation, cliquez sur le bouton [!UICONTROL **Outils**] icône .

   ![Icône Outils](images/reuse/tools-icon.png)

2. Sélectionner **Guides** dans le panneau de gauche.

3. Cliquez sur le bouton [!UICONTROL **Profils de dossier**] mosaïque.

   ![Profils de dossier](images/reuse/folder-profiles-tile.png)

4. Sélectionnez le profil souhaité. Par exemple, choisissez **Profil global**, qui est le profil par défaut.

   ![Profil global](images/lesson-3/global-profile-tile.png)

## Modification des attributs conditionnels dans le profil global

Une fois que vous avez accédé au profil global, vous pouvez modifier sa configuration. Les paramètres de profil global sont appliqués à tous les utilisateurs, sauf indication contraire.

1. Dans le profil global, sélectionnez la variable **Attributs conditionnels** .

2. Cliquez sur [!UICONTROL **Modifier**] dans le coin supérieur gauche de l’écran.

   ![Attributs conditionnels](images/lesson-3/edit-conditional-attributes.png)

3. Cliquez sur [!UICONTROL **Ajouter**].

4. Renseignez la variable **Nom**, **Valeur**, et **Libellé** pour la nouvelle condition.

   ![Nouvelle condition](images/lesson-3/new-condition.png)

5. Cliquez sur [!UICONTROL **Enregistrer**] dans le coin supérieur gauche de l’écran.
La nouvelle condition est désormais disponible pour tous les utilisateurs. Vous pouvez la sélectionner dans le panneau Propriétés du contenu et l’appliquer au contenu selon vos besoins.

## Création d’un profil de dossier

Outre le profil global par défaut, vous pouvez créer vos propres profils personnalisés.

1. Dans l’écran de navigation, cliquez sur le bouton [!UICONTROL **Outils**] icône .

   ![Icône Outils](images/reuse/tools-icon.png)

2. Sélectionner **Guides** dans le panneau de gauche.

3. Cliquez sur le bouton [!UICONTROL **Profils de dossier**] mosaïque.

   ![Profils de dossier](images/reuse/folder-profiles-tile.png)

4. Cliquez sur [!UICONTROL **Créer**].

5. Dans la boîte de dialogue Créer un profil de dossier .

   a. Nommez le profil.

   b. Spécifiez un chemin.

   c. Cliquez sur [!UICONTROL **Créer**].

   ![Créer un profil de dossier](images/lesson-3/create-folder-profile.png)

Une mosaïque avec le nouveau nom du profil s’affiche sur la page Profils de dossier .

## Ajout d’utilisateurs administratifs à partir de l’onglet Général

Les utilisateurs administratifs ont les droits de mettre à jour les attributs conditionnels, le modèle de création et les paramètres prédéfinis de sortie pour le profil de dossier.

1. Cliquez sur la mosaïque pour ouvrir le profil de dossier souhaité.

   ![Modifier le profil du dossier](images/lesson-3/edit-folder-profile.png)

2. Sélectionnez la **Général** .

3. Cliquez sur [!UICONTROL **Modifier**] en haut à gauche de l’écran.

4. Sous Utilisateurs administrateurs, sélectionnez un utilisateur dans la liste déroulante ou saisissez son nom.

5. Cliquez sur [!UICONTROL **Ajouter**].

   Si nécessaire, vous pouvez ajouter plusieurs utilisateurs administrateurs.

   ![Ajouter un administrateur](images/lesson-3/add-admin.png)

6. Cliquez sur [!UICONTROL **Enregistrer**] dans le coin supérieur droit de l’écran lorsque tous les utilisateurs ont été ajoutés.

Les utilisateurs administratifs sont désormais affectés à ce profil.

## Ajout d’une nouvelle audience à partir de l’onglet Attributs conditionnels

Une fois que vous avez accédé au profil global, vous pouvez modifier sa configuration. Les paramètres de profil global sont appliqués à tous les utilisateurs, sauf indication contraire.

1. Dans le profil de dossier souhaité, sélectionnez la variable **Attributs conditionnels** .

2. Cliquez sur [!UICONTROL **Modifier**] dans le coin supérieur gauche de l’écran.

   ![Modification des attributs conditionnels 2](images/lesson-3/edit-conditional-attributes-2.png)

3. Cliquez sur [!UICONTROL **Ajouter**].

4. Renseignez la variable **Nom**, **Valeur**, et **Libellé** pour la nouvelle condition.

   Cliquez sur le bouton [!UICONTROL **Plus**] sign vous permet d’ajouter des paires Valeur et Libellé supplémentaires pour l’attribut nommé.

   ![Ajout de conditions](images/lesson-3/add-conditions.png)

5. Cliquez sur [!UICONTROL **Enregistrer**] dans le coin supérieur gauche de l’écran.

Les nouveaux attributs conditionnels ont été ajoutés à ce profil.

## Choisissez un modèle et une map dans l’onglet Modèles de création

AEM Guides est fourni avec des modèles et des mappages de création prêts à l’emploi. Vous pouvez les limiter à des auteurs spécifiques. Par défaut, les modèles sont stockés à l’emplacement Ressources dans un dossier de modèles DITA.

1. Dans le profil de dossier souhaité, sélectionnez l’onglet Modèles de création .

2. Cliquez sur Modifier dans le coin supérieur gauche de l’écran.

3. Ajout d’un modèle de carte.

   a. Dans la **Modèles de mappage** , sélectionnez une option dans les cartes disponibles.

   b. Cliquez sur [!UICONTROL **Ajouter**].

   ![Modèles de mappage](images/lesson-3/map-templates.png)

4. Ajout d’un modèle de rubrique.

   a. Dans la **Modèles de rubrique** , sélectionnez une option dans les modèles disponibles.

   ![Modèles de rubrique](images/lesson-3/topic-templates.png)

5. Cliquez sur [!UICONTROL **Ajouter**].

6. Ajoutez d’autres modèles de rubrique selon les besoins.

7. Lorsque vous avez terminé, cliquez sur [!UICONTROL **Enregistrer**] en haut à gauche de l’écran.

Les nouveaux modèles de création ont été ajoutés à ce profil.

## Suppression de paramètres prédéfinis non essentiels de l’onglet Paramètres prédéfinis de sortie

Vous pouvez configurer chaque paramètre prédéfini de sortie en fonction du profil de dossier. Les paramètres de sortie prédéfinis qui ne sont pas nécessaires doivent être supprimés.

1. Dans le profil de dossier souhaité, sélectionnez la variable **Paramètres prédéfinis de sortie** .

2. Dans le panneau de gauche, cochez les cases des paramètres prédéfinis qui ne sont pas obligatoires.

   ![Suppression de paramètres prédéfinis](images/lesson-3/delete-presets.png)

3. Cliquez sur [!UICONTROL **Supprimer le paramètre prédéfini**] dans le coin supérieur gauche de l’écran.

4. Dans la boîte de dialogue Supprimer le paramètre prédéfini, cliquez sur [!UICONTROL **Supprimer**].

   ![Supprimer](images/lesson-3/delete.png)

Désormais, les seuls paramètres prédéfinis de sortie affichés sont ceux qui seront utilisés.

## Chargement d’un fragment de code à partir de l’onglet Configuration de l’éditeur XML

1. Dans le profil de dossier souhaité, sélectionnez la variable **Configuration de l’éditeur XML** .

2. Sous Fragments de code de l’éditeur XML, cliquez sur [!UICONTROL **Télécharger**].

   ![Transférer le fragment de code](images/lesson-3/upload-snippet.png)

3. Accédez à un fragment de code créé précédemment.

4. Cliquez sur [!UICONTROL **Ouvrir**].

5. Cliquez sur [!UICONTROL **Enregistrer**] en haut à gauche de l’écran.

Vous avez modifié la configuration de l’éditeur pour inclure des fragments de code.

## Spécification du profil de dossier dans le référentiel

Dans l’éditeur, vous pouvez voir les résultats des modifications que vous avez apportées aux profils de dossier.

1. Accédez à **Repository View**.

2. Cliquez sur le dossier du contenu que vous souhaitez utiliser.

3. Cliquez sur le bouton [!UICONTROL **Préférences utilisateur**] dans la barre d’outils supérieure.

   ![Préférences utilisateur](images/lesson-3/hr-user-prefs.png)

4. Dans la boîte de dialogue Préférences utilisateur, sélectionnez le profil de dossier de votre choix dans la liste déroulante.

   ![Sélectionner les préférences utilisateur](images/lesson-3/select-user-pref.png)

5. Cliquez sur [!UICONTROL **Enregistrer**].

Vous avez appliqué le profil de dossier à votre contenu. Désormais, lorsque vous créez une rubrique DITA, une liste restreinte de types de rubrique est affichée en fonction du profil de dossier. La condition d’audience contient les paramètres globaux ainsi que ceux spécifiques au profil de dossier. Le fichier de fragments de code que vous avez chargé a créé un ensemble de fragments de code par défaut dans lequel vous pouvez effectuer votre choix. Le tableau de bord des cartes affiche les paramètres prédéfinis de sortie restreints.

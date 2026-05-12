---
title: Profils de dossier
description: Créations et utilisation de profils de dossiers pour AEM Guides
exl-id: 5a0daa68-51ae-42d0-8320-6e8bdb1fe545
TQID: https://experienceleague.adobe.com/ztMvUcFQ-GJTOEU3ikB-2WFgj--ttbY7JoSyGW6Poa8
product_v2:
  - id: fae5e35a-80c9-4b94-9352-1a060a6aab1d
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: ab01a588-7dea-43f2-a699-0b3f128465d6
  - id: cb8c6a2a-3c38-4e40-867c-756f8c36bb0e
subfeature_v2:
  - id: ad602516-aca3-4247-9ae8-f393d958efa9
  - id: b0521e56-a0b2-40b6-bf47-ebc98751f9ba
  - id: b1ef4d86-3917-4b76-a0bc-4a4771f9b3b0
  - id: f89f75b0-cf2e-4e96-aec8-fe8c39cbd0ef
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 27ffc636d63300fb2e99903d92cab12f0cfcbb25
workflow-type: tm+mt
source-wordcount: 917
ht-degree: 2%

---

# Profils de dossier

AEM fournit un accès rapide aux outils de configuration. En personnalisant les profils de dossier, différents services ou produits peuvent avoir des modèles uniques, des environnements de création, des profils d’attributs conditionnels, des fragments de code ou même des configurations d’éditeur web.

Des exemples de fichiers que vous pouvez choisir d’utiliser pour cette leçon sont fournis dans le fichier [folderprofiles.zip](assets/folderprofiles.zip).

>[!VIDEO](https://video.tv.adobe.com/v/342758?quality=12&learn=on)

## Accéder aux profils de dossier

Les configurations sont gérées à l’aide de l’icône Profils de dossier .

1. Dans l’écran de navigation, cliquez sur l’icône [!UICONTROL **Outils**].

   ![&#x200B; Icône Outils &#x200B;](images/reuse/tools-icon.png)

1. Sélectionnez **Guides** dans le panneau de gauche.

1. Cliquez sur la mosaïque [!UICONTROL **Profils de dossier**].

   ![Profils de dossier](images/reuse/folder-profiles-tile.png)

1. Sélectionnez le profil souhaité. Par exemple, choisissez **Profil global**, qui est le profil par défaut.

   ![Profil global](images/lesson-3/global-profile-tile.png)

## Modification des attributs conditionnels dans le profil global

Une fois que vous avez accédé au profil global, vous pouvez modifier sa configuration. Sauf indication contraire, les paramètres du profil global s’appliquent à tous les utilisateurs.

1. Dans le profil global, sélectionnez l’onglet **Attributs conditionnels**.

1. Cliquez sur [!UICONTROL **Modifier**] dans le coin supérieur gauche de l’écran.

   ![Attributs conditionnels](images/lesson-3/edit-conditional-attributes.png)

1. Cliquez sur [!UICONTROL **Ajouter**].

1. Renseignez les champs **Nom**, **Valeur** et **Libellé** pour la nouvelle condition.

   ![nouvelle condition](images/lesson-3/new-condition.png)

1. Cliquez sur [!UICONTROL **Enregistrer**] dans le coin supérieur gauche de l’écran.
Le nouveau statut est désormais disponible pour tous les utilisateurs et utilisatrices. Vous pouvez la sélectionner dans le panneau Propriétés du contenu et l’appliquer au contenu selon vos besoins.

## Créer un nouveau profil de dossier

Outre le profil global par défaut, vous pouvez créer vos propres profils personnalisés.

1. Dans l’écran de navigation, cliquez sur l’icône [!UICONTROL **Outils**].

   ![&#x200B; Icône Outils &#x200B;](images/reuse/tools-icon.png)

1. Sélectionnez **Guides** dans le panneau de gauche.

1. Cliquez sur la mosaïque [!UICONTROL **Profils de dossier**].

   ![Profils de dossier](images/reuse/folder-profiles-tile.png)

1. Cliquez sur [!UICONTROL **Créer**].

1. Dans la boîte de dialogue Créer un profil de dossier .

   a. Nommez le profil.

   b. Spécifiez un chemin d’accès.

   c. Cliquez sur [!UICONTROL **Créer**].

   ![Créer un profil de dossier](images/lesson-3/create-folder-profile.png)

Une mosaïque portant le nouveau nom de profil s’affiche sur la page Profils de dossier.

## Ajout d’utilisateurs administratifs à partir de l’onglet Général

Les utilisateurs administrateurs ont les droits de mettre à jour les attributs conditionnels, le modèle de création et les paramètres prédéfinis de sortie pour le profil de dossier.

1. Cliquez sur la mosaïque pour ouvrir le profil de dossier souhaité.

   ![Modifier profil de dossier](images/lesson-3/edit-folder-profile.png)

1. Sélectionnez l’onglet **Général**.

1. Cliquez sur [!UICONTROL **Modifier**] en haut à gauche de l’écran.

1. Sous Utilisateurs administrateurs, sélectionnez un utilisateur dans la liste déroulante ou saisissez son nom.

1. Cliquez sur [!UICONTROL **Ajouter**].

   Vous pouvez ajouter plusieurs utilisateurs administrateurs si nécessaire.

   ![Ajouter un administrateur](images/lesson-3/add-admin.png)

1. Cliquez sur [!UICONTROL **Enregistrer**] dans le coin supérieur droit de l’écran lorsque tous les utilisateurs ont été ajoutés.

Les utilisateurs administratifs sont désormais affectés à ce profil.

## Ajoutez une nouvelle audience à partir de l’onglet Attributs conditionnels .

Une fois que vous avez accédé au profil global, vous pouvez modifier sa configuration. Sauf indication contraire, les paramètres du profil global s’appliquent à tous les utilisateurs.

1. Dans le profil de dossier souhaité, sélectionnez l’onglet **Attributs conditionnels**.

1. Cliquez sur [!UICONTROL **Modifier**] dans le coin supérieur gauche de l’écran.

   ![Modifier les attributs conditionnels 2](images/lesson-3/edit-conditional-attributes-2.png)

1. Cliquez sur [!UICONTROL **Ajouter**].

1. Renseignez les champs **Nom**, **Valeur** et **Libellé** pour la nouvelle condition.

   Cliquez sur le signe [!UICONTROL **Plus**] pour ajouter des paires Valeur et Libellé supplémentaires pour l’attribut nommé.

   ![Ajouter des conditions](images/lesson-3/add-conditions.png)

1. Cliquez sur [!UICONTROL **Enregistrer**] dans le coin supérieur gauche de l’écran.

Les nouveaux attributs conditionnels ont été ajoutés à ce profil.

## Choisissez un modèle et un mappage dans l’onglet Modèles de création .

AEM Guides est fourni avec des modèles et des mappages de création prêts à l’emploi. Vous pouvez les limiter à des auteurs spécifiques. Par défaut, les modèles sont stockés à l&#39;emplacement d&#39;Assets dans un dossier de modèles DITA.

1. Dans le profil de dossier souhaité, sélectionnez l’onglet Modèles de création .

1. Cliquez sur Modifier dans le coin supérieur gauche de l’écran.

1. Ajoutez un modèle de mappage.

   a. Dans le menu déroulant **Modèles de carte**, sélectionnez une option parmi les cartes disponibles.

   b. Cliquez sur [!UICONTROL **Ajouter**].

   ![Modèles de carte](images/lesson-3/map-templates.png)

1. Ajoutez un modèle de rubrique.

   a. Dans le menu déroulant **Modèles de rubrique**, sélectionnez une option parmi les modèles disponibles.

   ![Modèles de rubrique](images/lesson-3/topic-templates.png)

1. Cliquez sur [!UICONTROL **Ajouter**].

1. Ajoutez d&#39;autres modèles de rubriques, au besoin.

1. Lorsque vous avez terminé, cliquez sur [!UICONTROL **Enregistrer**] en haut à gauche de l’écran.

Les nouveaux modèles de création ont été ajoutés à ce profil.

## Suppression de paramètres prédéfinis non essentiels de l’onglet Paramètres prédéfinis de sortie

Vous pouvez configurer chaque paramètre prédéfini de sortie en fonction du profil de dossier. Les paramètres de sortie prédéfinis qui ne sont pas nécessaires doivent être supprimés.

1. Dans le profil de dossier souhaité, sélectionnez l’onglet **Paramètres prédéfinis de sortie**.

1. Dans le panneau de gauche, cochez les cases des paramètres prédéfinis qui ne sont pas obligatoires.

   ![Supprimer paramètres prédéfinis](images/lesson-3/delete-presets.png)

1. Cliquez sur [!UICONTROL **Supprimer le paramètre prédéfini**] dans le coin supérieur gauche de l’écran.

1. Dans la boîte de dialogue Supprimer le paramètre prédéfini , cliquez sur [!UICONTROL **Supprimer**].

   ![Supprimer](images/lesson-3/delete.png)

Désormais, les seuls paramètres prédéfinis de sortie qui s’affichent sont ceux qui seront utilisés.

## Téléchargez un fragment de code depuis l’onglet Configuration de l’éditeur XML .

1. Dans le profil de dossier souhaité, sélectionnez l’onglet **Configuration de l’éditeur XML**.

1. Sous Fragments de code de l’éditeur XML, cliquez sur [!UICONTROL **Télécharger**].

   ![Charger le fragment de code](images/lesson-3/upload-snippet.png)

1. Accédez à un fragment de code créé précédemment.

1. Cliquez sur [!UICONTROL **Ouvrir**].

1. Cliquez sur [!UICONTROL **Enregistrer**] en haut à gauche de l’écran.

Vous avez correctement modifié la configuration de l’éditeur pour inclure des fragments de code.

## Spécifier le profil de dossier dans le référentiel

Dans l’éditeur, vous pouvez voir les résultats des modifications que vous avez apportées aux profils de dossier.

1. Accédez à **Vue Référentiel**.

1. Cliquez sur le dossier correspondant au contenu que vous souhaitez utiliser.

1. Cliquez sur l’icône [!UICONTROL **Préférences utilisateur**] dans la barre d’outils supérieure.

   ![Préférences utilisateur](images/lesson-3/hr-user-prefs.png)

1. Dans la boîte de dialogue Préférences utilisateur , sélectionnez le profil de dossier souhaité dans la liste déroulante.

   ![Sélectionner les préférences utilisateur](images/lesson-3/select-user-pref.png)

1. Cliquez sur [!UICONTROL **Enregistrer**].

Vous avez appliqué le profil de dossier à votre contenu. Désormais, lorsque vous créez une rubrique DITA, une liste restreinte de types de rubriques basée sur le profil de dossier s&#39;affiche. La condition d’audience contient les paramètres globaux ainsi que ceux spécifiques au profil de dossier. Le fichier de fragments de code que vous avez chargé a créé un ensemble de fragments de code par défaut parmi lesquels choisir. Le tableau de bord des cartes affiche les paramètres prédéfinis de sortie restreints.

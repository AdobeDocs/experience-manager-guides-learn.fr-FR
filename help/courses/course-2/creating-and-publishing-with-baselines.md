---
title: Création et publication avec des lignes de base
description: Création et publication avec des lignes de base dans [!DNL Adobe Experience Manager Guides]
exl-id: 3c229c30-f2e0-4fb0-b60c-7bae60ef1a5b
source-git-commit: 1c4d278a05f2612bc55ce277efb5da2e6a0fa9a9
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 2%

---

# Création et publication avec des lignes de base

L’utilisation d’une ligne de base vous permet de créer une version de vos rubriques de mappage et du contenu de référence associé. Cela peut être basé sur une date, une heure ou des étiquettes spécifiques.

>[!VIDEO](https://video.tv.adobe.com/v/338993?quality=12&learn=on)

## Accès à l’onglet Lignes de base dans le tableau de bord des cartes

Vous pouvez accéder à vos lignes de base dans le tableau de bord des cartes.

1. Repository View, sélectionnez l’icône représentant des points de suspension sur votre carte pour ouvrir le menu Options, puis **Ouvrez le tableau de bord de la carte.**

   ![ellipsis-map-dashboard.png](images/ellipsis-map-dashboard.png)
Le tableau de bord des cartes s’ouvre dans un autre onglet.

2. Sélectionner **Lignes de base**.

   ![baseline-tab.png](images/baseline-tab.png)

L’onglet Lignes de base s’affiche.

## Création d’une ligne de base à partir de libellés

1. Dans l’onglet Lignes de base , sélectionnez **Créer**.

   ![create-baseline.png](images/create-baseline.png)

   Les informations de la nouvelle ligne de base s’affichent. Son nom par défaut dépend de sa date de création.

2. Si nécessaire, donnez un nouveau nom à votre ligne de base.

3. Sous l’en-tête &quot;Définir la version sur&quot;, sélectionnez le cercle correspondant au libellé.
   ![set-the-version.png](images/set-the-version.png)

   >[!NOTE]
   >
   >REMARQUE : Le *Utiliser la dernière version si l’étiquette n’est pas présente* est sélectionnée par défaut. Si cette option n’est pas sélectionnée et que des rubriques ou des fichiers multimédias sans le libellé choisi existent dans votre carte, le processus de création de ligne de base échoue.

4. Saisissez le libellé que vous souhaitez utiliser.

5. Sélectionnez **Enregistrer**.

Votre ligne de base est créée. Un tableau de toutes les rubriques et des informations associées s’affiche.

### Utilisation de la fonction Parcourir toutes les rubriques

La fonction Parcourir toutes les rubriques vous permet d’afficher les informations de la rubrique, y compris la version et le libellé, ainsi que de spécifier la version utilisée. Vous pouvez y accéder en sélectionnant **Parcourir toutes les rubriques** lors de la création ou de la modification de la ligne de base.

![browse-all-topics.png](images/browse-all-topics.png)

## Création d’une ligne de base basée sur la date et l’heure

Vous pouvez également créer des lignes de base qui sont un instantané dans le temps.

1. Assurez-vous que l’onglet Lignes de base est ouvert et sélectionnez Créer.

   ![create-baseline.png](images/create-baseline.png)

2. Sous l’en-tête &quot;Définir la version sur&quot;, sélectionnez le cercle correspondant à &quot;Version activée&quot;.

   ![version-on.png](images/version-on.png)

3. Sélectionnez l’icône du calendrier et indiquez la date et l’heure de votre choix.

   ![calendar.png](images/calendar.png)

4. Si nécessaire, donnez un nouveau nom à votre ligne de base.

5. Sélectionnez **Enregistrer**.

Votre ligne de base est créée. Un tableau de toutes les rubriques et des informations associées s’affiche.

### Ajout de libellés à votre ligne de base

Vous pouvez attribuer une nouvelle étiquette en bloc à tout le contenu de votre carte.

1. Sélectionnez la ligne de base pour laquelle vous souhaitez ajouter des libellés.

2. Sélectionner **Ajouter des étiquettes**.

   ![add-libellés.png](images/add-labels.png)

   La boîte de dialogue Ajouter un libellé s’affiche.

3. Saisissez le libellé à attribuer, puis sélectionnez **Ajouter**.

Le libellé a été ajouté à toutes les rubriques.

## Génération d’une sortie de site AEM à l’aide d’une ligne de base

1. Accédez à l’onglet Paramètres prédéfinis de sortie dans le tableau de bord des cartes.

2. Cochez la case AEM site .

   ![aem-site-checkbox.png](images/aem-site-checkbox.png)

3. Sélectionnez **Modifier**.

   ![edit-aem.png](images/edit-aem.png)

   Une nouvelle page s’affiche.

4. Cochez la case Utiliser la ligne de base , puis sélectionnez la ligne de base que vous souhaitez utiliser dans la liste déroulante.

   ![baseline.png](images/baseline.png)

5. Sélectionnez **Terminé**.

   ![done.png](images/done.png)

6. Sélectionner **Générer**.

   ![generate.png](images/generate.png)

   Votre sortie a été générée avec une ligne de base.

## Affichage de la sortie générée

1. Accédez à l’onglet Sorties du tableau de bord des cartes.

2. Sélectionnez le texte de la colonne Paramètre de génération pour ouvrir la sortie.
   ![aem-site-link.png](images/aem-site-link.png)

## Suppression d’une ligne de base

1. Dans l’onglet Lignes de base , sélectionnez la ligne de base à supprimer.

2. Sélectionner **Supprimer**.

   ![remove-baseline.png](images/remove-baseline.png)

   La boîte de dialogue Supprimer la ligne de base s’affiche.

3. Sélectionner **Supprimer**.

La ligne de base est supprimée.

## Duplication d’une ligne de base

1. Dans l&#39;onglet Lignes de base , sélectionnez la ligne de base que vous souhaitez dupliquer.

2. Sélectionner **Dupliquer**.

   ![duplicate.png](images/duplicate.png)

3. Sélectionnez **Enregistrer**.

   ![save.png](images/save.png)

La ligne de base en double est créée.

## Modification d’une ligne de base

Vous pouvez directement spécifier la version d’une rubrique utilisée dans une ligne de base.

1. Dans l&#39;onglet Lignes de base , sélectionnez la ligne de base que vous souhaitez modifier.
2. Sélectionnez **Modifier**.

   ![edit-aem.png](images/edit-aem.png)

3. Sélectionner **Parcourir toutes les rubriques**.

   ![browse-all-topics.png](images/browse-all-topics.png)

   Un tableau des rubriques et des informations associées s’affiche.

4. Pour les rubriques que vous souhaitez modifier, sélectionnez la version souhaitée dans la liste déroulante sous la colonne Version .

   ![version-dropdown.png](images/version-dropdown.png)

5. Sélectionnez **Enregistrer**.

Vos modifications ont été enregistrées. Votre ligne de base utilise désormais les versions de la rubrique que vous avez spécifiée.

## Création d’un paramètre prédéfini de sortie de site AEM personnalisé

Il est difficile de faire la distinction entre les sorties par défaut du même type dans l’onglet Sorties . L’utilisation d’un paramètre prédéfini de sortie personnalisé avec un nom unique et convivial vous permet de résoudre ce problème.

Dans ce cas, nous créons un paramètre prédéfini de sortie basé sur une ligne de base.

1. Accédez à l’onglet Paramètres prédéfinis de sortie dans le tableau de bord des cartes.

2. Sélectionnez **Créer**.

   ![create-output-preset.png](images/create-output-preset.png)

   Une nouvelle page de paramètres prédéfinis de sortie s’affiche, appelée Nouvelle sortie.
3. Dans le champ Nom du paramètre , saisissez un nom convivial.

4. Cochez la case Utiliser la ligne de base , puis sélectionnez la ligne de base souhaitée dans le menu déroulant.

   ![baseline.png](images/baseline.png)

5. Sélectionnez **Terminé**.

Votre nouveau paramètre prédéfini de sortie a été créé et s’affiche sur la page des paramètres prédéfinis de sortie.

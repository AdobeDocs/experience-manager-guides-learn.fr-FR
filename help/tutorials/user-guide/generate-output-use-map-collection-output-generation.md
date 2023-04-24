---
title: Utilisation de la collecte des cartes pour la génération de la sortie
description: Découvrez comment utiliser la collecte de cartes pour la génération de sortie
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 1%

---


# Utilisation de la collecte des cartes pour la génération de la sortie {#id1723F20G0HS}

Dans n’importe quelle organisation, un produit peut comporter plusieurs types de documentation. En tant que spécialiste de la publication, vous souhaitez contrôler la sortie que vous souhaitez générer pour quel document. Il doit également exister un moyen de publier par lots plusieurs documents en un seul clic.

AEM Guides vous permet d’organiser votre contenu pour la publication à l’aide d’un tableau de bord appelé Collection de cartes. Une collection de cartes vous permet d’assembler tous les types de documents différents en une seule unité. Vous pouvez choisir le type de sortie à générer pour chaque document de votre collection de cartes. De plus, vous pouvez également générer une sortie et voir la progression de la génération de la sortie depuis le tableau de bord de publication.

Collection de cartes vous offre la possibilité de voir si une modification est apportée à une carte à partir de la dernière sortie publiée. Vous pouvez afficher les détails dans l’onglet Cartes et paramètres prédéfinis de votre collection de cartes, puis republier la sortie si nécessaire. Pour plus d’informations, voir Ajout d’une carte à une collection de cartes.

## Création d’une collection de mappages et ajout de mappages DITA

Pour créer une collection de mappages et ajouter des mappages DITA à la collection, procédez comme suit :

1. Dans l’interface utilisateur d’Assets, cliquez sur **Mappage de collections**.

   Si le lien Mapper les collections n’est pas disponible, sélectionnez la variable **Navigation** dans le rail de gauche, puis cliquez sur **Mappage de collections**.

   ![](images/access-map-collection-left-rail.png)

1. Saisissez un titre pour votre collection de mappages.
1. Cliquez sur **Créer**.

   Un message de réussite s’affiche lors de la création de la collection de mappages.

1. Cliquez sur **Fermer** sur le message Succès .

   Le fichier de mappage nouvellement créé s’affiche sur la page Collections de mappages .

1. Cliquez sur la zone grise dans la mosaïque de la collection que vous souhaitez modifier.
1. Cliquez sur **Modifier** puis cliquez sur **Ajouter des mappages**.
1. Recherchez et ajoutez les mappages DITA à ajouter à la collection de mappages.

   Par défaut, tous les paramètres prédéfinis et paramètres régionaux associés à la carte sont ajoutés automatiquement.

1. Sélectionnez la sortie souhaitée en activant ou en désactivant le bouton coulissant.
1. Cliquez sur **Terminé**.

   Les fichiers de mappage DITA sont ajoutés à votre collection de cartes.


![](images/maps_presets_62_63.png)

Les options de filtrage et les détails de mappage suivants sont affichés sur la page de collection :

- **Filtre :** Le dernier rail affiche les filtres suivants :
   - **Modifié**: Vous pouvez sélectionner Oui ou Non. Si vous sélectionnez l’option Oui, seules les cartes DITA modifiées s’affichent dans le tableau Cartes et paramètres prédéfinis .
   - **Paramètre prédéfini**: Sélectionnez un paramètre prédéfini pour lequel vous souhaitez filtrer les fichiers map. Par exemple, si vous choisissez *AEM site* prédéfini, alors seules les cartes qui comportent la variable *AEM site* paramètre prédéfini de sortie configuré dessus.
   - **Langue**: Vous pouvez sélectionner l’un des codes de langue disponibles et afficher uniquement la langue sélectionnée dans le tableau Cartes et paramètres prédéfinis .
- **Cartes et paramètres prédéfinis** table : Le tableau Cartes et paramètres prédéfinis présente des informations dans les colonnes suivantes :
   - **Carte**: Affiche le titre du fichier de mappage DITA.
   - **Langue**: Affiche la langue du mappage DITA.
   - **Paramètre prédéfini**: Affiche le type de paramètre prédéfini de sortie configuré dans le fichier map.
   - **Modifié**: Indique si le mappage DITA est mis à jour après la dernière publication. En fonction de ces informations, vous pouvez décider si vous souhaitez republier la sortie pour ce mappage DITA ou non.
   - **Dernière génération**: Affiche la date et l’heure de la dernière sortie générée.

## Configuration et génération de la sortie à l’aide d’une collection de cartes

Pour configurer et générer la sortie à l’aide d’une collection de cartes, procédez comme suit :

1. Ouvrez la collection de cartes.
1. \(Facultatif\) Effectuez l’une des opérations suivantes selon vos besoins :
   - Appliquez des filtres à partir du rail de gauche pour filtrer les mappages, le paramètre prédéfini de sortie ou la langue modifiés.
   - Si nécessaire, cliquez sur **Modifier** et modifiez la sortie souhaitée en activant ou en désactivant le bouton coulissant.
1. Utilisez l’une des méthodes suivantes :

   - Pour générer la sortie des mappages sélectionnés, sélectionnez les fichiers de mappage et cliquez sur **Générer la sélection**.
   - Pour générer une sortie de toutes les cartes DITA avec leurs paramètres prédéfinis configurés, cliquez sur **Générer tout**.

   >[!IMPORTANT]
   >
   > Si un processus de génération de sortie pour un paramètre prédéfini ou un mappage DITA se trouve dans la file d’attente ou en cours, vous ne pouvez pas lancer une autre tâche de génération de sortie pour le même paramètre prédéfini ou le même mappage.


## Suppression d’une collection de cartes ou d’un mappage DITA de la collection de cartes

- Pour supprimer une collection de mappages, sélectionnez-la dans la page Collection de mappages, puis cliquez sur **Supprimer**.
- Pour supprimer un mappage DITA d’une collection de mappages, ouvrez la collection de mappages en mode d’édition, sélectionnez le fichier de mappage DITA, puis cliquez sur **Supprimer de la collection**.

   Cela supprime également tous les paramètres prédéfinis ou paramètres régionaux associés au mappage DITA de la collection de cartes.


## Annulation d’une tâche de génération de sortie à partir d’une collection de cartes

Semblable à la manière d’annuler une tâche de génération de sortie à partir de la fonction [Console de mappage DITA](generate-output-for-a-dita-map.md#id2061H100T5Z) ou le [Publier le tableau de bord](generate-output-publish-dashboard.md#), vous pouvez annuler une tâche de génération de sortie à partir d’une collection de cartes. Accédez à l’onglet Sorties d’une collection de cartes, accédez à la tâche de publication que vous souhaitez annuler, puis cliquez sur le bouton **Annuler Cette Tâche** pour annuler la tâche de publication.

![](images/cancel-publish-task-map-collection.png)

**Rubrique parente :**[ Génération de sortie](generate-output.md)


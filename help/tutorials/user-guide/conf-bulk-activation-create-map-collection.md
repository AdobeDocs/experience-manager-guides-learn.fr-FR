---
title: Création d’une collection de cartes d’activation en bloc
description: Découvrez comment créer une collection de cartes d’activation en bloc
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---


# Création d’une collection de cartes d’activation en bloc {#id214GG0E90EV}

Pour créer une collection de cartes d’activation en bloc, procédez comme suit :

1. Sélectionner **Guides** dans la liste des outils.

1. Cliquez sur le lien Adobe Experience Manager en haut de l’écran et choisissez **Outils**.

1. Cliquez sur le bouton **Tableau de bord de publication en bloc** mosaïque.

   Pour la première fois, une page de collections vierge s’affiche. Si vous avez déjà créé des collections d’activation en bloc, elles s’affichent sur cette page.

1. Cliquez sur **Créer**.

1. Saisissez le titre de votre collection de cartes d’activation en bloc, puis cliquez sur **Créer**.

   Un message de réussite s’affiche lors de la création de la collection de mappages d’activation en bloc.

1. Cliquez sur **Ouvrir** sur le message Succès .

1. Cliquez sur **Modifier** puis cliquez sur **Ajouter des mappages**.

1. Recherchez et ajoutez les mappages DITA à ajouter à la collection de mappages d’activation en bloc.

   Par défaut, tous les paramètres prédéfinis et paramètres régionaux associés à la carte sont ajoutés automatiquement.

1. Sélectionnez la sortie souhaitée en activant ou en désactivant le bouton coulissant.

   Vous pouvez choisir plusieurs paramètres prédéfinis de sortie pour toutes les langues disponibles.

1. Cliquez sur **Terminé**.

   Les fichiers de mappage DITA sont ajoutés à votre collecte de mappage d’activation en bloc.

   ![](images/bulk-activation-collection-created.png)


L’onglet Cartes et paramètres prédéfinis présente des informations dans les colonnes suivantes :

- **Carte**: Affiche le titre du fichier de mappage DITA.
- **Chemin de mappage**: Affiche le chemin d’accès complet du fichier de mappage DITA.

- **UUID**: Affiche l’identifiant unique associé au fichier.

- **Langue**: Affiche le code de langue du mappage DITA.
- **Paramètre prédéfini**: Affiche le type de paramètre prédéfini de sortie configuré dans le fichier map.
- **Modifié**: Indique si le mappage DITA est mis à jour après la dernière publication. En fonction de ces informations, vous pouvez décider si vous souhaitez activer ou non la sortie pour ce mappage DITA.
- **Généré**: Affiche la date et l’heure de la dernière sortie générée.
- **Publié**: Affiche la date et l’heure de la dernière sortie publiée \(ou activée\). Si vous cliquez sur le lien, la page Résultats de l’activation s’affiche avec des informations sur le chemin racine d’activation du contenu.


Les options de filtrage disponibles dans le panneau de gauche sont les suivantes :

- **Modifié**: Vous pouvez sélectionner Oui ou Non. Si vous sélectionnez oui, seules les cartes DITA modifiées s’affichent. Une carte modifiée est une carte qui a été générée depuis sa dernière publication.
- **Paramètre prédéfini**: Sélectionnez un paramètre prédéfini pour lequel vous souhaitez filtrer les fichiers map. Par exemple, si vous choisissez *AEM site* prédéfini, alors seules les cartes qui comportent la variable *AEM site* paramètre prédéfini de sortie configuré dessus.
- **Langue**: Vous pouvez sélectionner l’un des codes de langue disponibles et afficher uniquement la langue sélectionnée dans l’onglet Cartes et paramètres prédéfinis .

- **Filtre :** Le dernier rail affiche les filtres suivants :
- **Cartes et paramètres prédéfinis** table : Le tableau Cartes et paramètres prédéfinis présente les colonnes suivantes :

**Rubrique parente :**[ Activation en masse de contenu publié](conf-bulk-activation.md)


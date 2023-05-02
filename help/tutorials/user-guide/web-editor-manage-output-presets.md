---
title: Gestion des paramètres prédéfinis de sortie de profil global et de dossier
description: Découvrez comment gérer les paramètres prédéfinis de sortie de profil global et de dossier
source-git-commit: 3b33b27e4acb8d0b185427725e23b8beac0c2a46
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---


# Gestion des paramètres prédéfinis de sortie de profil global et de dossier {#id22BLJ0D0V1U}

Les paramètres prédéfinis de profil global et de dossier ne sont disponibles que pour les utilisateurs administratifs au niveau du dossier.

En tant qu’administrateur, AEM Guides vous permet de créer et de gérer des paramètres prédéfinis de sortie pour les profils globaux et de dossiers. Vous pouvez ensuite facilement utiliser ces paramètres prédéfinis de sortie pour générer une sortie pour toutes les cartes liées à ce profil global ou de dossier.

Effectuez les étapes suivantes pour créer un paramètre prédéfini de sortie pour les profils globaux et de dossier :

1. Sélectionnez le mappage DITA pour lequel vous souhaitez créer un paramètre prédéfini de sortie.
1. Sélectionnez la **Modifier les rubriques** de l’option **Options** du fichier map. Le fichier de mappage est ouvert pour modification dans l’éditeur web.
1. Dans le **Sortie** sélectionnez l’icône + pour créer un paramètre prédéfini de sortie pour votre mappage DITA.

   ![](images/add-global-output-preset.png){width="350" align="left"}

1. Saisissez les informations suivantes dans la variable **Ajouter un paramètre prédéfini** dialog :
   - Type
   - Nom
   - Target \(pour le paramètre prédéfini de la base de connaissances\)
1. Sélectionnez la **Ajouter au profil de dossier** pour créer un paramètre prédéfini de sortie pour le profil de dossier associé, puis cliquez sur **Ajouter**. Le paramètre prédéfini est créé et s’affiche sous la propriété **Sortie** de toutes les cartes associées. \( ![](images/global-preset-icon.svg)L’icône \) indique un paramètre prédéfini de niveau profil de dossier.
1. Renseignez les détails de la configuration.

   >[!NOTE]
   >
   > Ces paramètres prédéfinis ajoutés au profil de dossier sont indépendants des mappages. Par conséquent, les configurations spécifiques aux mappages ne sont pas présentes pour ces paramètres prédéfinis.

1. Vous pouvez sélectionner la variable **Générer un paramètre prédéfini** dans la partie supérieure pour générer la sortie pour les mappages liés au paramètre prédéfini de sortie créé. Vous verrez l’état du processus de génération de sortie. Pour afficher la sortie, placez le pointeur de la souris sur la rubrique et cliquez sur **Afficher la sortie**.

>[!NOTE]
>
> AEM Guides fournit également un paramètre prédéfini de sortie de PDF prêt à l’emploi pour générer la sortie pour vos mappages DITA.

**Autres opérations du menu Options**

Vous pouvez également effectuer les opérations suivantes sur le paramètre prédéfini à partir du menu Options :

- Sélectionnez le paramètre prédéfini comme paramètre prédéfini pdf par défaut. Le paramètre prédéfini sélectionné est alors utilisé comme paramètre prédéfini par défaut pour générer la sortie du PDF à l’aide de la fonction **Téléchargement en tant que PDF** pour une carte.
- **Modifier**, **Renommer**, **Dupliquer** ou **Supprimer** un paramètre prédéfini de sortie existant à partir de la fonction **Options** .

>[!NOTE]
>
> Lorsqu’un paramètre prédéfini de sortie dans les profils globaux et de dossiers est supprimé, il se reflète dans toutes les mappages connexes et n’apparaîtra pas sous le **Sortie** .

**Rubrique parente :**[ Utilisation de l’éditeur web](web-editor.md)

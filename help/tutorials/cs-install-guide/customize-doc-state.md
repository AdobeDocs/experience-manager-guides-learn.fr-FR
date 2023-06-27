---
title: Configuration des états du document
description: Découvrez comment configurer des états de document
source-git-commit: e3b2fc8c96ce535bb91e7bce935720aa389a917a
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 0%

---


# Configuration des états du document {#id181GB0400UI}

AEM Guides vous permet de définir les états du document pour les rubriques DITA en fonction des exigences de votre entreprise. Vous pouvez définir différents états de votre document du début à la fin. Par exemple, le premier état peut être Version préliminaire et il peut passer à Révision, Approuvé, Traduit et enfin à Publié.

Un sujet peut passer d’un état à un autre de deux façons : manuelle et automatique. Les états du document définis dans un profil peuvent être utilisés pour modifier manuellement l’état du document. Vous pouvez le faire à partir de la page Propriétés d’un fichier de rubrique. Vous pouvez également définir qui peut déplacer le document d’un état à un autre. Par exemple, un auteur peut créer un document et l’état par défaut du document peut être Version préliminaire. Lorsque l’auteur envoie le document pour révision, il peut modifier l’état du document en In-Review. Le réviseur peut modifier l’état du document en Approuvé ou en Version préliminaire en fonction du processus de révision. Si le document est Approuvé, l’éditeur peut modifier l’état du document en Traduit ou Publié selon le processus.

>[!NOTE]
>
> Si un utilisateur appartient à la variable *administrateurs* , l’utilisateur peut modifier l’état d’un document à partir de n’importe quel état, indépendamment des transitions d’état du document définies dans le système.

## Création d’un état de document

AEM Guides est fourni avec un ensemble d’états de document par défaut. Ces états sont les suivants :

- Brouillon
- Modifier
- En révision
- Approuvé
- Révisé
- Terminé

Ces états par défaut sont disponibles pour toutes les rubriques DITA créées sous DAM. Vous pouvez créer vos propres états de document et les affecter à un dossier spécifique. Tous les fichiers DITA créés sous ce dossier auront alors accès aux états de document nouvellement créés.

Pour créer des états de document à l’aide du profil de dossier, procédez comme suit :

1. Cliquez sur le lien Adobe Experience Manager en haut de l’écran et choisissez **Outils**.
1. Sélectionner **Guides** dans la liste des outils.
1. Cliquez sur la mosaïque États du document .

   La page Assets States (états des ressources) s’affiche. Par défaut, la page affiche un profil par défaut.

1. Cliquez sur **Créer un profil** et saisissez les informations suivantes :
   - Saisissez le nom du profil dans le champ Profil .
   - Indiquez le chemin d’accès auquel vous souhaitez appliquer le nouveau profil.
   - Spécifiez les états du document dans le **États autorisés** under **Etats**. Les états du document par défaut sont Brouillon, Modifier, En révision, Approuvé et Terminé.-

     Cliquez sur le bouton **Ajouter** pour ajouter un état de document.

      - Cliquez sur l’icône Supprimer pour supprimer un état de document.

     >[!NOTE]
     >
     > Ne supprimez pas un état de document si les documents sont toujours dans cet état. Si vous supprimez un état de document, vous ne pourrez pas modifier l’état du document de ces documents, à moins que vous n’apparteniez à l’événement *administrator* groupe d’utilisateurs.

   - Spécifiez l’état de début du document dans le **État de départ**.
   - Spécifiez l’état de fin du document dans le **État de fin**.
   - Spécifiez la transition d’état du document dans **De** et **À** under **Transition d’état**.

      - Spécifier les utilisateurs et les groupes d’utilisateurs pouvant modifier l’état du document dans **Groupes**.

      - Cliquez sur le bouton **Ajouter** pour ajouter une transition d’état.

      - Cliquez sur l’icône Supprimer pour supprimer une transition d’état.

     >[!NOTE]
     >
     > Ne supprimez pas une transition d’état si des documents sont toujours présents dans `From` état. Si vous supprimez une transition d’état, vous ne pourrez pas modifier l’état du document de ces documents, à moins que vous n’apparteniez au *administrator* groupe d’utilisateurs.

1. Cliquez sur **Terminé**.

## Création d’une copie d’un profil d’état de document

Selon vos besoins, vous pouvez créer une copie d’un profil d’état de document existant. Vous pouvez utiliser la copie comme base pour créer un autre profil de document.

Pour créer une copie d’un profil d’état de document, procédez comme suit :

1. Cliquez sur le lien Adobe Experience Manager en haut de l’écran et choisissez **Outils**.
1. Sélectionner **Guides** dans la liste des outils.
1. Cliquez sur la mosaïque États du document .

   La page Assets States (états des ressources) s’affiche.

1. Sélectionnez le profil d’état du document à dupliquer, puis cliquez sur **Duplication de profil**.
1. Apportez les modifications requises et cliquez sur **Terminé**.

## Suppression d’un état ou d’une transition d’état de document

>[!NOTE]
>
> Ne supprimez pas une transition d’état ou d’état du document si les documents se trouvent toujours à l’état ou dans une transition d’état. Si vous supprimez une transition d’état ou d’état, vous ne pourrez pas modifier l’état du document de ces documents, sauf si vous appartenez au *administrator* groupe d’utilisateurs.

Effectuez les étapes suivantes pour supprimer une transition d’état ou d’état de document d’un profil d’état de document :

1. Cliquez sur le lien Adobe Experience Manager en haut de l’écran et choisissez **Outils**.
1. Sélectionner **Guides** dans la liste des outils.
1. Cliquez sur la mosaïque États du document .

   La page Assets States (états des ressources) s’affiche.

1. Sélectionnez le profil d’état du document à partir duquel vous souhaitez supprimer l’état du document, puis cliquez sur **Modifier le profil**.
1. Supprimez la transition d’état ou d’état du document et cliquez sur **Terminé**.

## Suppression d’un profil d’état de document

Pour supprimer un profil d’état de document, procédez comme suit :

1. Cliquez sur le lien Adobe Experience Manager en haut de l’écran et choisissez **Outils**.
1. Sélectionner **Guides** dans la liste des outils.
1. Cliquez sur le bouton **États du document** mosaïque.

   La page Assets States (états des ressources) s’affiche.

1. Sélectionnez le profil d’état du document à supprimer, puis cliquez sur **Supprimer le profil**.

## Automatiser la modification de l’état du document

Si vous ne souhaitez pas modifier manuellement les états du document, vous pouvez créer un processus et automatiser la modification de l’état du document.

>[!NOTE]
>
> Les workflows automatisés doivent être conformes aux états et aux transitions du document définis dans la configuration. Le système n’effectue aucune vérification des modifications d’état effectuées par le biais de workflows automatisés.

1. Cliquez sur le lien Adobe Experience Manager en haut de l’écran et choisissez **Outils**.
1. Sélectionner **Workflow** dans la liste des outils.

1. Cliquez sur le bouton **Modèles** mosaïque.

1. Sélectionnez le workflow approprié, par exemple Rubriques de révision.

1. Cliquez sur **Modifier**.

   Le workflow s’ouvre dans un nouvel onglet.

1. Cliquez sur **Modifier** \(en haut à droite\).

1. Ouvrez le **Étapes** navigateur ; using **Activer/désactiver le panneau latéral**, à l’extrémité gauche de la barre d’outils supérieure

1. Faites glisser l’étape appropriée\(s\) vers l’emplacement requis dans le modèle.

1. Cliquez sur la nouvelle étape que vous avez ajoutée dans le modèle de workflow et sélectionnez **Configurer** à partir de la barre d’outils du composant.

1. Ouvrez le **Processus** .

1. Dans le **Processus** liste déroulante, sélectionnez **Définition de l’état du document pour n’importe quelle ressource DAM**.

1. Sélectionnez la **Avance du gestionnaire** .

   ![](assets/update-workflow-doc-state_cs.png)

1. Dans le **Arguments** , saisissez l’état du document vers lequel vous souhaitez effectuer la transition à partir du workflow sélectionné.

   >[!NOTE]
   >
   > Assurez-vous de saisir l’état correct du document dans la zone de texte Arguments . Si vous saisissez une valeur incorrecte, l’état du document est incorrect.

1. Confirmez la modification avec **Enregistrer et fermer**.


## Activer le workflow de validation

AEM Guides fournit un processus d’approbation de document qui vous aide à contrôler le cycle de vie de votre processus de développement de documents. Pour activer le workflow de validation, procédez comme suit :

1. Pour télécharger le fichier de configuration de l’interface utilisateur, connectez-vous à Adobe Experience Manager en tant qu’administrateur.

1. Cliquez sur le lien Adobe Experience Manager en haut de l’écran et choisissez **Outils**.
1. Sélectionner **Guides** dans la liste des outils, puis cliquez sur l’icône **Profils de dossier**.
1. Cliquez sur le bouton **Profil global** mosaïque.
1. Sélectionnez la **Configuration de l’éditeur XML** et cliquez sur **Modifier** icône en haut
1. Cliquez sur le bouton **Télécharger** pour télécharger le fichier ui\_config.json sur votre système local. Vous pouvez ensuite apporter des modifications au fichier, puis charger le même fichier.
1. Dans le `ui_config.json` , activez la fonction de workflow d’approbation en modifiant la variable *features* , comme illustré ci-dessous :

   ```
   "features":  
   { 
      "approvalWorkflow":  true 
   }
   ```

1. Enregistrez le fichier et téléchargez-le.

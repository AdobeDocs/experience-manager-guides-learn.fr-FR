---
title: Modification des rubriques dans l’éditeur web
description: Découvrez comment modifier des rubriques dans l’éditeur web
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---


# Modification des rubriques dans l’éditeur web {#id2056B040VUI}

L’éditeur web s’accompagne d’un éventail de fonctions d’édition qui vous permettent de créer ou de modifier facilement vos fichiers de rubrique. Pour modifier une rubrique dans l’éditeur web, procédez comme suit.

>[!IMPORTANT]
>
> Si vous rencontrez une erreur d’application lors de l’utilisation de l’éditeur Web, actualisez la page pour continuer à fonctionner.

1. Pour apporter des modifications à votre rubrique, cliquez dans la limite de texte de l’élément requis et commencez à apporter des modifications.

1. Pour insérer un élément spécifique, cliquez à la fin de l’élément après lequel vous souhaitez insérer le nouvel élément et cliquez sur l’icône de l’élément requis dans la barre d’outils. Vous pouvez également utiliser le raccourci clavier `Alt+Enter` pour appeler la fonction **Insérer un élément** s’affiche.

   Une liste d’éléments s’affiche et peut être utilisée dans la rubrique. AEM Guides effectue un placement intelligent d’éléments en fonction de leur emplacement valide dans la rubrique.

   >[!NOTE]
   >
   > Vous pouvez également choisir l’icône à afficher dans la barre d’outils en configurant la `ui_config.json` fichier situé à l’emplacement - `/etc/designs/fmdita/clientlibs/xmleditor/`. Pour plus d’informations sur la personnalisation des fonctionnalités, contactez votre administrateur système.

1. Une fois la modification du document terminée, cliquez sur **Enregistrer**.

   >[!NOTE]
   >
   > Si vous ne souhaitez pas valider de modifications dans AEM référentiel, cliquez sur **Fermer**, puis cliquez sur **Fermer sans enregistrer** dans la boîte de dialogue Modifications non enregistrées .

   **Actualiser le navigateur lors de la modification des fichiers**
AEM Guides permet d’actualiser le navigateur lorsque vous modifiez votre contenu dans l’éditeur web. Cette fonctionnalité vous permet de continuer à modifier le contenu si vous rencontrez une erreur d’application pendant que vous travaillez. Si vous appuyez sur l’actualisation du navigateur alors qu’un ou plusieurs fichiers contenant des modifications non enregistrées sont ouverts pour modification, vous êtes averti que les modifications non enregistrées risquent d’être perdues. Vous avez la possibilité d’annuler l’opération d’actualisation et d’enregistrer vos fichiers pour conserver vos modifications.

   Même lors de l’actualisation du navigateur, les vues des panneaux gauche et droit sont conservées dans l’éditeur web. Par exemple, la principale rubrique du panneau Référentiel s’ouvre à nouveau. Le panneau de mappage est conservé avec la carte précédemment ouverte.

   La rubrique principale ou le mappage DITA est rouvert dans la zone d’édition du contenu.

   Le panneau de droite est également rouvert et affiche la même vue qu’avant l’actualisation.

   **Indicateur de copie de travail**
AEM Guides fournit l’indicateur de copie de travail qui indique si la \(copie de travail\) actuelle du fichier est synchronisée ou non avec la version enregistrée. Si vous avez apporté des modifications à votre copie actuelle et n’avez pas enregistré votre fichier, une marque \* apparaît avec le titre dans l’onglet Fichier du sujet. Cet indicateur sert de rappel pour enregistrer les modifications et disparaît lorsque vous enregistrez votre fichier.

   ![](images/working-copy-text-update-indicator.png){width="550" align="left"}

   AEM Guides indique également si la dernière copie enregistrée \(en cours\) du fichier est synchronisée ou non avec la version enregistrée. Si vous constatez des modifications non enregistrées entre la copie de travail et la dernière version enregistrée, un signe \* s’affiche avec les informations de version affichées dans le coin supérieur droit de l’onglet du fichier de la rubrique. Cet indicateur sert de rappel pour enregistrer et créer une version à partir de votre copie \(en cours\) actuelle du fichier.

   ![](images/version-update-indicator.png){width="550" align="left"}


**Rubrique parente :**[ Utilisation de l’éditeur web](web-editor.md)


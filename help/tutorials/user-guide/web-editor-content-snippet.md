---
title: Insertion d’un fragment de contenu à partir de votre source de données
description: Découvrez comment insérer un fragment de contenu de votre source de données
source-git-commit: 84dbcd80d8b41ae52ec7389dd0d0a750ea8d6c65
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---


# Insertion d’un fragment de contenu à partir de votre source de données

AEM Guides fournit la fonctionnalité permettant de se connecter à votre source de données. Vous pouvez récupérer vos données, les insérer dans vos rubriques et les modifier. Vous pouvez facilement créer un fragment de contenu à l’aide du générateur de fragments de contenu et le réutiliser dans vos rubriques.

Effectuez les étapes suivantes pour créer un fragment de contenu à l’aide du générateur de fragments de contenu et l’insérer dans votre rubrique :

1. Sélectionner **Sources de données** ![](images/data-source-icon.svg)   dans le panneau de gauche pour afficher les sources de données connectées. Le panneau Sources de données s’ouvre et affiche toutes les sources de données connectées. Pour plus d’informations, voir [Configuration d’un connecteur de source de données](../cs-install-guide/conf-data-source-connector.md).
   >[!NOTE]
   >
   > Vous verrez les sources de données pour lesquelles votre administrateur a configuré le connecteur.

1. Sélectionnez une source de données pour afficher les générateurs de fragments de contenu disponibles pour la source de données sélectionnée.
   ![](images/code-snippet-generator.png){width="300" align="left"}
1. Sélectionner **Ajouter** pour ajouter un nouveau générateur de fragments de contenu. Le **Ajout d’un générateur de fragments de contenu** s’ouvre.

1. Saisissez la requête dans la zone de texte Requête de données .
1. Sélectionnez le modèle qui mappe avec votre source de données dans la **Modèle de mappage de données** menu déroulant.
Les modèles d’usine de la source de données sélectionnée s’affichent dans la liste déroulante. Par exemple, vous pouvez afficher le modèle &quot;sql-table&quot; pour la source de données nommée &quot;PostgreSQL&quot;.

   >[!NOTE]
   >  
   > Si votre administrateur a configuré des modèles personnalisés, ces modèles s’affichent également dans la liste déroulante (en fonction des configurations de chemin d’accès au modèle effectuées par votre administrateur).
1. Cliquez sur **Récupérer** pour récupérer les données de la source de données et appliquer le modèle aux données qui résultent de la requête SQL.
1. Vous pouvez afficher les données dans l’aperçu ou la vue source DITA.

   1. L&#39;aperçu montre comment les données seront affichées lorsqu&#39;elles seront insérées dans le contenu. L&#39;aperçu affiche une petite fraction des données au format du modèle sélectionné.
Par exemple :
      * Si vous avez sélectionné le modèle sql-table, vous pouvez visualiser les données SQL sous forme tabulaire.
      * Si vous avez sélectionné le modèle de liste jira, vous pouvez afficher une liste classée pour les problèmes Jira.

   1. La vue source affiche les données dans la vue source DITA.
      ![](images/add-content-snippet-generator.png){width="800" align="left"}
1. Pour enregistrer les résultats de la requête, saisissez le nom du générateur, puis cliquez sur **AJOUTER**.   Un nouveau générateur de fragments de contenu est ajouté à la liste.

   >[!NOTE]
   >
   > Vous devez respecter la convention d’affectation des noms de fichier pour le nom du nouveau générateur de contenu. Vous ne pouvez pas avoir d’espace dans le nom du générateur de fragments de contenu. En outre, vous ne pouvez pas enregistrer un nouveau générateur de contenu avec le nom d’un générateur de contenu existant. Une erreur se produit.

## Options d’un générateur de fragment de contenu

Cliquez avec le bouton droit de la souris sur un générateur de fragments de contenu pour ouvrir les options. Les options suivantes vous permettent d’effectuer les opérations suivantes :
* **Insérer**: Utilisez cette option pour insérer le fragment de contenu sélectionné dans la rubrique ouverte pour modification dans l’éditeur web. Comme les données sont insérées sous forme d’extrait de code, vous pouvez également modifier les données de votre rubrique dans l’éditeur web.

  >[!NOTE]
  > 
  > L’option Insérer s’affiche uniquement lorsque vous modifiez une rubrique.

* **Modifier**: Utilisez cette option pour apporter des modifications au générateur de fragments de contenu et enregistrez-le.
* **Supprimer**: Utilisez cette option pour supprimer le générateur de fragments de contenu sélectionné.
* **Dupliquer**: Utilisez cette option pour créer un doublon ou une copie du générateur de fragments de contenu sélectionné. Le doublon est créé par défaut avec un suffixe (tel que generator_1).

### Insertion d’un fragment de requête

Vous pouvez également utiliser la variable **Insérer un fragment de requête** ![](images/data-source-icon.svg)   de la barre d’outils principale pour insérer le fragment de données dans les rubriques.  Vous pouvez sélectionner un générateur dans la liste déroulante, modifier votre requête ou modifier le modèle et insérer les données dans votre rubrique.

![](images/insert-content-snippet.png){width="800" align="left"}





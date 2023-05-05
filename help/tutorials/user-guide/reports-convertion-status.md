---
title: Rapport d’état de conversion
description: Découvrez comment générer un rapport d’état de conversion
exl-id: 41887af2-404f-41d7-b54c-ec49797200f0
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Rapport d’état de conversion {#id205BBA00WZZ}

AEM Guides offre une fonctionnalité de conversion performante pour convertir des documents de divers formats en DITA. Le rapport État de conversion fournit une vue consolidée de toutes les tâches de conversion exécutées par AEM Guides.

Pour afficher le rapport d’état de conversion, procédez comme suit :

1. Cliquez sur le lien Adobe Experience Manager en haut de l’écran et choisissez **Outils**.

1. Sélectionner **Guides** dans la liste des outils.

1. Cliquez sur le bouton **Rapport d’état de conversion** mosaïque.

   Le rapport d’état de conversion s’affiche pour toutes les tâches de conversion exécutées sur le système.

   ![](images/conversion-status-report.png){width="800" align="left"}

1. La page du rapport se divise en deux parties :

   - **Filtrer:**

      Vous pouvez filtrer les données du rapport en fonction du type de fichier et de l’état de conversion. Dans le type de fichier, vous pouvez choisir d’afficher les données du rapport pour le document Word, le HTML structuré, XML et le type DocBook des documents. Dans l’état, vous pouvez choisir d’afficher les données du rapport pour les tâches ayant été exécutées avec succès, ayant échoué, Principal ou en file d’attente.

      La capture d’écran suivante présente les données du rapport pour les tâches de conversion dont l’état est En échec, Principal et En file d’attente.

      ![](images/conversion-report-failed-active-queued.png){width="800" align="left"}

   - **Données du rapport :**

      Les données du rapport contiennent les colonnes suivantes :

      - **Nom du fichier**: Nom du fichier source sur lequel le processus de conversion a été exécuté. Cliquez sur le lien Nom du fichier pour accéder à l’emplacement du document source.

      - **Type de fichier**: Type du document source, qui peut être Word, HTML structuré, XML et DocBook.

      - **Ajouté par**: Nom de l’utilisateur qui a exécuté la tâche de conversion.

      - **Date d’ajout**: Date à laquelle la tâche a été exécutée. Cliquez sur le lien Date d’ajout pour télécharger le fichier journal.

      - **Chemin**: Chemin complet du document source.

      - **État**: État des tâches de conversion : succès, échec, Principal ou en file d’attente.

      - **Sortie**: Chemin du document converti avec succès. Cliquez sur le lien Sortie pour accéder à l’emplacement d’enregistrement de la sortie.


**Rubrique parente :**[ Rapports](reports-intro.md)

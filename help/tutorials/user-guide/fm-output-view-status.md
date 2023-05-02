---
title: Afficher l'état de la tâche de génération de sortie
description: Découvrez comment afficher l’état de la tâche de génération de sortie
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# Afficher l&#39;état de la tâche de génération de sortie {#viewing_output_history}

Une fois que vous avez lancé la tâche de génération de sortie pour un document FrameMaker, AEM Guides envoie cette tâche à la file d’attente de génération de sortie. Cette file d’attente est mise à jour en temps réel, indiquant l’état de chaque tâche de génération de sortie dans la file d’attente.

Effectuez les étapes suivantes pour afficher la file d’attente de génération de sortie :

1. Dans l’interface utilisateur d’Assets, accédez au document FrameMaker et cliquez dessus pour lequel vous souhaitez vérifier l’état de génération de sortie.

1. Cliquez sur Sorties.

   ![](images/output-queued-fm.png)

1. La page Sorties est divisée en deux parties :

   - **Sorties en file d’attente :**

      Répertorie les sorties en attente de génération ou en cours de processus de génération. Vous pouvez également trouver le paramètre de génération de sortie ou le paramètre prédéfini utilisé pour la tâche en file d’attente, le type, l’utilisateur qui a lancé la tâche, le temps écoulé depuis que la tâche est en file d’attente et l’état actuel.

   - **Sorties générées**

      Répertorie les tâches de sortie qui ont été terminées. Ici encore, les informations affichées sont similaires à la section Sorties en file d’attente , avec la seule différence de temps de génération de sortie.

      Dans cette liste, vous pouvez avoir des tâches qui ont été exécutées avec succès ou des tâches qui ont échoué. Pour les tâches terminées avec succès, le processus de publication crée un fichier journal \(logs.txt\) accessible en cliquant sur le lien dans la colonne Généré à.


**Rubrique parente :**[ Génération d’une sortie de documents FrameMaker](fm-output-generatation.md)

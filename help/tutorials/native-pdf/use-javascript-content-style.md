---
title: Fonction de publication native d’un PDF | Utilisation de JavaScript pour travailler avec du contenu ou du style
description: Découvrez comment créer des feuilles de style et créer des styles pour votre contenu.
source-git-commit: 09918abbdade934468dea1c55d0ca2cd60622b35
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 1%

---


# Utilisation de JavaScript pour utiliser du contenu ou du style

La fonction Publication de PDF natif vous permet d’exécuter JavaScript pour manipuler le contenu ou le style appliqué au contenu avant la génération du PDF final. Cette fonctionnalité vous permet de contrôler entièrement la manière dont votre sortie finale est générée. Par exemple, vous pouvez ajouter des informations d’avis juridique à la sortie du PDF, qui réside dans un autre PDF. En utilisant JavaScript, vous pouvez ajouter les informations de notification légale une fois le PDF créé pour le contenu de base, mais avant la génération du PDF final.\
Pour prendre en charge l’exécution JavaScript, la fonction Publication de PDF natif vous donne les fonctions de rappel suivantes :

* `window.pdfLayout.onBeforeCreateTOC(callback)`: Cette fonction de rappel est exécutée avant la génération de la table des matières.
* `window.pdfLayout.onBeforePagination(callback)`: Cette fonction de rappel est exécutée après la génération de la table des matières, mais avant l’ajout de sauts de page dans le PDF.
* `window.pdfLayout.onAfterPagination(callback)`: Cette fonction de rappel est exécutée après l’ajout de la table des matières et des sauts de page dans le PDF.

>[!NOTE]
>
>En interne, une séquence d’exécution est conservée pour ces fonctions de légende. Tout d’abord, onBeforeCreateTOC est exécuté, suivi de onBeforePagination, et enfin, onAfterPagination est exécuté.

En fonction du type de contenu ou de modification de style que vous souhaitez effectuer, vous pouvez choisir la fonction de rappel à utiliser. Par exemple, si vous souhaitez ajouter du contenu, il est recommandé de le faire avant que la table des matières ne soit générée. De même, si vous souhaitez effectuer certaines mises à jour de style, celles-ci peuvent être effectuées avant ou après la pagination.

Dans l&#39;exemple suivant, la position des titres des illustrations est changée de au-dessus des images en dessous des images. Pour cela, vous devez activer l’option Exécution JavaScript dans le paramètre prédéfini. Pour ce faire, procédez comme suit :

1. Ouvrez le paramètre prédéfini à modifier.
1. Accédez au **Avancé** .
1. Sélectionnez la **Activation de JavaScript** .
1. Enregistrez le paramètre prédéfini et fermez-le.

Créez ensuite un fichier JavaScript avec le code suivant et enregistrez-le dans le dossier Ressources de votre modèle :

```css
...
/*
* DITA only allows the figure title to be placed above images 
* This JavaScript code is used to move the figure title below the image
* */
window.addEventListener('DOMContentLoaded', function () {
    window.pdfLayout.onBeforeCreateTOC(function() {
        var titleNodes = document.querySelectorAll('.fig > .title')
        for (var i = 0; i < titleNodes.length; i++) {
            var titleNode = titleNodes[i]
            var figNode = titleNode.parentNode
            var imageNode = figNode.querySelector('.image')
            if(imageNode && imageNode.parentNode !== figNode) {
              imageNode = imageNode.parentNode
            }
            if (figNode && imageNode && imageNode.parentNode === figNode) {
                figNode.insertBefore(imageNode, titleNode)
            }
        }
    })
});
...
```

>[!NOTE]
>
>Le `window.addEventListener('DOMContentLoaded', function ()` doit être appelée avant l’utilisation des fonctions de rappel.

Ensuite, ce script doit être appelé à partir d’un fichier de modèle utilisé pour générer la sortie du PDF. Dans notre exemple, nous l’ajouterons dans le modèle de table des matières. Assurez-vous que la variable `<script>` est ajoutée dans une balise prédéfinie `<div>` dans la balise `<body>` balise . Si vous l’ajoutez dans la variable `<head>` ou en dehors de la balise `<body>` , le script ne s’exécutera pas.

<img src="./assets/js-added-resources-template.png" width="500">

La sortie générée à l’aide de ce code et le modèle affiche le titre de la figure sous l’image :

<img src="./assets/fig-title-below-image.png" width="500">

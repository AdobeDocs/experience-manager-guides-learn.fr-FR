---
title: Personnalisation AEM dictionnaire par défaut
description: Découvrez comment personnaliser AEM dictionnaire par défaut
source-git-commit: 6051181e243cf71919901093c1b5590f21832545
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 1%

---


# Personnalisation AEM dictionnaire par défaut {#id209SD8000WU}

L’éditeur web peut être configuré pour utiliser AEM vérificateur orthographique ou le vérificateur orthographique du navigateur. Si vous choisissez de travailler avec AEM vérificateur orthographique, vous avez la possibilité de définir votre liste de mots personnalisée. Ces mots personnalisés sont ensuite ajoutés au dictionnaire d’AEM et ces mots ne sont pas marqués comme \(incorrects\) dans l’éditeur web.

Effectuez les étapes suivantes pour créer votre liste de mots personnalisés, qui sont ajoutés dans AEM dictionnaire :

1. Créez le fichier user\_dictionary.txt avec la liste des mots que vous souhaitez définir dans votre dictionnaire personnalisé.

   >[!NOTE]
   >
   > Chaque mot personnalisé doit être défini sur une nouvelle ligne.

1. Enregistrez le fichier à l’emplacement suivant dans le référentiel Git de Cloud Manager :

   /apps/fmdita/config

1. Enregistrez le fichier.

   Validez les modifications et exécutez le pipeline Cloud Manager \(CI/CD\) pour déployer les modifications de configuration.


Les auteurs doivent redémarrer leur session Web Editor pour que la liste des mots personnalisés soit mise à jour dans AEM dictionnaire.

**Rubrique parente :**[ Personnalisation de l’éditeur web](conf-web-editor.md)


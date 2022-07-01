---
title: Publication avec conditions
description: Publication avec des conditions avec les guides Adobe Experience Manager
exl-id: ea94824a-884b-447f-9562-e6c629b8133b
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 4%

---

# Publication avec conditions

La publication conditionnelle permet d’écrire une source de contenu pour une ou plusieurs audiences, produits ou plateformes. Ces informations peuvent ensuite être publiées dynamiquement et uniquement le contenu spécifiquement requis inclus dans la sortie.

>[!VIDEO](https://video.tv.adobe.com/v/339041)

## Préparation de l’exercice

Vous pouvez télécharger des fichiers d’exemple pour l’exercice ici.

[Exercise-Download](assets/exercises/publishing-with-conditions.zip)

## Marquage du contenu avec des attributs conditionnels

1. Ouvrez la rubrique à modifier.

2. Saisissez le texte qui doit devenir conditionnel. Par exemple, un ou plusieurs paragraphes, un tableau entier, une figure ou un autre contenu.

   ![Presenting-Information](images/presenting-info.png)

3. Sélectionnez le contenu spécifique auquel attribuer un attribut conditionnel. Par exemple, un seul paragraphe dans la source.

   ![Template-Choice](images/template-choice.png)

4. Dans le rail de droite, assurez-vous que les propriétés s’affichent.

5. Ajoutez un attribut pour l’audience, le produit ou la plateforme.

6. Attribuez une valeur à l’attribut . Les mises à jour de l’affichage du contenu pour afficher les balises conditionnelles ont été appliquées.

   ![Spécifier un modèle](images/specify-template.png)

## Prévisualiser du contenu conditionnel

1. Cliquez sur **Aperçu**. 

2. Sous **Filtres**, sélectionnez ou désélectionnez les conditions à afficher ou masquer.

3. Sélectionner ou désélectionner **Texte des conditions de mise en surbrillance**.

   ![Aperçu-Conditionnel-Content](images/preview-conditional-content.png)

## Création d’un paramètre prédéfini de condition

Un paramètre prédéfini de condition est un ensemble de propriétés qui définissent ce qui doit être inclus ou exclu, ou autrement marqué, pendant la génération de la sortie.

1. Dans le tableau de bord des cartes, sélectionnez la variable **Paramètres prédéfinis de condition** .

2. Cliquez sur **Créer**.

3. Sélectionner **Ajouter** (ou **Tout ajouter**).

4. Attribuez un nom à la condition.

5. Sélectionnez une combinaison d’attributs, de libellés et d’actions.

   ![Create-Condition-Preset](images/create-condition-preset.png)

6. Recommencez l’étape selon vos besoins.

7. Cliquez sur **Enregistrer**.

## Génération d’une sortie conditionnelle

Une fois les conditions appliquées au contenu, il peut être généré en tant que sortie. Cela peut utiliser un paramètre prédéfini de condition ou un fichier DITAval.

## Génération d’une sortie conditionnelle à l’aide d’un paramètre prédéfini de condition

1. Sélectionnez la **Paramètres prédéfinis de sortie** .

2. Sélectionnez un paramètre prédéfini de sortie.

3. Cliquez sur **Modifier**.

4. Sous **Appliquer la condition en utilisant** sélectionnez un paramètre prédéfini de condition.

   ![Générer une sortie conditionnelle](images/generate-conditional-output.png)

5. Cliquez sur **Terminé**.

6. Générez le paramètre prédéfini de sortie et passez en revue le contenu.

## Génération d’une sortie conditionnelle à l’aide d’un fichier DITAval

Le fichier DITAval peut être utilisé pour publier du contenu conditionnel. Pour ce faire, un fichier doit être créé ou chargé, puis référencé lors de la publication.

1. Sélectionnez la **Paramètres prédéfinis de sortie** .

2. Sélectionnez un paramètre prédéfini de sortie.

3. Cliquez sur **Modifier**.

4. Sous Appliquer la condition à l’aide de , sélectionnez un fichier DITAval.

   ![Generate-Using-DITAval](images/generate-using-ditaval.png)

5. Cliquez sur **Terminé**.

6. Générez le paramètre prédéfini de sortie et passez en revue le contenu.

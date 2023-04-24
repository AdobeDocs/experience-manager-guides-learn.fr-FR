---
title: Utilisation des paramètres de condition prédéfinis
description: Découvrez comment utiliser les paramètres prédéfinis de condition
source-git-commit: 6eb8d29e71301581e8dbb5b6a4252194c5a89f96
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 2%

---


# Utilisation des paramètres de condition prédéfinis {#id1825FL004PN}

Vous pouvez définir des attributs dans vos rubriques DITA et utiliser le paramètre prédéfini de condition pour spécifier ce qui se passe avec l’attribut dans la sortie finale. Par exemple, vous pouvez ajouter des attributs comme version 1.0 et version 2.0 dans votre contenu, et utiliser un paramètre prédéfini de condition pour inclure la version 1.0 de la version 1.0 et exclure la version 2.0. De même, vous pouvez ajouter des attributs comme OS Windows et OS Linux à votre contenu, puis inclure ou exclure le contenu approprié pour votre sortie finale en fonction du système d’exploitation.

## Création d’un paramètre prédéfini de condition

Pour créer un paramètre de condition prédéfini, procédez comme suit :

1. Cliquez sur **Paramètres prédéfinis de condition** dans la console de mappage DITA.
1. Cliquez sur **Créer** bouton .
1. Saisissez le nom du paramètre prédéfini dans **Condition de nom**.
1. Sélectionnez l’une des actions par défaut suivantes dans **Définir l’action par défaut sur** menu déroulant :

   - Inclure
   - Exclure
   - Passage
   - Indicateur L’action est définie comme action par défaut pour tous les attributs, qu’ils soient ajoutés ou non au paramètre de condition prédéfini.

   Par exemple, votre document contient 15 attributs de condition et vous en avez inclus quatre dans le paramètre prédéfini de condition. Si vous sélectionnez **exclude** comme action par défaut, elle est appliquée aux 15 attributs.

1. Pour ajouter les attributs, effectuez l’une des opérations suivantes :
   - Cliquez sur **Ajouter** à un attribut du paramètre prédéfini de condition. Vous pouvez répéter cette étape pour ajouter d’autres attributs.
   - Cliquez sur **Tout ajouter** pour ajouter tous les attributs au paramètre prédéfini de condition.
1. \(Facultatif\) Si nécessaire, vous pouvez remplacer l’action par défaut appliquée aux attributs à l’étape 4. Utilisez l’une des méthodes suivantes :
   - Sélectionner plusieurs attributs, choisissez une action parmi **Définissez l’action pour les conditions sélectionnées sur**, puis cliquez sur **Appliquer**.
   - Sélectionnez une action pour un attribut dans la **Action** menu déroulant.
1. Cliquez sur **Enregistrer**.

## Modifier un paramètre prédéfini de condition

Vous pouvez apporter des modifications à un paramètre prédéfini de condition existant afin de modifier les actions appliquées aux attributs dans le paramètre prédéfini de condition. Pour modifier un paramètre de condition prédéfini, procédez comme suit :

1. Cliquez sur **Paramètres prédéfinis de condition** dans la console de mappage DITA.
1. Cliquez sur **Modifier** bouton .
1. Apportez les modifications requises pour tous les attributs du paramètre prédéfini de condition.
1. Cliquez sur **Enregistrer**.

## Création d’une copie d’un paramètre prédéfini de condition

Vous pouvez créer une copie d’un paramètre prédéfini de condition, puis le modifier selon vos besoins. Pour créer une copie d’un paramètre prédéfini de condition, procédez comme suit :

1. Cliquez sur **Paramètres prédéfinis de condition** dans la console de mappage DITA.
1. Cliquez sur **Dupliquer** bouton .

   >[!NOTE]
   >
   > Le nom par défaut du paramètre prédéfini est `<selected condition preset name>_Duplicate`

   Vous pouvez modifier le nom selon vos besoins.

1. \(Facultatif\) Apportez les modifications requises pour tous les attributs du paramètre prédéfini de condition.
1. Cliquez sur **Enregistrer**.

## Supprimer le paramètre prédéfini de condition

Vous pouvez supprimer un ou plusieurs paramètres prédéfinis de condition dans la variable **Paramètre prédéfini de condition** de la console de mappage DITA. Pour supprimer des paramètres prédéfinis de condition, procédez comme suit :

1. Cliquez sur **Paramètres prédéfinis de condition** dans la console de mappage DITA.
1. Sélectionnez le ou les paramètres prédéfinis de condition que vous souhaitez supprimer.
1. Cliquez sur **Supprimer** bouton .
1. Cliquez sur **Supprimer** pour confirmer l’action.

**Rubrique parente :**[ Génération de sortie](generate-output.md)


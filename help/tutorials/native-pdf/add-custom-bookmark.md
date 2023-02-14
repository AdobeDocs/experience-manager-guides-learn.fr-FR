---
title: Fonction de publication native d’un PDF | Application d’un style personnalisé aux entrées de la table des matières et au contenu de la rubrique
description: Découvrez comment créer des feuilles de style et créer des styles pour votre contenu.
source-git-commit: fbb81704ea8d9d2793b066fa159b405460fa1dcf
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---


# Ajout d’un signet personnalisé dans la sortie PDF

En règle générale, la table des matières d’un mappage DITA est répliquée en tant que signets dans la sortie finale du PDF. Cette table des matières est créée à partir des titres de rubrique ou de section dans votre mappage DITA. Parfois, vous souhaiterez peut-être ajouter un signet personnalisé sur un contenu particulier dans la sortie de votre PDF pour une navigation facile. Pour ce faire, ajoutez une `outputclass` sur l’élément et en lui appliquant l’attribut suivant :

`bookmark-level: 3`

Ici, le `bookmark-level` est un attribut et un nombre `3` est la valeur qui indique le niveau dans la hiérarchie des signets où le signet est ajouté. Dans l&#39;exemple suivant, la rubrique de premier niveau &quot;Contacts&quot; comporte une table, &quot;Liste de contacts&quot;, sur laquelle nous avons ajouté une `outputclass` avec la valeur de `custom-bookmark`.

<img src="./assets/custom-bookmark-attribute.png" width="500">

La définition suivante de la variable `custom-bookmark` est ajoutée dans le fichier CSS :

```css
…
/*Adding a custom bookmark*/
.custom-bookmark{
    bookmark-level: 2
}
…
```

Dans la sortie du PDF, la variable *Liste de contacts* est ajouté au deuxième niveau dans la liste des signets du PDF, comme illustré ci-dessous :

<img src="./assets/custom-bookmark-in-pdf-output.png" width="500">

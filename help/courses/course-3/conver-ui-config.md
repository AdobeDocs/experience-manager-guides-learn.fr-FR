---
title: Configuration de l’éditeur d’AEM Guides
description: Personnalisation des configurations JSON et conversion des configurations d’interface utilisateur pour le nouvel éditeur AEM Guides.
exl-id: bb047962-0e2e-4b3a-90c1-052a2a449628
source-git-commit: 1ed48d543161be88becad9c0cd58014323aeda47
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 0%

---

# Vue d’ensemble

Lors de la migration de l’ancienne interface utilisateur vers la nouvelle interface utilisateur d’AEM Guides, les mises à jour de **ui_config** doivent être converties en configurations d’interface utilisateur plus flexibles et modulaires. Ce framework permet d’adopter facilement des modifications dans **editor_toolbar** et [autres barres d’outils](/help/courses/course-3/conver-ui-config.md#editing-json-for-different-screens). Le processus prend également en charge la modification d’autres vues et widgets dans l’application.

>[!NOTE]
>
>Les personnalisations appliquées à des boutons spécifiques peuvent rencontrer des problèmes lors de la transition vers la structure d’extension. Si cela se produit, vous pouvez créer un ticket d’assistance avec référence à cette page pour une assistance et une résolution rapides.

## Modification de JSON pour différents écrans

Les fichiers JSON peuvent être ajoutés à la section Configuration de l’interface utilisateur de l’éditeur XML pour divers écrans et widgets. Vous trouverez ci-dessous une liste des widgets couramment utilisés et de leurs identifiants :

1. [editor_toolbar](assets/toolbars/editor_toolbar.json) : barre d’outils de l’éditeur web composée d’actions sur les fichiers et le contenu.
1. [editor_tab_bar](assets/toolbars/editor_tab_bar.json) : la vue à onglets des fichiers ouverts dans webeditor contient des actions que vous pouvez exécuter sur les fichiers ouverts.
1. [file_mode_switcher](assets/toolbars/file_mode_switcher.json) : permet de basculer entre les différents modes disponibles (auteur, source, prévisualisation) pour les fichiers ouverts dans l’éditeur web.

   ![editor_toolbar](images/reuse/editor_toolbar.png)

1. [map_console_navigation_bar](assets/toolbars/map_console_navigation_bar.json) : il s’agit de la barre d’informations de la carte ouverte dans la console de carte. Il permet de modifier la carte et donne accès aux paramètres.
1. [map_console_action_bar](assets/toolbars/map_console_action_bar.json) : il s’agit de la barre d’actions des éléments de la console de mappage, tels que le paramètre prédéfini de sortie, la ligne de base, la traduction et les rapports, qui fournit des informations pertinentes ainsi que leurs boutons d’action respectifs.

   ![map_console](images/reuse/map_console.png)

1. [home_navigation_bar](assets/toolbars/home_navigation_bar.json) : barre d’en-tête de la page d’accueil des guides dans laquelle le message de bienvenue s’affiche avec le profil de dossier sélectionné.

   ![home_navigation_bar](images/reuse/home_navigation_bar.png)

<br>

## Structure générale de chaque fichier JSON

Chaque fichier JSON suit une structure cohérente :

1. `id` : indique le widget dans lequel le composant est personnalisé.
1. `targetEditor` : définit quand afficher ou masquer un bouton à l’aide des propriétés d’éditeur et de mode :

   Les options suivantes sont prises en charge sous `targetEditor` :

   - `mode`
   - `displayMode`
   - `editor`
   - `documentType`
   - `documentSubType`
   - `flag`

   Pour plus d’informations, consultez la section [Présentation des propriétés de targetEditor](#understanding-targeteditor-properties)

   >[!NOTE]
   >
   > La version 2506 de Experience Manager Guides introduit de nouvelles propriétés : `displayMode`, `documentType`, `documentSubType` et `flag`. Ces propriétés sont prises en charge uniquement à partir de la version 2506. De même, le passage de `toc` à `layout` dans la propriété mode s’applique également à partir de cette version.
   >
   > Un nouveau champ, `documentType`, est désormais disponible avec le champ `editor` existant.  Les deux champs sont pris en charge et peuvent être utilisés si nécessaire. Toutefois, il est recommandé d’utiliser `documentType` pour garantir la cohérence entre les implémentations, en particulier lorsque vous utilisez la propriété `documentSubType` . Le champ `editor` reste valide pour prendre en charge la rétrocompatibilité et les intégrations existantes.


1. `target` : indique l’emplacement où le nouveau composant sera ajouté. Cette méthode utilise des paires clé-valeur ou des index pour une identification unique. Les états d’affichage incluent :

   - **append** : ajoutez à la fin.

   - **prepend** : ajoutez au début.

   - **replace** : permet de remplacer un composant existant.

Exemple de structure JSON :

```json
{
  "id" : "editor_toolbar",
  "view": {
    "items": [
      {
        ...,
        "targetEditor": {
          "mode": [
            "preview"
          ],
          "editor": [
            "xml"
          ]
        },
        "target": {
          "key": "label",
          "value": "Table",
          "viewState": "prepend"
        },
        ...
      },
    ]
  }
}
```

<br>

## Compréhension des propriétés `targetEditor`

Vous trouverez ci-dessous une répartition de chaque propriété, son objectif et les valeurs prises en charge.

### `mode`

Définit le mode de fonctionnement de l’éditeur.

**Valeurs prises en charge** : `author`, `source`, `preview`, `layout` (précédemment `toc`), `split`

### `displayMode` *(facultatif)*

Contrôle la visibilité ou l’interactivité des composants de l’interface utilisateur. La valeur par défaut est définie sur `show` si elle n’est pas spécifiée.

**Valeurs prises en charge** : `show`, `hide`, `enabled`, `disabled`

Exemple :

```
 {
        "icon": "textBulleted",
        "title": "Custom Insert Bulleted",
        "on-click": "$$AUTHOR_INSERT_REMOVE_BULLETED_LIST",
        "key": "$$AUTHOR_INSERT_REMOVE_BULLETED_LIST",
        "targetEditor": {
          "documentType": [
            "ditamap"
          ],
          "mode": [
            "author"
          ],
          "displayMode": "hide"
        }
      },
```

### `editor`

Spécifie le type de document principal dans l&#39;éditeur.

**Valeurs prises en charge** : `ditamap`, `bookmap`, `subjectScheme`, `xml`, `css`, `translation`, `preset`, `pdf_preset`

### `documentType`

Indique le type de document principal.

**Valeurs prises en charge** : `dita`, `ditamap`, `bookmap`, `subjectScheme`, `css`, `preset`, `ditaval`, `reports`, `baseline`, `translation`, `html`, `markdown`, `conditionPresets`,

> Des valeurs supplémentaires peuvent être prises en charge pour des cas d’utilisation spécifiques.

Exemple :

```
 {
        "icon": "textNumbered",
        "title": "Custom Numbered List",
        "on-click": "$$AUTHOR_INSERT_REMOVE_NUMBERED_LIST",
        "key": "$$AUTHOR_INSERT_REMOVE_NUMBERED_LIST",
        "targetEditor": {
          "documentType": [
            "dita",
            "ditamap"
          ],
          "mode": [
            "author",
            "source"
          ]

        }
      },
```

### `documentSubType`

Classe ensuite le document en fonction des `documentType`.

- **Par`preset`** : `pdf`, `html5`, `aemsite`, `nativePDF`, `json`, `custom`, `kb`
- **Par`dita`** : `topic`, `reference`, `concept`, `glossary`, `task`, `troubleshooting`

> Des valeurs supplémentaires peuvent être prises en charge pour des cas d’utilisation spécifiques.

Exemple :

```
 {
        "icon": "rename",
        "title": "Custom Rename",
        "on-click": "$$PUBLISH_PRESETS_RENAME",
        "label": "Custom Rename",
        "key": "$$PUBLISH_PRESETS_RENAME",
        "targetEditor": {
          "documentType": [
            "preset"
          ],
          "documentSubType": [
            "nativePDF",
            "aemsite",
            "json"
          ]

        }
      },
```

### `flag`

Indicateurs booléens pour l’état ou les fonctionnalités du document.

**Valeurs prises en charge** : `isOutputGenerated`, `isTemporaryFileDownloadable`, `isPDFDownloadable`, `isLocked`, `isUnlocked`, `isDocumentOpen`

De plus, vous pouvez également créer un indicateur personnalisé à l’intérieur de `extensionMap` qui est utilisé comme indicateur dans `targetEditor`. Ici, `extensionMap` est une variable globale utilisée pour ajouter des clés personnalisées ou des valeurs observables.

Exemple :

```
 {
        "icon": "filePDF",
        "title": "Custom Export pdf",
        "on-click": "$$DOWNLOAD_TOPIC_PDF",
        "key": "$$DOWNLOAD_TOPIC_PDF",
        "targetEditor": {
          "documentType": [
            "markdown"
          ],
          "mode": [
            "preview"
          ],
          "flag": ["isPDFDownloadable"]

        }
      },
```


## Exemples

Vous trouverez ci-dessous un exemple d’ajout, de suppression ou de remplacement d’un bouton dans la barre d’outils de l’éditeur.

### Ajout d’un bouton

Ajout d&#39;un nouveau bouton **Insérer un tableau personnalisé** dans **editor_toolbar** pour ajouter un tableau simple visible uniquement en mode aperçu.

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "icon": "table",
        "title": "Insert Custom Table",
        "on-click": {
          "name": "$$AUTHOR_INSERT_ELEMENT",
          "args": [
            "simpletable",
            "table",
            "choicetable"
          ]
        },
        "key": "$$AUTHOR_INSERT_ELEMENT",
        "targetEditor": {
          "mode": [
            "preview"
          ],
        },
        "target": {
          "key": "label",
          "value": "Table",
          "viewState": "prepend"
        }
      }
    ]
  }
}
```

![Insérer un tableau personnalisé](images/reuse/insert-custom-table.png)

### Suppression d’un bouton

Suppression d’un bouton de la barre d’outils. Ici, nous supprimons le bouton Ajouter une image de la barre d’outils de l’éditeur.

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "hide": true,
        "target": {
          "key": "label",
          "value": "Image",
          "viewState": "replace"
        }
      }
    ]
  }
}
```

### Remplacement d’un bouton

Remplacement du bouton **Multimédia** de la barre d’outils par le bouton d’insertion de lien **Youtube** visible uniquement en mode création.

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "icon": "s2youtube",
        "title": "Youtube",
        "on-click": {
          "name": "$$AUTHOR_INSERT_ELEMENT",
          "args": "<object data='http://youtube.com'></object>"
        },
        "targetEditor": {
          "mode": [
            "author"
          ]
        },
        "target": {
          "key": "elementId",
          "value": "toolbar-multimedia",
          "viewState": "replace"
        }
      }
    ]
  }
}
```

![bouton Youtube](images/reuse/youtube-button.png)

<br>

### Ajout d&#39;un bouton en mode aperçu

Conformément à la conception, la visibilité des boutons est gérée séparément pour les modes verrouillé et déverrouillé (lecture seule) afin de conserver une expérience utilisateur claire et contrôlée. Par défaut, tout nouveau bouton ajouté est masqué lorsque l’interface est en mode lecture seule.
Pour rendre un bouton visible en mode **lecture seule** vous devez indiquer une cible qui le place dans une sous-section de la barre d’outils qui reste accessible même lorsque l’interface est verrouillée.
Par exemple, en spécifiant la cible en tant que **Télécharger sous forme de PDF**, vous pouvez vous assurer que le bouton apparaît dans la même section qu’un bouton visible existant, ce qui le rend accessible en mode déverrouillé.

```json
"target": {
  "key": "label",
  "value": "Download as PDF",
  "viewState": "prepend"
}
```

Ajout d’un bouton **Exporter en tant que PDF** en mode **Aperçu** qui sera visible à la fois en mode verrouillé et en mode déverrouillé.

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "icon": "filePDF",
        "title": "Export as PDF",
        "on-click": "$$DOWNLOAD_TOPIC_PDF",
        "key": "$$DOWNLOAD_TOPIC_PDF",
        "targetEditor": {
          "editor": [
            "ditamap",
            "xml"
          ],
          "mode": [
            "preview"
          ]
        },
        "target": {
          "key": "label",
          "value": "Download as PDF",
          "viewState": "prepend"
        }
      },
      {
        "icon": "filePDF",
        "title": "Export as PDF",
        "on-click": "$$DOWNLOAD_TOPIC_PDF",
        "key": "$$DOWNLOAD_TOPIC_PDF",
        "targetEditor": {
          "editor": [
            "ditamap",
            "xml"
          ],
          "mode": [
            "preview"
          ]
        }
      }
    ]
  }
}
```

Le fragment suivant présente le bouton **Exporter en tant que PDF** avec le scénario de verrouillage.

![Exporter sous PDF](images/reuse/lock.png)

En outre, le bouton **Exporter en tant que PDF** avec le scénario de déverrouillage est visible dans le fragment de code ci-dessous.

![Exporter sous PDF](images/reuse/unlock.png)

### Personnaliser les options affichées dans la liste déroulante Menu de la barre d’outils de l’éditeur

Vous pouvez ajouter, masquer, remplacer et ajouter des options personnalisées dans la liste déroulante Menu à l’aide des exemples suivants.

#### Appendice

Ajout d’une option dans le menu déroulant Menu . Ici, nous ajoutons **Bouton de menu personnalisé** dans les options de menu

```json
{
        "icon": "specialCharacter",
        "title": "Custom menu button",
        "on-click": "$$AUTHOR_INSERT_SYMBOL",
        "targetEditor": {
          "editor": [
            "ditamap"
          ],
          "mode": [
            "author"
          ]
        },
        "target": {
          "key": "label",
          "value": "Version label",
          "viewState": "append"
        }
      }
```

#### Remplacement de

Remplacement d’une option qui s’affiche dans le menu déroulant. Ici, nous remplaçons **Créer une tâche de révision** par **Bouton de menu personnalisé 3**.

```json
{
        "icon": "specialCharacter",
        "title": "Custom menu button 3",
        "on-click": "$$AUTHOR_INSERT_SYMBOL",
        "target": {
          "key": "label",
          "value": "Create review task",
          "viewState": "replace"
        }

      }
```

#### Masquage

Masquage d’une option qui s’affiche dans la liste déroulante Menu. Ici, nous masquons l’option **Rechercher et remplacer** du menu.

```json
{
        "hide": true,
        "target": {
          "key": "label",
          "value": "Find and replace",
          "viewState": "replace"
        }
      }
```

#### Ajout d&#39;une option personnalisée dans le sous-menu

Ajout d&#39;une option dans le sous-menu de la liste déroulante Menu .

```json
{
        "icon": "viewAllTags",
        "title": "Toggle Tags View Goziamasu",
        "key": "AUTHOR_TOGGLE_TAG_VIEW",
        "target": {
          "key": "label",
          "value": "Track changes",
          "viewState": "replace"
        },
        "targetEditor": {
          "documentType": [
            "dita"
          ],
          "mode": [
            "author"
          ]
        }

      }
```

## Comment charger des fichiers JSON personnalisés

1. Dans **Configuration de l’éditeur XML** cliquez sur **Modifier** dans la barre supérieure.
1. Désormais, dans la sous-section **Configuration de l’interface utilisateur de l’éditeur XML** vous pourrez voir un bouton **charger**.

   ![Bouton Charger](images/reuse/ui-config-upload.png){width="400" height="150"}

1. Vous pouvez cliquer sur et charger le fichier json modifié. (Le fichier json à charger doit porter le même nom que l’identifiant du widget personnalisé).
1. Une fois le chargement effectué, appuyez sur **Enregistrer** dans la barre supérieure.

   Pour chaque fichier chargé, vous pouvez également **supprimer** le fichier json pour supprimer sa personnalisation de l’interface utilisateur ou **télécharger** pour l’afficher ou le modifier à nouveau.

   ![bouton Télécharger](images/reuse/download-delete-json.png){width="400" height="150"}

<br>


## Comment charger un fichier CSS personnalisé

Vous pouvez également ajouter un CSS pour personnaliser l’aspect des boutons personnalisés ajoutés ou des widgets ou boutons existants dans l’interface utilisateur.

Pour un bouton personnalisé nouvellement ajouté, ajoutez un **extraclass** au bouton ou au composant personnalisé dans le fichier JSON.
Pour une ancienne classe, vous pouvez inspecter l’élément et modifier également les classes existantes.

```json
{
  "icon": "table",
  "title": "Insert Custom Table",
  "extraclass": "custom-css",
  "key": "$$AUTHOR_INSERT_ELEMENT",
  "targetEditor": {
    "mode": [
      "preview"
    ],
  },
  "target": {
    "key": "label",
    "value": "Table",
    "viewState": "prepend"
  }
}
```

1. Dans **Configuration de l’éditeur XML** cliquez sur **Modifier** dans la barre supérieure.
1. Désormais, dans la sous-section **Éditeur XML** mise en page de la page, un bouton **charger** s’affiche.

   ![Bouton Charger](images/reuse/page-layout-upload.png){width="400" height="150"}

1. Vous pouvez cliquer sur et charger le fichier CSS modifié. (Seuls les fichiers CSS sont pris en charge)
1. Une fois le chargement effectué, appuyez sur **Enregistrer** dans la barre supérieure.

   Pour chaque fichier chargé, vous pouvez également **supprimer** le fichier css pour supprimer sa personnalisation de l’interface utilisateur ou **télécharger** pour l’afficher ou le modifier à nouveau.

   ![bouton Télécharger](images/reuse/download-delete-css.png){width="400" height="150"}


<br>

### Exemple de personnalisation du css du bouton

Nous ajoutons ici un nouveau bouton **Insérer un tableau personnalisé** dans **editor_toolbar** pour ajouter un tableau simple visible uniquement en mode aperçu et y appliquer un CSS personnalisé.
Ce css modifie l’arrière-plan du bouton et la taille de police de son titre.

![ Exemple CSS ](images/reuse/css-customization.png)


```css
#editor_toolbar {
  .custom-css {
    background-color: burlywood;
    font-size: 2rem;  
  }
}
```

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "icon": "table",
        "title": "Insert Custom Table",
        "extraclass": "custom-css",
        ...
      }
    ]
  }
}
```

<br>

## Étapes de conversion de la configuration de l’interface utilisateur en Json modulaires

1. Dans l’écran de navigation, cliquez sur l’icône [!UICONTROL **Outils**].

   ![ Icône Outils ](images/reuse/tools.png)

1. Sélectionnez **Guides** dans le panneau de gauche.

1. Cliquez sur la mosaïque [!UICONTROL **Profils de dossier**].

   ![Profils de dossier](images/reuse/folder-profiles-tile.png)

1. Sélectionnez un profil de dossier.

1. Cliquez sur l’onglet [!UICONTROL **Configuration de l’éditeur XML**].

1. Vous pouvez cliquer sur le bouton **Convertir la configuration de l’interface utilisateur en JSON**. Cela génère le fichier json **editor_toolbar** et **map_console_action_bar** qui contient les modifications effectuées dans **ui_config**.

   ![Convertir la configuration de l’interface utilisateur en JSON](images/reuse/convert-ui-config-json.png)

1. Vous pouvez extraire les exemples de fichiers json générés pour [barre d’outils de l’éditeur](assets/editor_toolbar.json) et [barre d’actions de la console Carte](assets/map_console_action_bar.json)


>[!NOTE]
>
>Les modifications apportées aux sections **toolbar** et **topbar** sont ajoutées dans le fichier json **editor_toolbar** visible sur la page de l’éditeur. Les modifications apportées aux boutons liés aux paramètres prédéfinis ou à la traduction dans **ui_config** sont ajoutées au fichier json **map_console_action_bar** visible sur la page de la console de mappages.

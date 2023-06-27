---
title: Configuration de l’affichage des liens basés sur l’UUID
description: Découvrez comment configurer l’affichage des liens basés sur l’UUID
source-git-commit: 4f15166b1b250578f07e223b0260aacf402224be
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---


# Configuration de l’affichage des liens basés sur l’UUID {#id2035G20M0QN}

Par défaut, lorsque vous créez un lien à l’aide de l’option Insérer une référence ou Insérer un contenu réutilisé de l’éditeur web, le lien est créé à l’aide de l’UUID du contenu référencé. Le **Lien** La propriété \(dans le panneau Propriétés\) du contenu référencé peut être configurée pour afficher le chemin d’accès relatif au fichier du contenu référencé ou l’UUID. Par défaut, l’UUID du contenu référencé s’affiche dans le panneau Propriétés.

Suivez les instructions de la section [Remplacements de configuration](download-install-additional-config-override.md#) pour créer le fichier de configuration. Dans le fichier de configuration, fournissez les détails \(propriété\) suivants pour afficher le chemin relatif ou l’UUID du contenu référencé dans l’éditeur web :

| PID | Clé de propriété | Valeur de la propriété |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.uuid` | Booléen \(true/false\). Si vous souhaitez afficher le chemin relatif du contenu lié, définissez cette propriété sur false. <br> **Valeur par défaut**: true |

**Rubrique parente :**[ Personnalisation de l’éditeur web](conf-web-editor.md)

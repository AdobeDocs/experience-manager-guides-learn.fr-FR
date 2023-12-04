---
title: Ouvrir les fichiers de rubrique ou de mappage DITA dans le même onglet
description: Découvrez comment ouvrir une rubrique DITA ou mapper des fichiers dans le même onglet
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Ouvrir les fichiers de rubrique ou de mappage DITA dans le même onglet {#id223HI0P202H}

Dans certains workflows, lorsque vous cliquez sur un lien d’une rubrique ou d’un fichier de mappage, il s’ouvre dans un nouvel onglet. Cela peut entraîner l’ouverture de nombreux onglets dans votre navigateur, ce qui peut avoir un impact sur votre productivité. Vous pouvez modifier ce comportement en ouvrant un fichier de rubrique ou de mappage dans un nouvel onglet et le forcer à s’ouvrir dans l’onglet actif. Pour ce faire, effectuez les modifications de configuration suivantes :

1. Ouvrez la page de configuration de la console web Adobe Experience Manager .

   L&#39;URL par défaut pour accéder à la page de configuration est :

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. Recherchez et cliquez sur le bouton **com.adobe.fmdita.xmleditor.config.XmlEditorConfig** du lot.

1. Sélectionnez la variable **Ouvrir la rubrique/carte DITA dans le même onglet** .

1. Cliquez sur **Enregistrer**.


Ce paramètre a un impact sur les emplacements suivants d’où vous pouvez accéder aux fichiers de rubrique ou de mappage :

- Créez une rubrique DITA \(à la fin du processus, lorsque vous cliquez sur l’icône **Ouvrir la rubrique** button\)

- Créez une carte DITA \(à la fin du processus, lorsque vous cliquez sur la **Open Map** button\)

- Onglet Sujets dans la console de mappage DITA

- Onglet Lignes de base dans la console de mappage DITA

- Onglet Rapports dans la console de mappage DITA


**Rubrique parente :**[ Personnalisation de l’éditeur web](conf-web-editor.md)

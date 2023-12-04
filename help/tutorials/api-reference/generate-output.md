---
title: API Java pour travailler avec la génération de sortie
description: En savoir plus sur l’API Java à utiliser avec la génération de sortie
source-git-commit: 880cd344ceb65ea339be699ebcad41c0d62e168a
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# API Java pour travailler avec la génération de sortie {#id175UB30E05Z}

L’API Java suivante vous permet de générer une sortie pour une carte DITA. Cette API est disponible sous la forme d’un lot. Vous devez inclure ce lot dans votre code pour utiliser ces API.

Détails du lot :

- ID de groupe : **com.adobe.fmdita**

- ID d’artefact : **api**

- Version : **3,4**

- Package : ****com.adobe.fmdita.api.maps****

- Détails de la classe :

  ```JAVA
  public class **PublishUtils** extends Object
  ```

  La variable **`PublishUtils`** contient une méthode permettant de générer une sortie pour un ou plusieurs paramètres prédéfinis de sortie.


## Générer la sortie

La variable ``generateOutput`` génère une sortie pour un fichier de mappage DITA à l’aide des paramètres prédéfinis de sortie spécifiés.

**Syntaxe**:

```JAVA
public static void generateOutput(Session session,
String sourcePath,
String outputName)
throws GuidesApiException
```

**Paramètres**: |Nom|Type|Description| |—|—|—| |`session`|javax.jcr.Session|Une session JCR valide.| |``sourcePath``|String|Path \(dans le référentiel AEM\) du fichier de mappage DITA pour lequel la sortie doit être générée.| |``outputName``|Chaîne|Nom du paramètre prédéfini de sortie\(s\) à utiliser pour générer la sortie. Plusieurs paramètres prédéfinis de sortie peuvent être spécifiés à l’aide d’un délimiteur barre verticale \(&quot;\|&quot;\), par exemple. `aemsite\|pdfoutput`.

**Exception**: renvoie ``javax.jcr.RepositoryException``, `java.io.IOException`, et `java.lang.Exception`.

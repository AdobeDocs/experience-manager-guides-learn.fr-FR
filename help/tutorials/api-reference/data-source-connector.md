---
title: API REST pour enregistrer un connecteur de source de données
description: Découvrez l’API REST pour enregistrer un connecteur de source de données
source-git-commit: 8707acf3ba01b7488eea6597c434da73a901d037
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 3%

---


# API REST pour enregistrer un connecteur de source de données {#id236LG0Y0CXA}

L’API REST suivante vous permet d’enregistrer un connecteur de source de données.

## Enregistrement d’un connecteur de source de données

Méthode de GET qui enregistre un connecteur de source de données.

**URL de la demande**:
`http://server:port/bin/guides/v1/konnect/config/register?path=<uploaded file path>`

**Paramètre**: |Nom|Type|Obligatoire|Description| |—|—|—|— |`path`|String|Yes|Chaîne qui pointe vers un chemin d’accès dans le référentiel AEM. Il peut s’agir d’un chemin dans la variable `/content/dam or /var/dxml`.

**Exemple**:\
`http://host:4502/bin/guides/v1/konnect/config/register?path=/var/dxml/konnect/jira.json`


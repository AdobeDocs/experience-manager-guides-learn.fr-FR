---
title: Migration du contenu non UUID vers UUID
description: Découvrez comment migrer le contenu non UUID vers le contenu UID
exl-id: 093b380e-9a8b-4e60-aeaa-3458e8c257f2
source-git-commit: 21edbb2f8a49213ea95fac8a957056711219e7e4
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 2%

---

# Migration du contenu non UUID vers UUID {#id226TI0U20XA}

>[!IMPORTANT]
>
> Vous pouvez migrer votre contenu non UUID vers le serveur UUID. Pour migrer vers le serveur UUID, vous devez disposer d’un serveur non UUID sur lequel AEM guide version 4.0 doit être installé.

Effectuez les étapes suivantes pour migrer votre contenu non UUID :

>[!NOTE]
>
> Chaque étape est cruciale et l’absence de l’une d’elles peut entraîner l’échec ou la corruption des données du serveur. Assurez-vous d’effectuer toutes les étapes.

1. Assurez-vous que **Activation des lanceurs de workflow de post-traitement** in *com.adobe.fmdita.config.ConfigManager* et **Activation du post-traitement des versions** in *com.adobe.fmdita.postprocess.version.PostProcessVersionObservation* sont activées.

   ```http
   http://<server name>:<port>/system/console/configMgr/com.adobe.fmdita.config.ConfigManager
   ```

1. Installez la version UUID de la prochaine version majeure sur la version non UUID. Par exemple, si vous utilisez une version 4.0 non UUID, vous devez installer UID version 4.1.

1. Dans l’onglet Lanceur , désactivez les workflows suivants et tout autre workflow s’exécutant sur /content/dam à l’aide de lanceurs dans `http://localhost:4502/libs/cq/workflow/content/console.html`:

   - **Ressources de mise à jour de gestion des actifs numériques** workflow
   - **Écriture différée des métadonnées de gestion des actifs numériques** workflow

1. Désactiver **Activation des lanceurs de workflow de post-traitement** in *com.adobe.fmdita.config.ConfigManager* et désactiver **Activation du post-traitement des versions** in *com.adobe.fmdita.postprocess.version.PostProcessVersionObservation*.

   ```http
   http://<server name>:<port>/system/console/configMgr/com.adobe.fmdita.config.ConfigManager
   ```

1. Ajouter un journal distinct pour `com.adobe.fmdita.uuid.upgrade.UuidUpgrade.`

   La réponse du navigateur est également disponible à l’adresse /content/uuid-upgrade/logs.

1. Exécutez la requête donnée sur un dossier contenant des données plus petites avec `doReviews=false` avant de l’exécuter sur / content/dam : `http://localhost:4502/bin/dxml/uuid_upgrade?root=/content/dam/test&doReviews=false`

   >[!TIP]
   >
   >  Vous pouvez vérifier si tous les fichiers du dossier sont correctement mis à niveau et que toutes les fonctionnalités ne fonctionnent que pour ce dossier.

**Paramètres de la requête :**

    - `root` : Dossier racine où la mise à niveau doit avoir lieu \(utilisez /content/dam pour tous les référentiels.\)
    - &quot;doReviews&quot; : true/false \(Si les révisions doivent être mises à niveau ou non. La valeur par défaut est false.\)
    - doBaselines : true/false \(Si les lignes de base doivent être mises à niveau ou non. La valeur par défaut est true.\)
    - `processLevel` : -1\(échec sans restauration\), 0\(échec avec restauration\), 1\(échec avec erreurs\), 2\(mise à niveau réussie\) \(lors d’une nouvelle tentative de script après échec, seuls les fichiers avec &quot;fmUpgradeStatus&quot; &lt;= processLevel seront traités à nouveau, sinon ils seront ignorés. La valeur par défaut est 1.\)
    - `ignoreImageVersions` : true/false \(ignore le traitement des versions d’image. La valeur par défaut est false.\)
    
    >[!REMARQUE]
    >
    > Nous pouvons exécuter la migration du contenu au niveau du dossier ou de l’ensemble du contenu/dam ou sur le même dossier \(réexécuter la migration\).

1. Une fois la migration du serveur terminée, les workflows et le post-traitement suivants pourront continuer à fonctionner sur le serveur :

   - **Ressources de mise à jour de gestion des actifs numériques** workflow
   - **Métadonnées DAM** workflow

>[!NOTE]
>
> Si certains fichiers ne sont pas traités ou sont corrompus avant la migration, ils restent corrompus même après la migration.

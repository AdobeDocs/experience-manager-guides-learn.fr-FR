---
title: FMPS et guides d’AEM
description: Publication avec FMPS à l’aide des AEM Guides
source-git-commit: 82f010a97d0ed0e3c6351e6411e5955c79e0b01f
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---


# FrameMaker Publishing Server (FMPS) et AEM Guides

**L’intégration d’AEM Guides à FrameMaker Publishing Server peut être votre solution si vous recherchez une publication automatisée de haute qualité.\
L’article suivant vous aidera à configurer et à exécuter FMPS avec AEM Guides.**

## Compatibilité de FMPS avec AEM Guides :

- Compatibilité avec les AEM Guides 4.1 : [Lien](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/release-notes/on-prem-release-notes/release-notes-4.1.html?lang=en/#compatibility-matrix)
- Compatibilité avec les AEM Guides 4.0 : [Lien](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-4-0.html/#Compatibility%20matrix)
- Version future : [Lien](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/latest-release-info.html?lang=en)

## Installation:

### AEM Guides :

Installation et configuration : [Lien](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf)

### FMPS :

Pour l’installation FMPS, reportez-vous aux [Lien de la vidéo](https://www.youtube.com/watch?v=2deelyM5VA8&amp;t) ou [Documentation](https://help.adobe.com/en_US/framemaker/server/index.html#t=fmps-user-guide%2Finstall_config_fmps.html%23install_config_fmps&amp;rhtocid=_2)

## Configurations requises :

Votre contenu DITA peut être généré à l’aide de FrameMaker Publishing Server (FMPS). Vous pouvez créer une sortie dans n’importe lequel des nombreux formats pris en charge par FMPS. Dans la console web, modifiez les propriétés suivantes du lot com.adobe.fmdita.config.ConfigManager pour configurer AEM Guides d’utilisation de FMPS.

Pour ouvrir la console web, accédez à l’URL http://\&lt;server name=&quot;&quot;>:\&lt;port>/system/console/configMgr

**Propriétés de configuration et leur description :** [Lien](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf#page=89)

## Exécution du test :

Avec FMPS, vous pouvez publier automatiquement **PDF, HTML réactif5**, et **Epub** pour vos ressources DITA et FM.

Dans le menu &quot;Générer le PDF à l’aide de&quot;, sélectionnez FrameMaker Publishing Server.

L’utilisateur peut fournir &quot;settings File(.sts)&quot; et &quot;ditaval&quot;. Le filtrage sera effectué à l’aide de ditaval en fonction des conditions que vous fournissez.

- **définition du fichier**: Paramètre de publication FrameMaker/FMPS qui contient tous les paramètres que vous souhaitez que FMPS respecte lors de la publication. Par exemple : Générer une sortie avec le modèle personnalisé, Générer des marques et des fonds (PDF), Générer un PDF avec la table des matières, l’index, etc.
- **Paramètre prédéfini FMPS :** Combinaison prédéfinie de fichier ditaval et settings. Au lieu de fournir des fichiers distincts ditaval et settings, l’utilisateur peut précréer un paramètre prédéfini FMPS qui peut être réutilisé pour les besoins de publication.

**Remarque :** Si vous ne sélectionnez aucun des paramètres ou paramètre prédéfini FMPS, FMPS publiera avec le paramètre système par défaut.

Si vous avez sélectionné le paramètre prédéfini FMPS et fourni également le fichier settings/ditaval à partir d’AEM, cela va entrer en conflit et le paramètre prédéfini FMPS sera prioritaire sur le fichier de paramètres/ditaval personnalisé.

### Publication de base à l’aide de FMPS :

Vous pouvez publier vos lignes de base déjà créées avec FMPS2020.0.2 ou une version ultérieure.

**Exemple de fichier de paramètres FMPS (fichier .sts) pour commencer :** [Lien](https://acrobat.adobe.com/link/track?uri=urn:aaid:scds:US:ef750752-7a7e-4e51-923e-6b7d9861ed54) (décompressez ce fichier)

## FAQ et dépannage :

- La publication FMPS échoue avec &quot;Timeout Exception&quot;.

Vérifiez et augmentez la valeur du &quot;délai d’expiration FMPS&quot; (secondes) dans /system/console/configMgr/com.adobe.fmdita.config.ConfigManager&quot;.

- Impossible d’obtenir le paramètre prédéfini FMPS dans la liste déroulante.

Assurez-vous qu’un paramètre prédéfini FMPS prédéfini est créé sur le serveur et que vos paramètres de connexion sont corrects.

- Je reçois des PDF vierges lors de la publication.

Si vous utilisez l’UUID, assurez-vous d’avoir coché &quot;Utiliser le référencement basé sur l’UUID&quot; dans les préférences de modification de FrameMaker et vice versa pour les guides d’AEM non UUID.

- Mes paramètres/ditaval ne sont pas appliqués dans la sortie finale publiée.

Veillez à ne pas sélectionner à la fois le fichier de configuration/ditaval et le paramètre prédéfini FMPS de manière équivalente. Vérifiez manuellement la sortie à l’aide de FrameMaker.

- La ligne de base n’est pas publiée à partir de FMPS.

La publication de ligne de base est compatible avec la version FMPS2020.0.2 ou ultérieure.\
Assurez-vous que votre ligne de base est correctement créée, pour vérifier, accédez à la carte de téléchargement de rubrique du tableau de bord de carte et sélectionnez &quot;Utiliser la ligne de base&quot;.

- La publication des tâches à partir de FMPS prend plus de temps que les autres moteurs.

Il y aura un en-tête fixe idéal d’environ. 3 à 4 minutes seulement lors de la publication depuis FMPS que d’autres moteurs, si vous pensez que c’est plus que cela, contactez votre administrateur FMPS ou contactez l’assistance Adobe.

## Autres ressources:

[Formation et assistance pour FMPS](https://helpx.adobe.com/support/framemaker-publishing-server.html)

[Formation et assistance AEM](https://helpx.adobe.com/in/support/xml-documentation-for-experience-manager.html)

[FrameMaker et communauté FMPS](https://community.adobe.com/t5/framemaker/ct-p/ct-framemaker?page=1&amp;sort=latest_replies&amp;lang=all&amp;tabid=all)

[Communauté AEM Guides](https://experienceleaguecommunities.adobe.com/t5/experience-manager-guides/ct-p/aem-xml-documentation)

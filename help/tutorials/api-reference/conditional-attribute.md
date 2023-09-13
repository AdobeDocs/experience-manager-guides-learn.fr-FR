---
title: API REST pour travailler avec des attributs conditionnels
description: En savoir plus sur l’API REST pour utiliser les attributs conditionnels
source-git-commit: fad5049962f258bbe59c7d172436d82b3d6cd68f
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---


# API REST pour travailler avec des attributs conditionnels {#id175UB30E05Z}

L’API REST suivante vous permet d’ajouter des attributs conditionnels dans un profil de dossier.

## Ajout d’un attribut conditionnel dans un profil au niveau du dossier

Méthode de POST qui ajoute des attributs conditionnels à un profil donné au niveau du dossier.

**URL de la demande**:\
http://*&lt;aem-guides-server>*: *&lt;port-number>*/bin/fmdita/folder profiles

**Paramètres**:\
|Nom|Type|Obligatoire|Description| |—|—|—|— |`:operation`|String|Yes|Nom de l’opération en cours d’appel. La valeur de ce paramètre est ``ADDATTRIBUTEPROFILES``. <br> **Remarque :** La valeur n’est pas sensible à la casse.| |`profilename`|String|Yes|Nom d’affichage du profil au niveau du dossier dans lequel les attributs conditionnels doivent être ajoutés.| |`conditionalprofiles`|Tableau JSON|Oui|Un tableau JSON constitué du nom et des valeurs de l’attribut conditionnel. L’exemple de fragment de code suivant affiche le tableau JSON avec deux attributs - `platform` et `product` avec plusieurs valeurs qui leur sont affectées.|

```JSON
[  {    name: "platform",    
        values: [       
                {value: "win", label: "Windows"},       
                {value: "mac", label: "Mac OS"}    
                ]},
                {    
                    name: "product",    
                    values: [      
                        {value: "aem_1", label: "AEM 6.1"},     
                        {value: "aem_4,  label: "AEM 6.4"}  
                        ]  
                }]
```

**Valeurs de réponse**:\
Renvoie une réponse HTTP 200 \(Succès\).

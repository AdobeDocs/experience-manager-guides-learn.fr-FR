---
title: Guides de publication Benchmarks sur AEMaaCS
description: Découvrez les limites du système relatives à la publication sur AEM Cloud.
source-git-commit: e64430bb968b18090c3981cc2d21ebe6593ba933
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 7%

---


# AEM Guides de publication Benchmarks sur AEMaaCS

Actuellement, le service cloud de Guides AEM certaines limites sur les tailles des cartes de publication que l’équipe de Guides s’efforce activement de résoudre.

L’équipe de guides a déjà introduit une variable évolutive [Publication de microservice](publish-microservice-architecture-and-performance.md) pour prendre en charge les cartes volumineuses et la publication simultanée multiple. Pour l’instant, ce microservice prend en charge un sous-ensemble de types de sortie et la prise en charge d’autres types est en cours de développement principal.

Pour configurer le nouveau service de publication pour tout environnement cloud AEM, reportez-vous à la section [Configuration de la nouvelle publication basée sur un microservice](configure-microservices.md)

## Environnement d’exécution

    Version d’AEM : 2023.5.11983.20230511T173830Z
    Guide Add On Release : 2023.6.0
    Modèle de site AEM : Modèle d’AEM Guides prêts à l’emploi
    Version DITA-OT : 3.5.4
    Type de processus de publication : Fractionner le processus de publication
    Sortie prise en charge par microservice : PDF, PDF natif (Dita-OT)

## Numéros de génération de sortie

| Type de sortie | Taille de la carte (références de rubrique) | Délai d’exécution (en secondes) | Publication de microservice |
|---------------|------------------------------|----------------------------|-----------------------|
| AEM site | 3500 | 5220 | Non |
| PDF natif | 3500 | 780 | Oui |
| PDF (DITA-OT) | 11000 | 960 | Oui |
| HTML 5 | 3500 | 240 | Non |
| Personnalisé | 300 | 300 | Non |

## Points clés à retenir

- AEM Site crée de nombreux noeuds cq:Page et aplatisse en les rendant unitairement au cours de la génération. C’est pourquoi il est conseillé d’éviter d’exécuter plusieurs publications simultanées AEM site, car cela peut surcharger le système.
- AEM temps de génération du site dépend du modèle utilisé. Le temps d’exécution peut augmenter en cas d’utilisation d’un modèle complexe.
- Le temps d’exécution de publication personnalisé correspond à un exemple de sortie personnalisée. Le temps de publication personnalisé dépend uniquement de la logique de transformation du client.

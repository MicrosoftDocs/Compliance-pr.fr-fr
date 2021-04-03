---
title: Surveillance et auto-ressource des données dans Microsoft 365
description: Dans cet article, vous allez découvrir les fonctionnalités de surveillance et de auto-ressource de Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: baf73746fff5e4866c36975e082c84017e0b3083
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496940"
---
# <a name="data-monitoring-and-self-healing-in-microsoft-365"></a>Surveillance et auto-ressource des données dans Microsoft 365

Étant donné l’échelle de Microsoft 365, il serait impossible de maintenir la résilience des données client et la sécurité contre les programmes malveillants sans une surveillance intégrée complète, des alertes intelligentes et autorésilientes rapides et fiables. La surveillance d’un ensemble de services à l’échelle de Microsoft 365 est très difficile. De nouveaux esprit et méthodologies doivent être introduits, et de nouveaux ensembles de technologies doivent être créés pour exploiter et gérer le service dans un environnement global connecté. Nous avons quitté l’approche de surveillance traditionnelle de la collecte et du filtrage des données pour créer des alertes à une approche basée sur l’analyse des données . en prenant des signaux et en faisant confiance à ces données, puis en utilisant l’automatisation pour récupérer ou résoudre le problème. Cette approche permet de sortir les humains de l’équation de récupération, ce qui rend les opérations moins coûteuses, plus rapides et moins sujettes aux erreurs. 

La surveillance Microsoft 365 repose sur un ensemble de technologies qui composent notre moteur d’informations sur les données, qui repose sur azure, SQL Azure et la technologie de base de données de diffusion en continu [open source.](https://cassandra.apache.org/) Il est conçu pour collecter et agréger des données et parvenir à des conclusions. Actuellement, il traite plus de 500 millions d’événements par heure à partir de plus de 100 000 serveurs (environ 15 To par jour) répartis sur des dizaines de centres de données dans de nombreuses régions, et ces nombres augmentent. 

Microsoft 365 utilise *la* surveillance externe, qui implique la création de transactions synthétiques pour tester tout ce qui est important. Par exemple, dans Exchange Online, chaque scénario teste toutes les bases de données dans le monde entier toutes les cinq minutes de manière à assurer une couverture quasi continue de tout ce qui se trouve dans le système. À partir de plusieurs emplacements, 250 millions de transactions de test par jour sont effectuées pour créer une planification ou une pulsation robuste pour le service. 

Microsoft 365 utilise également le concept d’alerte *rouge,* qui réduit tous les signaux de surveillance de tous les ordinateurs de nos centres de données à un objet gérable par un être humain. Le concept est assez simple : si un événement se produit entre plusieurs signaux, il doit se produire quelque chose. Il ne s’agit pas de renforcer la confiance en un signal, mais d’avoir une fidélité raisonnable pour chaque signal afin d’obtenir une plus grande précision. Ce système de surveillance est si puissant que nous n’avons pas de personnel 24 heures sur 24 et 7 jours sur 7 qui surveille nos moniteurs . Tout ce que nous avons, c’est l’effet qui s’en vient s’il détecte un problème, auquel cas il va pagner le personnel d’appel approprié, ou plus souvent comme c’est le cas, il va continuer et résoudre le problème. Une fois que nous avons commencé à collecter des signaux et à créer des alertes rouges, nous pouvons commencer à tguler dans toutes nos partitions de service. 

En fonction de la combinaison de l’alerte d’échec et des alertes rouges, cette alerte indique exactement quels composants peuvent être problématiques et que le système va tenter de résoudre le problème par lui-même en redémarrage d’un serveur de boîtes aux lettres. 

En plus des fonctionnalités de auto-rétablissement telles que la restauration d’une seule page, Exchange Online inclut plusieurs fonctionnalités qui prennent une approche de surveillance et de auto-rétablissement, qui se concentre sur la conservation de l’expérience de l’utilisateur final. Ces fonctionnalités incluent *la* disponibilité gérée, qui fournit des actions intégrées de surveillance et de récupération, et AutoReseed, qui restaure automatiquement la redondance des bases de données après une défaillance de disque. 

## <a name="managed-availability"></a>Disponibilité gérée 

La disponibilité gérée fournit une solution native de vérification et de récupération d’état qui surveille et protège l’expérience de l’utilisateur final par le biais d’actions orientées récupération. La disponibilité gérée est l’intégration des actions intégrées de surveillance et de récupération avec la plateforme de haute disponibilité Exchange. Elle est conçue pour détecter des problèmes et procéder à une récupération dès qu'ils apparaissent ou sont découverts par le système. À la différence des techniques et solutions externes de surveillance précédentes pour Exchange, la disponibilité gérée ne tente pas d'identifier ni de communiquer la cause première d'un incident. Au lieu de cela, il se concentre sur les aspects de récupération qui abordent trois domaines clés de l’expérience de l’utilisateur final :

- **Disponibilité** : les utilisateurs peuvent-ils accéder au service ? 
- **Latence :** quelle est l’expérience pour les utilisateurs ? 
- **Erreurs** : les utilisateurs sont-ils en mesure d’accomplir ce qu’ils veulent ? 

La disponibilité gérée est une fonctionnalité interne qui s’exécute sur chaque serveur Microsoft 365 exécutant Exchange Online. Elle interroge et analyse des centaines de paramètres d'intégrité par seconde. Si un problème est trouvé, il est résolu automatiquement la plupart du temps. Toutefois, il y aura toujours des problèmes que la disponibilité gérée ne sera pas en mesure de résoudre elle-même. Dans ce cas, la disponibilité gérée fait resserre le problème à une équipe de support Microsoft 365 au moyen de la journalisation des événements.

## <a name="autoreseed"></a>AutoReseed

Les serveurs Exchange Online sont déployés dans une configuration qui stocke plusieurs bases de données et leurs flux de journaux sur le même disque non RAID. Cette configuration est souvent appelée simplement une bande de *disques* (JBOD), car aucun mécanisme de redondance du stockage, tel que RAID, n’est utilisé pour dupliquer les données sur le disque. Lorsqu’un disque tombe en panne dans un environnement JBOD, les données de ce disque sont perdues. 

Étant donné la taille d’Exchange Online et le fait qu’il soit déployé à l’intérieur de millions de lecteurs de disque, les défaillances de disque sont une occurrence régulière dans Exchange Online. En fait, plus de 100 échouent chaque jour. En cas de panne d’un disque dans un déploiement d’entreprise local, un administrateur doit remplacer manuellement le disque défectueux et restaurer les données affectées. Dans un déploiement cloud de la taille de Microsoft 365, le fait d’avoir des opérateurs (administrateurs cloud) remplaçant manuellement les disques n’est ni pratique ni économiquement réalisable. 

Le réassage automatique, ou *AutoReseed,* est une fonctionnalité qui remplace ce qui est normalement une action pilotée par l’opérateur en réponse à une défaillance de disque, à un événement de corruption de base de données ou à tout autre problème nécessitant le réaxage d’une copie de base de données. La fonctionnalité AutoReseed permet de restaurer automatiquement la redondance de base de données après une défaillance de disque par le biais de disques de rechange qui ont été configurés sur le système. En cas de panne d’un disque, les copies de base de données stockées sur ce disque sont automatiquement réassées sur un disque de rechange préconfiguré sur le serveur, ce qui rétablit la redondance. 
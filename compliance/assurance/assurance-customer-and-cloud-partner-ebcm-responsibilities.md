---
title: Responsabilités des partenaires d’entreprise client et cloud en terme de continuité de l’activité
description: Comprendre ce que fait Microsoft au cours d’un incident de service pour vous permettre de mieux préparer les plans de continuité de votre activité.
author: chrfox
ms.author: chrfox
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: efcbc57f2b22c185f023fc49c928fbab86f1f02e
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507077"
---
# <a name="enterprise-business-continuity-management-customer-and-cloud-partner-responsibilities"></a>Gestion de la continuité des activités de l’entreprise et responsabilités des partenaires client et cloud

Donner l’accès aux services cloud de Microsoft 365 à vos utilisateurs donne lieu à un partenariat entre votre organisation et Microsoft. Microsoft fournit les services. Vous êtes responsable de la connexion des points de terminaison clients, de la gestion des identités et des accès et de la façon dont ces services sont utilisés. Certaines responsabilités sont partagées, telles que les infrastructures d’identité et d’annuaire. Cet article décrit certains des éléments critiques que vous devez garder à l’esprit pour assurer le fonctionnement de votre entreprise en cas d’incident de service, et vous éclaire sur les actions que Microsoft prendra dans ce cas.

## <a name="transparency-during-service-incidents"></a>Transparence pendant les incidents de service

En tant que partenaire approuvé, Microsoft développe des services cloud hautement résilients et suit des procédures structurées pour résoudre les incidents de service lorsqu’ils se produisent. Quand un incident de service se produit, Microsoft tient compte du fait que des communications **précises**, **ciblées** et **disponibles rapidement** sont critiques pour les clients.

## <a name="timely"></a>Précision

Microsoft informe les administrateurs Microsoft 365 en mettant à jour le tableau de bord Intégrité des services propre au client sur le portail d'administration Microsoft 365. Les mises à jour des incidents de service sont normalement effectuées toutes les heures. Si un intervalle de temps différent est nécessaire, vous serez informé de la modification dans les publications du tableau de bord.

## <a name="targeted"></a>Ciblage

Dans la plupart des cas, lorsque nos systèmes de surveillance détectent un problème, nous pouvons identifier la base de clients affectée, que ce soit un seul client, toute la région ou au-delà, et adresser les communications nécessaires à ces clients. Cela vous permet d’obtenir uniquement les informations pour votre entreprise et de ne pas être distrait par des notifications sonores qui ne vous concernent pas. Par exemple, si une base de données de boîtes aux lettres spécifique est impactée, nous sommes en mesure d’identifier précisément les clients qui ont des utilisateurs sur l’infrastructure affectée et de diriger nos communications vers ceux-ci. Si l’étendue de l’impact de l’incident est peu claire, nous diffusons nos communications au groupe le plus large de clients éventuellement impactés.

## <a name="highly-available"></a>Hautement disponible

Microsoft propose aux utilisateurs plusieurs canaux pour les communications sur l’état du service.

- En cas d’indisponibilité du centre d’administration ou du tableau de bord Intégrité des services dans le centre d’administration, vous pouvez surveiller l’état du service sur notre [site de sauvegarde](https://status.office365.com/).
- Nous conservons un compte Twitter [@MSFT365Status](https://twitter.com/msft365status?lang=en) où nous répondons aux rapports d’impact et publions les mises à jour sur les événements concernant le tableau de bord.
- L’application administrateur pour les administrateurs de client Microsoft 365 vous permet de vous connecter à l’état du service Microsoft 365 de votre organisation lorsque vous êtes en déplacement. Les administrateurs clients peuvent consulter les informations de l'état du service et les mises à jour de l'état de maintenance depuis leurs appareils mobiles. Pour plus d’informations, consultez le [FAQ sur l’application d’administration](https://docs.microsoft.com/office365/admin/admin-overview/admin-mobile-app).
- L'[API Microsoft 365 sur les communications du service](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/service-health-and-continuity#office-365-service-communications-api) vous permet d’accéder aux communications du service afin de faciliter la surveillance de votre environnement. Vous pouvez vous connecter à l’API, recevoir des données sur l’état du service en temps réel et publier les informations sur un tableau de bord interne afin d’informer les utilisateurs d’entreprise des incidents. La diffusion des informations en interne permet de réduire le trafic de votre support technique pendant une interruption.
- Pour les incidents plus graves, Microsoft publie des rapports post-incidents (PIR) sur le tableau de bord Intégrité des services dans le centre d’administration. Les PIR contiennent des informations clés relatives à l’incident afin de vous aider à comprendre la nature de la panne. On y trouve les sections suivantes :
    - impact sur les utilisateurs
    - étendue de l’impact
    - date et heure de début et de fin de l’incident
    - cause initiale
    - actions prises
    - étapes suivantes
- Des communications complémentaires sont disponibles dans le centre de messagerie Microsoft 365, comme les notifications de modifications à venir, les nouvelles fonctionnalités ou la maintenance planifiée.
- Pour plus d’informations, voir le [guide sur l’État des services](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/service-health-and-continuity) pour en savoir plus sur les différents canaux de communication et la surveillance de l’état du service.

Le fait de donner l’accès aux services en ligne de Microsoft 365 représente un partenariat entre votre organisation et Microsoft. Le tableau suivant résume l’équilibre des responsabilités entre Microsoft et le client lors d’un incident de service et pendant l’exploitation normale.

![équilibre des responsabilités entre Microsoft et le client](../media/responsibilities.png)

## <a name="your-environment---service-continuity"></a>Votre environnement – continuité de service

Lorsque vous élaborez votre plan de continuité, pensez aux événements susceptibles d’avoir un impact sur votre organisation et sur sa capacité à communiquer. À un niveau élevé, trois facteurs peuvent avoir un impact sur votre activité.

### <a name="people"></a>Les personnes

Pensez aux événements qui pourraient avoir un impact sur votre personnel, comme une catastrophe naturelle ou une épidémie. Ils sont souvent négligés, en raison de la nature peu probable d’un impact à grande échelle si votre personnel est largement réparti. Cependant, si un pourcentage important de votre personnel se retrouve hors connexion, votre entreprise peut-elle continuer à fonctionner ? Comment atténuer ce problème ?

### <a name="location"></a>L’emplacement

De nombreuses organisations imposent aux employés de se trouver dans des emplacements physiques ou réseau spécifiques pour se connecter aux systèmes d’entreprise et aux services cloud.  
Microsoft publie des [principes de connectivité réseau](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-network-connectivity-principles) qui guident les entreprises avec des recommandations pour la configuration de la connectivité réseau aux ressources cloud. Les exemples d’optimisation incluent l’implémentation d’un VPN en tunnellisation partagée pour autoriser les connexions directement à partir du réseau d’un utilisateur plutôt que d’un tunnel VPN.  Bien que ces principes de connectivité soient importants pour maintenir les connexions à faible latence, la résilience de service nécessite d’autres méthodes de connexion aux ressources d’entreprise pour une collaboration générale.

### <a name="systems"></a>Les systèmes

De nombreuses solutions de collaboration dépendent des systèmes, tels que le réseau étendu (WAN) de l’entreprise. Lorsque ces systèmes ne sont pas disponibles, comment votre organisation peut-elle répondre ?
Ce graphique représente des problèmes qui peuvent avoir une incidence sur plusieurs zones. Le tableau joint fournit des exemples à prendre en considération.

![Diagramme de Venn de systèmes](../media/venn-diagram.png)

Vos plans de continuité doivent prendre en compte chacune de ces zones. Par exemple, si vous voulez que les utilisateurs soient sur le réseau d’entreprise et qu’il y a une tempête de neige, comment ces utilisateurs peuvent-ils accéder aux ressources clés ? Si la neige empêche de venir au bureau et que les ingénieurs de service doivent se connecter au réseau d’entreprise, existe-t-il un programme prévoyant que leurs ordinateurs portables d’entreprise soient disponibles chez eux ?

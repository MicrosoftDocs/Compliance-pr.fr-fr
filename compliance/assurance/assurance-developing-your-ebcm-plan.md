---
title: Considérations relatives à votre plan de gestion de la continuité d’activité de l’entreprise
description: Éléments à prendre en compte lors du développement de votre plan de continuité d’activité de l’entreprise dans le Cloud.
author: robmazz
ms.author: robmazz
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e8c031727c77d1106f8bd255a643fd9794cc856a
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497585"
---
# <a name="developing-your-business-continuity-plan"></a>Développement de votre plan de continuité d’activité

Cette rubrique fournit des conseils sur le développement d’un plan de continuité d’activité qui prend en compte les dépendances de Microsoft 365. Nous vous recommandons ici d’utiliser des méthodes pour analyser vos fonctions et identifier celles qui dépendent des services Microsoft 365. Vous effectuerez cette analyse en vous attendant à ce qu’il y ait des défaillances de service et à ce que vous deviez vous préparer à ces éventualités.

De manière générale, la planification de la continuité d’activité de l’entreprise comporte quatre aspects : l’évaluation, la planification, la validation des capacités, ainsi que la communication et la coordination.

## <a name="assessment"></a>Évaluation
Tout d’abord, vous devez identifier les fonctions dans votre organisation, ainsi que les services et processus qui les prennent en charge. Cela comprend la réalisation d’une analyse de l’impact sur l’entreprise, où chaque fonction de l’entreprise est classée en fonction de son degré d’importance et où vous identifiez les processus et les services dont dépend chacun d’eux. Voici un exemple de tableau que vous pouvez consulter pour vous aider à commencer votre propre évaluation.

**Exemple d’évaluation d’impact commercial (BIA)**

Il s’agit d’un document BIA pour `name of the service, system, process, or function`

|Champs BIA|Description|
|---------|---------|
|Type de BIA|`is it a business process or technology, service or system?`|
|Nom du BIA|`name of the service/system/function/process`|
|description de service|`give a full description of the service, process, or function`|
|fonction de l’entreprise|`some examples: customer services; legal; marketing; risk management, security, sales, information technology, production, manufacturing`|
|exercice fiscal|`the current fiscal year, re-evaluate these on a regular basis`|
|criticité|`develop your own classifications, but here are some examples: mission critical, important, deferrable`|
|unité commerciale|`name of the business unit that owns this business function`|
|processus (service, fonctionnalité)|`the name of the process, service, or feature`|
|responsable principal de groupe professionnel|`the name and contact information of the senior leader of the business group that owns this business process`|
|La technologie dispose-t-elle d’un contrat SLA ou OLA interne établi ?|`please explain in as much detail as possible`|
|La technologie dispose-t-elle d’un contrat SLA ou OLA **externe** établi ?|`please explain in as much detail as possible`|
|La technologie dispose-t-elle d’un mandat connu responsable de l’adoption d’un contrat SLA spécifique ? Si oui, expliquez en détail.|`details here`|
|La perte ou la compromission des données associées à ce service déclenchera-t-elle un événement majeur ? Si oui, expliquez en détail.|`details here`|
|Le service dispose-t-il d’une solution de contournement ou d’une alternative pour certaines ou l’ensemble de ses fonctions et fonctionnalités clés ? Si oui, expliquez en détail.|`details here`|
|Est-ce que le service traite, stocke ou transmet les données client, telles que les informations d’identification personnelle (PII) ? Si oui, expliquez en détail.|`details here`|
|état BIA|`develop your own status classification, here are some examples: planned, started, in-progress, complete, on-hold, expired`|
|date de finalisation|`the date this BIA was completed`|
|facilitateur BIA|`name of the person or group who is responsible for developing and maintaining this BIA`|
|approbation BIA|`name of the person or group who is the executive sponsor of this BIA and who has responsibility for approving it.`|
|contributeurs|`optional list of the people who helped develop this BIA and their contact information`|
|emplacement d’approbation BIA|`indicate where the executive approval is located, or attach proof to this document`|

## <a name="planning"></a>Planification

Ensuite, vous examinez les processus d’entreprise pour voir s’il existe des relations de dépendance en cascade. En fonction des résultats, vous définissez les priorités et élaborez les stratégies de résilience, ainsi que les procédures d’exploitation standard prenant en charge vos stratégies.

Vous pouvez utiliser [Microsoft Service Map](/azure/azure-monitor/insights/service-map) pour vous aider à effectuer ce mappage. Microsoft Service Map découvre automatiquement les composants d’application sur les systèmes Windows et Linux et mappe toutes les dépendances TCP, identifie les connexions et les systèmes tiers distants dont dépend l’application. Il mappe également les dépendances aux zones de votre réseau qui sont traditionnellement sombres comme Active Directory.

Voici un exemple d’analyse de dépendances (DA) à partir duquel vous pouvez commencer. Dans votre analyse de dépendances (DA), vous identifierez et examinerez les dépendances de processus. Veillez à inclure des personnes, des fournisseurs, des clients, des partenariats et des installations. Les données de cette analyse seront utilisées pour identifier les écarts entre les exigences de récupération d’un processus et les fonctionnalités de récupération des dépendances.


|champ|description|
|---------|---------|
|type de processus|         |
|facilitateur|         |
|réalisé par|         |
|date de réalisation|         |
|contributeurs|         |
  
## <a name="capability-validation"></a>Validation de la fonctionnalité

Une fois que vous avez répertorié vos processus d’entreprise et établi des relations avec d’autres processus et technologies, vous devez élaborer des scénarios de validation pour tous les processus. Pour résumer, vous devez déterminer comment vous devez valider vos plans de continuité des processus d’entreprise. Vous constaterez probablement que certains sont plus importants que d’autres et vous voudrez établir des priorités.
N’oubliez pas que la formation régulière des employés sur les mesures d’intervention en cas d’incident et sur les mesures de continuité est importante une fois que le plan est établi. Les révisions post-incidents devraient être effectuées pour améliorer vos stratégies de résilience en incorporant ce que vous avez appris de chaque validation ou test.

![visio de validation de la fonctionnalité](../media/capability-validation-visio.png)

## <a name="incident-coordination-and-communication"></a>Coordination et communication des incidents

Au cours d’un incident de service, les canaux de communication normaux peuvent être affectés ou détériorés. Vous devez donc trouver d’autres solutions pour aider votre organisation à rester connectée pendant un incident. Il est essentiel que les canaux de communication soient établis, vérifiés pour assurer la sécurité et la conformité, et que les utilisateurs reçoivent une formation sur leur utilisation avant une interruption. Lors d’une défaillance, il est préférable de passer d’un état connu à un autre état connu plutôt que de trouver des solutions ad hoc et inconnues au milieu d’une crise.

Chez Microsoft, chaque équipe de service a mis en place d’autres canaux de communication internes pour nous aider à coordonner les cas où nos canaux de communication normaux ne sont pas disponibles. Celles-ci incluent des solutions de téléphonie et d’audioconférence de secours, des groupes Yammer, des groupes d’équipes, des tableaux de bord internes Intégrité des services et des logiciels internes de gestion des incidents.

Au cours de l’analyse de l’impact et de l’analyse de dépendances de votre entreprise, vous devez mapper les processus critiques et les technologies ou services dont ils dépendent. Portez une attention particulière à la communication pendant cette phase de planification et pensez à des alternatives. En voici quelques exemples.

- Si la messagerie électronique constitue votre méthode principale pour informer vos utilisateurs et parties prenantes, et que votre service de messagerie est détérioré ou indisponible, vous pouvez utiliser un autre service tel que Microsoft Teams, Yammer ou un autre service tiers comme solution de secours. L’essentiel est de les établir à l’avance et de former vos utilisateurs pour qu’ils sachent comment procéder. Un Yammer thread n’est pas utile si personne ne sait qu’il existe ou si personne ne l’a mis en signet.  
- Si vos processus de gestion des incidents internes s’appuient sur des communications vocales pour coordonner vos réponses, établissez une solution de téléphonie alternative à utiliser en cas d’urgence. Cette solution n’a pas besoin d’avoir une parité totale avec votre service principal, mais elle doit fournir le niveau minimal de collaboration pour coordonner vos équipes de continuité d’activité et de gestion des incidents. De plus, demander aux utilisateurs de publier leurs numéros de téléphone mobile dans votre liste d’adresses globale peut fournir une couche supplémentaire de communication de secours dans des cas extrêmes.
- Vous souhaiterez peut-être créer un tableau de bord Intégrité des services personnalisé, ou un autre site, qui peut fournir des mises à jour d’état pendant un incident. En apprenant aux utilisateurs à savoir où chercher des informations à l’avance, vous réduirez le nombre d’appels inutiles au support technique et vous rassurerez vos utilisateurs sur le fait que la situation est traitée rapidement et efficacement. Utilisez l’API O365 Service Communications pour lier ces informations à Microsoft 365 pour un niveau de visibilité encore plus élevé.  
- Il est essentiel que l’emplacement de vos plans de continuité d’activité et procédures d’exploitation standard soit bien connu. Nous vous recommandons de conserver des copies en ligne et hors connexion de la documentation critique, par exemple avec SharePoint Online ou OneDrive Entreprise configurés pour la synchronisation automatique avec les appareils locaux. Pour les centres d’opérations de service/réseau et d’autres équipes similaires qui seront essentielles pour la récupération, vous pouvez également conserver les copies papier disponibles pour être utilisées en cas d’urgence.

## <a name="know-your-external-points-of-integration"></a>Identifier vos points d’intégration externes

Quel que soit le modèle d’entreprise, chaque entreprise a des points d’intégration avec ses clients, ses partenaires et ses fournisseurs. La chaîne d’approvisionnement de la valeur commerciale est basée sur l’intégration avec des entités externes. L’amélioration de la continuité des opérations en cas de perturbation du service nécessite une prise en compte (et une protection) de chaque point d’intégration.  
Au fur et à mesure que vous analysez votre chaîne d’approvisionnement, les communications externes doivent être considérées de la même manière que les communications internes sont analysées. Vos clients comptent-ils sur vos serveurs Exchange Online comme seul moyen de vous contacter ? Avez-vous sensibilisé vos fournisseurs et mis en place avec eux d’autres méthodes de communication en cas d’impact sur le temps de disponibilité ? Voici un exemple de tableau qui suggère comment organiser votre raisonnement.

|nom de l’entité externe|scénario d’incident ayant une incidence|services Microsoft 365 intégrés|alternatives|
|---------|---------|---------|---------|
|`vendor name`|flux de messagerie|Exchange Online est le seul moyen de communication avec Contoso|mettre en place des canaux Microsoft Teams externes ou un logiciel de collaboration tiers          |
|`service supplier name`|conversation|Microsoft Teams|messagerie instantanée tierce|
|`partner name`|voix|Microsoft Teams|PSTN mobile ou public      |
|`supplier name`|partage de fichiers|sites SharePoint et OneDrive partagés en externe|partage de fichiers tiers         |

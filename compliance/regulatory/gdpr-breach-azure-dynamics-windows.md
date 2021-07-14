---
title: Notification de violation Azure, Dynamics 365 et Windows dans le cadre du RGPD
description: Protection d’Azure et Dynamics 365 vis-à-vis des violations de données personnelles, et réponse et notification de Microsoft en cas de violation.
keywords: Azure, Microsoft 365, Dynamics 365, documentation Microsoft 365, RGPD
localization_priority: Priority
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: ac740f31a7d09353752eea93a4ce41f2230e3178
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53378245"
---
# <a name="azure-dynamics-365-and-windows-breach-notification-under-the-gdpr"></a>Notification de violation Azure, Dynamics 365 et Windows dans le cadre du RGPD

Microsoft prend au sérieux ses obligations dans le cadre du Règlement Général sur la Protection des Données Personnelles (RGPD). Microsoft prend des mesures de sécurité étendues au sein de ses services en ligne pour protéger contre les violations des données. Ces mesures incluent des contrôles de sécurité physique et logique, ainsi que des processus de sécurité automatisés, des politiques de confidentialité et de sécurité des informations complètes, et des formations sur la confidentialité et la sécurité pour tout le personnel.

La sécurité est intégrée à Microsoft Azure à partir de la base, en commençant par [Security Development Lifecycle](https://www.microsoft.com/sdl/), un processus de développement obligatoire qui incorpore des méthodologies de confidentialité par conception et de confidentialité par défaut. Le principe directeur de stratégie de sécurité de Microsoft est de « partir du principe qu’il y a une violation, » qui est une extension de la stratégie de défense en profondeur. En défiant constamment les fonctionnalités de sécurité d’Azure, Microsoft peut devancer les menaces émergentes. Pour plus d’informations sur la sécurité Azure, consultez ces [ressources](https://www.microsoft.com/trustcenter/security/azure-security).

Microsoft propose un service d’intervention dédié en cas d’incident qui fonctionne 24h/24 et 7j/7 pour atténuer les conséquences des attaques contre Microsoft Azure. Attesté par plusieurs audits de sécurité et de conformité (par exemple, [ISO/IEC 27018](offering-iso-27018.md)), Microsoft utilise des opérations et processus rigoureux au niveau de ses centres de données pour empêcher tout accès non autorisé, y compris la surveillance vidéo 24h/24 et 7j/7, du personnel de sécurité compétent, des cartes à puce et des contrôles biométriques.

## <a name="detection-of-potential-breaches"></a>Détection de violations potentielles

En raison de la nature du cloud computing moderne, toutes les violations de données se produisant dans un environnement cloud client n’impliquent pas les services Microsoft Azure. Microsoft utilise un modèle de responsabilité partagée pour les services Azure pour définir la sécurité et les responsabilités opérationnelles. La responsabilité partagée est importante dans le cas de la sécurité d’un service cloud, car le fournisseur de services cloud et le client sont responsables de certaines parties de la sécurité dans le cloud.

Microsoft ne surveille pas les incidents de sécurité et n’y répond pas dans le domaine de la responsabilité du client. Une compromission de la sécurité du client uniquement ne serait pas traitée comme un incident de sécurité Azure et exigerait que le client du client gère l’effort de réponse. La réponse à un incident client peut impliquer la collaboration du [service clientèle](https://azure.microsoft.com/support/options/) de Microsoft Azure, avec des contrats de service appropriés. Microsoft Azure propose également différents services (par exemple, le [Centre de sécurité Azure](https://azure.microsoft.com/services/security-center/)) que les clients peuvent utiliser pour développer et gérer la réponse aux incidents de sécurité.

Azure répond à une violation des données potentielle selon le processus de réponse à un incident de sécurité, qui est un sous-ensemble du plan de gestion des incidents de Microsoft Azure. La réponse aux incidents de sécurité Azure de Microsoft est implémentée à l’aide d’un processus en cinq étapes : détecter, évaluer, diagnostiquer, stabiliser et fermer. L’équipe de réponse aux incidents de sécurité peut alterner entre l’étape de diagnostic et de stabilisation au fur et à mesure que l’examen avance. Vous trouverez ci-dessous une vue d’ensemble du processus de réponse aux incidents de sécurité :

| Phase | Description |
|:------- |------------- |
| ***1 : Détecter*** | Première indication d’un incident potentiel. |
| ***2 : Évaluer*** | Un membre de l’équipe d’invervention en cas d’incidents évalue les conséquences et la gravité de l’événement. En fonction des données probantes, l’évaluation peut ou non aboutir à un signalement supplémentaire à l’équipe d’intervention en matière de sécurité. |
| ***3 : Diagnostiquer*** | Des spécialistes d’intervention en matière de sécurité effectuent une enquête technique ou scientifique, et identifient des stratégies de limitation, d’atténuation et de contournement. Si l’équipe de sécurité pense que les données client ont pu être exposées à un individu non autorisé ou ayant commis des actes illicites, l’exécution du processus de notification des incidents du client débute en parallèle. |
| ***4 : Stabiliser et récupérer*** | L’équipe d’intervention en cas d’incidents crée un plan de récupération pour atténuer le problème. Les étapes de limitation de crise telles que la mise en quarantaine des systèmes concernés peuvent avoir lieu immédiatement et parallèlement au diagnostic. Des enquêtes à plus long terme peuvent être planifiées et avoir lieu une fois que le risque immédiat est passé. |
| ***5 : Fermeture et post-mortem*** | L’équipe de réponse aux incidents de sécurité crée un post-mortem décrivant les détails de l’incident, avec l’intention de réviser les stratégies, procédures et processus afin d’éviter que l’événement se reproduise. |

Les processus de détection utilisés par Microsoft Azure sont conçus pour découvrir les événements mettant en danger la confidentialité, l’intégrité et la disponibilité des services Azure. Plusieurs événements peuvent déclencher une enquête :

- Les alertes système automatisées via la surveillance interne et les infrastructures d’alertes. Ces alertes peuvent survenir en tant qu’alarmes basées sur la signature (par exemple, les logiciels anti-programme malveillant, la détection de l’intrusion) ou via des algorithmes conçus pour profiler l’activité prévue et signaler des anomalies.
- Les rapports de première partie des services Microsoft exécutés sur Microsoft Azure et Azure Government.
- Les vulnérabilités de sécurité sont signalées au [Centre de réponse aux problèmes de sécurité Microsoft (MSRC)](https://www.microsoft.com/msrc) via [Signaler un problème](https://msrc.microsoft.com/create-report). MSRC fonctionne avec des partenaires et des chercheurs en sécurité dans le monde entier afin d’éviter les incidents de sécurité et améliorer la sécurité des produits Microsoft.
- Les rapports client via le [Portail de support client](https://www.windowsazure.com/support/contact/) ou Microsoft Azure et le portail Azure Government Management, qui décrivent une activité suspecte attribuée à l’infrastructure Azure (par opposition à l’activité ayant lieu dans le domaine de la responsabilité du client).
- Sécurité activité [d’Équipe Rouge et Équipe Bleue](https://azure.microsoft.com/blog/red-teaming-using-cutting-edge-threat-simulation-to-harden-the-microsoft-enterprise-cloud/). Cette stratégie utilise une équipe rouge hautement qualifiée d’experts en matière de sécurité Microsoft pour découvrir et attaquer les faiblesses potentielles dans Azure. L’équipe de sécurité couleur bleue doit détecter et se défendre contre l’activité de l’équipe rouge. Les actions des équipes rouge et bleue sont utilisées pour vérifier que le travail de réponse de sécurité Azure gère efficacement les incidents de sécurité. Les activités de la sécurité des équipes rouge et bleue sont régies par les règles d'engagement, afin de garantir la protection des données client.
- Les signalements par des opérateurs des services Azure. Les employés de Microsoft sont formés pour identifier et transmettre les éventuels problèmes de sécurité.

## <a name="azures-data-breach-response"></a>Réponse d’Azure à une violation des données

Microsoft affecte les niveaux de priorité et de gravité appropriés à l’examen en déterminant l’impact fonctionnel, la capacité de récupération et l’impact sur les informations de l’incident. La priorité et la gravité peuvent changer au cours de l’enquête, en fonction de nouveaux résultats et conclusions. Les événements de sécurité impliquant des risques immédiats ou confirmés pour les données client sont traités comme une gravité élevée et ont été résolus 24h/24.

L’équipe de réponse de sécurité collabore avec des ingénieurs de sécurité Microsoft Azure et des experts techniques pour classer l’événement en fonction des données factuelles des éléments de preuve. Un événement de sécurité peut-être classé de la façon suivante :

- **Faux positif**: événement qui répond aux critères de détection mais qui fait partie d’une pratique métier normale et qui peut être filtré. Les équipes de service identifient la cause racine des faux positifs et les traitent systématiquement pour les ajuster en fonction des besoins.
- **Événement de sécurité**: occurrence observable dans un système, un service et/ou un réseau pour une tentative d’attaque, le contournement des contrôles de sécurité ou un problème identifié où les faits indiquent que les données client ou les données personnelles peuvent avoir été perdues, détruites, modifiées, divulguées ou consultées sans autorisation.
- **Incident de sécurité/Incident de sécurité/Incident CRSPI (Customer Reportable Security/Privacy Incident)**: violation confirmée (par exemple, déclarée) de la sécurité entraînant la destruction accidentelle ou illégale, la perte, la modification, la divulgation non autorisée ou l’accès aux données client ou à données personnelles lors du traitement par Microsoft.
- **Événement de confidentialité**: événement de sécurité qui affecte le traitement des données personnelles ou des données, ce qui entraîne des conséquences inattendues sur la confidentialité, notamment la non-conformité avec les stratégies, normes et contrôles de confidentialité Microsoft.
- **Incident de confidentialité/Incident de sécurité/confidentialité pouvant être signalé par le client (CRSPI)**: un incident de sécurité qui affecte les données personnelles, les données ou le traitement des données, ce qui entraîne des conséquences inattendues pour la confidentialité, notamment la non-conformité avec les stratégies de confidentialité, les normes et les contrôles Microsoft.

Pour qu’un CRSPI soit déclaré, Microsoft doit déterminer que l’accès non autorisé aux données client a ou a très probablement eu lieu et/ou qu’une notification juridique ou contractuelle doit être envoyée. Il est souhaitable, sans être obligatoire, de connaître l’impact spécifique sur les clients, l’accès aux ressources et les étapes de réparation. Un incident est généralement déclaré comme CRSPI à la fin de l’étape de diagnostic d’un incident de sécurité ; toutefois, la déclaration peut arriver à tout moment une fois toutes les informations pertinentes disponibles.

Microsoft vérifie que le risque du client et de l’entreprise est maîtrisé et que les mesures correctives sont mises en œuvre. Si nécessaire, des plans d’urgence et d’atténuation visant à résoudre les risques de sécurité immédiats sont mis en œuvre.

Microsoft effectue aussi un post-mortem interne pour les violations de données. Dans le cadre de cet exercice, le niveau suffisant de réponse et les procédures d’exploitation sont évaluées, et les mises à jour pouvant être nécessaires à la procédure d’exploitation standard de la réponse aux incidents de sécurité ou les processus connexes sont identifiés et mis en œuvre. Les post-mortems internes pour les violations de données sont des enregistrements hautement confidentiels qui ne sont pas accessibles aux clients. Les post-mortems peuvent toutefois être synthétisés et inclus dans d’autres notifications d’événement client. Ces rapports sont fournis aux auditeurs externes pour révision, dans le cadre du cycle d’audit de routine d’Azure.

## <a name="customer-notification"></a>Notification du client

Microsoft avertit les clients et les autorités réglementaires concernés en cas de violations des données, le cas échéant. Microsoft se base sur une compartimentation interne importante dans l’exploitation d’Azure. Les journaux de flux de données sont également puissants. Cette conception présente des avantages car la plupart des incidents peuvent être limités à des clients spécifiques. L’objectif consiste à fournir aux clients concernés une notification précise et exploitable en temps voulu dès qu’il y a violation de leurs données.

Suite à un CRSPI déclaré, le processus de notification intervient dans les meilleurs délais, sachant que les risques de sécurité évoluent rapidement. En règle générale, le processus d’élaboration des notifications a lieu alors que l’analyse de l’incident est en cours. Les notifications client sont envoyées dans un délai maximal de 72 heures à partir du moment où nous avons déclaré une violation, *sauf* dans les cas suivants :

- Microsoft pense que l’exécution d’une notification augmente le risque pour d’autres clients. Par exemple, l’action de notification peut donner un conseil à un adversaire, ce qui provoque une incapacité à corriger.
- D’autres circonstances inhabituelles ou extrêmes examinées par le service juridique de Microsoft et le gestionnaire exécutif des incidents.
- Le délai de 72 heures peut laisser certains détails sur l'incident disponibles. Ces détails sont fournis aux clients et aux autorités réglementaires au fur et à mesure que l’enquête progresse.

Microsoft fournit aux clients affectés des informations détaillées leur permettant d’effectuer des enquêtes internes et de répondre aux engagements des utilisateurs finaux, sans retarder le processus de notification de façon excessive.

La notification d’une divulgation de données personnelles sera envoyée au client affecté par tout moyen que Microsoft sélectionne, y compris par courrier électronique. La notification d’une divulgation de données sera envoyée à la liste des contacts de sécurité fournis dans Azure Security Center, qui peut être configurée en suivant les [instructions d’implémentation](/azure/security-center/security-center-provide-security-contact-details). Si les informations de contact ne sont pas fournies dans Azure Security Center (centre de sécurité Azure), la notification est envoyée à un ou plusieurs administrateurs dans un abonnement Azure. Pour vous assurer que les notifications peuvent être remises correctement, il incombe au client de s’assurer que les informations de contact des administrateurs sur les portails de services en ligne et les abonnements concernés sont correctes.

L’équipe Microsoft Azure ou Azure Government peut également choisir d’avertir d’autres membres du personnel Microsoft, tels que les membres de l’équipe du service de support technique (CSS) de Microsoft et le ou les responsables de comptes (AM) du client ou les gestionnaires de comptes techniques (TAM). Ces personnes ont souvent des relations proches avec le client et peuvent faciliter une correction plus rapide.

## <a name="microsoft-dynamics-365-built-in-security-features"></a>Fonctionnalités de sécurité intégrées de Microsoft Dynamics 365

Microsoft Dynamics 365 tire parti de l’infrastructure du service cloud et des fonctionnalités de sécurité intégrées pour assurer la protection des données au moyen de mesures et de mécanismes de sécurité. Par ailleurs, Dynamics 365 offre des fonctionnalités efficaces d’accès aux données et de collaboration garantissant l’intégrité des données et la confidentialité dans les domaines suivants : [sécurisation des identités, protection des données, sécurité basée sur les rôles et gestion des menaces](https://www.microsoft.com/trustcenter/security/dynamics365-security).

L’offre Microsoft Dynamics 365 suit les mêmes mesures techniques et organisationnelles que prennent une ou plusieurs équipes de service Microsoft Azure pour la sécurisation des données contre leur divulgation. Par conséquent, les informations décrites dans le document de notification « Violation de données Microsoft Azure » sont similaires au service Microsoft Dynamics 365.

## <a name="windows-diagnostic-data-processor-configuration"></a>Configuration du processeur données de diagnostic Windows

La configuration du processeur [données de diagnostic Windows](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) tire parti de l’infrastructure de service cloud et des fonctionnalités de sécurité intégrées pour assurer la sécurité des données à l’aide de mesures et de mécanismes de sécurité pour protéger les données.

Il suit les mêmes mesures techniques et organisationnelles qu’une ou plusieurs Microsoft Azure équipes de service prennent pour sécuriser contre les processus de violation de données. Par conséquent, toutes les informations documentées dans le document de notification « Violation des données Microsoft Azure » ici sont analogues à la configuration du processeur données de diagnostic Windows également.

## <a name="learn-more"></a>En savoir plus

[Centre de gestion de la confidentialité Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)

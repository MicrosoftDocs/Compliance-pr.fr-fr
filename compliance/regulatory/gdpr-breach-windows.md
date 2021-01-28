---
title: Service de traitement de données pour la notification Windows Enterprise sous RGPD
description: Service de traitement de données pour la protection de Windows Enterprise vis-à-vis des violations de données personnelles, et réponse et notification de Microsoft en cas de violation.
keywords: Service de traitement des données pour Windows Enterprise, Microsoft 365, documentation Microsoft 365, RGPD
localization_priority: Priority
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmaz
manager: laurawi
ms.reviewer: delinat
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
ms.openlocfilehash: d1d0acae943bf0a0af4b6f81f948208e4bd58ef6
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012920"
---
# <a name="data-processor-service-for-windows-enterprise-breach-notification-under-the-gdpr"></a>Service de traitement de données pour la notification de violation Windows Enterprise sous RGPD

>[!NOTE]
>Cette rubrique est destinée aux participants au programme de prévisualisation du service de traitement des données pour Windows Enterprise et nécessite l'acceptation de conditions d'utilisation spécifiques. Pour en savoir plus sur le programme et accepter les conditions d’utilisation, voir [https://aka.ms/WindowsEnterprisePublicPreview](https://aka.ms/WindowsEnterprisePublicPreview).

Le service de traitement des données de Microsoft pour Windows Enterprise prend au sérieux ses obligations au titre du règlement général sur la protection des données (RGDP). Le service de traitement des données de Microsoft pour Windows Enterprise prend des mesures de sécurité étendues pour se protéger contre les violations de données. Il s’agit notamment d’équipes spécialisées dans la gestion des menaces, qui anticipent, bloquent et atténuent les accès malveillants de manière proactive.  Les mesures de sécurité interne telles que l’analyse des ports, l’analyse des vulnérabilités du périmètre et la détection des intrusions détectent et bloquent l’accès malveillant, ainsi que les processus de sécurité automatisés, les stratégies de sécurité et de confidentialité des informations, ainsi que la sécurité et la confidentialité pour tous les membres du personnel. 

La sécurité est intégrée dans le service de traitement des données de Microsoft pour Windows Enterprise depuis le début, en commençant par le [Cycle de développement de la sécurité](https://www.microsoft.com/sdl/), un processus de développement obligatoire qui incorpore des méthodologies de confidentialité par conception et de confidentialité par défaut. Le principe de base de la stratégie de sécurité de Microsoft consiste à « assumer une violation », qui est une extension de la stratégie de défense en profondeur. En remettant constamment en question les fonctionnalités de sécurité du service de traitement des données pour Windows Enterprise, Microsoft peut garder une longueur d'avance sur les nouvelles menaces. Pour plus d’informations sur le service de traitement de données pour la sécurité Windows Enterprise, consultez ces [ressources](https://www.microsoft.com/TrustCenter/Security/windows10-security) le service de traitement de données pour Windows Enterprise répond à une violation potentielle de données en fonction du processus de réponse aux incidents de sécurité. Le service de traitement des données pour la réponse aux incidents de sécurité de Windows Enterprise est implémenté à l'aide d'un processus en cinq étapes : détecter, évaluer, diagnostiquer, stabiliser et fermer. L’équipe de réponse aux incidents de sécurité peut alterner entre les étapes de diagnostique et de stabilisation au fur et à mesure de la progression de l’examen. Voici une vue d’ensemble du processus de réponse aux incidents de sécurité : 

|**Stade**|**Description**|
|:------- |:------------- |
| **_1 : Détecter_* _ | Première indication d’un incident potentiel. |
| _*_2 : Évaluer_*_ | Un membre de l’équipe d’invervention en cas d’incidents évalue les conséquences et la gravité de l’événement. En fonction des données probantes, l’évaluation peut ou non aboutir à un signalement supplémentaire à l’équipe d’intervention en matière de sécurité. |
| _*_3 : Diagnostiquer_*_ | Des spécialistes d’intervention en matière de sécurité effectuent une enquête technique ou scientifique, et identifient des stratégies de limitation, d’atténuation et de contournement. Si l’équipe de sécurité pense que les données client ont pu être exposées à un individu non autorisé ou ayant commis des actes illicites, l’exécution du processus de notification des incidents du client débute en parallèle. |
| _*_4 : Stabiliser et récupérer_*_ | L’équipe d’intervention en cas d’incidents crée un plan de récupération pour atténuer le problème. Les étapes de limitation de crise telles que la mise en quarantaine des systèmes concernés peuvent avoir lieu immédiatement et parallèlement au diagnostic. Des enquêtes à plus long terme peuvent être planifiées et avoir lieu une fois que le risque immédiat est passé. |
| _*_5 : Fermeture et post-mortem_*_ | L’équipe d’intervention en cas d’incidents crée un post-mortem qui décrit les détails de l’incident, avec l’intention de réviser les stratégies, procédures et processus afin d’éviter la récurrence de l’événement. |

Les processus de détection utilisés par le service de traitement de données Microsoft pour Windows Enterprise sont conçus pour découvrir les événements susceptibles de menacer la confidentialité, l’intégrité et la disponibilité du service de traitement de données pour Windows Enterprise. Plusieurs événements peuvent déclencher un examen :

- Alertes système automatisées via des infrastructures de surveillance interne et d’alertes. Ces alertes peuvent survenir en tant qu’alarmes basées sur la signature (par exemple, les programmes malveillants, la détection de l’intrusion) ou via des algorithmes conçus pour profiler l’activité prévue et signaler des anomalies.
- Les rapports de première partie des services Microsoft exécutés sur Microsoft Azure et Azure Government.
- Les vulnérabilités de sécurité sont signalées à [MSRC (Microsoft Security Response Center)](https://technet.microsoft.com/security/dn440717) via [secure@microsoft.com] (mailto:secure@microsoft.com). MSRC fonctionne avec des partenaires et des chercheurs en sécurité dans le monde entier afin d’éviter les incidents de sécurité et améliorer la sécurité des produits Microsoft.
- Les rapports client via le portail de support client ou Microsoft Azure et le portail Azure Government Management, qui décrivent une activité suspecte attribuée à l’infrastructure Azure (par opposition à l’activité ayant lieu dans le domaine de la responsabilité du client).
- Sécurité activité [d’Équipe Rouge et Équipe Bleue](https://azure.microsoft.com/blog/red-teaming-using-cutting-edge-threat-simulation-to-harden-the-microsoft-enterprise-cloud/). Cette stratégie utilise une équipe rouge hautement qualifiée d’experts en matière de sécurité Microsoft pour découvrir et attaquer les faiblesses potentielles dans Azure. L’équipe de sécurité couleur bleue doit détecter et se défendre contre l’activité de l’équipe rouge. Les actions des équipes rouge et bleue sont utilisées pour vérifier que le travail de réponse de sécurité Azure gère efficacement les incidents de sécurité. Les activités de la sécurité des équipes rouge et bleue sont régies par les règles d'engagement, afin de garantir la protection des données client.
- Escalades des opérateurs des services Azure. Les employés de Microsoft sont formés pour identifier et transmettre les éventuels problèmes de sécurité.

## <a name="data-processor-service-for-windows-enterprise-data-breach-response"></a>Service de traitement de données pour la réponse aux violations de données Windows Enterprise

 Microsoft affecte l’enquête à des niveaux de priorité et de gravité appropriés en déterminant l’impact fonctionnel, la récupérabilité et l’impact sur les informations de l’incident. La priorité et la gravité peuvent changer au cours des enquêtes, sur la base de nouveaux résultats et conclusions. Les événements de sécurité impliquant des risques imminents ou confirmés pour les données client sont traités comme présentant un niveau de gravité élevé et 24 heures sur 24 pour résoudre le problème. Le service de traitement des données de Microsoft pour Windows Enterprise classe l'impact des informations de l'incident dans les catégories de violation suivantes :

| _ *Catégorie** | **Définition** |
|:------------ |:-------------- |
| **_Aucune_* _ | Aucune information n’a été supprimée, modifiée, supprimée ni compromise d’une façon ou d’une autre. |
| _*_Violation de la confidentialité_*_ | Des données personnelles sensibles des contribuables, employés, bénéficiaires, etc. ont été consultées ou supprimées. |
| _*_Violation d’informations confidentielles_*_ | Des informations confidentielles non classifiées, telles que des informations sur les infrastructures critiques protégées (PCII), ont été consultées ou supprimées. |
| _*_Perte d’intégrité_*_ | Des informations sensibles ou confidentielles ont été modifiées ou supprimées. |

L’équipe de réponse de sécurité collabore avec le service de traitement des données de Microsoft pour les ingénieurs de sécurité Windows Enterprise et les PME pour classer l’événement en fonction des données factuelles des éléments de preuve. Un événement de sécurité peut être classifié comme suit :

- _*Faux positif** : un événement qui répond aux critères de détection, mais qui est considéré comme faisant partie d’une pratique commerciale normale et peut nécessiter un filtrage. L’équipe de service identifie la cause première des faux positifs et les traite d’une manière systématique en utilisant des sources de détection et en les ajustant au besoin.
- **Incident de sécurité** : un incident provoqué par un accès non autorisé à des données client ou à des données du support stockées sur un équipement de Microsoft ou dans des installations de Microsoft, ou tout accès non autorisé à ces équipement ou installations provoquant la perte, divulgation ou altération des données client ou des données de support.
- **Incident de sécurité déclarable au client** : un accès illégal ou non autorisé ou une utilisation illégale ou non autorisée de systèmes, équipements ou installations Microsoft provoquant la divulgation, modification ou perte de données client.
- **Violation de la confidentialité** : sous-type d’incident de sécurité impliquant des données personnelles. Les procédures de gestion sont les mêmes que celles concernant un incident de sécurité.

 Pour déclarer les CRSI (Incident de sécurité déclarable au client), Microsoft doit déterminer qu’un accès non autorisé aux données client a eu lieu ou a probablement eu lieu et/ou qu’il existe un engagement juridique ou contractuel qu’une notification doit se produire. Il est souhaitable, mais pas obligatoire, que l’impact du client spécifique, l’accès aux ressources et les étapes de réparation soient connus. Un incident est généralement déclaré comme un CRSI après la conclusion de l’étape de diagnostic d’un incident de sécurité ; toutefois, la déclaration peut se produire à tout moment où toutes les informations pertinentes sont disponibles. Le gestionnaire des incidents de sécurité doit établir des preuves au-delà de tout doute raisonnable qu’un événement déclarable s’est produit pour commencer l’exécution du processus de notification d’un incident client.

Tout au long de l’enquête, l’équipe de réponse de sécurité collabore étroitement avec des conseillers juridiques pour vérifier que l’enquête judiciaire est menée conformément aux obligations juridiques et aux engagements vis-à-vis des clients. Il existe également des restrictions importantes sur la gestion et l’affichage des données client et système dans différents environnements d’exploitation. Les données sensibles ou confidentielles et les données client ne sont pas transférées en dehors de l’environnement de production sans l’approbation écrite explicite du gestionnaire des incidents enregistrée dans le ticket des incidents correspondant.

Microsoft vérifie que le risque du client et de l’entreprise est maîtrisé et que les mesures correctives sont mises en œuvre. Si nécessaire, des plans d’urgence et d’atténuation visant à résoudre les risques de sécurité immédiats sont mis en œuvre.

Microsoft effectue aussi un post-mortem interne pour les violations de données. Dans le cadre de cet exercice, le niveau suffisant de réponse et les procédures d’exploitation sont évalués, et les mises à jour pouvant être nécessaires pour les stratégies de l’équipe de réponse de sécurité ou des processus connexes sont identifiées et mises en œuvre. Les post-mortems internes pour les violations de données sont des enregistrements hautement confidentiels qui ne sont pas accessibles aux clients. Les post-mortems peuvent toutefois être synthétisés et inclus dans d’autres notifications d’événement au client. Ces rapports sont fournis à des auditeurs externes pour révision dans le cadre du cycle d’audit de routine du service de traitement de données pour Windows Enterprise.

## <a name="customer-notice"></a>Avis client

Le service de traitement des données de Microsoft pour Windows Enterprise informe les clients et les autorités de régulation des violations de données, le cas échéant. Microsoft s'appuie sur une forte compartimentation interne dans le fonctionnement du service de traitement des données pour Windows Enterprise. Les journaux de flux de données sont également fiables. L'avantage de cette conception est que la plupart des incidents peuvent être liés à des clients spécifiques. L’objectif est de donner aux clients concernés un avis précis, exploitable et opportun, lorsque leurs données ont été violées.

Suite à un CRSI déclaré, le processus de notification intervient dans les meilleurs délais, sachant que les risques de sécurité évoluent rapidement. En règle générale, le processus d’élaboration des notifications a lieu alors que l’analyse de l’incident est en cours. Les notifications du client sont livrées dans un délai maximal de 72 heures à partir du moment où nous avons déclaré une violation, sauf dans les cas suivants :

- Microsoft estime que le fait d’exécuter une notification augmentera le risque pour d’autres clients. Par exemple, la notification peut avertir un adversaire, et ainsi empêcher de résoudre le problème.
- D’autres circonstances inhabituelles ou extrêmes examinées par le service juridique Corporate External and Legal Affairs (CELA) de Microsoft et le gestionnaire exécutif des incidents.

 Le service de traitement des données de Microsoft pour Windows Enterprise fournit aux clients des informations détaillées leur permettant d’effectuer des enquêtes internes et de répondre aux engagements des utilisateurs finaux, sans retarder le processus de notification de façon excessive.

La notification d’une divulgation de données personnelles sera envoyée au client par tout moyen que Microsoft sélectionne, y compris par courrier électronique. La notification d’une divulgation de données sera envoyée à la liste des contacts de sécurité fournis dans Azure Security Center, qui peut être configurée en suivant les [instructions d’implémentation](https://docs.microsoft.com/azure/security-center/security-center-provide-security-contact-details). Si les informations de contact ne sont pas fournies dans Azure Security Center (centre de sécurité Azure), la notification est envoyée à un ou plusieurs administrateurs dans un abonnement Azure. Pour vous assurer que les notifications peuvent être remises correctement, il incombe au client de s’assurer que les informations de contact des administrateurs sur les portails de services en ligne et les abonnements concernés sont correctes.

Le service de traitement des données de Microsoft pour l’équipe Windows Enterprise peut également choisir d’informer d’autres membres du personnel Microsoft (par exemple, le service client et le gestionnaire de compte du client ou le gestionnaire de compte technique). Ces personnes ont souvent des relations étroites avec le client et peuvent favoriser une correction plus rapide.

Pour plus d’informations sur la façon dont Microsoft détecte et répond à une violation des données personnelles, reportez-vous à l’article [Notification des violations de données en vertu du RGPD](https://servicetrust.microsoft.com/ViewPage/GDPRBreach) dans le portail d’approbation de services.

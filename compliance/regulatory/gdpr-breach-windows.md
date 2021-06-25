---
title: Service de traitement de données pour la notification Windows Enterprise sous RGPD
description: Service de traitement de données pour la protection de Windows Enterprise vis-à-vis des violations de données personnelles, et réponse et notification de Microsoft en cas de violation.
keywords: Service de traitement des données pour Windows Enterprise, Microsoft 365, documentation Microsoft 365, RGPD
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
ms.openlocfilehash: 1fbbdb16fd1231d6044ed556090823cd36f90c78
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088863"
---
# <a name="data-processor-service-for-windows-enterprise-breach-notification-under-the-gdpr"></a>Service de traitement de données pour la notification de violation Windows Enterprise sous RGPD

>[!NOTE]
>Cette rubrique est destinée aux participants au programme de prévisualisation du service de traitement des données pour Windows Enterprise et nécessite l'acceptation de conditions d'utilisation spécifiques. Pour en savoir plus sur le programme et accepter les conditions d’utilisation, voir [https://aka.ms/WindowsEnterprisePublicPreview](https://aka.ms/WindowsEnterprisePublicPreview).

Le service de traitement des données de Microsoft pour Windows Enterprise prend au sérieux ses obligations au titre du règlement général sur la protection des données (RGDP). Le service de traitement des données de Microsoft pour Windows Enterprise prend des mesures de sécurité étendues pour se protéger contre les violations de données. Il s’agit notamment d’équipes spécialisées dans la gestion des menaces, qui anticipent, bloquent et atténuent les accès malveillants de manière proactive.  Les mesures de sécurité interne telles que l’analyse des ports, l’analyse des vulnérabilités du périmètre et la détection des intrusions détectent et bloquent l’accès malveillant, ainsi que les processus de sécurité automatisés, les stratégies de sécurité et de confidentialité des informations, ainsi que la sécurité et la confidentialité pour tous les membres du personnel.

La sécurité est intégrée dans le service de traitement des données de Microsoft pour Windows Enterprise depuis le début, en commençant par le [Cycle de développement de la sécurité](https://www.microsoft.com/sdl/), un processus de développement obligatoire qui incorpore des méthodologies de confidentialité par conception et de confidentialité par défaut. Le principe de base de la stratégie de sécurité de Microsoft consiste à « assumer une violation », qui est une extension de la stratégie de défense en profondeur. En remettant constamment en question les fonctionnalités de sécurité du service de traitement des données pour Windows Enterprise, Microsoft peut garder une longueur d'avance sur les nouvelles menaces. Pour plus d’informations sur le service de traitement de données pour la sécurité Windows Enterprise, consultez ces [ressources](https://www.microsoft.com/TrustCenter/Security/windows10-security) le service de traitement de données pour Windows Enterprise répond à une violation potentielle de données en fonction du processus de réponse aux incidents de sécurité. Le service de traitement des données pour la réponse aux incidents de sécurité de Windows Enterprise est implémenté à l'aide d'un processus en cinq étapes : détecter, évaluer, diagnostiquer, stabiliser et fermer. L’équipe de réponse aux incidents de sécurité peut alterner entre les étapes de diagnostique et de stabilisation au fur et à mesure de la progression de l’examen. Voici une vue d’ensemble du processus de réponse aux incidents de sécurité :

|**Stade**|**Description**|
|:------- |:------------- |
| **_1 : Détecter_* _ | Première indication d’un incident potentiel. |
| _*_2 : Évaluer_*_ | Un membre de l’équipe d’invervention en cas d’incidents évalue les conséquences et la gravité de l’événement. En fonction des données probantes, l’évaluation peut ou non aboutir à un signalement supplémentaire à l’équipe d’intervention en matière de sécurité. |
| _*_3 : Diagnostiquer_*_ | Des spécialistes d’intervention en matière de sécurité effectuent une enquête technique ou scientifique, et identifient des stratégies de limitation, d’atténuation et de contournement. Si l’équipe de sécurité pense que les données client ont pu être exposées à un individu non autorisé ou ayant commis des actes illicites, l’exécution du processus de notification des incidents du client débute en parallèle. |
| _*_4 : Stabiliser et récupérer_*_ | L’équipe d’intervention en cas d’incidents crée un plan de récupération pour atténuer le problème. Les étapes de limitation de crise telles que la mise en quarantaine des systèmes concernés peuvent avoir lieu immédiatement et parallèlement au diagnostic. Des enquêtes à plus long terme peuvent être planifiées et avoir lieu une fois que le risque immédiat est passé. |
| _*_5 : Fermeture et post-mortem_*_ | L’équipe d’intervention en cas d’incidents crée un post-mortem qui décrit les détails de l’incident, avec l’intention de réviser les stratégies, procédures et processus afin d’éviter la récurrence de l’événement. |

Les processus de détection utilisés par le service de traitement de données Microsoft pour Windows Enterprise sont conçus pour découvrir les événements susceptibles de menacer la confidentialité, l’intégrité et la disponibilité du service de traitement de données pour Windows Enterprise. Plusieurs événements peuvent déclencher une enquête :

- Les alertes système automatisées via la surveillance interne et les infrastructures d’alertes. Ces alertes peuvent survenir en tant qu’alarmes basées sur la signature (par exemple, les logiciels anti-programme malveillant, la détection de l’intrusion) ou via des algorithmes conçus pour profiler l’activité prévue et signaler des anomalies.
- Les rapports de première partie des services Microsoft exécutés sur Microsoft Azure et Azure Government.
- Les vulnérabilités de sécurité sont signalées à [MSRC (Microsoft Security Response Center)](https://technet.microsoft.com/security/dn440717) via [secure@microsoft.com] (mailto:secure@microsoft.com). MSRC fonctionne avec des partenaires et des chercheurs en sécurité dans le monde entier afin d’éviter les incidents de sécurité et améliorer la sécurité des produits Microsoft.
- Les rapports client via le portail de support client ou Microsoft Azure et le portail Azure Government Management, qui décrivent une activité suspecte attribuée à l’infrastructure Azure (par opposition à l’activité ayant lieu dans le domaine de la responsabilité du client).
- Sécurité activité [d’Équipe Rouge et Équipe Bleue](https://azure.microsoft.com/blog/red-teaming-using-cutting-edge-threat-simulation-to-harden-the-microsoft-enterprise-cloud/). Cette stratégie utilise une équipe rouge hautement qualifiée d’experts en matière de sécurité Microsoft pour découvrir et attaquer les faiblesses potentielles dans Azure. L’équipe de sécurité couleur bleue doit détecter et se défendre contre l’activité de l’équipe rouge. Les actions des équipes rouge et bleue sont utilisées pour vérifier que le travail de réponse de sécurité Azure gère efficacement les incidents de sécurité. Les activités de la sécurité des équipes rouge et bleue sont régies par les règles d'engagement, afin de garantir la protection des données client.
- Les signalements par des opérateurs des services Azure. Les employés de Microsoft sont formés pour identifier et transmettre les éventuels problèmes de sécurité.

## <a name="data-processor-service-for-windows-enterprise-data-breach-response"></a>Service de traitement de données pour la réponse aux violations de données Windows Enterprise

 Microsoft affecte les niveaux de priorité et de sévérité appropriés de l’enquête en déterminant l’impact fonctionnel, la récupération et l’impact des informations de l’incident. La priorité et la sévérité peuvent changer au fur et à mesure que l’enquête avance, en fonction des nouvelles découvertes et conclusions. Les événements de sécurité impliquant un risque imminent ou confirmé pour les données client sont traités comme une sévérité élevée et résolu en priorité. Le service du sous-traitant de données Microsoft pour Windows Enterprise classe l’impact des informations de l’incident dans les catégories de violation suivantes :

| _ *Catégorie** | **Définition** |
|:------------ |:-------------- |
| **_Aucune_* _ | Aucune information n’a été supprimée, modifiée, supprimée ni compromise d’une façon ou d’une autre. |
| _*_Violation de la confidentialité_*_ | Des données personnelles sensibles des contribuables, employés, bénéficiaires, etc. ont été consultées ou supprimées. |
| _*_Violation d’informations confidentielles_*_ | Des informations confidentielles non classifiées, telles que des informations sur les infrastructures critiques protégées (PCII), ont été consultées ou supprimées. |
| _*_Perte d’intégrité_*_ | Des informations sensibles ou confidentielles ont été modifiées ou supprimées. |

L’équipe de réponse de sécurité collabore avec des ingénieurs de sécurité Microsoft Azure et des experts techniques pour classer l’événement en fonction des données factuelles des éléments de preuve. Un événement de sécurité peut-être classé de la façon suivante :

- _*Faux positif** : un événement qui répond aux critères de détection mais qui fait partie d’une pratique d’entreprise normale et nécessite peut-être d’être filtré. L’équipe de service identifiera la cause première des faux positifs et les résoudra de manière systématique en utilisant des sources de détection et en les ajustant en fonction des besoins.
- **Incident de sécurité** : un incident provoqué par un accès non autorisé à des données client ou à des données du support stockées sur un équipement de Microsoft ou dans des installations de Microsoft, ou tout accès non autorisé à ces équipement ou installations provoquant la perte, divulgation ou altération des données client ou des données de support.
- **Incident de sécurité déclarable au client** : un accès illégal ou non autorisé ou une utilisation illégale ou non autorisée de systèmes, équipements ou installations Microsoft provoquant la divulgation, modification ou perte de données client.
- **Violation de la confidentialité** : un sous-type d’incident de sécurité impliquant des données personnelles. La gestion des procédures ne sont pas différentes d’un incident de sécurité.

 Pour déclarer les CRSI (Incident de sécurité déclarable au client), Microsoft doit déterminer qu’un accès non autorisé aux données client a eu lieu ou a probablement eu lieu et/ou qu’il existe un engagement juridique ou contractuel qu’une notification doit se produire. Il est souhaitable, mais pas obligatoire, que l’impact du client spécifique, l’accès aux ressources et les étapes de réparation soient connus. Un incident est généralement déclaré comme un CRSI après la conclusion de l’étape de diagnostic d’un incident de sécurité ; toutefois, la déclaration peut se produire à tout moment où toutes les informations pertinentes sont disponibles. Le gestionnaire des incidents de sécurité doit établir des preuves au-delà de tout doute raisonnable qu’un événement déclarable s’est produit pour commencer l’exécution du processus de notification d’un incident client.

Tout au long de l’enquête, l’équipe de réponse de sécurité collabore étroitement avec des conseillers juridiques pour vérifier que l’enquête judiciaire est menée conformément aux obligations juridiques et aux engagements vis-à-vis des clients. Il existe également des restrictions importantes sur la gestion et l’affichage des données client et système dans différents environnements d’exploitation. Les données sensibles ou confidentielles et les données client ne sont pas transférées en dehors de l’environnement de production sans l’approbation écrite explicite du gestionnaire des incidents enregistrée dans le ticket des incidents correspondant.

Microsoft vérifie que le risque du client et de l’entreprise est maîtrisé et que les mesures correctives sont mises en œuvre. Si nécessaire, des plans d’urgence et d’atténuation visant à résoudre les risques de sécurité immédiats sont mis en œuvre.

Microsoft effectue aussi un post-mortem interne pour les violations de données. Dans le cadre de cet exercice, le niveau suffisant de réponse et les procédures d’exploitation sont évaluées, et les mises à jour pouvant être nécessaires à la procédure d’exploitation standard de la réponse aux incidents de sécurité ou les processus connexes sont identifiés et mis en œuvre. Les post-mortems internes pour les violations de données sont des enregistrements hautement confidentiels qui ne sont pas accessibles aux clients. Les post-mortems peuvent toutefois être synthétisés et inclus dans d’autres notifications d’événement client. Ces rapports sont fournis aux auditeurs externes pour révision, dans le cadre du cycle d’audit de routine du service sous-traitant de données.

## <a name="customer-notice"></a>Avis client

Le service sous-traitant de données Microsoft pour Windows Enterprise avertit les clients et les autorités réglementaires en cas de violations des données, le cas échéant. Microsoft se base sur une compartimentation interne importante dans l’opération du service sous-traitant de données pour Windows Enterprise. Les journaux de flux de données sont également puissants. Cette conception présente des avantages car la plupart des incidents peuvent être limités à des clients spécifiques. L’objectif consiste à fournir aux clients concernés une notification précise et exploitable en temps voulu dès qu’il y a violation de leurs données.

Après la déclaration d’un CRSI, le processus de notification a lieu aussi rapidement que possible, en sachant que les risques de sécurité se déplacent rapidement. Généralement, le processus d’élaboration des notifications a lieu alors que l’analyse de l’incident est en cours. Les notifications client sont envoyées au plus tard 72 heures après la déclaration d’une violation sauf dans les cas suivants :

- Microsoft estime que le fait d’exécuter une notification augmentera le risque pour d’autres clients. Par exemple, la notification peut avertir un adversaire, et ainsi empêcher de résoudre le problème.
- D’autres circonstances inhabituelles ou extrêmes examinées par le service juridique Corporate External and Legal Affairs (CELA) de Microsoft et le gestionnaire exécutif des incidents.

 Le service de traitement des données de Microsoft pour Windows Enterprise fournit aux clients des informations détaillées leur permettant d’effectuer des enquêtes internes et de répondre aux engagements des utilisateurs finaux, sans retarder le processus de notification de façon excessive.

La notification d’une divulgation de données personnelles sera envoyée au client par tout moyen que Microsoft sélectionne, y compris par courrier électronique. La notification d’une divulgation de données sera envoyée à la liste des contacts de sécurité fournis dans Azure Security Center, qui peut être configurée en suivant les [instructions d’implémentation](/azure/security-center/security-center-provide-security-contact-details). Si les informations de contact ne sont pas fournies dans Azure Security Center (centre de sécurité Azure), la notification est envoyée à un ou plusieurs administrateurs dans un abonnement Azure. Pour vous assurer que les notifications peuvent être remises correctement, il incombe au client de s’assurer que les informations de contact des administrateurs sur les portails de services en ligne et les abonnements concernés sont correctes.

Le service sous-traitant pour l’équipe Windows Enterprise peut également choisir d’informer d’autres membres du personnel Microsoft (par exemple, le service client et le gestionnaire de compte du client ou le gestionnaire de compte technique). Ces personnes ont souvent des relations étroites avec le client et peuvent permettre une résolution plus rapide des problèmes.

Pour plus d’informations sur la façon dont Microsoft détecte et répond à une violation des données personnelles, reportez-vous à l’article [Notification des violations de données en vertu du RGPD](https://servicetrust.microsoft.com/ViewPage/GDPRBreach) dans le portail d’approbation de services.

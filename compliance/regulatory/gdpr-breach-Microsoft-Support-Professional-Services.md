---
title: Support Microsoft, services professionnels et notification des violations dans le cadre du RGPD
description: Protection du support Microsoft et des services professionnels vis-à-vis des violations de données personnelles, et réponse et notification de Microsoft en cas de violation.
keywords: Microsoft 365, Microsoft 365 Éducation, documentation Microsoft 365, RGPD
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
ms.openlocfilehash: 1006a30e803adbb21aa27fc6002612a7ef96b487
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507143"
---
# <a name="microsoft-support-and-professional-services-and-breach-notification-under-the-gdpr"></a>Support Microsoft, services professionnels et notification des violations dans le cadre du RGPD

Le Support Microsoft et les services professionnels prennent au sérieux les obligations imposées par le Règlement général sur la protection des données (RGPD).

Les services professionnels Microsoft sont constitués d’un groupe divers d’architectes techniques, d’ingénieurs, de consultants et de professionnels du support qui se consacrent à remplir la mission de Microsoft consistant à donner aux clients les moyens d’être plus productifs. Notre équipe des services professionnels comprend plus de 21 000 consultants, conseillers numériques, agents de support, ingénieurs et autres commerciaux, opérant dans 191 pays et 46 langues différentes, gérant plusieurs millions d’engagements par mois et interagissant avec les clients et partenaires à l’aide d’outils locaux automatisés basés sur le téléphone, le web et la communauté. L’organisation apporte une grande expertise dans le portefeuille Microsoft, tirant parti d’un important réseau de partenaires, de communautés techniques, d’outils, de diagnostics et de canaux qui nous connectent à nos clients professionnels.

Les objectifs de l’équipe de réponse aux incidents de protection des données globales des Services professionnels Microsoft sont les suivants : (a) utiliser des opérations et des processus rigoureux en vue d’éviter la survenue d’incidents de protection des données, (b) les gérer de façon professionnelle et efficace lorsqu’ils se produisent et (c) tirer des leçons de ces incidents de protection des données via des post-mortem réguliers et des améliorations du programme. Les processus et les résultats de l’équipe de réponse aux incidents de protection des données des Services professionnels Microsoft sont vérifiés et confirmés par plusieurs audits de sécurité et de conformité (par exemple, ISO/IEC 27001).

## <a name="data-protection-incident-response-overview"></a>Présentation de la réponse aux incidents de protection des données 

La division Services professionnels Microsoft s’implique dans la protection de ses clients et prend toutes les mesures nécessaires pour empêcher les incidents de protection des données de survenir, dans une optique de maintien de la confiance des clients. Pour la division Services professionnels, un incident de protection des données correspond à une violation de sécurité entraînant, de manière accidentelle ou illégale, la destruction, la perte, l’altération, la divulgation non autorisée de données personnelles ou de données de support ou de conseil, ou l’accès à ces données, lors de leur traitement par Microsoft. Les clients commerciaux abonnés au support Premier, au support Unifié ou aux services de conseil Microsoft doivent se reporter à la réponse aux incidents de protection des données dans leur langue dans l’addenda sur la protection des données des services professionnels, à l’adresse <https://aka.ms/professionalservicesdpa/>.

## <a name="scope--limits-of-data-protection-incident-response-process"></a>Étendue et limites du processus de réponse aux incidents de protection des données

Le processus de notification de violation de données personnelles démarre lorsque nous déclarons qu’une [violation de données personnelles] s’est produite.

Pour que celle-ci soit déclarée, l’équipe de réponse aux incidents de protection des données Microsoft doit déterminer qu’un incident de protection des données répondant à la définition précédemment s’est effectivement produit. La déclaration s’effectue dès que toutes les informations pertinentes sont disponibles pour déterminer qu’un incident de protection des données s’est produit.

En raison de la nature des services professionnels, certains événements ressemblant à des incidents de protection des données Microsoft n’en sont pas, car ils sont le résultat d’actions du client ou se sont produits sur les systèmes du client. Microsoft n’est pas responsable de la surveillance ou de la réaction aux incidents de protection des données survenus dans le cadre du domaine de responsabilité du client. Toutefois, lorsque Microsoft est informé d’un incident de protection des données occasionné par le client, nous classons celui-ci dans la catégorie des incidents de protection des données causés par le client (ce que l’équipe de réponse aux incidents de protection des données appelle un « événement »), informons le client de notre observation et, s’il le demande, lui fournissons notre assistance, en fonction de son interaction avec Microsoft. Les incidents de protection des données causés par les clients incluent par exemple l’envoi de mots de passe ou d’autres informations sensibles des clients à Microsoft, les demandes de suppression de données ou encore les fraudes.

Certaines actions sont totalement en dehors du champ d’application de ce processus, notamment les questions d’ordre général sur nos stratégies ou nos normes de protection des données, les demandes sur les droits de la personne concernée par le traitement des données, les demandes de retrait, les listes de vœux de produits ou les rapports de bogues non associés à la protection des données, les incidents de protection des données n’impliquant pas les données du client et les fraudes à l’encontre de Microsoft.

## <a name="types-of-data-protection-incidents"></a>Types d’incidents de protection des données

L’équipe de réponse aux incidents de protection des données a identifié un ensemble de scénarios qui peuvent survenir dans le cadre de services professionnels. Tout en respectant le cadre initial de réponse aux incidents de protection des données, certaines procédures ont été développées et personnalisées pour accélérer le processus de réponse. Par exemple, un message électronique mal dirigé ne demande pas d’examen approfondi. En revanche, l’identification de personnel malveillant peut nécessiter une enquête légale complète en raison de la nature clandestine des activités du coupable. Ces scénarios peuvent fournir aux services professionnels des informations sur le processus de réponse aux incidents de protection des données.

## <a name="data-protection-incident-response-process"></a>Processus de réponse aux incidents de protection des données

Lorsque les services professionnels Microsoft identifient un incident de protection des données, un processus de tri se produit pour (a) évaluer l’événement, (b) déterminer s’il est dans le champ d’application du processus, (c) déterminer s’il était malveillant, (d) effectuer un examen préliminaire et affecter un niveau de gravité et (e) alerter et coordonner les parties prenantes appropriés au sein de Microsoft. L’équipe commence également à enregistrer des détails à des fins de suivi et de post-mortem.

### <a name="detection"></a>Détection

Les services professionnels Microsoft surveillent en permanence l’émergence d’incidents de protection des données sur l’ensemble des banques de données contenant des données personnelles, en ligne et hors ligne. Nous faisons appel à différentes méthodes pour détecter les incidents de protection des données, notamment des alertes automatisées, des rapports de clients, des rapports de tiers, des observations d’anomalies et des indications d’activités malveillantes ou de piratage.

Les processus de détection utilisés par les services professionnels Microsoft sont conçus pour découvrir les incidents de protection des données et déclencher des enquêtes. Par exemple :

- Les violations de sécurité sont signalées au système de création de rapports général de Microsoft à des fins de référence ou sont signalées directement à l’équipe de réponse aux incidents de protection de données des services professionnels.
- Les clients envoient des rapports décrivant les activités douteuses via le [portail de Support client](https://support.microsoft.com).
- Le personnel des services professionnels envoie les signalements. Les employés de Microsoft sont formés pour identifier et transmettre les éventuels problèmes de sécurité.
- Pour les outils et les systèmes utilisés dans le processus de fourniture de services professionnels, l’équipe des opérations utilise des alertes système automatisées via la surveillance interne et les infrastructures d’alertes. Ces alertes peuvent survenir en tant qu’alarmes basées sur la signature (par exemple, les programmes malveillants, la détection de l’intrusion) ou via des algorithmes conçus pour profiler l’activité prévue et signaler des anomalies.

### <a name="data-protection-incident-response-drills-testing-of-data-protection-incident-response-plan"></a>Exercices de réponse aux incidents de protection des données, tests du plan de réponse aux incidents de protection des données

En plus de la formation en continu, les services professionnels exécutent chaque année des exercices en partenariat avec les départements internes appropriés en vue de communiquer les procédures de transmission des incidents de protection des données, les rôles et les responsabilités de chacun à tous les membres de l’équipe de stabilisation. Cette formation prépare les principales parties prenantes aux incidents de protection des données réels, que ceux-ci soient de nature sécuritaire, physique ou de confidentialité. Ces exercices s’effectuent notamment avec des représentants de l’équipe de réponse aux incidents de protection des données, de l’équipe de sécurité, des équipes juridiques et de l’équipe de communications.

Suite aux exercices, nous documentons les résultats et les méthodes de résolution que nous avons décidé d’utiliser.

### <a name="data-protection-incident-response-training"></a>Formation à la réponse aux incidents de protection des données

La formation du personnel est un élément clé du processus de réponse aux incidents de protection des données, dans le but de faciliter l’identification et la signalisation des incidents de protection des données. Le personnel des services professionnels est dans l’obligation de suivre une formation qui couvre les principes de base de la confidentialité, la réglementation RGPD et les meilleures pratiques d’identification et de déclaration des incidents de protection des données.

Des sessions de formation en ligne standard sont disponibles et obligatoires pour tous les membres du personnel. Le programme de formation inclut des tests, des enquêtes, des sessions de sensibilisation et un suivi conçu pour assurer que la formation a été comprise et assimilée.

### <a name="process"></a>Processus

Lorsque l’organisation de services professionnels Microsoft identifie un incident de protection des données, elle suit un plan de réponse standard documenté, qui commence par déterminer si les critères d’un incident de protection des données sont satisfaits. Lorsqu’un incident de protection des données survient, il est généralement déclaré immédiatement après le tri mais, en fonction de sa complexité, la déclaration peut se produire dès lors qu’un niveau d’informations nécessaires est disponible, notamment après l’étape d’enquête. D’autre part, l’équipe a la liberté de déclarer un incident de protection des données sur un simple soupçon raisonnable d’occurrence. L’équipe peut également passer d’une étape à l’autre à mesure de l’avancement de l’enquête.

En fonction du niveau de gravité, Microsoft peut aussi effectuer un post-mortem interne pour les incidents de protection des données. Dans le cadre de cet exercice, le niveau suffisant de réponse et les procédures d’exploitation sont évaluées, et les mises à jour pouvant être nécessaires à la *procédure d’exploitation standard de la réponse aux incidents de protection des données* ou des processus associés sont identifiées et mises en œuvre. Les post-mortem internes pour les violations de données sont des enregistrements hautement confidentiels qui ne sont pas accessibles aux clients. Les post-mortem peuvent toutefois être synthétisés et inclus dans des notifications d’événement client. Dans le cadre d’un cycle d’audit de routine, les processus de post-mortem sont vérifiés par des auditeurs externes pour assurer leur suivi.

### <a name="notification"></a>Notification

Lorsque les Services professionnels Microsoft déclarent un incident de protection des données dans le cadre du RGPD, la notification de nos clients dans un délai de 72 heures est notre priorité. 

Une fois qu’un incident de protection des données a été déclaré, le processus de notification s’effectue aussi rapidement que possible, tout en tenant compte des risques d’une progression trop rapide. Pour garantir la remise de la notification, il incombe au client de s’assurer que les informations de contact d’administration sur chaque compte, abonnement et portail de services concerné sont correctes. Bien que l’objectif soit d’offrir aux clients concernés un signalement précis, exploitable et opportun, il se peut que, pour respecter l’engagement des 72 heures, la notification initiale ne comprenne pas nécessairement l’ensemble des détails, certains d’entre eux pouvant ne pas être disponibles lors des phases initiales d’un incident de protection des données. Par ailleurs, Microsoft peut devoir ne pas divulguer certains détails en raison de la nature de l’incident de protection des données. Par exemple, il peut être nécessaire de cacher des détails si le fait de fournir une notification augmente le risque pour d’autres clients ou empêche Microsoft ou les autorités judiciaires d’arrêter un individu malveillant.

En tant que responsable du traitement des données, Microsoft reconnaît que les clients sont responsables de déterminer si une notification est appropriée et, le cas échéant, d’avertir l’autorité de protection des données (DPA) compétente et leurs propres personnes concernées par le traitement des données de toute violation de données personnelles. La division Services professionnels Microsoft fera le nécessaire pour fournir à ses clients les informations requises pour donner suite à la notification dans ces circonstances.

Lors de la notification aux clients d’une violation de données personnelles, Microsoft inclut les informations suivantes, si elles sont applicables et connues :

- Nature de la violation
- Mesures d’atténuation prises ou proposées par Microsoft
- Application, service ou produit concerné
- Durée de l’exposition des données personnelles, si connue
- Volume d’enregistrements de données concerné/exposé, si connu
- Détails sur le responsable du traitement/fournisseur, si associé à la violation

## <a name="learn-more"></a>En savoir plus

En savoir plus sur les Services professionnels Microsoft (<https://aka.ms/pstrust>).

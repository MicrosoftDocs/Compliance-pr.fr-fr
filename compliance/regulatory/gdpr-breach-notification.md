---
title: Notification de violation
description: Découvrez comment les services Microsoft assurent une protection contre les violations de données personnelles, et comment Microsoft réagit et envoie des notifications en cas de violation.
keywords: Microsoft 365, Microsoft 365 Éducation, documentation Microsoft 365, RGPD
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
ms.custom:
- seo-marvel-mar2020
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: f75a8e0f87a5a3e893a296bf487668078b5aef94
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377791"
---
# <a name="gdpr-breach-notification"></a>Notification de violation RGPD

Le règlement général sur la protection des données (RGPD) présente de nouvelles règles pour les organisations qui offrent des produits et des services aux membres de l’Union européenne (UE), ou qui collectent et analysent des données pour les résidents de l’UE quel que soit l’endroit où vous vous trouvez et celui où se trouve votre entreprise. Pour plus de détails, consultez la [rubrique Synthèse RGPD](gdpr.md). Ce document vous permet d’obtenir des informations sur la fin des notifications de violation dans le cadre du RGPD à l’aide des produits et des services Microsoft.

## <a name="what-constitute-a-breach-of-personal-data-under-the-gdpr"></a>Selon le RGPD, qu’est-ce qu’une violation de données personnelles ?

Les données personnelles correspondent aux informations relatives à un individu permettant de l’identifier directement ou indirectement. Une violation de données personnelles correspond à « une violation de la sécurité entraînant la destruction involontaire ou contraire à la loi de données personnelles transmises, stockées ou autrement traitées, ou bien leur perte, modification ou divulgation ou consultation non autorisée ».

## <a name="terminology"></a>Terminologie

Définitions utiles pour les termes RGPD utilisés dans ce document :

- *Contrôleur de données (contrôleur)* : la personne morale, l’autorité publique, le service ou tout autre organisme qui, seul ou conjointement avec d’autres entités, détermine les finalités et les moyens de traitement des données personnelles.  
- *Données personnelles* et *personne concernée* : toutes les informations relatives à une personne physique identifiée ou identifiable (personne concernée); une personne physique identifiable est une personne qui peut être identifiée, directement ou indirectement.  
- *Responsable du traitement* : la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui traite des données à caractère personnel pour le compte de l’entité de contrôle.  
- *Données client* : les données produites et stockées dans les opérations quotidiennes dans le cadre du fonctionnement de votre entreprise.

## <a name="microsoft-and-breach-notification"></a>Microsoft et Notification de violation

Microsoft prend au sérieux les obligations imposées par le Règlement général sur la protection des données (RGPD). Un incident de sécurité ou une violation de données font référence à des événements tels qu’un accès illégal aux données du client stockées sur un équipement Microsoft ou dans des installations Microsoft, ou un accès non autorisé à celles-ci qui peut entraîner la perte, la divulgation ou l’altération des données client.

En tant que responsable du traitement des données, Microsoft s’assure que les clients du service peuvent répondre aux exigences de notification de violation RGPD en tant que contrôleurs de données. Notre notification fournit les informations nécessaires pour effectuer cette évaluation. Microsoft informe les clients de toute divulgation de données personnelle, à l’exception des cas où les données personnelles sont confirmées comme inintelligibles (par exemple, les données chiffrées pour lesquelles l’intégrité des clés est confirmée).

Les contrôleurs de données sont chargés d'évaluer les risques liés à la confidentialité des données et de déterminer si le contrat de traitement des données d’un client doit être notifié en cas de violation. Microsoft fournit les informations requises ainsi que votre stratégie de conformité RGPD pour effectuer cette évaluation.

La notification initiale inclut une description de la nature de la violation, l’impact approximatif de l’utilisateur et la procédure d’atténuation (le cas échéant). Si notre enquête n'est pas terminée au moment de la notification initiale, nous indiquerons les prochaines étapes et le calendrier des communications ultérieures. Pour plus d’informations sur la façon dont Microsoft détecte et répond à une violation des données personnelles, reportez-vous à l’article [Notification des violations de données en vertu du RGPD](https://servicetrust.microsoft.com/ViewPage/GDPRBreach) dans le portail d’approbation de services.

Les détails relatifs à la notification de violation de certains produits et services Microsoft sont indiqués ci-dessous.
  
1. **[Office 365](gdpr-breach-Office365.md)**  
    Microsoft investit massivement dans des systèmes, des processus et du personnel pour réduire le risque de violation de données personnelles et pour détecter rapidement et limiter les conséquences d’une violation dans le cas où elle se produirait. Pour plus de détails, consultez la rubrique [Investissements d’Office 365 dans la sécurité des données](/microsoft-365/compliance/gdpr-breach-office365#office-365-investments-in-data-security).

    Il se peut qu’un client soit informé d’une violation et qu’il souhaite contacter Microsoft. Dans ce cas, contactez le Support Microsoft, qui interviendra avec les équipes d’ingénieurs pour obtenir plus d’informations.

2. **[Azure, Dynamics 365 & Windows](gdpr-breach-azure-dynamics-windows.md)** Microsoft dispose d'un service mondial de réponse aux incidents, disponible à tout moment des 24 heures et des 7 jours. Il s'efforce d'atténuer les effets des attaques contre la configuration des processeurs de données de diagnostic de Microsoft Azure, de Dynamics 365 et de Windows.

    - *Détection des violations* : étant donné que Microsoft et le client ont des obligations en matière de sécurité, les services Azure utilisent un modèle de responsabilité partagée pour définir la sécurité et les responsabilités opérationnelles. Microsoft ne surveille pas les incidents de sécurité relevant de la responsabilité du client et n'intervient pas dans de tels cas. L’intervention en cas d’incidents du client peut impliquer une collaboration avec [le support client Azure](https://azure.microsoft.com/support/options/) sous réserve de contrats de services appropriés. Microsoft Azure offre également différents services (par exemple, [Azure Security Center](https://azure.microsoft.com/services/security-center/)) que les clients peuvent utiliser pour développer et gérer les réponses aux incidents de sécurité.

        Pour obtenir la liste des événements déclenchant une enquête sur la violation dans Microsoft Azure, consultez la rubrique [Détection de violations potentielles](/microsoft-365/compliance/gdpr-breach-azure-dynamics#detection-of-potential-breaches). La rubrique [Azure et notification de violation en vertu du RGPD](gdpr-breach-azure-dynamics-windows.md) donne des détails supplémentaires sur la façon dont Microsoft examine, gère et répond aux incidents de sécurité dans Azure.

    - *Réponse à la violation de données* : Microsoft détermine les niveaux de priorité et de gravité appropriés d’une violation en examinant l’impact fonctionnel, la récupérabilité et l’impact sur les informations de l’incident. La priorité et la gravité peuvent changer au cours des enquêtes, sur la base de nouveaux résultats et conclusions.
    L’équipe en charge de la sécurité de Microsoft travaille étroitement avec des conseillers juridiques mondiaux afin de garantir l’exécution d’une enquête conforme aux obligations légales et aux engagements envers les clients. Ces processus sont détaillés dans la [Réponse d’Azure à une violation des données](/microsoft-365/compliance/gdpr-breach-azure-dynamics#azures-data-breach-response).

    - *Notification du client* : Microsoft Azure informe les clients et les autorités de réglementation des violations de données, le cas échéant. Les notifications du client sont livrées dans un délai maximal de 72 heures à partir du moment où nous avons déclaré une violation, sauf dans les cas suivants :

        - Microsoft estime que l’envoi d’une notification augmente le risque pour d’autres clients.
        - Le délai de 72 heures peut laisser certains détails sur l'incident disponibles. Ces détails-ci vous sont fournis à mesure que l’enquête est menée.

        Pour plus d’informations, consultez la [Notification du client](/microsoft-365/compliance/gdpr-breach-azure-dynamics#customer-notification).

3. **[Support Microsoft et services professionnels](gdpr-breach-Microsoft-Support-Professional-Services.md)**  
    En raison de la nature des services professionnels, certains incidents liés à la protection des données peuvent relever de la responsabilité du client. Lorsque les services professionnels Microsoft identifient un incident lié à la protection des données, il suit le plan de réponse standard documenté de l'industrie tel que décrit dans la rubrique [Étendue et limites du processus de réponse aux incidents de protection des données](/microsoft-365/compliance/gdpr-breach-microsoft-support-professional-services#scope--limits-of-data-protection-incident-response-process).

## <a name="breach-notification-admin-tools"></a>Outils d’administration de la notification de violation

- **Définir le contact de votre organisation en matière de confidentialité** Les administrateurs de locataire peuvent utiliser le [portail d’administration Azure Active Directory](https://go.microsoft.com/fwlink/p/?linkid=2052736) pour définir le contact de confidentialité de votre organisation dont Microsoft a besoin pour communiquer avec eux.

## <a name="learn-more"></a>En savoir plus

- [Centre de gestion de la confidentialité Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)

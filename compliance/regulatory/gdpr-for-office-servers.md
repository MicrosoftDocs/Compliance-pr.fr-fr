---
title: RGPD pour les serveurs Office
description: Découvrez comment répondre aux exigences en matière de Règlement général sur la protection des données (RGPD) dans les serveurs locaux d’Office.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.collection: MS-Compliance
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: 58f3d9108fe36175c2ce879054a35c2cc94d93c8
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496078"
---
# <a name="gdpr-for-office-on-premises-servers"></a>RGPD pour les serveurs Office locaux

Le Règlement général sur la protection des données (RGPD) présente les exigences que doivent respecter les organisations pour protéger les données personnelles et répondre aux demandes de personnes concernées de façon appropriée. Cette série d’articles présente les approches recommandées pour les charges de travail locales :

- [SharePoint Server](gdpr-for-sharepoint-server.md)

- [Exchange Server](gdpr-for-exchange-server.md)

- [Skype Entreprise Server](gdpr-for-skype-for-business-server.md)

- [Project Server](gdpr-for-project-server.md)

- [Office Web Apps Server et Office Online Server](gdpr-for-office-online-server.md)

- [Partages de fichiers en local](gdpr-for-on-premises-file-shares.md)

Pour plus d’informations sur le RGPD et sur l’aide que peut vous apporter Microsoft, reportez-vous au [centre de gestion de la confidentialité](https://www.microsoft.com/trust-center/privacy/gdpr-overview
).

Avant d’entreprendre toute action concernant des données locales, consultez vos équipes juridiques et de conformité pour leur demander conseil et pour en savoir plus sur les schémas de classification existants et les approches en matière d’utilisation de données personnelles. Microsoft fournit des recommandations pour développer et améliorer les schémas de classification dans son Kit de détection de données du RGPD à l’adresse [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>). Ce kit décrit également les approches possibles pour déplacer des données locales vers le cloud, dans lequel vous pouvez utiliser des fonctionnalités de gouvernance des données plus avancées si vous le souhaitez. Les articles de cette section fournissent des recommandations pour les données qui sont destinées à rester au niveau local.

L’illustration suivante regroupe les fonctionnalités que nous vous recommandons d’utiliser pour chacune des charges de travail suivantes afin de repérer, classer, protéger et surveiller les données personnelles. Consultez les articles de cette section pour obtenir plus d’informations.

![Diagramme décrivant les fonctionnalités de découverte, de classement, de protection et de surveillance des données personnelles dans les charges de travail](../media/gdpr-for-office-servers-image1.png)

## <a name="illustration-description"></a>Description de l’illustration

Concernant l’accessibilité, le tableau suivant fournit les mêmes exemples dans l’illustration.

****

|Action|Partages de fichiers Windows Server|SharePoint Server|Exchange Server|Skype Entreprise|Project Server|
|---|---|---|---|---|---|
|Découvrir|Scanneur Azure Information Protection<sup>\*</sup>|Centre de recherche ou eDiscovery (une fois les données classées) <br/><br/> Scanneur Azure Information Protection<sup>\*</sup>|Portail eDiscovery Exchange|Portail eDiscovery Exchange|Scripts SQL de découverte et d’exportation|
|Classer|Scanneur Azure Information Protection<sup>\*</sup> <br/><br/> Types d'informations sensibles Office 365|Scanneur Azure Information Protection<sup>\*</sup> <br/><br/> Types d'informations sensibles Office 365|Balises et stratégies de rétention Exchange|Balises et stratégies de rétention Exchange||
|Protéger||Règles de protection contre la perte de données Exchange Server <br/><br/> Autorisations, protection par IRM pour les bibliothèques|Règles de protection contre la perte de données Exchange Server <br/><br/> Intégration IRM à Exchange Server|||
|Surveiller|Intégrer des outils SIEM aux journaux|Intégrer des outils SIEM aux journaux|Intégrer des outils SIEM aux journaux|Intégrer des outils SIEM aux journaux|Intégrer des outils SIEM aux journaux|
|

<sup>\*</sup>Veuillez noter qu’une protection chiffre le fichier. Cela empêche SharePoint Server de trouver les types d’informations sensibles dans les fichiers protégés.

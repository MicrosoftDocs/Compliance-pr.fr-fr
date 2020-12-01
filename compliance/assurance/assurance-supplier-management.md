---
title: Présentation de la gestion des fournisseurs
description: En savoir plus sur la gestion des fournisseurs dans Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH'
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: e46a7d2121a3ed1f314a3126c51911248362ff59
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507276"
---
# <a name="supplier-management-overview"></a>Présentation de la gestion des fournisseurs

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>Comment Microsoft gère-t-il les risques liés aux fournisseurs ?

Microsoft collabore avec des sociétés tierces pour répondre aux besoins de nos clients. Ces sociétés tierces sont qualifiées de fournisseurs ou de sous-traitants. La sécurité et la confidentialité des fournisseurs de Microsoft sont régies par notre [programme de sécurité et de garantie de la confidentialité (qualité de l’assurance-vie privée)](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6), un ensemble d’exigences à l’échelle de l’entreprise pour tous les fournisseurs qui s’associent à Microsoft pour proposer nos services en ligne. Bien que le programme de la SSPA offre une gouvernance et une gestion complètes de notre base de fournisseurs, les divisions individuelles, telles que Microsoft 365, peuvent conserver des exigences supplémentaires pour leurs fournisseurs.

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>Comment le programme de sécurité et de confidentialité des fournisseurs de Microsoft protège-t-il les données client ?

La SSPA est un partenariat entre l’approvisionnement Microsoft, les affaires externes et juridiques de l’entreprise, et la sécurité de l’entreprise pour s’assurer que les fournisseurs respectent les principes de confidentialité et de sécurité de Microsoft. L’étendue de la SSPA couvre tous les fournisseurs qui traitent des données personnelles ou des données confidentielles Microsoft. L’adhésion au programme de la SSPA inclut le respect des exigences de la protection des données de Microsoft (DPR). Le DPR comprend les contrôles de sécurité et de confidentialité que les fournisseurs doivent mettre en œuvre avant de commencer à travailler avec Microsoft. Tous les fournisseurs signés s’auto-attestent de la conformité avec le DPR annuellement.

Les exigences de DPR sont étendues en fonction de six catégories de traitement des données distinctes pour lesquelles un fournisseur peut être approuvé dans le cadre de leur inscriptions dans la SSPA. Ces catégories permettent d’identifier les risques associés aux services fournis par un fournisseur à Microsoft. Le profil de traitement des données du fournisseur détermine les contrôles DPR considérés comme étant inclus dans la protection des données. Les fournisseurs qui traitent les données considérées comme un risque plus élevé doivent être conformes à toutes les exigences d’DPR et peuvent également avoir besoin de vérifier la conformité de manière indépendante. Les outils d’achat Microsoft valident l’état de la SSPA pour tous les fournisseurs, y compris la conformité avec les parties applicables du DPR, avant d’autoriser l’approvisionnement de ce fournisseur.

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>Quels types de sous-processus fournissent des services pour Microsoft ?

Un « sous-traitant » est un tiers que Microsoft engage dont les tâches incluent le traitement des données personnelles Microsoft pour lesquelles Microsoft est un processeur. Les sous-processeurs de Microsoft se répartissent en trois catégories distinctes. Chacun doit prouver la conformité avec la SSPA avant de pouvoir traiter les données client au nom de Microsoft.

- **Les technologies** sous-processus fournissent des technologies utilisées pour fournir des services en ligne Microsoft spécifiques. Si un client déploie l’un de ces services, les sous-processeurs identifiés pour ce service peuvent traiter, stocker ou accéder à des données personnelles ou des données personnelles tout en aidant à fournir ce service.
- Les sous-processus **connexes** fournissent des services qui prennent en charge, exploitent et gèrent les services en ligne. Si un client déploie l’un de ces services, les sous-processus identifiés peuvent traiter, stocker ou accéder à des données personnelles ou des données clientes limitées tout en fournissant leurs services auxiliaires.
- Les sous-processus d' **augmentation du personnel** prennent deux formes différentes : dans les deux scénarios, les données personnelles ne résident que dans des installations Microsoft, sur les systèmes Microsoft, et sont soumises aux stratégies et à la surveillance de Microsoft.

    - La première forme de l’augmentation du personnel fournit une équipe qui prend en charge, opère et gère les services Microsoft Online. Lorsque vous comblez leurs responsabilités, ces sous-processus peuvent être exposés à des données client ou à des données personnelles. Par exemple, un sous-processus peut effectuer un dépannage à distance sur un serveur Microsoft, tandis que cela peut être exposé aux extraits de données client dans un journal de vidage de blocage de serveur.
    - La deuxième forme de l’augmentation du personnel implique des sous-processus qui travaillent en parallèle avec les employés à plein temps de Microsoft pour prendre en charge, exploiter et gérer Microsoft Online Services. Ces sous-traites peuvent être exposés à des données par pseudonyme dans le cadre de leur travail parallèle aux employés à temps plein de Microsoft.

Des techniques et des sous-processus complémentaires sont nécessaires pour implémenter les contrôles d’accès conformément aux exigences de Microsoft en matière de protection des données (DPR). Ces exigences respectent ou dépassent les engagements contractés par Microsoft auprès de ses clients dans les conditions de service en ligne (OST). Les fournisseurs qui effectuent des tâches d’augmentation du personnel sont soumis aux mêmes contrôles d’accès en place pour les employés à plein temps de Microsoft.

## <a name="how-does-microsoft-onboard-suppliers"></a>Comment Microsoft a-t-il intégré les fournisseurs ?

Les fournisseurs tiers sont tenus de signer un accord maître Microsoft dans le cadre du processus d’intégration. Le présent contrat régit la relation entre Microsoft et ses fournisseurs et garantit une gestion cohérente des relations des fournisseurs. Dans le cadre de l’intégration, les fournisseurs s’inscrivent au sein de la SSPA et doivent remplir toutes les conditions requises pour pouvoir être approuvés pour toute catégorie de traitement des données. Les unités d’entreprise Microsoft peuvent uniquement créer des engagements avec des fournisseurs lorsque l’activité de traitement des données pour l’engagement correspond aux catégories de traitement des données pour lesquelles le fournisseur a été approuvé.

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>Comment Microsoft informe-t-il les clients des modifications apportées aux fournisseurs qui traitent leurs données ?

Par le Microsoft Online Service Data Protection Addendum (DPA), Microsoft fait des engagements supplémentaires concernant les périodes de préavis pour l’ajout de n’importe quel sous-processeur. Les délais d’expiration des notifications dépendent du type de données traitées par le sous-processus au nom de Microsoft. Comme indiqué dans le DPA, Microsoft s’engage à fournir des avis aux clients au moins six mois avant la mise en place d’un nouveau sous-processus qui traitera les données client. Pour toutes les autres données personnelles, Microsoft fournira au moins 30 jours de notification. Notification est fournie par la mise à jour de la liste de sous- [traités Microsoft Online Services](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=926b2cf5-6b6e-43ca-9bc3-f73e961aad5f&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List).

## <a name="related-external-regulations--certifications"></a>Certifications & des réglementations externes connexes

Les services en ligne de Microsoft sont régulièrement vérifiés pour la conformité aux réglementations et aux certifications externes. Reportez-vous au tableau ci-dessous pour valider les contrôles liés à la gestion des fournisseurs.

| **Audits externes** | **Section** | **Date du dernier rapport** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CA-3 : interconnexions système <br> IA-4 : gestion des identificateurs <br> PS-6 : accords d’accès <br> PS-7 : sécurité du personnel tiers <br> SA-4 : processus d’acquisitions <br> SA-9 : services du système d’information externe <br> SA-12 : protection de la chaîne d’approvisionnement | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 15.1 : sécurité des informations dans les relations avec les fournisseurs | 22 février 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 15.1 : sécurité des informations dans les relations avec les fournisseurs | 22 février 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A. 8.1 : divulgation du traitement des données personnelles sous-traitées | 30 septembre 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-53 : analyse de tiers | 30 septembre 2019 |

## <a name="resources"></a>Ressources

- [Programme de confidentialité et d’assurance de la sécurité des fournisseurs](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)

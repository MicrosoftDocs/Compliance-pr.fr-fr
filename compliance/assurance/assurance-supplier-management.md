---
title: Aperçu sur la gestion des fournisseurs
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
ms.openlocfilehash: 4da4775332989c4a40738777dfae7318e27086f0
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787373"
---
# <a name="supplier-management-overview"></a>Aperçu sur la gestion des fournisseurs

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>Comment Microsoft gère-t-il les risques liés aux fournisseurs ?

Microsoft s’associe à des sociétés tierces pour répondre aux besoins de nos clients. Ces sociétés tierces sont appelées fournisseurs ou sous-traitants. La sécurité et la confidentialité des fournisseurs chez Microsoft sont régies par notre programme [DSPA (Supplier Security and Privacy Assurance),](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)un ensemble d’exigences à l’échelle de l’entreprise pour tous les fournisseurs qui s’associent à Microsoft pour fournir nos services en ligne. Bien que le programme SSPA offre une gouvernance et une gestion complètes de notre base de fournisseurs, les unités commerciales individuelles, telles que Microsoft 365, peuvent maintenir des exigences supplémentaires pour leurs fournisseurs.

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>Comment le programme DSPA (Supplier Security and Privacy Assurance) de Microsoft protège-t-il les données client ?

La SSPA est un partenariat entre Microsoft Achat, Affaires juridiques et externes de l’entreprise et Sécurité d’entreprise pour s’assurer que les fournisseurs respectent les principes de confidentialité et de sécurité de Microsoft. L’étendue de la SSPA couvre tous les fournisseurs qui traitent des données personnelles ou des données confidentielles Microsoft. L’inscription au programme SSPA inclut le respect des exigences de Protection des données (DPR) de Microsoft. Le DPR se compose de contrôles de sécurité et de confidentialité que les fournisseurs doivent implémenter avant de commencer à travailler avec Microsoft. Tous les fournisseurs inscrits s’certifient eux-mêmes de la conformité avec le DPR annuellement.

Les exigences de DPR sont limitées en fonction de six catégories de traitement de données distinctes pour qui un fournisseur peut être approuvé dans le cadre de son inscription à la SSPA. Ces catégories sont utilisées pour identifier le risque associé aux services qu’un fournisseur fournit à Microsoft. Le profil de traitement des données du fournisseur détermine quels contrôles de DPR sont considérés comme étant dans l’étendue pour fournir une protection appropriée des données. Les fournisseurs qui traitées des données considérées comme à risque plus élevé doivent se conformer à toutes les exigences de DPR et peuvent également avoir besoin de fournir une vérification indépendante de la conformité. Les outils d’achat Microsoft valident l’état de la SSPA de tous les fournisseurs, y compris la conformité avec les parties applicables du DPR, avant d’autoriser l’approvisionnement de ce fournisseur.

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>Quels types de sous-traitants fournissent des services à Microsoft ?

Un « sous-traitant » est un tiers que Microsoft engage, dont les tâches incluent le traitement des données personnelles Microsoft pour lesquelles Microsoft est un sous-traitant. Les sous-traitants de Microsoft se distinguent par trois catégories distinctes. Chacun d’eux doit démontrer la conformité avec la SSPA avant de pouvoir traiter les données client au nom de Microsoft.

- **Les technologies** sous-processus fournissent des technologies utilisées pour fournir des services en ligne Microsoft spécifiques. Si un client déploie l’un de ces services, les sous-traitants identifiés pour ce service peuvent traiter, stocker ou accéder à des données client ou à des données personnelles tout en aidant à fournir ce service.
- **Les sous-traitants auxiliaires** fournissent des services qui assurent la prise en charge, l’exploitation et la maintenance des services en ligne. Si un client déploie l’un de ces services, les sous-traitants identifiés peuvent traiter, stocker ou accéder à des données client limitées ou à des données personnelles tout en fournissant leurs services auxiliaires.
- **Les** sous-processus d’augmentation du personnel prennent deux formes différentes : dans les deux scénarios, les données personnelles résident uniquement dans les installations de Microsoft, sur les systèmes Microsoft et sont soumises aux stratégies et à la supervision de Microsoft.

    - La première forme de l’augmentation du personnel fournit une équipe qui prend en charge, opère et gère les services Microsoft Online. Lorsque vous comblez leurs responsabilités, ces sous-processus peuvent être exposés à des données client ou à des données personnelles. Par exemple, un sous-processus peut effectuer un dépannage à distance sur un serveur Microsoft, tandis que cela peut être exposé aux extraits de données client dans un journal de vidage de blocage de serveur.
    - La deuxième forme d’augmentation du personnel implique des sous-traitants qui travaillent côte à côte avec les employés à plein temps de Microsoft pour prendre en charge, exploiter et gérer les services en ligne Microsoft. Ces sous-traites peuvent être exposés à des données par pseudonyme dans le cadre de leur travail parallèle aux employés à temps plein de Microsoft.

La technologie et les sous-processus auxiliaires sont requis pour implémenter des contrôles d’accès conformes aux exigences de Protection des données (DPR) de Microsoft. Ces exigences respectent ou dépassent les engagements contractuels que Microsoft prend à l’égard de ses clients dans les conditions d’ost (Online Service Terms). Les fournisseurs qui effectuent des opérations d’augmentation du personnel sont soumis aux mêmes contrôles d’accès en place pour les employés à plein temps de Microsoft.

## <a name="how-does-microsoft-onboard-suppliers"></a>Comment Microsoft intégrera-t-il les fournisseurs ?

Les fournisseurs tiers doivent signer un contrat maître Microsoft dans le cadre du processus d’intégration. Cet accord régit la relation entre Microsoft et ses fournisseurs et garantit une gestion cohérente des relations avec les fournisseurs. Dans le cadre de l’intégration, les fournisseurs s’inscrivent à la SSPA et doivent remplir toutes les conditions requises avant de pouvoir être approuvés pour toutes les catégories de traitement des données. Les unités commerciales Microsoft peuvent uniquement créer des engagements avec des fournisseurs lorsque l’activité de traitement des données pour l’engagement correspond aux catégories de traitement des données pour lesquelles le fournisseur a été approuvé.

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>Comment Microsoft informe-t-il les clients des modifications apportées aux fournisseurs qui traitées leurs données ?

Selon la DPA (Microsoft Online Service Data Protection Addendum), Microsoft prend des engagements supplémentaires concernant les périodes de préavis pour l’ajout de tout sous-traitant. Notez que les délais dépendent du type de données que le sous-traitant traitera pour le compte de Microsoft. Comme indiqué dans la DPA, Microsoft s’engage à fournir une notification aux clients au moins six mois avant tout nouveau sous-traitant qui traitera les données client. Pour toutes les autres données personnelles, Microsoft fournit au moins 30 jours de préavis. L’avis est fourni par la mise à jour de la [Microsoft Online Services liste des sous-traitants.](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=926b2cf5-6b6e-43ca-9bc3-f73e961aad5f&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List)

## <a name="related-external-regulations--certifications"></a>Réglementations externes associées & certifications

Les services en ligne de Microsoft sont régulièrement audités pour assurer la conformité avec les réglementations et certifications externes. Reportez-vous au tableau ci-dessous pour la validation des contrôles liés à la gestion des fournisseurs.

| **Audits externes** | **Section** | **Date de rapport la plus récente** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CA-3 : Interconnexions système <br> IA-4 : gestion des identificateurs <br> PS-6 : accords d’accès <br> PS-7 : sécurité du personnel tiers <br> SA-4 : processus d’acquisition <br> SA-9 : services de système d’information externe <br> SA-12 : Protection de la chaîne d’approvisionnement | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1 : Sécurité des informations dans les relations avec les fournisseurs | 22 février 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1 : Sécurité des informations dans les relations avec les fournisseurs | 22 février 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A.8.1 : Divulgation du traitement des informations d’pii sous-traitées | 24 décembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-53 : surveillance tierce | 24 décembre 2020 |

## <a name="resources"></a>Ressources

- [Programme d’assurance et de confidentialité de la sécurité des fournisseurs](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)

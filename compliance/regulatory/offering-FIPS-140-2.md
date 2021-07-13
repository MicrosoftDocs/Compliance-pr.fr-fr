---
title: Publication FIPS (Federal Information Processing Standard) 140-2
description: Microsoft certifie que ses modules de chiffrement sont conformes à la norme de traitement des informations fédérales des États-Unis.
keywords: Offres pour la conformité Microsoft 365
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 2c51979122aaedda90bac74740e95c9d1265de74
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385004"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>Publication FIPS (Federal Information Processing Standard) 140-2

## <a name="fips-140-2-standard-overview"></a>Vue d’ensemble de la norme FIPS 140-2

La publication FIPS (Federal Information Processing Standard) 140-2 est une norme gouvernementale américaine qui définit les exigences de sécurité minimales pour les modules de chiffrement dans les produits informatiques, comme défini à la section 5131 de la loi de 1996 sur la réforme de la gestion des technologies de l’information.

Le Programme de validation de [module](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) de chiffrement (CMVP), un effort conjoint du National Institute of Standards and Technology (NIST) des États-Unis et du Centre canadien pour la cybersécurité (VPNS), valide les modules de chiffrement selon la norme Security *Requirements for Cryptographic Modules* (par exemple, FIPS 140-2) et les normes de chiffrement FIPS associées. Les exigences de sécurité FIPS 140-2 couvrent 11 domaines liés à la conception et à l’implémentation d’un module de chiffrement. Le Laboratoire des technologies de l’information du NIST exploite un programme connexe qui valide les algorithmes de chiffrement approuvés par la FIPS dans le module.

## <a name="microsofts-approach-to-fips-140-2-validation"></a>Approche de Microsoft pour la validation FIPS 140-2

Microsoft s’engage activement à répondre aux exigences 140-2, ayant validé les modules de chiffrement depuis la création de la norme en 2001. Microsoft valide ses modules de chiffrement dans le cadre [](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) du Programme de validation de module de chiffrement (CMVP) du National Institute of Standards and Technology (NIST). Plusieurs produits Microsoft, y compris de nombreux services cloud, utilisent ces modules de chiffrement.

Pour plus d’informations techniques sur les modules de chiffrement Microsoft Windows, la stratégie de sécurité pour chaque module et le catalogue de détails de certificat CMVP, voir le contenu WINDOWS et [Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plateformes cloud microsoft dans l’étendue & services

Alors que les recommandations d’implémentation FIPS 140-2 CMVP actuelles empêchent une validation FIPS 140-2 pour un service cloud lui-même ; Les fournisseurs de services cloud peuvent choisir d’obtenir et d’exploiter des modules de chiffrement validés PAR LA FIPS 140 pour les éléments informatiques qui composent leur service cloud. Les services en ligne Microsoft qui incluent des composants, qui ont été validés par la fiPS 140-2, incluent, entre autres :

- Azure et Azure Government
- Dynamics 365 et Dynamics 365 Government
- Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense

## <a name="azure-dynamics-365-and-fips-140-2"></a>Azure, Dynamics 365 et FIPS 140-2

Pour plus d’informations sur Azure, Dynamics 365 et d’autres services en ligne, voir l’offre [FiPS 140-2 Azure.](/azure/compliance/offerings/offering-fips-140-2)

## <a name="office-365-and-fips-140-2"></a>Office 365 et FIPS 140-2

### <a name="office-365-cloud-environments"></a>Office 365 cloud

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 applicabilité et services dans l’étendue

Utilisez le tableau suivant pour déterminer l’applicabilité de vos services Office 365 et de votre abonnement :

| **Applicabilité** | **Services dans l’étendue** |
|:------------------|:----------------------|
| Office 365, Cloud de la communauté du secteur public, Cloud de la communauté du secteur public High, DoD | Voir [Validation FIPS 140-2](/windows/security/threat-protection/fips-140-validation) |

### <a name="frequently-asked-questions"></a>Questions fréquemment posées

**Quelle est la différence entre « FIPS 140 Validé » et « FiPS 140 conforme » ?**

« FIPS 140 Validé » signifie que le module de chiffrement, ou un produit qui incorpore le module, a été validé (« certifié » par le CMVP pour répondre aux exigences FIPS 140-2. La « conformité FIPS 140 » est un terme du secteur pour les produits it qui s’appuient sur les produits validés FIPS 140 pour la fonctionnalité de chiffrement.

**Quand Microsoft entre-t-il en validation FIPS 140 ?**

La cadence de démarrage d’une validation de module s’aligne sur les mises à jour de fonctionnalités de Windows 10 et Windows Server. Au fil de l’évolution du secteur logiciel, les systèmes d’exploitation sont publiés plus fréquemment, avec des mises à jour logicielles mensuelles. Microsoft s’engage à valider les fonctionnalités publiées, mais entre les deux, cherche à minimiser les modifications apportées aux modules de chiffrement.

**Quels ordinateurs sont inclus dans une validation FIPS 140 ?**

Microsoft valide les modules de chiffrement sur un échantillon représentatif de configurations matérielles Windows 10 et Windows Server. Il est courant que le secteur accepte cette validation FIPS 140-2 lorsqu’un environnement utilise du matériel, ce qui est similaire aux exemples utilisés pour le processus de validation.

**De nombreux modules sont répertoriés sur le site web NIST. Comment savoir laquelle s’applique à mon agence ?**

Si vous devez utiliser des modules de chiffrement validés via FIPS 140-2, vous devez vérifier que la version que vous utilisez apparaît dans la liste de validation. Le CMVP et Microsoft conservent une liste de modules de chiffrement validés, organisés par version de produit, ainsi que des instructions pour identifier les modules installés sur un système Windows. Pour plus d’informations sur la configuration de systèmes conformes, voir le contenu [Windows et Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**Que signifie « Lorsqu’il est géré en mode FIPS » sur un certificat ?**

Cette mise en garde informe le lecteur que les règles de configuration et de sécurité requises doivent être suivies pour utiliser le module de chiffrement d’une manière cohérente avec sa stratégie de sécurité FIPS 140-2. Chaque module possède sa propre stratégie de sécurité (spécification précise des règles de sécurité sous lesquelles il fonctionnera) et utilise des algorithmes de chiffrement approuvés, la gestion des clés de chiffrement et des techniques d’authentification. Les règles de sécurité sont définies dans la stratégie de sécurité pour chaque module. Pour plus d’informations, y compris des liens vers la stratégie de sécurité pour chaque module validé par le biais du CMVP, voir le contenu Windows et [Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**FedRAMP nécessite-t-il la validation FIPS 140-2 ?**

Oui, le Programme de gestion des risques et d’autorisations (FedRAMP) s’appuie sur les lignes de base de contrôle définies par le [NIST SP 800-53 Revision 4,](https://nvd.nist.gov/800-53/Rev4/)y compris la protection cryptographique [SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) qui impose l’utilisation du chiffrement validé par fiPS ou du chiffrement approuvé par la NSA.

**Puis-je utiliser l’adhésion de Microsoft à FIPS 140-2 dans le processus de certification de mon agence ?**

Pour se conformer à fiPS 140-2, votre système doit être configuré pour s’exécuter dans un mode de fonctionnement approuvé PAR FIPS, ce qui inclut la garantie qu’un module de chiffrement utilise uniquement les algorithmes approuvés par FIPS. Pour plus d’informations sur la configuration de systèmes conformes, voir le contenu [Windows et Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**Quelle est la relation entre fiPS 140-2 et critères communs ?**

Il s’existe deux normes de sécurité distinctes à des fins différentes, mais complémentaires. FIPS 140-2 est conçu spécifiquement pour valider les modules de chiffrement logiciels et matériels, tandis que les critères communs sont conçus pour évaluer les fonctions de sécurité dans les logiciels informatiques et les produits matériels. Les évaluations de critères courants s’appuient souvent sur les validations FIPS 140-2 pour garantir que la fonctionnalité de chiffrement de base est correctement implémentée.

### <a name="resources"></a>Ressources

- [Exigences de sécurité fiPS Pub 140-2 pour les modules de chiffrement](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [Programme de validation de module de chiffrement NIST](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows, Windows Server et FIPS 140-2](/windows/security/threat-protection/fips-140-validation)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)

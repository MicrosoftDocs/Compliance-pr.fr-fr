---
title: Publication 140-2 (Federal Information Processing Standard)
description: Microsoft certifie que ses modules de chiffrement sont conformes à la norme américaine Federal Information Processing Standard.
keywords: Offres pour la conformité Microsoft 365
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
ms.openlocfilehash: 4555553c4da1bece5e27f0905aa60504102b1eb1
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506768"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>Publication 140-2 (Federal Information Processing Standard)

## <a name="fips-140-2-standard-overview"></a>Vue d’ensemble de la norme FIPS 140-2

La publication 140-2 FIPS (Federal Information Processing Standard) est une norme de gouvernement américain qui définit les exigences minimales de sécurité pour les modules de chiffrement dans les produits informatiques, comme défini dans la section 5131 de la réforme de l’information sur la gestion des technologies de l’information de 1996.

Le [programme de validation du module de chiffrement](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVp), un effort commun de l’Institut NIST (National Institute of Standards and Technology) et le Centre canadien pour la sécurité informatique (CCCS), valide les modules de chiffrement aux *exigences de sécurité pour les modules de chiffrement* standard (par exemple, FIPS 140-2) et les normes de chiffrement FIPS associées. Les exigences de sécurité FIPS 140-2 couvrent 11 domaines liés à la conception et l’implémentation d’un module de chiffrement. Le laboratoire NIST Information Technology opère un programme connexe qui valide les algorithmes de chiffrement approuvés FIPS dans le module.

## <a name="microsofts-approach-to-fips-140-2-validation"></a>Approche de Microsoft pour la validation FIPS 140-2

Microsoft entretient un engagement actif pour répondre aux exigences 140-2, avec des modules de chiffrement validés depuis le début de la norme dans 2001. Microsoft valide ses modules cryptographiques dans le cadre du [programme de validation du module de chiffrement](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) NIST (National Institute of Standards and Technology) (CMVp). Plusieurs produits Microsoft, y compris de nombreux services Cloud, utilisent ces modules de chiffrement.

Pour obtenir des informations techniques sur les modules de chiffrement Microsoft Windows, la stratégie de sécurité pour chaque module et le catalogue des détails du certificat CMVP, consultez la rubrique [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).

## <a name="microsoft-in-scope-cloud-services"></a>Services Cloud Microsoft concernés

Alors que le Guide d’implémentation actuel de CMVP FIPS 140-2 exclut une validation FIPS 140-2 pour un service Cloud lui-même ; les fournisseurs de services Cloud peuvent choisir d’obtenir et d’utiliser des modules de chiffrement validés FIPS 140 pour les éléments informatiques qui composent leur service Cloud. Les services Microsoft Online qui incluent des composants, qui ont été validés par FIPS 140-2 incluent, entre autres :

- [Azure et Azure Government](https://docs.microsoft.com/azure/azure-government/documentation-government-plan-security)
- [Dynamics 365 et Dynamics 365 Government](https://docs.microsoft.com/microsoft-365/compliance/office-365-encryption-in-microsoft-dynamics-365)
- [Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense](https://docs.microsoft.com/microsoft-365/compliance/office-365-encryption-risks-and-protections)

## <a name="frequently-asked-questions"></a>Foire aux questions

**Quelle est la différence entre « FIPS 140 Valided » et « FIPS 140 compatible » ?**

« FIPS 140 validée » signifie que le module de chiffrement, ou un produit qui incorpore le module, a été validé (« certifié ») par le CMVP en tant que répondant aux exigences FIPS 140-2. « FIPS 140 compatible » est un terme industriel pour les produits informatiques qui s’appuient sur des produits validés FIPS 140 pour les fonctionnalités cryptographiques.

**Quand Microsoft engage-t-il une validation FIPS 140 ?**

La cadence de démarrage d’une validation de module s’aligne sur les mises à jour des fonctionnalités de Windows 10 et Windows Server. À mesure que l’industrie logicielle a évolué, les systèmes d’exploitation sont publiés plus fréquemment, avec des mises à jour logicielles mensuelles. Microsoft s’efforce de valider les versions de fonctionnalité, mais entre les versions, vise à réduire les modifications apportées aux modules de chiffrement.

**Quels ordinateurs sont inclus dans une validation FIPS 140 ?**

Microsoft valide les modules de chiffrement sur un échantillon représentatif de configurations matérielles exécutant Windows 10 et Windows Server. Il est pratique commune d’accepter cette validation FIPS 140-2 lorsqu’un environnement utilise du matériel, ce qui est similaire aux exemples utilisés pour le processus de validation.

**Un grand nombre de modules sont répertoriés sur le site Web NIST. Comment savoir quel est celui qui s’applique à mon agence ?**

Si vous devez utiliser des modules de chiffrement validés via FIPS 140-2, vérifiez que la version que vous utilisez apparaît dans la liste validation. Le CMVP et Microsoft gèrent une liste de modules de chiffrement validés, organisés par version de produit, ainsi que des instructions pour l’identification des modules installés sur un système Windows. Pour plus d’informations sur la configuration des systèmes de façon à ce qu’ils soient conformes, consultez le [contenu Windows et Windows Server FIPS 140-2](https://aka.ms/AA6ehud).

**Qu’est-ce que’quand fonctionne en mode FIPS’signifie sur un certificat ?**

Ce inconvénient informe le lecteur que les règles de configuration et de sécurité requises doivent être suivies pour utiliser le module de chiffrement de manière cohérente avec sa stratégie de sécurité 140-2 FIPS. Chaque module possède sa propre stratégie de sécurité, une spécification précise des règles de sécurité sous lesquelles elle fonctionne, et utilise des algorithmes de chiffrement approuvés, la gestion de clés de chiffrement et les techniques d’authentification. Les règles de sécurité sont définies dans la stratégie de sécurité pour chaque module. Pour plus d’informations, notamment des liens vers la stratégie de sécurité pour chaque module validé via le CMVP, voir le [contenu Windows et Windows Server FIPS 140-2](https://aka.ms/AA6ehud).

**FedRAMP nécessite-t-il une validation FIPS 140-2 ?**

Oui, le programme fédéral de gestion des autorisations et d’autorisation (FedRAMP) s’appuie sur les configurations de référence de contrôle définies par le [Pack NIST SP 800-53 révision 4](https://nvd.nist.gov/800-53/Rev4/), y compris la [protection de chiffrement SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) exigeant l’utilisation d’un chiffrement validé par FIPS ou un chiffrement approuvé par la NSA.

**Comment Microsoft Azure prend-il en charge FIPS 140-2 ?**

Azure est conçu avec une combinaison de matériel, de systèmes d’exploitation disponibles dans le commerce (Linux et Windows) et d’Azure version de Windows. Par le biais du [cycle de vie de développement de sécurité](https://www.microsoft.com/securityengineering/sdl/) Microsoft (SDL), tous les services Azure utilisent des algorithmes approuvés FIPS 140-2 pour la sécurité des données, car le système d’exploitation utilise les ALGORITHMes certifiés FIPS 140-2 lors du fonctionnement dans un nuage hyper-Scale.

**Puis-je utiliser le service d’adhésion de Microsoft au FIPS 140-2 dans le processus de certification de mon agence ?**

Pour être conforme à la norme FIPS 140-2, votre système doit être configuré pour s’exécuter dans un mode de fonctionnement approuvé par FIPS, ce qui inclut la vérification qu’un module de chiffrement utilise uniquement des algorithmes approuvés par FIPS. Pour plus d’informations sur la configuration des systèmes de façon à ce qu’ils soient conformes, consultez le [contenu Windows et Windows Server FIPS 140-2](https://aka.ms/AA6ehud).

**Quelle est la relation entre FIPS 140-2 et les critères communs ?**

Il s’agit de deux normes de sécurité distinctes avec des objectifs différents, mais complémentaires. FIPS 140-2 est conçu spécifiquement pour la validation des modules de chiffrement logiciels et matériels, tandis que le critère commun est conçu pour évaluer les fonctions de sécurité dans les produits logiciels et matériels informatiques. Les évaluations de critères communs s’appuient souvent sur les validations FIPS 140-2 pour garantir que la fonctionnalité de chiffrement de base est implémentée correctement.

## <a name="resources"></a>Ressources

- [Exigences de sécurité de la publication 140-2 FIPS pour les modules de chiffrement](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [Programme de validation du module de chiffrement NIST](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows, Windows Server et FIPS 140-2](https://docs.microsoft.com/windows/security/threat-protection/fips-140-validation)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)

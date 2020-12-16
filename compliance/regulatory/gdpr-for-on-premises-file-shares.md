---
title: RGPD pour les partages de fichiers en local
description: Découvrez comment répondre aux exigences en matière de Règlements généraux sur la protection des données (RGPD) dans les partages de fichiers Windows Server locaux.
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
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
ms.openlocfilehash: b750fcc6bceec12a13b909e65dc6283b8938c6da
ms.sourcegitcommit: fc1da22cf40dfd807c182d3f6df967eee192eacd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "49669725"
---
# <a name="gdpr-for-on-premises-windows-server-file-shares"></a>RGPD pour les partages de fichiers Windows Server en local

L’approche principale recommandée pour les partages de fichiers est la suivante :

-   Vous pouvez attribuer des étiquettes aux données sensibles à l’aide d’Azure Information Protection.

-   Vous pouvez rechercher des données à l’aide du scanneur Azure Information Protection

L’approche recommandée pour les partages de fichiers est la suivante :

1.  **Installez et configurez le scanneur Azure Information Protection.**

    -   Déterminez les types de données sensibles à utiliser.

    -   Indiquez les dossiers locaux et les partages réseau à utiliser.

2.  **Effectuez un cycle de détection.**

    -   Exécutez le scanneur en mode de détection et validez les résultats.

    -   Si nécessaire, optimisez les conditions et les types d’informations sensibles.

    -   Évaluez l’incidence que peut avoir l’application automatique d’étiquettes.

3.  **Exécutez le scanneur Azure Information Protection pour appliquer des étiquettes aux documents correspondants**.

4.  **Pour une meilleure protection :**

    -   Configurez des règles de protection contre la perte de données Exchange pour protéger les documents avec l’étiquette souhaitée.

    -   Veillez à déterminer des autorisations pour restreindre les personnes pouvant accéder aux fichiers.

5.  **Pour la surveillance, intégrez un outil SIEM aux journaux Windows Server.**

    -   Pour rechercher des données personnelles dans le cadre de demandes de personnes concernées, utilisez le scanneur Azure Information Protection. Vous pouvez également configurer la recherche SharePoint Server pour analyser les partages de fichiers.

Si vous souhaitez en savoir plus sur l’utilisation du scanneur Azure Information Protection pour la recherche et l’étiquetage de données personnelles, veuillez consulter la rubrique [Déployer le scanneur AIP](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner).

Pour plus d’informations sur la configuration du scanneur pour diverses conditions et sur l’utilisation des types d’informations sensibles Office 365 dans le cadre de la protection contre la perte de données, reportez-vous à l’article [Comment configurer des conditions pour la classification automatique et recommandée pour Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-classification). Notez que les nouveaux types d’informations sensibles Office 365 ne pourront pas immédiatement être utilisés avec le scanneur et que les types d’informations sensibles personnalisés ne peuvent pas être utilisés avec le scanneur.

---
title: Analyses d’impact sur la protection des données
description: Ces documents visent à fournir les informations qui permettront aux contrôleurs de données de déterminer si une analyse d’impact sur la protection des données est nécessaire et, le cas échéant, les informations à inclure.
keywords: Analyse d’impact sur la protection des données, DPIA, Dynamics 365, Microsoft Professional Services, services professionnels Microsoft, Microsoft 365, documentation Microsoft 365, RGPD
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
hideEdit: true
ms.openlocfilehash: eb609f081f3f2aeb182bfe7a24327ebc89513a9c
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496313"
---
# <a name="data-protection-impact-assessment-for-the-gdpr"></a>Analyses d’impact sur la protection des données pour le RGPD

Le règlement général sur la protection des données (RGPD) présente de nouvelles règles pour les organisations qui offrent des produits et des services aux membres de l’Union européenne (UE), ou qui collectent et analysent des données pour les résidents de l’UE quel que soit l’endroit où vous vous trouvez et celui où se trouve votre entreprise. Pour plus de détails, consultez la [rubrique Synthèse RGPD](gdpr.md). Ce document vous apporte des informations concernant les analyses d’impact sur la protection des données (DPIA) en vertu du RGPD lorsque vous utilisez les produits et services Microsoft.

## <a name="terminology"></a>Terminologie

Définitions utiles pour les termes RGPD utilisés dans ce document :

- *Contrôleur de données (contrôleur)*  : la personne morale, l’autorité publique, le service ou tout autre organisme qui, seul ou conjointement avec d’autres entités, détermine les finalités et les moyens de traitement des données personnelles.  
- *Données personnelles* et *personne concernée* : toutes les informations relatives à une personne physique identifiée ou identifiable (personne concernée); une personne physique identifiable est une personne qui peut être identifiée, directement ou indirectement.  
- *Responsable du traitement* : la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui traite des données à caractère personnel pour le compte de l’entité de contrôle.  
- *Données client* : les données produites et stockées dans les opérations quotidiennes dans le cadre du fonctionnement de votre entreprise.

## <a name="what-is-a-dpia"></a>Qu'est-ce qu’une DPIA ?

Le RGPD requiert des contrôleurs de préparer une analyse d’impact sur la protection des données (DPIA) pour les opérations « susceptibles de générer un risque élevé pour les droits et libertés des personnes physiques ». Il n’existe aucun élément inhérent aux produits et services Microsoft nécessitant la création d’une DPIA. Toutefois, étant donné que les produits et services Microsoft sont hautement personnalisables, une DPIA peut être nécessaire selon les détails de votre configuration Microsoft. Microsoft ne contrôle pas et n’a pas ou peu de connaissances sur les informations de ce type. En tant que contrôleur de données, vous devez déterminer les utilisations appropriées de ces données.

## <a name="dpia-in-action"></a>DPIA en action

Les recommandations DPIA s’appliquent à Office 365, Azure, Dynamics 365, au support Microsoft et aux services professionnels. Ces recommandations incluent les éléments suivants :

**Quand une DPIA est-elle nécessaire ?**

Les facteurs de risque répertoriés ci-dessous doivent être traités lorsque vous envisagez d’effectuer une DPIA. D’autres facteurs potentiels et des informations supplémentaires sont disponibles dans la partie 1 de chacune des instructions.  

- Analyse systématique et approfondie des données sur la base d’un traitement automatisé.  
- Traitement à grande échelle de catégories spéciales de données (données révélant des informations uniques identifiant une personne physique) ou de données à caractère personnel relatives aux condamnations pénales et aux délits commis.
- Surveillance systématique d’une zone publiquement accessible à grande échelle.

Le RGPD précise « Le traitement des données à caractère personnel ne doit pas être considéré comme un traitement à grande échelle s'il concerne des données à caractère personnel de patients ou de clients par un médecin, un autre professionnel de la santé ou un avocat. Dans ce cas, une évaluation de l’impact de la protection des données ne doit pas être obligatoire ».

**Qu’est-ce qui est requis pour effectuer une DPIA ?**

Une DPIA doit fournir des informations spécifiques sur le traitement prévu, qui sont détaillées dans la partie 2 de l’aide. Ces informations sont les suivantes :

- Évaluation du besoin et de la proportionnalité du traitement des données par rapport aux finalités prévues de la DPIA.  
- Évaluation des risques concernant les droits et les libertés des personnes physiques.
- Les mesures envisagées pour lutter contre les risques, notamment les garanties, les mesures de sécurité et les mécanismes pour assurer la protection des données à caractère personnel et prouver la conformité avec le RGPD.
- Finalités de traitement  
- Catégories de données à caractère personnel traitées  
- Rétention des données  
- Emplacement et transferts de données à caractère personnel  
- Partage de données avec des sous-processeurs tiers  
- Partage de données avec des tiers indépendants  
- Droits des personnes concernées par les données

## <a name="additional-considerations"></a>Considérations supplémentaires

Vous trouverez ci-dessous des détails spécifiques pouvant être utiles à votre implémentation Microsoft.

- [Office 365](gdpr-dpia-office365.md) : ce document s’applique aux applications et services Office 365, y compris, mais sans s’y limiter, à Exchange Online, SharePoint Online, Yammer, Skype Entreprise et Power BI. Pour plus d'informations, reportez-vous aux tableaux [1](/microsoft-365/compliance/gdpr-dpia-office365#part-1--determining-whether-a-dpia-is-needed) et [2](/microsoft-365/compliance/gdpr-dpia-office365#part-2--contents-of-a-dpia).  
- [Azure](gdpr-dpia-azure.md) : les clients sont encouragés à collaborer avec leurs responsables de la confidentialité et leur conseiller juridique pour déterminer la nécessité et le contenu de toute DPIA relative à l’utilisation de Microsoft Azure.  
- [Dynamics 365](gdpr-dpia-dynamics.md) : le contenu d’une analyse d’impact sur la protection des données peut varier en fonction des outils Dynamics 365 que vous utilisez. Pour des détails spécifiques, reportez-vous à [Partie 2 : contenu d’une analyse d’impact sur la protection des données](/microsoft-365/compliance/gdpr-dpia-dynamics#part-2--contents-of-a-dpia).
- [Support Microsoft et services professionnels](gdpr-dpia-prof-services.md) : les services professionnels ne procèdent pas à un traitement de données de routine ou automatisées et ne sont pas destinés à traiter des catégories spéciales ou à effectuer des tâches qui facilitent ou nécessitent la surveillance de données accessibles au public. Pour plus d’informations, reportez-vous à [Partie 1 : déterminer si une analyse d’impact sur la protection des données est nécessaire](/microsoft-365/compliance/gdpr-dpia-prof-services#part-1--determining-whether-a-dpia-is-needed). Les contrôleurs doivent prendre en considération les éléments de l’analyse d’impact sur la protection des données décrits ci-dessus, ainsi que d’autres facteurs pertinents, dans le contexte des implémentations spécifiques du contrôleur et des utilisations des services professionnels. Pour plus d’informations sur les services professionnels, reportez-vous à [Partie 2 : contenu d’une analyse d’impact sur la protection des données (DPIA)](/microsoft-365/compliance/gdpr-dpia-prof-services#part-2--contents-of-a-dpia).

## <a name="learn-more"></a>En savoir plus

- [Centre de gestion de la confidentialité Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)

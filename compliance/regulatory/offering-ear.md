---
title: Réglementation de l’administration des exportations américaines (EAR)
description: Les services de Cloud Computing Microsoft aident les clients soumis aux réglementations de l’administration des exportations américaines à respecter les exigences de conformité et à gérer le risque de contrôle d’exportation.
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
ms.openlocfilehash: ec70c3cd09302445d3e7b4e2ac394837cdabe557
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506899"
---
# <a name="us-export-administration-regulations-ear"></a>Réglementation de l’administration des exportations américaines (EAR)

## <a name="about-the-ear"></a>À propos de l’oreille

Le ministère américain du commerce applique les réglementations de l’administration des exportations (EAR) par le [Bureau de l’industrie et la sécurité (bis)](https://www.bis.doc.gov/). L’oreille régit et impose des contrôles sur l’exportation et la réexportation de la plupart des biens commerciaux, logiciels et technologies, y compris les éléments « double utilisation » qui peuvent être utilisés à des fins commerciales et militaires et pour certains éléments de défense.

Les directives BIS tiennent compte du fait que, lorsque des données ou des logiciels sont chargés dans le Cloud ou transférés entre des nœuds d’utilisateur, le client, et non le fournisseur de Cloud, est le « exportateur » qui est chargé de s’assurer que les transferts, le stockage et l’accès à ces données ou logiciels sont conformes aux EAR.

[Conformément à la BRI](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file), l' *exportation* désigne le transfert de technologies protégées ou de données techniques vers une destination étrangère ou sa publication vers une personne étrangère aux États-Unis (également appelé « *exportation présumée*»). L’oreille régit largement :

- Exportations à partir des États-Unis.
- Réexporte ou retransfère des éléments d’origine et certains éléments d’origine étrangère avec plus *d’une partie de la* teneur en US-Origin.
- Transferts ou divulgations à des personnes d’autres pays.

Les éléments soumis à l’oreille se trouvent dans la liste contrôle de commerce (CCL), où chaque élément est affecté d’un [numéro de classification de contrôle d’exportation unique (ECCN)](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn). Les éléments qui ne sont pas répertoriés sur le CCL sont désignés comme EAR99 et la plupart des produits commerciaux EAR99 ne nécessitent pas l’exportation d’une licence. Toutefois, en fonction de l’utilisation de destination, de l’utilisateur final ou de l’utilisation finale de l’élément, même un élément EAR99 peut exiger une licence d’exportation BIS.

La [règle finale](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations), publiée en juin 2016, a clarifié que les exigences en matière de licences Ear ne s’appliquaient pas non plus à la transmission et au stockage de données techniques et de logiciels non classés s’ils étaient chiffrés de bout en bout à l’aide de modules cryptographiques validés par FIPS 140-2 et n’étaient pas stockés intentionnellement dans un pays sous embargo militaire ou dans la Fédération russe

## <a name="microsoft-and-the-ear"></a>Microsoft et l’oreille

Les technologies, produits et services Microsoft sont soumis à la réglementation américaine sur l’administration des exportations (EAR). Bien qu’il n’existe pas de certification de conformité pour les EAR, Microsoft Azure, Microsoft Azure Government et Microsoft Office 365 Government (environnements GCCHigh et DoD), il offre des fonctionnalités et des outils importants pour aider les clients éligibles à l’oreille à gérer les risques de contrôle d’exportation et à respecter les exigences de conformité.

Le service de commerce américain, qui applique les EAR, a pris la position que les clients, pas les fournisseurs de service Cloud tels que Microsoft, sont considérés comme exportateurs de leurs propres données client. Alors que la plupart des données client ne sont pas considérées comme des « technologies » ou des « données techniques » soumises aux contrôles d’exportation EAR, les services Cloud de Microsoft à l’échelle de l’étendue sont structurés pour aider les clients à gérer et à atténuer de manière significative les risques de contrôle d’exportation potentiels auxquels ils sont confrontés. En règle générale, Microsoft recommande l’utilisation de ses services Cloud gouvernementaux pour les clients éligibles. Avec une planification appropriée, les clients peuvent utiliser les outils suivants et leurs procédures internes pour garantir une conformité complète avec les contrôles d’exportation US.

- **Contrôles à l’emplacement des données**. Les clients ont une visibilité sur l’emplacement de stockage de leurs données et l’accès à des outils puissants pour limiter leur stockage. Ils peuvent donc s’assurer que leurs données sont stockées aux États-Unis et réduire le transfert de technologies contrôlées ou de données techniques en dehors des États-Unis. En outre, les données client ne sont pas stockées dans un emplacement non conforme, conformément aux interdictions de l’oreille sur les emplacements où les données sont « stockées intentionnellement » : aucun centre de données Azure n’est situé dans l’un des 25 groupes D :5 pays ou Fédération russe.
- **Chiffrement de bout en bout**. En tirant parti de la sphère de sécurité de bout en bout pour les emplacements de stockage physique spécifiés dans l’oreille, les services Cloud de Microsoft à l’échelle de l’étendue offrent des fonctionnalités de chiffrement qui peuvent vous aider à vous protéger contre les risques liés au contrôle d’exportation. Ils offrent également aux clients un [large éventail d’options pour le chiffrement des données](https://aka.ms/Azure-Encryption-Overview) en transit et au repos, ainsi que la flexibilité nécessaire pour choisir les options de chiffrement.
- **Les outils et les protocoles pour empêcher l’exportation non autorisée**. L’utilisation du chiffrement contribue également à assurer une protection contre une exportation potentielle (ou une réexportation réputée) sous l’oreille, car même si une personne non-américaine a accès aux données chiffrées, rien n’est révélé s’il ne peut pas lire ou comprendre les données pendant qu’il est chiffré ; par conséquent, il n’y a pas de « libération » de données contrôlées.

## <a name="microsoft-in-scope-cloud-services"></a>Services Cloud Microsoft concernés

- [Azure et Azure Government](https://aka.ms/AzureCompliance)
- [Office 365 gouvernement (GCC-High et DoD)](https://aka.ms/Office-365-Export-Controls)
- Intune

## <a name="how-to-implement"></a>Modalités de mise en œuvre

Vue d’ensemble des États-Unis exporter des contrôles et des conseils pour les clients qui évaluent leurs obligations en vertu des EAR.

- [Azure](https://aka.ms/Azure-Export-Controls)
- [Office 365](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a>Questions fréquentes (FAQ)

**Que dois-je faire pour se conformer aux contrôles d’exportation lors de l’utilisation des services de Cloud Computing Microsoft ?**

Sous la languette, lorsque les données sont téléchargées vers un serveur Cloud tel que le Cloud Microsoft, le client propriétaire des données, et non le fournisseur de services Cloud, est considéré comme exportateur. Pour cette raison, le propriétaire des données, c’est-à-dire le client Microsoft, doit évaluer avec soin comment leur utilisation du Cloud Microsoft peut mettre en cause les contrôles d’exportation US et déterminer si les données qu’ils souhaitent utiliser ou stocker peuvent être soumises à des contrôles de l’oreille et, si c’est le cas, les contrôles qui s’appliquent. En savoir plus sur la façon dont les services Cloud [Azure](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers) et [Office 365](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI) peuvent aider les clients à garantir leur conformité complète avec les contrôles d’exportation US.

**Les technologies, produits et services Microsoft sont-ils soumis aux EAR ?**

La plupart des technologies, produits et services Microsoft :

- Ne sont pas soumis aux EAR et ne sont donc pas dans la liste de contrôle de commerce et n’ont pas de ECCN ;
- Ou il s’agit d’un marché de masse EAR99 ou 5D992, éligible pour l’auto-classification par Microsoft et pouvant être exporté vers des pays non embargoés sans licence obligatoire (NLR).

Cela étant dit, certains produits Microsoft ont reçu une ECCN qui peut nécessiter ou non une licence. Consultez la EAR ou le conseiller juridique pour déterminer le type de licence approprié et les pays éligibles à des fins d’exportation.

**Quelle est la différence entre les EAR et le trafic international des armes (ITAR) ?**

Les principaux contrôles des exportations américaines avec la plus grande application sont les EAR, administrés par le ministère américain du commerce. L’oreille s’applique aux éléments à double utilisation qui ont des applications commerciales et militaires, ainsi qu’aux éléments avec des applications purement commerciales.

Les États-Unis ont également des réglementations de contrôle d’exportation distinctes et plus spécialisées, telles que le ITAR, qui régit les éléments et la technologie les plus sensibles. Géré par le ministère américain de l’État, il impose des contrôles sur l’exportation, l’importation temporaire, la ré-exportation et le transfert de nombreux éléments militaires, de défense et d’aide (également appelés « Articles de défense »), y compris les données techniques associées.

## <a name="resources"></a>Ressources

- [Exportation de produits Microsoft : vue d’ensemble](https://www.microsoft.com/exporting/overview.aspx)
- [Exportation de produits Microsoft : FAQ](https://www.microsoft.com/exporting/faq.aspx)
- [Exportation de produits Microsoft : recherche de produits](https://www.microsoft.com/exporting/exporting-information.aspx)
- [Exporter des restrictions sur le chiffrement](https://docs.microsoft.com/windows/uwp/security/export-restrictions-on-cryptography)
- [Microsoft et FIPS 140-2](offering-fips-140-2.md)
- [Microsoft et ITAR](offering-itar.md)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)

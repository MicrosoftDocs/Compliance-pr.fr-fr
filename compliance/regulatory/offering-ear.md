---
title: Réglementations américaines en matière d’administration des exportations (EAR)
description: Les services cloud de Microsoft aident les clients soumis aux réglementations américaines en matière d’administration des exportations (EAR) à respecter leurs exigences de conformité et à gérer les risques de contrôle d’exportation.
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
ms.openlocfilehash: 0c05010d43ea345024b63e2653e37eb0f42443f4
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089768"
---
# <a name="us-export-administration-regulations-ear"></a>Réglementations américaines en matière d’administration des exportations (EAR)

## <a name="about-the-ear"></a>À propos de l’écouteur

Le département du Commerce des États-Unis applique les réglementations d’administration des exportations (EAR) via le [Bureau of Industry and Security (BIS).](https://www.bis.doc.gov/) L’EAR régit et impose des contrôles sur l’exportation et la ré-exportation de la plupart des biens commerciaux, logiciels et technologies, y compris les éléments à double usage qui peuvent être utilisés à des fins commerciales et civiles, ainsi que certains éléments de défense.

Les conseils bis indiquent que, lorsque des données ou des logiciels sont téléchargés vers le cloud ou transférés entre des développeurs d’utilisateurs, le client, et non le fournisseur de cloud, est l'« exportateur » chargé de s’assurer que les transferts, le stockage et l’accès à ces données ou logiciels sont conformes à l’EAR.

[Conformément](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file)à la bis *,* l’exportation fait référence au transfert de technologies protégées ou de données techniques vers une destination étrangère ou à sa publication à une personne étrangère aux États-Unis (également appelée exportation considérée *comme* étant une exportation). L’ear régit largement :

- Exporte à partir des États-Unis.
- Ré-exporte ou retransférer des éléments d’origine américaine et certains éléments d’origine étrangère avec plus d’une partie *de minimis* du contenu d’origine américaine.
- Transferts ou divulgations à des personnes d’autres pays.

Les éléments soumis à la fonction EAR se trouvent dans la liste de contrôle commercial (CCL) où chaque élément est affecté d’un numéro [eccn (Export Control Classification Number)](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn)unique. Les éléments qui ne sont pas répertoriés dans la liste de contrôle d’accès sont désignés comme EAR99 et la plupart des produits commerciaux EAR99 ne nécessitent pas de licence pour être exportés. Toutefois, selon la destination, l’utilisateur final ou l’utilisation finale de l’élément, même un élément EAR99 peut nécessiter une licence d’exportation BIS.

La dernière [règle,](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations)publiée en juin 2016, a permis de clarifier que les exigences de licence EAR ne s’appliquent pas non plus à la transmission et au stockage de données techniques et de logiciels non classifiés s’ils sont chiffrés de bout en bout à l’aide de modules de chiffrement validés par la FIPS 140-2 et qu’ils n’ont pas été stockés intentionnellement dans un pays étranger ou dans la Fédération de Russie.

## <a name="microsoft-and-the-ear"></a>Microsoft et la technologie EAR

Les technologies, produits et services Microsoft sont soumis aux réglementations américaines en matière d’exportation (EAR). Bien qu’il n’existe aucune certification de conformité pour les environnements EAR, Microsoft Azure, Microsoft Azure Government et Microsoft Office 365 Government (environnements GCCHigh et DoD) offrent des fonctionnalités et des outils importants pour aider les clients éligibles soumis à l’ear à gérer les risques de contrôle d’exportation et à répondre à leurs exigences de conformité.

Le département du Commerce des États-Unis, qui applique l’ear, a pris la position selon laquelle les clients, et non les fournisseurs de services cloud tels que Microsoft, sont considérés comme des exportateurs de leurs propres données client. Bien que la plupart des données client ne soient pas considérées comme des « technologies » ou des « données techniques » soumises aux contrôles d’exportation EAR, les services cloud microsoft dans l’étendue sont structurés pour aider les clients à gérer et atténuer considérablement les risques potentiels liés au contrôle d’exportation auxquels ils sont confrontés. Microsoft recommande généralement, mais pas exclusivement, l’utilisation de ses services cloud pour le gouvernement pour les clients éligibles. Avec une planification appropriée, les clients peuvent utiliser les outils suivants et leurs propres procédures internes pour garantir la conformité totale avec les contrôles d’exportation américains.

- **Contrôles sur l’emplacement des données**. Les clients ont une visibilité sur l’endroit où leurs données sont stockées et ont accès à des outils robustes pour limiter leur stockage. Ils peuvent par conséquent s’assurer que leurs données sont stockées aux États-Unis et minimiser le transfert de technologies contrôlées ou de données techniques en dehors des États-Unis. En outre, les données client ne sont pas stockées dans un emplacement non conforme, conformément aux interdictions EAR sur l’endroit où les données sont « stockées intentionnellement » : aucun centre de données Azure n’est situé dans l’un des 25 pays du groupe D:5 ou dans la Fédération de Russie.
- **Chiffrement de bout en bout.** En profitant de la sphère de sécurité de chiffrement de bout en bout pour les emplacements de stockage physiques spécifiés dans l’ear, les services cloud microsoft dans le périmètre offrent des fonctionnalités de chiffrement qui peuvent vous protéger contre les risques de contrôle d’exportation. Ils offrent également aux clients un large éventail [d’options](https://aka.ms/Azure-Encryption-Overview) pour le chiffrement des données en transit et au repos, et la flexibilité de choix parmi les options de chiffrement.
- **Outils et protocoles permettant d’empêcher l’exportation considérée comme non autorisée.** L’utilisation du chiffrement permet également de se protéger contre une exportation considérée comme potentielle (ou considérée comme ré-exportée) sous l’ear, car même si une personne non américaine a accès à des données chiffrées, rien n’est révélé s’il ne peut pas lire ou comprendre les données pendant qu’elles sont chiffrées ; par conséquent, il n’existe aucune « publication » de données contrôlées.

## <a name="microsoft-in-scope-cloud-services"></a>Services Cloud Microsoft concernés

- [Azure et Azure Government](https://aka.ms/AzureCompliance)
- [Office 365 Secteur Public (Cloud de la communauté du secteur public-High et DoD)](https://aka.ms/Office-365-Export-Controls)
- Intune

## <a name="how-to-implement"></a>Modalités de mise en œuvre

Vue d’ensemble des contrôles d’exportation aux États-Unis et des conseils pour les clients qui évaluent leurs obligations dans le cadre de l’ear.

- [Azure](https://aka.ms/Azure-Export-Controls)
- [Office 365](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a>Questions fréquentes (FAQ)

**Que dois-je faire pour me conformer aux contrôles d’exportation lors de l’utilisation des services cloud de Microsoft ?**

Dans le cadre de la technologie EAR, lorsque les données sont téléchargées vers un serveur cloud tel que le cloud Microsoft, le client propriétaire des données (et non le fournisseur de services cloud) est considéré comme l’exportateur. Pour cette raison, le propriétaire des données, c’est-à-dire le client Microsoft, doit évaluer avec soin la façon dont leur utilisation du cloud Microsoft peut insérable les contrôles d’exportation américains et déterminer si des données qu’ils souhaitent utiliser ou stocker y sont soumises à des contrôles EAR et, le cas chef, quels contrôles s’appliquent. En savoir plus sur la façon [dont azure](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers) [et Office 365](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI) services cloud peuvent aider les clients à assurer leur conformité totale avec les contrôles d’exportation aux États-Unis.

**Les technologies, produits et services Microsoft sont-ils soumis à l’ear ?**

La plupart des technologies, produits et services Microsoft :

- Ne sont pas soumis à l’EAR et ne sont donc pas dans la liste de contrôles commerciaux et n’ont pas d’ECCN ;
- Ou bien, ils sont éligibles au marché de masse EAR99 ou 5D992 pour une classification autonome par Microsoft et peuvent être exportés vers des pays non-abonnés sans licence en tant qu’aucune licence requise (NLR).

Cela dit, certains produits Microsoft se sont vus attribuer un ECCN qui peut ou non nécessiter une licence. Consultez l’ear ou le conseiller juridique pour déterminer le type de licence approprié et les pays éligibles à des fins d’exportation.

**Quelle est la différence entre la réglementation EAR et la réglementation ITAR (International Traffic in Arms Regulations) ?**

Les principaux contrôles d’exportation aux États-Unis avec l’application la plus large sont l’EAR, administré par le département du Commerce des États-Unis. L’ear s’applique aux éléments à double utilisation qui ont des applications commerciales et américaines, ainsi qu’aux éléments avec des applications purement commerciales.

Les États-Unis ont également des réglementations distinctes et plus spécialisées en matière de contrôle des exportations, telles que la loi ITAR, qui régissent les éléments et technologies les plus sensibles. Administrés par le département d’État des États-Unis, ils imposent des contrôles sur l’exportation, l’importation temporaire, la ré-exportation et le transfert de nombreux éléments de sécurité, de défense et d’intelligence (également appelés « articles de défense »), y compris les données techniques connexes.

## <a name="resources"></a>Ressources

- [Exportation des produits Microsoft : vue d’ensemble](https://www.microsoft.com/exporting/overview.aspx)
- [Exportation des produits Microsoft : FAQ](https://www.microsoft.com/exporting/faq.aspx)
- [Exportation des produits Microsoft : recherche de produits](https://www.microsoft.com/exporting/exporting-information.aspx)
- [Restrictions d’exportation sur le chiffrement](/windows/uwp/security/export-restrictions-on-cryptography)
- [Microsoft et FIPS 140-2](offering-fips-140-2.md)
- [Microsoft et ITAR](offering-itar.md)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)

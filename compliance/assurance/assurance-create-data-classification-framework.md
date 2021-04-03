---
title: Créer une infrastructure de classification des données bien conçue
description: Dans cet article, vous trouverez une vue d’ensemble de la création d’une infrastructure de classification des données bien conçue pour Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: df2bc373fea046ac120c40c57af2ba061d2b0781
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497795"
---
# <a name="create-a-well-designed-data-classification-framework"></a>Créer une infrastructure de classification des données bien conçue

Au cours du développement, de la réorganisation ou de l’affinement de votre infrastructure de classification des données, prenez en compte les pratiques principales suivantes :

- Ne vous attendez pas à passer de 0 à **100** le jour 1 : Microsoft recommande une approche d’analyse pas à pas, en hiér donc les fonctionnalités critiques pour l’organisation et en les missant par rapport à une chronologie. Terminez la première étape, assurez-vous qu’elle a réussi, puis passe à la phase suivante en appliquant les leçons apprises. N’oubliez pas que votre organisation peut toujours être exposée à des risques pendant que vous concevez votre infrastructure de classification des données. Il est donc possible de commencer petit avec quelques niveaux de classification et de le développer ultérieurement si nécessaire.
- Vous **n’écrivez** pas seulement pour les professionnels de la cybersécurité : les cadres de classification des données sont destinés à un large public, y compris les membres de votre personnel moyen, vos équipes juridiques et de conformité et votre équipe informatique. Il est important d’écrire des définitions claires et faciles à comprendre pour vos niveaux de classification des données, en fournissant des exemples concrets autant que possible. Essayez d’éviter le jargon et envisagez un glossaire pour les acronymes et les termes hautement techniques. Par exemple, utilisez « Informations d’identification personnelle » et fournissez une définition au lieu de simplement dire « PII ».
- **Les infrastructure de classification des données** sont destinées à être implémentées : pour que les infrastructure de classification des données réussissent, elles doivent être implémentées. Il est particulièrement pertinent lors de la création des exigences de contrôle pour chaque niveau de classification des données. Assurez-vous que les exigences sont clairement définies et qu’elles anticipent et lèvent toute ambiguïté qui pourrait survenir lors de l’implémentation. Par exemple, si vous avez un contrôle sur les informations d’identification personnelle, veillez à préciser exactement ce que signifie ce contrôle, tel que la sécurité sociale ou le numéro de passeport.
- **Ne soyez granulaire que si vous avez besoin :** les frameworks de classification des données contiennent généralement entre 3 et 5 niveaux de classification des données. Mais le simple fait que *vous pouvez* inclure cinq niveaux ne signifie pas que vous devez *le faire.* Prenez en compte les critères suivants lorsque vous décidez du nombre de niveaux de classification dont vous avez besoin :

    - Votre secteur d’activité et vos obligations réglementaires associées (les secteurs hautement réglementés ont tendance à avoir besoin de niveaux de classification plus élevés)
    - La surcharge opérationnelle requise pour maintenir une infrastructure plus complexe
    - Vos utilisateurs et leur capacité à se conformer à la complexité et à la nuance accrues associées à un plus grand nombre de niveaux de classification
    - Expérience utilisateur et accessibilité lorsque vous cherchez à appliquer une classification manuelle sur plusieurs types d’appareils

- **Impliquer les bonnes personnes**: la participation d’une partie prenante senior est essentielle à la réussite, car de nombreux projets ont du mal à démarrer ou à prendre plus de temps sans le backing de la direction. Les infrastructure de classification des données sont généralement la propriété des équipes informatiques, mais elles peuvent avoir des implications légales, de conformité, de confidentialité et de gestion des changements. Pour vous assurer que vous créez une infrastructure qui vous aide à protéger votre entreprise, veillez à inclure les parties prenantes en matière de confidentialité et juridiques telles que votre responsable de la protection de la vie privée et le conseiller général dans le développement de votre stratégie. Si votre organisation dispose d’une division conformité, de professionnels de la gouvernance des informations ou d’une équipe de gestion des enregistrements, ils peuvent également avoir des informations précieuses. Comme votre infrastructure est déployée pour l’entreprise, votre service communications a également un rôle clé à jouer pour la messagerie interne et l’adoption.
- **Trouver un équilibre entre sécurité et commodité**: une erreur courante consiste à rédiger une infrastructure de classification des données sécurisée mais trop restrictive. Cette infrastructure a peut-être été conçue avec la sécurité à l’esprit, mais elle est souvent difficile à implémenter dans la pratique. Si les utilisateurs doivent suivre des procédures complexes, strictes et chronophages pour appliquer l’infrastructure dans leur vie quotidienne, il existe toujours un risque qu’ils ne pensent plus en sa valeur et qu’ils arrêtent de suivre les procédures. Ce risque existe à tous les niveaux de l’organisation, y compris les responsables de niveau exécutif (C-suite) au sein de l’organisation. Un bon équilibre entre sécurité et commodité, ainsi que des outils faciles à utiliser, conduit généralement à une adoption et une utilisation plus larges par les utilisateurs. En cas de lacunes dans votre infrastructure, n’attendez pas que tout soit parfait pour démarrer l’implémentation. Au lieu de cela, évaluez le risque ou l’écart, créez un plan pour atténuer et continuer à avancer. N’oubliez pas que la protection des informations est un parcours, mais qu’elle n’est pas activée du jour au lendemain, puis effectuée. Planifiez, implémentez certaines fonctionnalités, confirmez la réussite et itérez au prochain jalon à mesure que les outils évoluent et que les utilisateurs gagnent en maturité et en expérience.

Gardez également à l’esprit qu’une infrastructure de classification des données traite uniquement de ce que votre organisation doit faire pour protéger les données sensibles.  Les cadres de classification des données sont souvent  accompagnés de règles ou de directives de gestion des données qui définissent comment mettre en place ces stratégies du point de vue technique et technologique. Dans les sections suivantes, nous vous présentons quelques conseils pratiques sur la façon de transformer votre infrastructure de classification des données d’un document de stratégie en une initiative entièrement implémentée et actionnable.

## <a name="pain-points-in-creating-a-data-classification-framework"></a>Points sensibles lors de la création d’une infrastructure de classification des données

Par nature, les efforts de classification des données touchent presque toutes les fonctions d’entreprise au sein d’une entreprise. En raison de cette étendue et de la complexité de la gestion du contenu dans les environnements numériques modernes, les entreprises rencontrent souvent des difficultés pour savoir par où commencer, comment gérer une implémentation réussie et mesurer leur progression. Les problèmes courants sont souvent les suivants :

- Conception d’une infrastructure de classification des données robuste et facile à comprendre, y compris la détermination des niveaux de classification et des contrôles de sécurité associés.
- Développement d’un plan de mise en œuvre qui inclut la confirmation de la solution technologique appropriée, l’alignement du plan sur les processus d’entreprise existants et l’identification de l’impact sur le personnel.
- Configuration d’une infrastructure de classification des données dans la solution technologique choisie et adressant les lacunes entre les fonctionnalités technologiques de l’outil et l’infrastructure elle-même.
- Établir une structure de gouvernance qui supervise la maintenance et l’état en cours des efforts de classification des données.
- Identification d’indicateurs de performance clés spécifiques pour surveiller et mesurer la progression.
- Sensibilisation et compréhension accrues des stratégies de classification des données, pourquoi elles sont importantes et comment les respecter.
- Conformité aux vérifications d’audit internes qui ciblent les contrôles de perte de données et de cybersécurité.
- Formation et implication des utilisateurs afin qu’ils se soucient de la nécessité d’une classification correcte dans leur travail quotidien et appliquent les mesures de classification adéquates.

## <a name="change-management-and-training"></a>Gestion et formation des changements

Les organisations utilisent actuellement des outils tels que Microsoft 365 pour implémenter leur infrastructure de classification des données. L’objectif est d’essayer d’automatiser la classification des données et de ne pas augmenter la charge sur votre personnel. Cette structure ne signifie pas que votre organisation n’est pas responsable de la nécessité de gérer le contenu et de protéger l’organisation contre les risques abordés dans ce document. La pratique principale continue d’effectuer une formation de sensibilisation au sein de l’organisation dans le cadre de la planification annuelle de la formation. Notre expérience montre qu’un effort solide et complet pour former vos utilisateurs, qui sont les principaux publics qui effectuent ce travail, augmente leur « buy-in » et peut améliorer l’adoption et la qualité. [L’ajout de recommandations en matière](/microsoft-365/compliance/apply-sensitivity-label-automatically#recommend-that-the-user-apply-a-sensitivity-label) d’étiquettes et de conseils dans l’application peut insérez ces efforts. Cette formation n’a pas besoin d’être un cours autonome complet. Votre organisation peut l’intégrer à d’autres formations régulières, telles que votre formation annuelle sur la sécurité des informations, puis inclure une vue d’ensemble des niveaux et définitions de classification des données. L’essentiel est que vos employés comprennent que même si l’outil automatise la classification des données, cela n’élimine pas la responsabilité globale de chaque utilisateur en matière de protection des données conformément à la stratégie de votre entreprise.

En outre, vous devez envisager une formation plus approfondie pour les équipes informatiques et de sécurité des informations afin de renforcer la préparation opérationnelle. Les équipes qui gèrent l’outil et l’infrastructure de classification des données doivent se trouver sur la même page. Cette coordination peut vous obliger à investir dans un calendrier de formation plus robuste qui peut être plus souvent qu’une fois par an. L’investissement dans une formation plus fréquente représente une autre façon de réduire les risques pour votre organisation. Cette équipe est responsable de l’implémentation et peut par conséquent être un point de défaillance si elle n’est pas formée sur l’outil et la stratégie.

Si vous devez baliser manuellement le contenu dans l’outil, le développement d’un groupe de super utilisateurs qui ont reçu une formation plus avancée est approprié. Ces super utilisateurs seraient impliqués dans les situations où les utilisateurs doivent baliser manuellement des documents avec des étiquettes de sensibilité aux données et qui ont une connaissance approfondie de l’infrastructure de classification des données de votre organisation et des exigences réglementaires.

Enfin, votre direction doit hiérarchiser le champion des comportements de sécurité des informations pour renforcer l’importance des initiatives de gestion des risques pour les employés. Il s’agit notamment du développement et de l’implémentation d’une infrastructure de classification des données robuste et de l’affectation de responsables clés pour promouvoir l’initiative, parfois appelées ambassadeurs ou ambassadeurs du changement.

## <a name="governance-and-maintenance"></a>Gouvernance et maintenance

Une fois que vous avez développé et implémenté votre infrastructure de classification des données, la gouvernance et la maintenance en cours sont essentielles à votre réussite. En plus de suivre la façon dont les étiquettes de niveau de sensibilité sont utilisées dans la pratique, vous devez mettre à jour vos exigences de contrôle en fonction des modifications apportées aux réglementations, des pratiques de pointe en matière de cybersécurité et de la nature du contenu que vous gérez. Les efforts de gouvernance et de maintenance peuvent inclure :

- Mettre en place un organisme de gouvernance dédié à la classification des données ou ajouter une responsabilité de classification des données à la structure d’un organisme de sécurité des informations existant.
- Définition des rôles et des responsabilités pour les utilisateurs qui supervisent la classification des données.
- Établir des KPIs pour surveiller et mesurer la progression.
- Suivi des principales pratiques en matière de cybersécurité et des modifications réglementaires.
- Développement de procédures d’exploitation standard qui prisent en charge et appliquent une infrastructure de classification des données.

## <a name="industry-considerations"></a>Considérations sur le secteur

Bien que les principes de base du développement d’une infrastructure de classification des données forte soient universels, les détails de votre infrastructure dépendent de la nature de votre secteur d’activité et des facteurs de conformité et de sécurité uniques que vos données exigent.

Par exemple, les entreprises de services financiers peuvent avoir besoin d’envisager la conformité avec plusieurs cadres réglementaires en fonction de l’étendue de leur activité et des régions dans lesquelles elles opèrent. Les sociétés de titres aux États-Unis doivent se conformer aux réglementations de compte telles que la règle [SEC 17a-4(f)](/compliance/regulatory/offering-sec-17a-4) ou la [règle 4511](/microsoft-365/compliance/offering-finra-4511) de la FINRA qui respectent les exigences relatives à la sécurité et à la conservation des livres et des enregistrements. De même, les entreprises qui opèrent au Royaume-Uni doivent prendre en compte la [conformité FCA.](/microsoft-365/compliance/offering-fca-uk)

Les agences gouvernementales font face à différentes réglementations régissant leurs données, qui varient en fonction du territoire et de la nature de leur travail. Aux États-Unis, par exemple, les agences gouvernementales et leurs agents qui accèdent aux informations fiscales fédérales sont soumis à [l’IRS 1075,](/microsoft-365/compliance/offering-irs-1075)qui vise à minimiser les risques de perte, de violation ou d’utilisation abusive des informations fiscales fédérales.

Bien que les entreprises de services financiers et les agences gouvernementales figurent parmi les organisations les plus réglementées au monde, la plupart des entreprises ont des considérations spécifiques au secteur qui doivent être envisagées. Voici quelques exemples :

- Les organisations du secteur [de la santé assurent la conformité avec la loi HIPAA.](/microsoft-365/compliance/offering-hipaa-hitech)
- Établissements d’enseignement, des établissements scolaires de la primaire à la 12e année, en charge de la gestion de la [conformité FERPA.](/microsoft-365/compliance/offering-ferpa)
- Les fabricants de produits de la santé qui s’emploient à se conformer aux [directives GxP](/microsoft-365/compliance/offering-gxp) dans leur pays ou leur région en matière de sécurité des informations.
- Les médias, la vente au détail et de nombreuses autres sociétés traitant de la [conformité R GDPR](/microsoft-365/compliance/gdpr).
- Distribution et stockage de contenu de divertissement, de logiciels et d’informations traitant [de CDSA.](/microsoft-365/compliance/offering-cdsa)
- Sécurité des informations du secteur de l’énergie conforme à la norme CIP de [la NERC.](/microsoft-365/compliance/offering-nerc-cip)

## <a name="implementing-your-data-classification-framework-in-microsoft-365"></a>Mise en œuvre de votre infrastructure de classification des données dans Microsoft 365

Une fois que vous avez développé votre infrastructure de classification des données, l’étape suivante consiste à l’implémentation. Le Centre de conformité [Microsoft 365](https://compliance.microsoft.com/) permet aux administrateurs de découvrir, classifier, examiner et surveiller leurs données conformément à leur infrastructure de classification des données. Les étiquettes de sensibilité peuvent être utilisées pour protéger vos données en appliquant diverses protections telles que le chiffrement et le marquage de contenu. Elles peuvent être appliquées aux données manuellement ; par défaut, en fonction des paramètres de stratégie ; ou automatiquement, à la suite d’une condition telle que les piI identifiées.

Pour les organisations de plus petite taille ou les organisations avec une structure de classification des données relativement rationalisée, la création d’une étiquette de niveau de sensibilité unique pour chacun de vos niveaux de classification des données peut suffire. L’exemple suivant montre un niveau de classification des données un-à-un pour le mappage des étiquettes de sensibilité :

|**Étiquette de classification**|**Étiquette de sensibilité**|**Paramètres d’étiquette**|**Publié sur**|
|:-----------------------|:--------------------|:-----------------|:---------------|
| Non restreint | Non restreint | Appliquer le pied de groupe « Non restreint » | Tous les utilisateurs |
| Général | Général | Appliquer le pied de groupe « Général » | Tous les utilisateurs |

>[!TIP]
>Au cours d’un projet pilote de protection des informations interne à Microsoft, il a été difficile de comprendre et d’utiliser l’étiquette « Personnel ». Les utilisateurs n’ont pas pu déterminer s’il s’agissait de données personnelles ou simplement d’un problème personnel. L’étiquette a été modifiée en « non-business » pour être plus claire. Cet exemple montre que la taxonomie n’a pas besoin d’être parfaite depuis le début. Commencez par ce que vous pensez être le bon, pilotez-la et ajustez l’étiquette en fonction des commentaires si nécessaire

Pour les grandes organisations ayant une portée globale ou des besoins plus complexes en matière de sécurité des informations, il se peut que cette relation un-à-un entre le nombre de niveaux de classification dans votre stratégie et le nombre d’étiquettes de confidentialité dans votre environnement Microsoft 365 soit un défi. Ce défi est particulièrement vrai dans les organisations globales où un niveau de classification des données donné tel que « Restreint » peut avoir une définition différente ou un ensemble différent de contrôles en fonction de la région.

Pour plus d’informations sur l’implémentation, voir [Comprendre la classification des](/microsoft-365/compliance/data-classification-overview) données et en savoir plus sur les [étiquettes de sensibilité.](/microsoft-365/compliance/sensitivity-labels)

## <a name="references"></a>Références

- [Offres pour la conformité Microsoft](/microsoft-365/compliance/offering-home)

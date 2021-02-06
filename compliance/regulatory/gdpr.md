---
title: Règlement général sur la protection des données
description: Découvrez les conseils techniques de Microsoft et trouvez des informations utiles concernant le Règlement général sur la protection des données (RGPD)
keywords: Microsoft 365, Microsoft 365 Éducation, documentation Microsoft 365, RGPD
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
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 44df81658719397271020f38088d3287e67774a1
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121433"
---
# <a name="general-data-protection-regulation-summary"></a>Sythèse du règlement général sur la protection des données

Le règlement général sur la protection des données (RGPD) présente de nouvelles règles pour les organisations qui offrent des produits et des services aux membres de l’Union européenne (UE), ou qui collectent et analysent des données pour les résidents de l’UE quel que soit l’endroit où vous vous trouvez et celui où se trouve votre entreprise. Ce document vous apporte des informations pour vous aider à honorer vos droits et à respecter les obligations en vertu du RGPD lorsque vous utilisez les produits et services Microsoft. Un [plan d’action recommandé pour le RGPD](gdpr-action-plan.md) et les [listes de vérification de préparation sur la responsabilité](gdpr-arc.md) fournissent des ressources supplémentaires pour l’évaluation et la mise en œuvre de la conformité RGPD.

## <a name="terminology"></a>Terminologie

Définitions utiles pour les termes RGPD utilisés dans ce document :

- **Contrôleur de données (contrôleur)**  : la personne morale, l’autorité publique, le service ou tout autre organisme qui, seul ou conjointement avec d’autres entités, détermine les finalités et les moyens de traitement des données personnelles.  
- **Données personnelles et personne concernée** : toutes les informations relatives à une personne physique identifiée ou identifiable (personne concernée); une personne physique identifiable est une personne qui peut être identifiée, directement ou indirectement.  
- **Responsable du traitement** : la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui traite des données à caractère personnel pour le compte de l’entité de contrôle.  
- **Données client** : les données produites et stockées dans les opérations quotidiennes dans le cadre du fonctionnement de votre entreprise.

## <a name="what-is-the-gdpr"></a>Qu’est-ce que le RGPD ?

Le RGPD donne aux personnes les droits de gérer les données personnelles rassemblées par une organisation. Ces droits peuvent être exercés via une demande de la personne concernée (DSR). L’organisation doit fournir des informations opportunes concernant les DSR et les brèches de données, et effectuer des analyses d’impact sur la protection des données (DPIA).

Plusieurs points doivent être pris en considération lors de l’implémentation ou de l’analyse de besoins RGPD :

- Développement ou analyse de votre politique de confidentialité des données de conformité RGPD.
- Analyser la sécurité des données de votre organisation.
- Qui est votre contrôleur de données ?
- Quels sont les processus de sécurité des données que vous devez effectuer ?

Le [plan d’action recommandé pour le RGPD](gdpr-action-plan.md) et les [listes de vérification de préparation sur la responsabilité](gdpr-arc.md) peuvent inviter à d’autres points de réflexion.

Les tâches suivantes sont impliquées pour satisfaire les normes RGPD. Pour plus d’informations sur l’implémentation, suivez les liens de la liste.  

- **[Demandes des personnes concernées (DSR)](gdpr-data-subject-requests.md)**. Une demande officielle d’une personne concernée à un responsable du traitement pour effectuer une action (changement, restriction, accès) sur ses données personnelles.
- **[Notification de violation](gdpr-breach-notification.md)**. En vertu du RGPD, une violation de données personnelles correspond à « une violation de la sécurité entraînant la destruction involontaire ou contraire à la loi de données personnelles transmises, stockées ou autrement traitées, ou bien leur perte, modification ou divulgation ou consultation non autorisée ».
- **[Analyses d’impact sur la protection des données](gdpr-data-protection-impact-assessments.md)**. Les contrôleurs de données sont requis en vertu du RGPD de préparer une analyse d’impact sur la protection des données pour les opérations de données « susceptibles de générer un risque élevé pour les droits et libertés des personnes physiques ».

Comme indiqué ci-dessus, le plan d’action recommandé pour le RGPD et les listes de vérification de préparation sur la responsabilité fournissent un guide pour l’implémentation ou l’analyse de la conformité RGPD à l’aide de produits et services Microsoft.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Utilisez le Gestionnaire de Conformité Microsoft pour évaluer vos risques

[Le Gestionnaire de Conformité Microsoft](/microsoft-365/compliance/compliance-manager) est une fonctionnalité dans le [centre de conformité Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) pour vous aider à comprendre la position de la conformité de votre organisation et à prendre des mesures pour réduire les risques. Le Gestionnaire de conformité offre une évaluation prédéfinie de cette réglementation pour les clients d’Entreprise E5. Recherchez le modèle de création de l’évaluation sur la page **des modèles d’évaluation** dans le Gestionnaire de Conformité. Découvrez comment [créer des évaluations dans le Gestionnaire de Conformité](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="data-subject-request-dsr"></a>Demandes des personnes concernées (DSR)

Le RGPD octroie aux individus (ou aux personnes concernées par les données) certains droits en lien avec le traitement de leurs données personnelles, y compris le droit de corriger des données incorrectes, d’effacer des données ou de limiter leur traitement, de recevoir leur données et de remplir une demande afin de transmettre leurs données à un autre contrôleur. Le contrôleur se charge de fournir une réponse opportune et cohérente au RGPD. Pour plus d’informations techniques, reportez-vous à [Demandes des personnes concernées](gdpr-data-subject-requests.md).  

### <a name="dsr-faqs"></a>Forum aux questions sur le DSR

**Quelles actions seront requises pour effectuer un DSR ?**

Une demande de personne concernée implique six activités : découverte, accès, rectification, restriction, exportation et suppression.

**Quelles sont vos sources de données ?**

Une grande partie des données d’une organisation est générée dans les [applications Office](/microsoft-365/compliance/gdpr-dsr-office365#using-the-content-search-ediscovery-tool-to-respond-to-dsrs) telles qu’Excel et Outlook. Vous pouvez également trouver des données pertinentes pour une DSR dans les [informations](/microsoft-365/compliance/gdpr-dsr-office365#part-2-responding-to-dsrs-with-respect-to-insights-generated-by-office-365) générées par les produits et services Microsoft et les [journaux générés par le système](/microsoft-365/compliance/gdpr-dsr-office365#part-3-responding-to-dsrs-for-system-generated-logs).

**Quels types de données doivent faire l’objet d’une recherche ?**

Les données à caractère personnel peuvent se trouver dans les données client, les informations générées par les produits et services Microsoft et les journaux générés par le système.

**Comment les données à caractère personnel doivent-elles être recherchées ?**

La recherche de données à caractère personnel peut varier entre les produits et services Microsoft. Les outils de recherche incluent la [recherche de contenu](/microsoft-365/compliance/gdpr-dsr-office365#using-the-content-search-ediscovery-tool-to-respond-to-dsrs) ou la capacité [de recherche dans l’application](/microsoft-365/compliance/gdpr-dsr-office365#using-in-app-functionality-to-respond-to-dsrs). Les administrateurs peuvent accéder aux [journaux générés par le système](/microsoft-365/compliance/gdpr-dsr-office365#part-3-responding-to-dsrs-for-system-generated-logs) associés à l’activité d’un utilisateur.  

**Dans quels formats est-ce que les données personnelles doivent être disponibles ?**

Le « droit à la portabilité des données » du RGPD permet à la personne concernée par le traitement des données de demander une copie des données à caractère personnel dans un « format lisible par machine, fréquemment utilisé et structuré » et demander à votre organisation de transmettre ces fichiers à une autre entité de contrôle des données.

**Quelles sont les exigences du RGPD et quelles sont mes responsabilités en tant que contrôleur ?**

En tant que contrôleur, le RGPD exige que vous puissiez effectuer ce qui suit :

- Fournir aux personnes concernées une copie de leurs données personnelles, ainsi qu’une description des catégories des données qui sont traitées, des objectifs de ce traitement et des catégories de tiers auxquels leurs données peuvent être divulguées.
- Aider les individus à exercer leur droit de corriger des données personnelles incorrectes, d’effacer des données ou de limiter leur traitement, de recevoir leurs données dans un formulaire lisible et, le cas échéant, de remplir une demande afin de transmettre leurs données à un autre contrôleur.

**Quelles sont les exigences du RGPD et quelles sont les responsabilités de Microsoft en tant que responsable du traitement ?**

Nous devons implémenter les mesures techniques et organisationnelles appropriées afin de vous aider à répondre aux demandes des personnes concernées par le traitement des données cherchant à exercer leurs droits indiqués ci-dessus.

**Où puis-je trouver des informations sur le RGPD pour les serveurs locaux ?**

Vous trouverez ici une série d'articles relatifs à la RGPD. Produits par Microsoft, ils fournissent les approches recommandées pour la charge de travail locale pour SharePoint Server, Exchange Server, Project Server, Office Web Apps Server, Office Online Server et les partages de fichiers locaux.

**Moyens mis à votre disposition par Microsoft pour vous permettre de répondre aux demandes des personnes concernées ?**

Online Services offre un éventail de fonctionnalités pour vous permettre, en tant que contrôleur, de répondre à la demande d’une personne concernée par les données. Les contrôles administratifs et les services en ligne d’entreprise de Microsoft vous aident à réagir concernant les données personnelles en réponse aux demandes de droits des personnes concernées par les données, ce qui vous permet de repérer, disposer, rectifier, limiter, supprimer et exporter des données personnelles qui résident dans les données gérées par le contrôleur stockées dans le cloud Microsoft. Online Services fournit également les données dans un formulaire lisible par machine si nécessaire.

## <a name="data-protection-impact-assessment"></a>Analyses d’impact sur la protection des données

En vertu du RGPD, les contrôleurs de données sont requis de préparer une [analyse d’impact sur la protection des données](gdpr-data-protection-impact-assessments.md) (DPIA) pour les opérations « susceptibles de générer un risque élevé pour les droits et libertés des personnes physiques ». Il n’existe aucun élément inhérent aux produits et services Microsoft nécessitant la création d’une DPIA. Cela dépend plutôt des détails de la configuration Microsoft. Une liste de détails devant être pris en compte dans Office est disponible dans [Contenu d’une DPIA](/microsoft-365/compliance/gdpr-dpia-office365#part-2--contents-of-a-dpia)

### <a name="dpia-faqs"></a>Forum aux questions sur la DPIA

**Quand devez-vous mener une DPIA ?**

Les contrôleurs sont requis d’effectuer une DPIA pour résoudre les problèmes relatifs à la sécurité des données à caractère personnel ou en raison d’une violation de données. Des exemples spécifiques de facteurs de risque dans Office sont traités dans [Déterminer si une analyse d’impact sur la protection des données est nécessaire](/microsoft-365/compliance/gdpr-dpia-office365#part-1--determining-whether-a-dpia-is-needed).  

**Qu’est-ce qui est requis pour effectuer une DPIA ?**

Le RGPD impose qu’une DPIA inclut les éléments suivants :

- Évaluation du besoin et de la proportionnalité du traitement des données par rapport aux finalités prévues de la DPIA.
- Évaluation des risques concernant les droits et les libertés des personnes concernées par les données.
- Les mesures envisagées pour lutter contre les risques, les garanties, les mesures de sécurité et les mécanismes pour assurer la protection des données à caractère personnel et prouver la conformité avec le RGPD.

**Quelles sont mes responsabilités en tant que contrôleur ?**

Selon le RGPD, en tant que contrôleur, vous devez effectuer les analyses d’impact sur la protection des données avant tout traitement de données pouvant potentiellement entraîner un risque élevé concernant les droits et libertés des personnes, en particulier pour les traitements utilisant les nouvelles technologies. Le RGPD fournit la liste non exhaustive suivante des cas où les analyses d’impact sur la protection des données doivent être effectuées :

- Traitement automatisé à des fins de profilage et d’activités similaires ayant des conséquences légales ou un impact significatif sur les personnes concernées ;  
- Traitement à grande échelle de catégories spéciales de données personnelles (révélant l’origine raciale ou ethnique, les opinions politiques et autres) ou de données relatives aux condamnations pénales et aux délits commis ;  
- Surveillance systématique d’une zone publiquement accessible à grande échelle.  

Le RGPD exige également que vous consultiez votre autorité de protection des données (DPA) avant de commencer tout traitement si vous ne pouvez pas identifier les processus suffisants pour réduire au maximum les risques élevés pour les personnes concernées. 

**Quelles sont les responsabilités Microsoft ?**

Microsoft pratique la confidentialité dès la conception et la confidentialité par défaut dans ses fonctions métiers et d’ingénierie. Dans le cadre de ces efforts, Microsoft soumet à des vérifications de confidentialité complètes les opérations de traitement des données susceptibles d’avoir un impact sur les droits et libertés individuelles des personnes concernées. Les équipes responsables de la confidentialité intégrées aux groupes de service vérifient la conception et l’implémentation des services pour s’assurer que le traitement des données personnelles respecte les lois internationales, les attentes de l’utilisateur et nos engagements explicites.

Ces vérifications de la confidentialité tendent à être granulaires : un même service peut en recevoir des dizaines, voire des centaines. Microsoft répète ces vérifications granulaires de la confidentialité dans les analyses d’impact sur la protection des données (DPIA) couvrant les principaux groupements de traitement, que le délégué à la protection des données de Microsoft UE vérifie. Le délégué à la protection des données évalue les risques liés au traitement des données pour s’assurer que la quantité d’atténuations mises en place est suffisante. S’il repère des risques non atténués, es modifications sont recommandées à nouveau au groupe Ingénierie. Si les risques liés à la protection des données changent, les analyses d’impact sur la protection des données sont vérifiées et mises à jour.


En tant que responsable du traitement des données, Microsoft est tenu d’aider les contrôleurs à assurer la conformité aux exigences de DPIA définies dans le RGPD. Dans le souci d’accompagner nos clients, des résumés des différentes sections des DPIA de Microsoft seront prochainement disponibles dans cette section. Ils serviront de base aux contrôleurs qui utilisent les services Microsoft pour la création de leurs propres DPIA.

## <a name="breach-notification"></a>Notification de violation

Le RGPD impose des exigences de notification aux responsables du traitement des données et aux contrôleurs pour une violation de données à caractère personnel. En tant que responsable du traitement des données, Microsoft s’assure que les clients peuvent répondre aux exigences de notification de violation du RGPD. Les contrôleurs de données sont chargés d'évaluer les risques liés à la confidentialité des données et de déterminer si le contrat de traitement des données d’un client doit être notifié en cas de violation. Microsoft fournit les informations nécessaires pour effectuer cette évaluation. Plus d’informations sur la façon dont Microsoft détecte et répond à une violation des données à caractère personnel dans [Notification des violations de données en vertu du RGPD](gdpr-breach-notification.md).

### <a name="breach-notification-faqs"></a>Foires aux questions sur la notification de violation

**Selon le RGPD, qu’est-ce qu’une violation de données personnelles ?**

Les données personnelles correspondent aux informations relatives à un individu permettant de l’identifier directement ou indirectement. Une violation de données personnelles correspond à « une violation de la sécurité entraînant la destruction involontaire ou contraire à la loi de données personnelles transmises, stockées ou autrement traitées, ou bien leur perte, modification ou divulgation ou consultation non autorisée ».

**Quelles sont vos responsabilités en tant que contrôleur ?**

Si une violation de données personnelles susceptible d’entraîner un risque élevé pour les droits et libertés des personnes (par exemple, la discrimination, l’usurpation d’identité, la fraude, la perte financière ou l’atteinte à leur réputation) se produit, le RGPD exige que vous procédiez comme indiqué ci-dessous :

- Informez l’autorité de protection des données (DPA) appropriée dans les 72 heures suivant la découverte d’une violation, par exemple après la notification de Microsoft. Si vous n’informez pas la DPA avant la fin de ce délai, vous devez vous justifier auprès d’elle. Cette notification à la DPA est obligatoire, même si elle représente un risque pour les individus tant que ce risque n’est pas élevé.
- Avertissez dès que possible les personnes concernées par les données en cas de violation.
- Documentez la violation, notamment avec une description de la nature de la violation, par exemple, le nombre de personnes affectées, le nombre d’enregistrements de données concernés, les conséquences de la violation et les mesures correctives proposées par votre organisation.

**Quelles sont les responsabilités Microsoft en tant que responsable du traitement ?**

Une fois informés d’une violation de données personnelles, nous sommes tenus par le RGPD de vous en informer dans les meilleurs délais. Lorsque Microsoft est un responsable du traitement, nos obligations reflètent les exigences du RGPD et nos dispositions contractuelles internationales standard. Nous estimons que toutes les violations de données personnelles confirmées sont concernées. Il n’existe aucun seuil de risque. Nous informons nos clients lorsque la violation de données a été subie directement par Microsoft ou par l’un de nos sous-traitants. Nous avons mis en place des processus permettant d’identifier et de contacter rapidement le personnel chargé de la sécurité en cas d’incident que vous avez identifié dans votre organisation. Par ailleurs, tous les sous-traitants sont contractuellement tenus de signaler leurs propres violations à Microsoft et d’offrir des garanties à cet effet.

**Comment MIcrosoft détecte une violation de données ?**

Tous nos services et employés suivent les procédures de gestion des incidents internes pour s’assurer que nous prenons les précautions appropriées afin d’éviter les violations de données. De plus, Online Services dispose de contrôles de sécurité spécifiques sur nos plateformes pour détecter les rares cas de violations de données.

**Comment Microsoft réagit face à une violation de données ?**

Pour vous assister en cas de violation de données personnelles, Microsoft dispose de ce qui suit :
    - Un personnel chargé de la sécurité formé aux procédures spécifiques à suivre.
    - Des stratégies, des procédures et des contrôles visant à vous assurer que Microsoft conserve des enregistrements détaillés. Cette réponse inclut la documentation sur les détails de l’incident, ses effets et les mesures correctives adoptées, ainsi que les informations de suivi et de stockage dans nos systèmes de gestion des incidents.

**Comment Microsoft m’avertit en cas de violation de données ?**

Microsoft a établi des stratégies et des procédures pour vous avertir rapidement. Pour vous permettre de remplir vos obligations en matière de notification à la DPA, nous fournissons une description du processus utilisé pour déterminer si une violation de données personnelles s’est produite, de la nature de la violation et des mesures que nous avons prises pour la corriger.

## <a name="accountability-readiness-checklists-for-the-gdpr"></a>Listes de vérification de préparation sur la responsabilité concernant le RGPD

Ces [listes de vérification](gdpr-arc.md) permettent d’accéder en toute simplicité aux informations dont vous pouvez avoir besoin pour prendre en charge le RGPD lors de l’utilisation de produits Microsoft. Vous pouvez gérer les éléments de la liste de vérification à l’aide du [Gestionnaire de Conformité Microsoft](/microsoft-365/compliance/compliance-manager) en indiquant l’ID de Contrôle et le Titre de Contrôle sous Contrôles Gérés par le Client dans la vignette RGPD.

## <a name="gdpr-faqs"></a>Forum aux questions sur le RGPD

**Microsoft a-t-il des engagements envers ses clients en ce qui concerne le RGPD ?**

Oui. Le RGPD exige que les responsables du traitement (telles des organisations utilisant les services en ligne d’entreprise de Microsoft ) utilisent uniquement des sous-traitants de données (tels que Microsoft) offrant des garanties suffisantes quand à leur capacité à satisfaire aux principales exigences du RGPD. Microsoft a pris l’initiative de prendre ces engagements envers tous ses clients titulaires de licences en volume dans le cadre de leurs contrats.

**Comment est-ce que Microsoft me permet de me conformer ?**

Microsoft fournit des outils et de la documentation pour vous aider à assumer les responsabilités liées à votre RGPD. Cela inclut la prise en charge des droits de l’objet de données, l’exécution de vos propres analyses d’impact sur la protection des données et la collaboration pour résoudre les violations de données personnelles.

**Quels engagements se trouvent dans les conditions RGPD ?**

Les conditions RGPD de Microsoft reflètent les engagements requis des responsables du traitement à l’article 28. L’article 28 exige que les responsables du traitement s’engagent à :

- N’utiliser que les sous-responsables du traitement avec le consentement du contrôleur et demeurez responsable des sous-responsables du traitement.
- Traiter les données personnelles uniquement pour les instructions du contrôleur, y compris en relation avec les transferts.
- Assurer que les personnes qui traitent des données personnelles s'engagent à respecter la confidentialité.
- Mettre en place des mesures techniques et organisationnelles appropriées pour garantir un niveau de sécurité des données personnelles approprié au risque.
- Assister les contrôleurs dans leur obligation de répondre aux demandes des sujets de données pour exercer leurs droits RGPD.
- Répondre aux exigences en matière de notification de violation et d’assistance.
- Aider les contrôleurs à réaliser des analyses d’impact sur la protection des données et à consulter les autorités de contrôle.
- Supprimer ou renvoyer des données personnelles à la fin de la prestation de services.
- Prendre en charge du contrôleur avec une preuve de conformité avec le RGPD.

**Sous quelle base Microsoft facilite-t-il le transfert de données personnelles en dehors de l’UE ?**

Microsoft utilise depuis longtemps les clauses contractuelles standard (également appelées clauses de modèle) comme base de transfert de données pour ses services en ligne d'entreprise. Les clauses contractuelles standard sont des termes standard fournis par la Commission européenne, qui peuvent être utilisés pour transférer des données en dehors de l’espace économique européen de façon conforme. Microsoft a incorporé les clauses contractuelles standard dans tous nos contrats de licence en volume via les [Conditions d’utilisation des services en ligne](http://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46). L’article 29 a détecté que la mise en place des clauses contractuelles standard par Microsoft est conforme. Lorsque le bouclier de protection des données UE-US est devenu disponible, Microsoft a été la première entreprise à certifier. Pour plus d’informations, consultez [Certification Microsoft du bouclier de protection des données](https://www.privacyshield.gov/participant?id=a2zt0000000KzNaAAK&status=Active)et lisez les [Conditions d’utilisation des services en ligne](http://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46). Le bouclier de protection des données EU-US permet aux clients qui souhaitent transférer leurs données vers les États-Unis de façon cohérente avec leurs obligations en matière de protection des données.

**Quelles sont les autres offres de conformité Microsoft ?**

En tant qu’entreprise mondiale avec des clients dans presque tous les pays au monde, Microsoft dispose d’un solide portefeuille de conformité pour aider ses clients. Pour consulter la liste complète des offres de conformité, notamment FedRamp, HIPAA/Hi, ISO 27001, ISO 27002, ISO 27018, NIST 800-171, G-Cloud Royaume-Uni et bien d’autres encore, visitez nos [rubriques d’offre de conformité](offering-home.yml).

**Quel effet le RGPD aura-t-il sur mon entreprise ?**

Le RGPD impose de nombreuses exigences sur les organisations qui collectent ou traitent des données personnelles, y compris une obligation de respecter les six principes clés :

- *Transparence*, *équité* et *légalité* dans la manipulation et l’utilisation des données personnelles. Vous devrez être clair avec les personnes concernées sur la façon dont vous utilisez les données à caractère personnel et vous avez également besoin d'une « base licite » pour traiter ces données.
- Limiter le traitement de données personnelles à *spécifié*, *explicite* et *à des fins légitimes*. Vous ne pourrez pas réutiliser ou divulguer des données personnelles à des fins non « compatibles » avec l’objectif pour lequel les données ont été collectées à l’origine.
- *Réduire la collecte et le stockage des données personnelles* à celles qui sont adéquates et pertinentes pour l’objectif attendu.
- Garantir la *l’exactitude des données personnelles* et leur permettre d’être *effacé ou rectifié*. Vous devez prendre des mesures pour vous assurer que les données personnelles que vous conservez sont exactes et peuvent être corrigées en cas d’erreur.
- *Limiter le stockage des données personnelles*. Vous devez vous assurer que vous conservez les données personnelles uniquement pendant toute la durée nécessaire pour atteindre les objectifs pour lesquels les données ont été collectées.
- Garantir *la sécurité*, *l’intégrité* et la *confidentialité des données personnelles*. Votre organisation doit prendre des mesures pour assurer la sécurité des données personnelles par le biais de mesures de sécurité techniques et organisationnelles.

Vous devez comprendre quelles sont les obligations spécifiques de votre organisation envers le RGPD et comment les respecter, même si Microsoft est là pour vous aider dans votre parcours de mise en conformité du RGPD.

**Quels droits les entreprises doivent-elles respecter dans le cadre du RGPD ?**

Le RGPD offre aux résidents de l’UE un contrôle sur leurs données personnelles par l’intermédiaire d’un groupe de « droits de sujet de données ». Cela inclut le droit à :

- Accéder à des informations sur l’utilisation des données personnelles.
- Accéder à des données personnelles détenues par une organisation.
- Des données personnelles incorrectes ont été supprimées ou corrigées.
- Faire rectifier et effacer les données personnelles dans certaines circonstances (parfois appelé « droit à être oublié »).
- Limiter ou s'opposer au traitement automatisé des données personnelles.
- Recevoir une copie des données personnelles.

**Que désignent les termes « sous-traitants » et « responsables du traitement » ?**

Un responsable du traitement est une personne physique ou morale, une autorité publique, une agence ou un autre organisme qui, seul ou conjointement avec d’autres, détermine les finalités et les moyens du traitement des données à caractère personnel. Une responsable du traitement est une personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui traite des données personnelles pour le compte de l’entité de contrôle.

**Le RGPD s’applique-t-il aux responsables du traitement et aux contrôleurs ?**

Oui, le RGPD s’applique aux contrôleurs et responsables du traitement. Les contrôleurs doivent utiliser uniquement les responsables du traitement qui prennent des mesures pour satisfaire aux exigences du RGPD. Dans le cadre du RGPD, les responsables du traitement ont des obligations et des responsabilités supplémentaires pour la non-conformité, ou à l’extérieur des instructions fournies par le contrôleur, comparées à la directive sur la protection des données. Les obligations du responsable du traitement incluent, sans s’y limiter à :

- Traiter les données uniquement conformément aux instructions du contrôleur.
- Utiliser des mesures techniques et organisationnelles appropriées pour protéger les données personnelles.
- Assister le contrôleur avec des demandes d’objet de données.
- S’assurer que les sous-responsables du traitement qu'elle engage répondent à ces exigences.

**Quel est le montant des amendes auxquelles les entreprises s’exposent en cas de non-conformité ?**

Les entreprises peuvent se voir infliger des amendes allant jusqu'à &euro;20 millions d'euros ou 4 % du chiffre d'affaires mondial annuel, le montant le plus élevé étant retenu, pour non-respect de certaines exigences du RGPD. D’autres recours peuvent augmenter votre risque si vous ne parvenez pas à respecter les exigences du RGPD.

**Mon entreprise doit-elle nommer un délégué à la protection des données (DPO) ?**

Cela dépend de plusieurs facteurs identifiés dans le règlement. L’article 37 du RGPD indique que les contrôleurs et les responsables du traitement désignent un délégué à la protection des données, quel qu’en soit le cas : (a) le traitement est effectué par une autorité ou un organisme public, à l’exception des tribunaux qui agissent en leur qualité judiciaire ; (b) les activités fondamentales du contrôleur ou du responsable du traitement sont des opérations de traitement qui, de par leur nature, leur champ d’application et/ou leur finalité, ont besoin d’une surveillance régulière et systématique des sujets de données à grande échelle. ou (c) les activités fondamentales du contrôleur ou du responsable du traitement sont des traitements sur une grande échelle de catégories de données spéciales conformément à l’article 9 et des données personnelles relatives aux convictions pénales et aux infractions visées à l’article 10.

**Quel sera le coût de la mise en conformité avec le RGPD ?**

Se conformer au GDPR coûtera du temps et de l'argent à la plupart des organisations, bien que la transition puisse être plus facile pour celles qui opèrent dans un modèle de services cloud bien architecturé et qui ont mis en place un programme efficace de gouvernance des données.

**Comment savoir si les données traitées par mon organisation sont couvertes par le RGPD ?**

Le RGPD régule la collecte, l’espace de stockage, l’utilisation et le partage des « données personnelles ». Dans le RGPD, les données personnelles sont définies de façon générale comme toute donnée relative à une personne physique identifiée ou identifiable.

Les données personnelles peuvent inclure, sans s’y limiter, les identifiants en ligne (par exemple, les adresses IP), les informations des employés, les bases de données des ventes, les données des services clients, les formulaires de commentaires des clients, les données de localisation, les données biométriques, le métrage CCTV, les enregistrements de la fidélité, l’état d’intégrité et les informations financières, et bien plus encore. Elles peuvent même inclure des informations qui ne semblent pas être personnelles (par exemple, photo d’un paysage sans personne) où ces informations sont liées à l’aide d’un numéro de compte ou d’un code unique à un individu identifiable. Et même les données personnelles qui ont été pseudonymisées peuvent être des données personnelles si le pseudonyme peut être lié à un individu particulier. 

Le traitement de certaines catégories « spéciales » de données personnelles, telles que les données personnelles révélant l’origine raciale ou ethnique de la personne, ou le problème de santé ou de son orientation sexuelle, est soumis à des règles plus strictes que le traitement des données personnelles « ordinaires ». Cette évaluation des données personnelles est fortement précise. Nous vous recommandons donc de faire appel à un expert pour évaluer vos propres circonstances.

**Mon organisation ne traite des données que pour le compte d'autres personnes. Est-il encore nécessaire de respecter les RGPD ?**

Oui. Bien que les règles diffèrent quelque peu, le RGPD s’applique aux organisations qui collectent et traitent des données pour leurs propres objectifs (« contrôleurs »), ainsi qu’aux organisations qui traitent des données pour le compte d’autres personnes (« responsables de traitement »). Cette exigence s'écarte de l'actuelle directive sur la protection des données, qui s'applique aux contrôleurs.

**Quelles données sont spécifiquement considérées comme étant de caractère personnel ?**

Les données à caractère personnel englobent toutes les informations relatives à une personne identifiée ou identifiable. Aucune distinction n’est faite entre les rôles privé, public et professionnel d’une personne. Les données personnelles peuvent inclure :

- Nom
- Adresse privée
- Adresse de travail
- Numéro de téléphone
- Numéro de portable
- Adresse e-mail
- Numéro de passeport
- Numéro de carte d’identité nationale
- Numéro de sécurité sociale (ou équivalent)
- Permis de conduire
- Informations physiques, physiologiques ou génétiques
- Informations médicales
- Identité culturelle
- Coordonnées bancaires / numéros de compte
- Numéro de dossier fiscal
- Adresse de travail
- Numéro de carte de crédit/débit
- Billets de réseaux sociaux
- Adresse IP (région UE)
- Données de localisation/GPS
- Cookies

**Est-il possible de transférer des données hors de l’UE ?**

Oui. Toutefois, le RGPD réglemente strictement les transferts de données personnelles des résidents européens aux destinations en dehors de l’espace économique européen. Vous devrez peut-être configurer un mécanisme juridique spécifique (par exemple, contrat) ou adhérer à un mécanisme de certification pour activer ces transferts. Microsoft détaille les mécanismes que nous utilisons dans les conditions d’utilisation des services en ligne.

**Nous respectons les exigences en matière de rétention des données. Ces exigences ont-elles priorité sur le droit d’effectuer l’effacement ?**

Lorsqu’il existe des raisons légitimes de continuer à traiter et de répartir les données, telles que « pour assurer le respect d’une obligation légale, qui exige un traitement par l’Union ou la Loi de l’État membre auquel le responsable est soumis » (article 17 paragraphe 3 point b), le RGPD reconnaît que Il se peut que les organisations soient tenues de conserver les données. Toutefois, vous devez vous assurer que vous faites appel à votre conseiller juridique pour vous assurer que les justifications de la rétention sont pesées par rapport aux droits et libertés des sujets de données, à leurs attentes au moment de la collecte des données, etc.

**Le RGPD a-t-il trait au chiffrement ?**

Le chiffrement est identifié dans le RGPD comme mesure de protection qui rend les données personnelles inintelligibles lorsqu’elles sont affectées par une violation. Par conséquent, la possibilité d’utiliser ou non le chiffrement peut avoir un impact sur les exigences en matière de notification de divulgation de données personnelles. Le RGPD indique également le chiffrement en tant que mesure technique ou organisationnelle appropriée dans certains cas, en fonction des risques. Le chiffrement est également requis par la norme de sécurité de l'industrie des cartes de paiement et qui fait partie des recommandations en matière de conformité strictes spécifiques au secteur des services financiers. Les produits et services Microsoft tels qu’Azure, Dynamics 365, Enterprise Mobility + Security, Office Microsoft 365, Serveur SQL /base de données Azure SQL et Windows 10 proposent un chiffrement fiable pour les données en transit et les données au repos.

**Comment le RGPD modifie-t-il la réponse d’une organisation aux violations de données personnelles ?**

Le RGPD modifie les exigences en matière de protection des données et impose des obligations plus strictes aux responsables de données et aux contrôleurs en relation avec les violations de données personnelles. Dans le cadre du nouveau règlement, le responsable du traitement doit avertir le contrôleur de données d’une violation de données personnelles, une fois qu’il a pris connaissance de celle-ci, sans délai injustifié. Une fois qu'il a connaissance d'une violation de données personnelles, le contrôleur doit en informer l'autorité compétente en matière de protection des données dans un délai de 72 heures. Si la violation risque de générer un risque élevé pour les droits et libertés de personnes, les contrôleurs devront également avertir les personnes concernées sans délai injustifié. Des conseils supplémentaires sur ce sujet sont mis au point par l’article 29 de l’UE.

Les produits et services Microsoft (par exemple, Azure, Dynamics 365, Enterprise Mobility + Security, Microsoft Office 365 et Windows 10) intègrent actuellement des solutions pour vous aider à détecter et évaluer les menaces et violations à la sécurité et à respecter la notification de violation du RGPD résultant.

## <a name="additional-resources"></a>Ressources supplémentaires

- [Répondez à vos besoins en matière de RGPD avec l’un de nos partenaires mondiaux proposant des solutions basées sur Microsoft](https://aka.ms/findgdprpartner)
- [Découvrez comment Microsoft gère vos données, leur emplacement, les utilisateurs qui peuvent y accéder et les conditions d’utilisation, et bien plus encore.](https://www.microsoft.com/trust-center/privacy)
- [Découvrez comment Microsoft respecte les principes de l’UE-US. cadre de bouclier de protection des données](https://blogs.microsoft.com/eupolicy/2016/07/11/eu-u-s-privacy-shield-progress-for-privacy-rights/)
- [Comment Microsoft détecte et répond à une violation de données personnelles, puis vous en informe dans le cadre du RGPD](https://www.microsoft.com/trust-center/privacy/gdpr-data-breach)
- [Évaluez votre état de préparation au RGPD aujourd’hui](https://discover.microsoft.com/gdpr-readiness-assessment/)

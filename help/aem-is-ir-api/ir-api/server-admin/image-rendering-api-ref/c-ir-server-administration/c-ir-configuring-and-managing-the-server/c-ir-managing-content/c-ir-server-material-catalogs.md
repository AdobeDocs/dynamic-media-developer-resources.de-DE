---
description: Materialkataloge bieten viele Bildwiedergabekonfigurationseinstellungen.
solution: Experience Manager
title: Materialkataloge
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Materialkataloge{#material-catalogs}

Materialkataloge bieten viele Bildwiedergabekonfigurationseinstellungen.

Materialkataloge ordnen Vignetten- und Material-IDs, die in Anforderungen verwendet werden, tatsächlichen Dateipfaden zu, können alle mit Materialien verknüpften Metadaten speichern und Container für Vorlagen bereitstellen. Sie verfolgen die ICC-Profil und Kommandomakros.

Auf Materialkataloge kann nur über die Java-Komponente des Image Rendering (in Zusammenarbeit mit dem Plattformserver) zugegriffen werden. Katalogattributdateien müssen das Suffix [!DNL .ini] haben und im registrierten Katalogordner ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)) abgelegt werden. Der Standard-Materialkatalog ( [!DNL default.ini]) muss immer vorhanden sein und mit allen Attributen gefüllt werden, damit Image Serving ordnungsgemäß funktioniert.

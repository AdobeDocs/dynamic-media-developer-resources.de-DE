---
description: Materialkataloge bieten viele Bildwiedergabekonfigurationseinstellungen.
seo-description: Materialkataloge bieten viele Bildwiedergabekonfigurationseinstellungen.
seo-title: Materialkataloge
solution: Experience Manager
title: Materialkataloge
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d209019-f9ca-43e4-900b-3597c7044a79
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Materialkataloge{#material-catalogs}

Materialkataloge bieten viele Bildwiedergabekonfigurationseinstellungen.

Materialkataloge ordnen Vignetten- und Material-IDs, die in Anforderungen verwendet werden, tatsächlichen Dateipfaden zu, können alle mit Materialien verknüpften Metadaten speichern und Container für Vorlagen bereitstellen. Sie verfolgen die ICC-Profil und Kommandomakros.

Auf Materialkataloge kann nur über die Java-Komponente des Image Rendering (in Zusammenarbeit mit dem Plattformserver) zugegriffen werden. Katalogattributdateien müssen über ein [!DNL .ini] Suffix verfügen und im registrierten Katalogordner ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)) abgelegt werden. Der Standardmaterialkatalog ( [!DNL default.ini]) muss immer vorhanden sein und mit allen Attributen gefüllt werden, damit Image Serving ordnungsgemäß funktioniert.

---
description: Materialkataloge bieten viele Konfigurationseinstellungen für das Image Rendering.
solution: Experience Manager
title: Materialkataloge
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# Materialkataloge{#material-catalogs}

Materialkataloge bieten viele Konfigurationseinstellungen für das Image Rendering.

Materialkataloge ordnen Vignetten und Material-IDs, die in Anforderungen verwendet werden, den tatsächlichen Dateipfaden zu, können alle mit Materialien verknüpften Metadaten speichern und Container für Vorlagen bereitstellen. Sie verfolgen ICC-Profile und Befehlsmakros.

Auf Materialkataloge kann nur über die Java-Komponente des Image Rendering (gemeinsam mit dem Platform Server) zugegriffen werden. Katalogattributdateien müssen das Suffix [!DNL .ini] aufweisen und im registrierten Katalogordner ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)) abgelegt werden. Der Standard-Materialkatalog ( [!DNL default.ini]) muss immer vorhanden sein und mit allen Attributen ausgefüllt werden, damit das Image Serving ordnungsgemäß funktioniert.

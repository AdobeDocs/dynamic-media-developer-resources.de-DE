---
description: Materialkataloge bieten viele Image-Rendering-Konfigurationseinstellungen.
solution: Experience Manager
title: Materialkataloge
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Materialkataloge{#material-catalogs}

Materialkataloge bieten viele Image-Rendering-Konfigurationseinstellungen.

Materialkataloge ordnen Vignetten- und Material-IDs, die in Anfragen verwendet werden, tatsächlichen Dateipfaden zu, können alle mit Materialien verknüpften Metadaten speichern und Container für Vorlagen bereitstellen. Sie verfolgen ICC-Profile und Befehlsmakros.

Auf Materialkataloge kann nur über die Java-Komponente des Bild-Renderings zugegriffen werden (die sich zusammen mit dem [!DNL Platform Server] befindet). Katalogattributdateien müssen ein [!DNL .ini] Suffix aufweisen und im registrierten Katalogordner platziert werden ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Der Standardmaterialkatalog ([!DNL default.ini]) muss immer vorhanden sein und mit allen Attributen ausgefüllt sein, damit die Bildbereitstellung ordnungsgemäß funktioniert.

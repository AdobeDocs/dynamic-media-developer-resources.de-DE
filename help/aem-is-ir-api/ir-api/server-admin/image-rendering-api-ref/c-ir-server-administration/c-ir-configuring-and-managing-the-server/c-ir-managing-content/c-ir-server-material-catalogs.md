---
description: Materialkataloge bieten viele Image-Rendering-Konfigurationseinstellungen.
solution: Experience Manager
title: Materialkataloge
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
TQID: 'https://experienceleague.adobe.com/FOwuQrKYaRJ78mdRbPeoy71crT9GHj4R5MXFbMGnrZE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 0%

---

# Materialkataloge{#material-catalogs}

Materialkataloge bieten viele Image-Rendering-Konfigurationseinstellungen.

Materialkataloge ordnen Vignetten- und Material-IDs, die in Anfragen verwendet werden, tatsächlichen Dateipfaden zu, können alle mit Materialien verknüpften Metadaten speichern und Container für Vorlagen bereitstellen. Sie verfolgen ICC-Profile und Befehlsmakros.

Auf Materialkataloge kann nur über die Java-Komponente des Bild-Renderings zugegriffen werden (die sich zusammen mit dem [!DNL Platform Server] befindet). Katalogattributdateien müssen ein [!DNL .ini] Suffix aufweisen und im registrierten Katalogordner platziert werden ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Der Standardmaterialkatalog ([!DNL default.ini]) muss immer vorhanden sein und mit allen Attributen ausgefüllt sein, damit die Bildbereitstellung ordnungsgemäß funktioniert.


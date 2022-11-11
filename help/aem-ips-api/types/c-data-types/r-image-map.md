---
description: Targeting einer Klickaktion im Browser.
solution: Experience Manager
title: Imagemap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 7%

---

# [!DNL ImageMap]{#imagemap}

Targeting einer Klickaktion im Browser.

Immer mit einem Bild verknüpft. Sie erhalten eine `ImageMap` Zielgruppe aus `ImageInfo`.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| imageMapHandle | `xsd:string` | Imagemap-Handle. |
| [!DNL name] | `xsd:string` | Name der Imagemap. |
| [!DNL region] | `xsd:string` | Imagemap-Koordinaten. Das Format basiert auf der HTML `<area>` Tag-Attribut. |
| [!DNL action] | `xsd:string` | Andere Attribute, die in die HTML aufgenommen werden sollen `<area>` -Tag, einschließlich `href` URL. |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] -Wert. |
| [!DNL position] | `xsd:string` | Position im Format der HTML `<area>` -Element [!DNL coords] -Attribut. Beispiel: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | True , wenn die Imagemap aktiviert ist. |
| lastModified | `xsd:dateTime` | Datum und Uhrzeit der letzten Änderung der Imagemap. |

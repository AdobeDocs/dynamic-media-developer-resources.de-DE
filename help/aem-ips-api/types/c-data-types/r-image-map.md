---
description: Ziel für eine Klick-Aktion im Browser.
solution: Experience Manager
title: Imagemap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---

# [!DNL ImageMap]{#imagemap}

Ziel für eine Klick-Aktion im Browser.

Immer mit einem Bild verknüpft. Sie können eine `ImageMap` Zielgruppe von `ImageInfo` erhalten.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| imageMapHandle | `xsd:string` | Imagemap-Handle. |
| [!DNL name] | `xsd:string` | Name der Imagemap. |
| [!DNL region] | `xsd:string` | Imagemap-Koordinaten. Das Format basiert auf dem `<area>`-Tag-Attribut von HTML. |
| [!DNL action] | `xsd:string` | Andere Attribute, die in das HTML-`<area>`-Tag aufgenommen werden sollen, einschließlich der `href`-URL. |
| formType | `xsd:boolean` | Ein [!DNL RegionShape]. |
| [!DNL position] | `xsd:string` | Position im Format des `<area>`-Attributs des HTML-[!DNL coords]. Beispiel: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | True, wenn die Imagemap aktiviert ist. |
| lastModify | `xsd:dateTime` | Datum und Uhrzeit der letzten Änderung der Imagemap. |

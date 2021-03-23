---
description: Zielgruppe für eine Klickaktion im Browser.
seo-description: Zielgruppe für eine Klickaktion im Browser.
seo-title: Imagemap
solution: Experience Manager
title: Imagemap
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 12%

---


# Imagemap{#imagemap}

Zielgruppe für eine Klickaktion im Browser.

Jederzeit einem Bild zugeordnet. Sie können eine `ImageMap`-Zielgruppe von `ImageInfo` abrufen.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | Imagemap-Handle. |
| `*`name`*` | `xsd:string` | Imagemap-Name. |
| `*`Region`*` | `xsd:string` | Imagemap-Koordinaten. Das Format basiert auf dem HTML `<area>`-Tag-Attribut. |
| `*`Aktion`*` | `xsd:string` | Andere Attribute, die in das HTML `<area>`-Tag eingeschlossen werden sollen, einschließlich der `href`-URL. |
| `*`shapeType`*` | `xsd:boolean` | Ein [!DNL RegionShape]-Wert. |
| `*`position`*` | `xsd:string` | Position im Format des HTML `<area>`-Elementattributs [!DNL coords]. Beispiel: `coords ="0,0,84,128"`. |
| `*`aktiviert`*` | `xsd:boolean` | True, wenn die Imagemap aktiviert ist. |
| `*`lastModified`*` | `xsd:dateTime` | Datum und Uhrzeit der letzten Änderung der Imagemap |


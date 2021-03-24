---
description: Zielgruppe für eine Klickaktion im Browser.
solution: Experience Manager
title: Imagemap
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '104'
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


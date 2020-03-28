---
description: Zielgruppe für eine Klickaktion im Browser.
seo-description: Zielgruppe für eine Klickaktion im Browser.
seo-title: Imagemap
solution: Experience Manager
title: Imagemap
topic: Scene7 Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Imagemap{#imagemap}

Zielgruppe für eine Klickaktion im Browser.

Jederzeit einem Bild zugeordnet. Sie können eine `ImageMap` Zielgruppe von `ImageInfo`.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | Imagemap-Handle. |
| ` *`name`*` | `xsd:string` | Imagemap-Name. |
| ` *`Region`*` | `xsd:string` | Imagemap-Koordinaten. Das Format basiert auf dem HTML- `<area>` Tag-Attribut. |
| ` *`Aktion`*` | `xsd:string` | Andere Attribute, die in das HTML- `<area>` Tag eingeschlossen werden sollen, einschließlich der `href` -URL. |
| ` *`shapeType`*` | `xsd:boolean` | Ein [!DNL RegionShape] Wert. |
| ` *`Position`*` | `xsd:string` | Position im Format des HTML- `<area>` - [!DNL coords] Elementattributs. Beispiel: `coords ="0,0,84,128"`. |
| ` *`aktiviert`*` | `xsd:boolean` | True, wenn die Imagemap aktiviert ist. |
| ` *`lastModified`*` | `xsd:dateTime` | Datum und Uhrzeit der letzten Änderung der Imagemap |


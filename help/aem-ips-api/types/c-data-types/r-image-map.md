---
description: Targeting einer Klickaktion im Browser.
solution: Experience Manager
title: Imagemap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 12%

---

# Imagemap{#imagemap}

Targeting einer Klickaktion im Browser.

Immer mit einem Bild verknüpft. Sie können ein `ImageMap`-Ziel von `ImageInfo` abrufen.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | Imagemap-Handle. |
| `*`name`*` | `xsd:string` | Name der Imagemap. |
| `*`Region`*` | `xsd:string` | Imagemap-Koordinaten. Das Format basiert auf dem HTML-Tag-Attribut `<area>` . |
| `*`Aktion`*` | `xsd:string` | Andere Attribute, die in das HTML-Tag `<area>` aufgenommen werden sollen, einschließlich der URL `href` . |
| `*`shapeType`*` | `xsd:boolean` | Ein [!DNL RegionShape] -Wert. |
| `*`position`*` | `xsd:string` | Position im Format des `<area>`-Attributs des HTML-Elements [!DNL coords]. Beispiel: `coords ="0,0,84,128"`. |
| `*`aktiviert`*` | `xsd:boolean` | True , wenn die Imagemap aktiviert ist. |
| `*`lastModified`*` | `xsd:dateTime` | Datum und Uhrzeit der letzten Änderung der Imagemap. |

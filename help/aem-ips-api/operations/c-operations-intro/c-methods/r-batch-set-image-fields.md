---
description: Legt bildspezifische Felder für ein oder mehrere Bild-Assets fest.
solution: Experience Manager
title: batchSetImageFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 10%

---

# batchSetImageFields{#batchsetimagefields}

Legt bildspezifische Felder für ein oder mehrere Bild-Assets fest.

Syntax

## Autorisierte Benutzertypen {#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-4969815cf67c4d11b13bb2017b3604e8}

**Eingabe (batchSetImageFields)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle für das Unternehmen, das die Bild-Assets enthält. |
| `*`updateArray`*` | `types:ImageFieldUpdateArray` | Ja | Das Array des Bildfelds wird aktualisiert. |

**Ausgabe (batchSetImageFields)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Ja | Die Anzahl der erfolgreich eingerichteten Bildfelder. |
| `*`warningCount`*` | `xsd:int` | Ja | Die Anzahl der Warnungen, die generiert wurden, wenn der Vorgang versuchte, die Bildfelder festzulegen. |
| `*`errorCount`*` | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch des Vorgangs erzeugt wurden, die Bildfelder festzulegen. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind, die Warnungen generiert haben, wenn der Vorgang versucht hat, die Aktualisierungen anzuwenden. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind, die Fehler generiert haben, wenn der Vorgang versucht hat, die Aktualisierungen anzuwenden. |

## Beispiele {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

In diesem Beispiel werden Daten in die Felder zweier Bilder in einem Aktualisierungs-Array gesetzt. Im Array werden die Bilder durch ihre Asset-Handles angegeben und enthalten die Auflösung in Pixel, X- und Y-Position-Ankerkoordinaten und Benutzerdaten. Die Antwort gibt an, dass Felder für beide Bilder erfolgreich festgelegt wurden.

**Anforderung**

```java
<batchSetImageFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|140626|1|102524</assetHandle>
         <resolution>72</resolution>
         <anchorX>50</anchorX>
         <anchorY>100</anchorY>
         <userData>nada1</userData>
      </items>
      <items>
         <assetHandle>a|96680|1|64865</assetHandle>
         <resolution>150</resolution>
         <anchorX>100</anchorX>
         <anchorY>50</anchorY>
         <userData>nada2</userData>
      </items>
   </updateArray>
</batchSetImageFieldsParam>
```

**Antwort**

```java
<batchSetImageFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetImageFieldsReturn>
```

---
description: Legt bildspezifische Felder für ein oder mehrere Bild-Assets fest.
seo-description: Legt bildspezifische Felder für ein oder mehrere Bild-Assets fest.
seo-title: batchSetImageFields
solution: Experience Manager
title: batchSetImageFields
topic: Scene7 Image Production System API
uuid: e0ad7da4-cb28-4402-8b47-a600916d23b3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 9%

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

**Input (batchSetImageFields)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, die die Bild-Assets enthält. |
| ` *`updateArray`*` | `types:ImageFieldUpdateArray` | Ja | Das Array der Bildfelder wird aktualisiert. |

**Output (batchSetImageFields)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Die Anzahl der erfolgreich eingerichteten Bildfelder. |
| ` *`warningCount`*` | `xsd:int` | Ja | Die Anzahl der Warnungen, die beim Versuch des Vorgangs generiert wurden, die Bildfelder festzulegen. |
| ` *`errorCount`*` | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch des Vorgangs generiert wurden, die Bildfelder festzulegen. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit Details zu den Assets, die Warnungen generiert haben, wenn der Vorgang versuchte, die Aktualisierungen anzuwenden. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit Details zu den Assets, die Fehler generiert haben, wenn der Vorgang versuchte, die Aktualisierungen anzuwenden. |

## Beispiele {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

In diesem Beispiel werden Daten in die Felder zweier Bilder in einem Aktualisierungsarray eingestellt. Im Array werden die Bilder durch ihre Asset-Handles angegeben und enthalten die Auflösung in Pixel, Ankerkoordinaten mit x- und y-Position sowie Benutzerdaten. Die Antwort zeigt an, dass Felder für beide Bilder erfolgreich festgelegt wurden.

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


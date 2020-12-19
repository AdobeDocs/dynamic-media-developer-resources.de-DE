---
description: Legt Metadatenfelder für Schriftarten fest.
seo-description: Legt Metadatenfelder für Schriftarten fest.
seo-title: batchSetFontFields
solution: Experience Manager
title: batchSetFontFields
topic: Scene7 Image Production System API
uuid: 0209865e-32b3-4bea-a508-05771a0365e1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 14%

---


# batchSetFontFields{#batchsetfontfields}

Legt Metadatenfelder für Schriftarten fest.

## Autorisierte Benutzertypen {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-836f5948d00a46e98ccb62f0573e4e68}

**Input (batchSetFontFieldsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Behandeln Sie die Firma, in der sich die Schriftarten befinden. |
| ` *`updateArray`*` | `types:FontFieldUpdateArray` | Ja | Array von Aktualisierungen für Schriftartenfelder. |

**Output (batchSetFontFieldsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Die Anzahl der erfolgreich eingerichteten Schriftartfelder. |
| ` *`warningCount`*` | `xsd:int` | Ja | Anzahl der Warnungen, die beim Versuch des Vorgangs generiert wurden, Schriftartfelder festzulegen. |
| ` *`errorCount`*` | `xsd:int` | Ja | Anzahl der Fehler, die beim Versuch des Vorgangs generiert wurden, Schriftartfelder festzulegen. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit Details zu den Assets, die Warnungen generiert haben, wenn der Vorgang versuchte, die Aktualisierungen anzuwenden. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit Details zu den Assets, die Fehler generiert haben, wenn der Vorgang versuchte, die Aktualisierungen anzuwenden. |

## Beispiele {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**Anforderung**

```java
<batchSetFontFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
          <assetHandle>a|450|14|19</assetHandle>
          <fontName>Bookman Old Style Font Name</fontName>
          <postscriptName>Bookman Old Style PostScript</postscriptName>
          <rtfName>Bookman Old Style RTF</rtfName>
          <fontFamily>Bookman Old Style Family</fontFamily>
          <style>BoldItalic</style>
          <typeName>Open Type</typeName><type>OTF</type>
      </items>
   </updateArray>
</batchSetFontFieldsParam>
```

**Antwort**

```java
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```


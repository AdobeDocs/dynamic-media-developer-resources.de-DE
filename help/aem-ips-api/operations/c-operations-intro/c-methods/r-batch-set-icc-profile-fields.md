---
description: Legt Metadatenfelder für ICC-Profile fest.
solution: Experience Manager
title: batchSetIccProfileFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 13%

---

# batchSetIccProfileFields{#batchseticcprofilefields}

Legt Metadatenfelder für ICC-Profile fest.

Syntax

## Autorisierte Benutzertypen {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**Input (batchSetIccProfileFields)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handle an das Unternehmen, das die ICC-Profile enthält. |
| Array aktualisieren | `xsd:string` | Ja | Array von ICC-Profilaktualisierungen. |

**Output (batchSetIccProfileFields)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Die Anzahl der erfolgreich eingerichteten ICC-Profilfelder. |
| warningCount | `xsd:int` | Ja | Die Anzahl der Warnungen, die generiert wurden, wenn der Vorgang versuchte, die ICC-Profilfelder festzulegen. |
| errorCount | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch des Vorgangs erzeugt wurden, die ICC-Profilfelder festzulegen. |
| warningDetailArray | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind, die Warnungen generiert haben, wenn der Vorgang versucht hat, die Aktualisierungen anzuwenden. |
| errorDetailArray | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind, die Fehler generiert haben, wenn der Vorgang versucht hat, die Aktualisierungen anzuwenden. |

## Beispiele {#section-5dc90cfbd9b1411485b44859032f7cb9}

**Anfrage**

```java {.line-numbers}
<batchSetIccProfileFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|1808|13|169</assetHandle>
         <class>Output</class>
         <colorSpace>CMYK</colorSpace>
         <pcsType>Luv</pcsType>
      </items>
   </updateArray>
</batchSetIccProfileFieldsParam>
```

**Antwort**

```java {.line-numbers}
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```

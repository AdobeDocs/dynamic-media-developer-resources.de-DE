---
description: Aktualisiert ein Bildset.
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: d8d5fb80-17f1-424f-8a61-27189f87d603
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 20%

---

# updateImageSet{#updateimageset}

Aktualisiert ein Bildset.

Syntax

## Parameter {#section-3be47dbbce474ce78676b05e163492e3}

**Eingabe (updateImageSetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, das das zu ändernde Bildset enthält. |
| assetHandle | `xsd:string` | JS | Das Handle für das Bildset, das Sie ändern möchten. |
| memberArray | `types:ImageSetMemberUpdateArray` | Nein | Setzt Bildset-Mitglieder zurück. |
| thumbAssetHandle | `xsd:string` | Nein | Der Handle des Assets, das als Miniaturansicht für das Bildset dient. |

**Ausgabe (updateImageSetReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| Sequenz |  |  |  |

## Beispiele {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Anforderung**

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**Antwort**

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

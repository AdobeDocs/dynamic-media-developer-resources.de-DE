---
description: Ruft ein Array von Elementen ab, die sich in einem Bildset befinden.
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 14%

---

# getImageSetMembers{#getimagesetmembers}

Ruft ein Array von Elementen ab, die sich in einem Bildset befinden.

Syntax

## Autorisierte Benutzertypen {#section-eaa3a167fa77403ea1b374b05fff4ded}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Erfordert Lesezugriff auf das Bild und das Elementset-Asset.

## Parameter {#section-a67ba98095574533980997c83ceaa316}

**Input (getImageSetMembersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, das das Bildset enthält. |
| assetHandle | `xsd:string` | Ja | Das Bildset-Asset-Handle. |

**Ausgabe (getImageSetMembersReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| memberArray | `types:ImageSetMemberArray` | Nein | Array von Bildset-Mitgliedern. |

## Beispiele {#section-888a9a78033346f39b171229de93dfa0}

Dieses Codebeispiel gibt bestimmte Bildset-Member zurück. Die Antwort gibt ein leeres -Array zurück.

**Anfrage**

```java
<ns1:getImageSetMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>34195|22|927</ns1:assetHandle>
</ns1:getImageSetMembersParam>
```

**Antwort**

```java
<getImageSetMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray></memberArray>
</getImageSetMembersReturn>
```

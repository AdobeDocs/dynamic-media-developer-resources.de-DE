---
description: Ruft ein Array von Mitgliedern ab, die sich in einem Bildsatz befinden.
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic, SDK/API, Bildsätze
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 15%

---


# getImageSetMembers{#getimagesetmembers}

Ruft ein Array von Mitgliedern ab, die sich in einem Bildsatz befinden.

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
>Erfordert Lesezugriff auf das Bild- und Mitgliederset-Asset.

## Parameter {#section-a67ba98095574533980997c83ceaa316}

**Input (getImageSetMembersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zu der Firma, die den Bildsatz enthält. |
| `*`assetHandle`*` | `xsd:string` | Ja | Das Asset-Handle des Bildsatzes. |

**Output (getImageSetMembersReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`memberArray`*` | `types:ImageSetMemberArray` | Nein | Array von Bildsatzmitgliedern. |

## Beispiele {#section-888a9a78033346f39b171229de93dfa0}

Dieses Codebeispiel gibt bestimmte Bildsatzmitglieder zurück. Die Antwort gibt ein leeres Array zurück.

**Anforderung**

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


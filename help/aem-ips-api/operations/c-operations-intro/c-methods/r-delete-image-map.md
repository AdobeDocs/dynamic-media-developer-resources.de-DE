---
description: Löscht eine Imagemap.
seo-description: Löscht eine Imagemap.
seo-title: deleteImageMap
solution: Experience Manager
title: deleteImageMap
uuid: 0abdf72c-f445-41d0-bd88-63b7ad1359d5
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 11%

---


# deleteImageMap{#deleteimagemap}

Löscht eine Imagemap.

Syntax

## Autorisierte Benutzertypen {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss Lese- und Schreibzugriff auf das Asset haben.

## Parameter {#section-28de12bab79045a5977c68855e37ae3d}

**Input (deleteImageMapParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zu der Firma, die die zu löschende Imagemap enthält. |
| `*`imageMapHandle`*` | `xsd:string` | Ja | Der Griff zur zu löschenden Imagemap. |

**Output (deleteImageMapParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Dieses Codebeispiel löscht eine Imagemap aus einer Firma. Sie müssen den Imagemap-Handle von einem anderen Vorgang abrufen.

**Anforderung**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Antwort**

Keine

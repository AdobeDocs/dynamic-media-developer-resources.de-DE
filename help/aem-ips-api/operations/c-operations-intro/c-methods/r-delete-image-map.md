---
description: Löscht eine Imagemap.
seo-description: Löscht eine Imagemap.
seo-title: deleteImageMap
solution: Experience Manager
title: deleteImageMap
topic: Scene7 Image Production System API
uuid: 0abdf72c-f445-41d0-bd88-63b7ad1359d5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 12%

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff zu der Firma, die die zu löschende Imagemap enthält. |
| ` *`imageMapHandle`*` | `xsd:string` | Ja | Der Griff zur zu löschenden Imagemap. |

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

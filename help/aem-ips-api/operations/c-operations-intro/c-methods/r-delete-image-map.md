---
description: Löscht eine Imagemap.
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 10%

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

**Eingabe (deleteImageMapParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handle für das Unternehmen, das die zu löschende Imagemap enthält. |
| imageMapHandle | `xsd:string` | Ja | Der Handle zur zu löschenden Imagemap. |

**Ausgabe (deleteImageMapParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Dieses Codebeispiel löscht eine Imagemap aus einer Firma. Sie müssen das Imagemap-Handle von einem anderen Vorgang abrufen.

**Anfrage**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Antwort**

Keine

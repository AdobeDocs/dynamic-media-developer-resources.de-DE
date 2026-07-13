---
description: Löscht ein Vignettenveröffentlichungsformat.
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
TQID: 'https://experienceleague.adobe.com/e1qIrpGHPuodTx79J1ke-7ULFptiCa6ZoIXyldJvSBY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 12%

---

# deleteVignettePublishFormat{#deletevignettepublishformat}

Löscht ein Vignettenveröffentlichungsformat.

## Autorisierte Benutzertypen {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-789625ba29df4b5f880914d4c64f77ce}

**Eingabe (deleteVignettePublishFormatParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Griff für das Unternehmen, zu dem die Vignette gehört. |
| vignetteFormatHandle | `xsd:string` | Ja | Der Ziehgriff zum Vignettenveröffentlichungsformat, das gelöscht werden soll. |

**Ausgabe (deleteVignettePublishFormatParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Dieses Codebeispiel löscht ein Vignettenveröffentlichungsformat, das durch seinen Handle angegeben ist.

**Anfrage**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Antwort**

Keine.


---
description: Löscht ein Bildformat. Rufen Sie den Bildformathandle von saveImageFormat ab.
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
TQID: 'https://experienceleague.adobe.com/BOhXqXdUG6BUA9VsI9faDIeRfdCwlqYsj6sqS-uQ330'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 9%

---

# deleteImageFormat{#deleteimageformat}

Löscht ein Bildformat. Rufen Sie den Bildformathandle von saveImageFormat ab.

Syntax

## Autorisierte Benutzertypen {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-462c05d9aad746ee8d2be0656041b693}

**Eingabe (deleteImageFormatParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, das das Bildformat enthält, das Sie löschen möchten. |
| imageFormatHandle | `xsd:string` | Ja | Der Ziehgriff auf das Bildformat, das Sie löschen möchten. |

**Ausgabe (deleteImageFormatParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

Dieses Codebeispiel löscht ein Bildformat aus einer Firma. Abrufen des Bildformathandles aus einem anderen Vorgang.

**Anfrage**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**Antwort**

Keine.

**Verwandtes Thema:**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)


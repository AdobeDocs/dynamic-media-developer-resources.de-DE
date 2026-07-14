---
description: Erstellen oder bearbeiten Sie ein Zoom-Ziel.
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
TQID: 'https://experienceleague.adobe.com/rw-joRwkyumLI261ifPiWTeIgy4mvx-4MpgmaKcX5-E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 19%

---

# saveZoomTarget{#savezoomtarget}

Erstellen oder bearbeiten Sie ein Zoom-Ziel.

Syntax

## Autorisierter Benutzertyp {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-4a23983cae4e49a098e9bbe736933996}

**Eingabe (saveZoomTargetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Griff für die Firma mit dem Zoom-Ziel, das Sie speichern möchten. |
| assetHandle | `xsd:string` | Ja | Der Ziehgriff zum Zoom-Ziel. |
| zoomTargetHandle | `xsd:string` | Nein | Bearbeitet oder erstellt ein Zoom-Ziel. |
| name | `xsd:string` | Ja | Name des Zoomziels. |
| xPosition | `xsd:int` | Ja | Position des linken Pixels. |
| yPosition | `xsd:int` | Ja | Top-Pixel-Position. |
| Breite | `xsd:int` | Ja | Zielbreite zoomen. |
| Höhe | `xsd:int` | Ja | Zielhöhe zoomen. |
| userData | `xsd:string` | Ja | Für kundenspezifische Informationen. Kann jeden Datentyp enthalten. |

**Ausgabe (saveZoomTargetReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| zoomTargetHandle | `xsd:string` | Ja | Gehen Sie zum neu erstellten Zoom-Ziel. |

## Beispiele {#section-509c472c316549cdb228d7e1cfa8400a}

Dieses Code-Beispiel speichert ein Zoom-Ziel. Die Antwort gibt den Ziehgriff des Zoomziels zurück.

**Anfrage**

```java
<saveZoomTargetParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <name>My Zoom Target</name>
   <xPosition>2</xPosition>
   <yPosition>2</yPosition>
   <width>10</width>
   <height>10</height>
   <userData>My User Data</userData>
</saveZoomTargetParam>
```

**Antwort**

```java
<saveZoomTargetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <zoomTargetHandle>34194|9|301</zoomTargetHandle>
</saveZoomTargetReturn>
```


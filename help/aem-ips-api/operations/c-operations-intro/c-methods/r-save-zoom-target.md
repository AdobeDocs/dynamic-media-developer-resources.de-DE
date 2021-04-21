---
description: Erstellen oder bearbeiten Sie eine Zoom-Zielgruppe.
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 20%

---


# saveZoomTarget{#savezoomtarget}

Erstellen oder bearbeiten Sie eine Zoom-Zielgruppe.

Syntax

## Autorisierter Benutzertyp {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-4a23983cae4e49a098e9bbe736933996}

**Input (saveZoomTargetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma mit der zu speichernden Zoom-Zielgruppe. |
| `*`assetHandle`*` | `xsd:string` | Ja | Der Griff zur Zoom-Zielgruppe. |
| `*`zoomTargetHandle`*` | `xsd:string` | Nein | Bearbeitet oder erstellt eine Zoom-Zielgruppe. |
| `*`name`*` | `xsd:string` | Ja | Name der Zoom-Zielgruppe. |
| `*`xPosition`*` | `xsd:int` | Ja | Position des linken Pixels. |
| `*`yPosition`*` | `xsd:int` | Ja | Position der obersten Pixel. |
| `*`width`*` | `xsd:int` | Ja | Breite der Zoom-Zielgruppe. |
| `*`height`*` | `xsd:int` | Ja | Höhe der Zoom-Zielgruppe. |
| `*`Benutzerdaten`*` | `xsd:string` | Ja | Für kundenspezifische Informationen. Kann beliebige Datentypen enthalten. |

**Output (saveZoomTargetReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`zoomTargetHandle`*` | `xsd:string` | Ja | Behandeln Sie die neu erstellte Zoom-Zielgruppe. |

## Beispiele {#section-509c472c316549cdb228d7e1cfa8400a}

In diesem Codebeispiel wird eine Zoom-Zielgruppe gespeichert. Die Antwort gibt den Zifferngriff der Zielgruppe zurück.

**Anforderung**

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


---
description: Erstellen oder bearbeiten Sie ein Zoomziel.
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 19%

---

# saveZoomTarget{#savezoomtarget}

Erstellen oder bearbeiten Sie ein Zoomziel.

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
| companyHandle | `xsd:string` | Ja | Der Griff zum Unternehmen mit dem Zoomziel, das Sie speichern möchten. |
| assetHandle | `xsd:string` | Ja | Der Griff zum Zoomziel. |
| zoomTargetHandle | `xsd:string` | Nein | Bearbeiten oder erstellen Sie ein Zoomziel. |
| name | `xsd:string` | Ja | Zoom-Zielname. |
| xPosition | `xsd:int` | Ja | Position des linken Pixels. |
| yPosition | `xsd:int` | Ja | Position des obersten Pixels. |
| Breite | `xsd:int` | Ja | Zoom der Zielbreite |
| Höhe | `xsd:int` | Ja | Zoom der Zielhöhe. |
| userData | `xsd:string` | Ja | Für kundenspezifische Informationen. Kann beliebige Datentypen enthalten. |

**Output (saveZoomTargetReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| zoomTargetHandle | `xsd:string` | Ja | Bearbeiten Sie das neu erstellte Zoomziel. |

## Beispiele {#section-509c472c316549cdb228d7e1cfa8400a}

Mit diesem Codebeispiel wird ein Zoomziel gespeichert. Die Antwort gibt den Zoom-Ziel-Handle zurück.

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

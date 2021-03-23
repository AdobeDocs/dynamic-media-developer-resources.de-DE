---
description: Legt die mit einem Asset-Bild verknüpfte Zoom-Zielgruppe fest. Es überschreibt vorhandene Zoom-Zielgruppen.
seo-description: Legt die mit einem Asset-Bild verknüpfte Zoom-Zielgruppe fest. Es überschreibt vorhandene Zoom-Zielgruppen.
seo-title: setZoomTargets
solution: Experience Manager
title: setZoomTargets
uuid: 5d0aecec-ebd8-4c69-9514-c29fae347ee6
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 11%

---


# setZoomTargets{#setzoomtargets}

Legt die mit einem Asset-Bild verknüpfte Zoom-Zielgruppe fest. Es überschreibt vorhandene Zoom-Zielgruppen.

Syntax

## Autorisierte Benutzertypen {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-161f8c733cc4439f94a06e12119d4226}

**Input (setZoomTargetsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| `*`assetHandle`*` | `xsd:string` | Ja | Asset mit der Zoom-Zielgruppe, die Sie einstellen möchten. |
| `*`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | Ja | Array von Definitionen zur Zoomfunktion. |

**Output (setZoomTargetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`zoomTargetHandleArray`*` | `types:HandleArray` | Ja | Der Satz von Griffen für die Zoom-Zielgruppen, die durch diesen Vorgang erstellt werden. |

## Beispiele {#section-a2f14c7a1499443e96d099ea8a76c182}

In diesem Codebeispiel wird ein Array von Zoom-Zielgruppen nach Name, Position (X- und Y-Achse), Breite und Höhe definiert und das Array einem Asset zugewiesen. Die Antwort enthält Griffe zu den neu erstellten Zoom-Zielgruppen.

**Anforderung**

```java
<setZoomTargetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <zoomTargetArray>
      <items>
         <name>zoomTarget2</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
      <items>
         <name>zoomTarget3</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
   </zoomTargetArray>
</setZoomTargetsParam>
```

**Antwort**

```java
<setZoomTargetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zoomTargetHandleArray>
      <items>a|947|9|41</items>
      <items>a|948|9|42</items>
   </zoomTargetHandleArray>
</setZoomTargetsReturn>
```


---
description: Legt das mit einem Asset-Bild verknüpfte Zoomziel fest. Es überschreibt vorhandene Zoomziele.
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# setZoomTargets{#setzoomtargets}

Legt das mit einem Asset-Bild verknüpfte Zoomziel fest. Es überschreibt vorhandene Zoomziele.

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
| companyHandle | `xsd:string` | Ja | Handle des Unternehmens. |
| assetHandle | `xsd:string` | Ja | Asset mit dem Zoomziel, das Sie festlegen möchten. |
| zoomTargetArray | `types:ZoomTargetDefinitionArray` | Ja | Array von Zoom-Zieldefinitionen. |

**Output (setZoomTargetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| zoomTargetHandleArray | `types:HandleArray` | Ja | Die Griffe für die Zoomziele, die durch diesen Vorgang erstellt werden. |

## Beispiele {#section-a2f14c7a1499443e96d099ea8a76c182}

Dieses Codebeispiel definiert ein Array von Zoomzielen nach Name, Position (X- und Y-Achse), Breite und Höhe und weist das Array einem Asset zu. Die Antwort enthält Handles zu den neu erstellten Zoomzielen.

**Anfrage**

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

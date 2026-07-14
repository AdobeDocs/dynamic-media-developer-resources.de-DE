---
description: Legt das Zoom-Ziel fest, das mit einem Asset-Bild verknüpft ist. Dadurch werden vorhandene Zoom-Ziele überschrieben.
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
TQID: 'https://experienceleague.adobe.com/JQfWp3-Xm1rGlAmd1qisxzo2irZy3aedScXmeBbL1Pk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 12%

---

# setZoomTargets{#setzoomtargets}

Legt das Zoom-Ziel fest, das mit einem Asset-Bild verknüpft ist. Dadurch werden vorhandene Zoom-Ziele überschrieben.

Syntax

## Autorisierte Benutzertypen {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-161f8c733cc4439f94a06e12119d4226}

**Eingabe (setZoomTargetsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Firmengriff. |
| assetHandle | `xsd:string` | Ja | Asset mit dem Zoom-Ziel, das Sie festlegen möchten. |
| zoomTargetArray | `types:ZoomTargetDefinitionArray` | Ja | Array von Zoom-Zieldefinitionen. |

**Ausgabe (setZoomTargetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| zoomTargetHandleArray | `types:HandleArray` | Ja | Der Satz von Ziehpunkten für die Zoom-Ziele, die durch diesen Vorgang erstellt werden. |

## Beispiele {#section-a2f14c7a1499443e96d099ea8a76c182}

Dieses Codebeispiel definiert ein Array von Zoom-Zielen nach Name, Position (X- und Y-Achse), Breite und Höhe und weist das Array einem Asset zu. Die Antwort enthält Handles zu den neu erstellten Zoom-Zielen.

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


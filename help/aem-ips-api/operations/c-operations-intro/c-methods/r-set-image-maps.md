---
description: Legt die Imagemap für ein Asset fest.
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
TQID: 'https://experienceleague.adobe.com/sOGDO0ruTEK1DS5Sc-4nhLfViddEKCLDLJlpC-8H3g0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 10%

---

# setImageMaps{#setimagemaps}

Legt die Imagemap für ein Asset fest.

Sie müssen die Imagemaps bereits erstellt haben. Imagemaps werden in der Reihenfolge angewendet, in der sie aus dem Array abgerufen werden. Das bedeutet, dass die zweite Imagemap die erste überlagert, die dritte die zweite und so weiter.

## Autorisierte Benutzertypen {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-2292ec1aead947ef8741dd0653a41f42}

**Input (setImageMapsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Firmengriff. |
| assetHandle | `xsd:string` | Ja | Asset-Handle. |
| imageMapArray | `types:ImageMapDefinitionArray` | Ja | Array von vordefinierten Imagemaps. |

**Ausgabe (setImageMapsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | Ja | Ein Array mit Imagemap-Handles, die auf das Asset angewendet wurden. |

## Beispiele {#section-fe2e35662a6a4ee29cf250c9fd180371}

In diesem Code-Beispiel werden zwei Imagemaps für ein Bild-Asset festgelegt. Der Code gibt den Formtyp, die Region und die Aktion an, die beim Aufrufen der Imagemaps ausgeführt wird. Die Antwort enthält ein -Array mit Handles für die Imagemaps.

**Anfrage**

```java
<setImageMapsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <imageMapArray>
      <items>
         <name>ImageMap2</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>true</enabled>
      </items>
      <items>
         <name>ImageMap3</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>false</enabled>
      </items>
   </imageMapArray>
</setImageMapsParam>
```

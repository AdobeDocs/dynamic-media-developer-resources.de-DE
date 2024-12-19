---
description: Legt die Imagemap für ein Asset fest.
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '134'
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

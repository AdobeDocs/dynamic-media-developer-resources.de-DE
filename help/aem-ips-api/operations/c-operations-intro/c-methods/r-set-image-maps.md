---
description: Legt die Imagemap für ein Asset fest.
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 11%

---

# setImageMaps{#setimagemaps}

Legt die Imagemap für ein Asset fest.

Sie müssen die Imagemaps bereits erstellt haben. Imagemaps werden in der Reihenfolge des Abrufs aus dem Array angewendet. Das bedeutet, dass die zweite Imagemap die erste, die dritte die zweite und so weiter überlagert.

## Autorisierte Benutzertypen {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-2292ec1aead947ef8741dd0653a41f42}

**Eingabe (setImageMapsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handle des Unternehmens. |
| assetHandle | `xsd:string` | Ja | Asset-Handle. |
| imageMapArray | `types:ImageMapDefinitionArray` | Ja | Array von vordefinierten Imagemaps. |

**Ausgabe (setImageMapsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | Ja | Ein Array mit Imagemap-Handles, die auf das Asset angewendet werden. |

## Beispiele {#section-fe2e35662a6a4ee29cf250c9fd180371}

In diesem Codebeispiel werden zwei Imagemaps für ein Bild-Asset festgelegt. Der Code gibt den Formtyp, den Bereich und die Aktion an, die beim Aufrufen der Imagemaps ausgeführt werden. Die Antwort enthält ein Array mit Griffen an die Imagemaps.

**Anforderung**

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

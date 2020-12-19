---
description: Legt die Imagemap für ein Asset fest.
seo-description: Legt die Imagemap für ein Asset fest.
seo-title: setImageMaps
solution: Experience Manager
title: setImageMaps
topic: Scene7 Image Production System API
uuid: 1dd7e032-34b4-464d-8ec6-7ad282d12891
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 10%

---


# setImageMaps{#setimagemaps}

Legt die Imagemap für ein Asset fest.

Sie müssen die Imagemaps bereits erstellt haben. Imagemaps werden in der Reihenfolge angewendet, in der sie aus dem Array abgerufen werden. Das bedeutet, dass die zweite Imagemap die erste, die dritte die zweite Überlagerung usw. überlagert.

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Asset-Handle. |
| ` *`imageMapArray`*` | `types:ImageMapDefinitionArray` | Ja | Array vordefinierter Imagemaps. |

**Output (setImageMapsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`imageMapHandleArray`*` | `types:HandleArray` | Ja | Ein Array mit Imagemap-Handles, die auf das Asset angewendet werden. |

## Beispiele {#section-fe2e35662a6a4ee29cf250c9fd180371}

In diesem Codebeispiel werden zwei Imagemaps für ein Bild-Asset festgelegt. Der Code gibt den Formtyp, den Bereich und die Aktion an, die beim Aufrufen der Imagemaps durchgeführt werden. Die Antwort enthält ein Array mit Griffen auf die Imagemaps.

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


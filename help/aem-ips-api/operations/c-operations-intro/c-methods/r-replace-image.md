---
description: Ersetzt Bilddaten für ein Bild-Asset.
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic, SDK/API, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 15%

---


# replaceImage{#replaceimage}

Ersetzt Bilddaten für ein Bild-Asset.

Syntax

## Autorisierte Benutzertypen {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**Input (replaceImageParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | Ja | Der Griff zur Firma mit dem Bild, das Sie ersetzen möchten. |
| `*`assetHandle`*` | `xsd:string` | Ja | Das Handle des Assets, das Sie ersetzen möchten. |
| `*`urlModifier`*` | `xsd:string` | Ja | Image-Server-Befehle, die neue Bilddaten generieren. |

**Output (replaceImageReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Ja | Umgang mit dem neuen Asset. |

## Beispiele {#section-cebb93576bde4cb98cb27356ca66783b}

Dieses Codebeispiel ersetzt ein Bild und wendet ein `urlModifier` durch einen Befehl an, der angibt, dass der Image-Server beim Ersetzen keine Aktion ausführt.

**Anforderung**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**Antwort**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```


---
description: Ersetzt Bilddaten für ein Bild-Asset.
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 14%

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
| companyName | `xsd:string` | Ja | Das Handle für das Unternehmen mit dem Bild, das Sie ersetzen möchten. |
| assetHandle | `xsd:string` | Ja | Das Handle des Assets, das Sie ersetzen möchten. |
| urlModifier | `xsd:string` | Ja | Image-Server-Befehle, die neue Bilddaten generieren. |

**Ausgabe (replaceImageReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| assetHandle | `xsd:string` | Ja | Verarbeiten Sie das neue Asset. |

## Beispiele {#section-cebb93576bde4cb98cb27356ca66783b}

Dieses Code-Beispiel ersetzt ein Bild und wendet ein `urlModifier` mit einem Befehl an, der angibt, dass der Bild-Server beim Ersetzen keine Aktion ausführt.

**Anfrage**

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

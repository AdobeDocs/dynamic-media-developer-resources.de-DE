---
description: Legt die Befehle des Image Serving- oder Image Rendering-Protokolls für das angegebene Asset fest. Diese Befehle ändern die Darstellung des Assets, ohne ihn zu zerstören.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 7%

---


# setUrlModifier{#seturlmodifier}

Legt die Befehle des Image Serving- oder Image Rendering-Protokolls für das angegebene Asset fest. Diese Befehle ändern die Darstellung des Assets, ohne ihn zu zerstören.

Für Image Serving werden Befehle im Parameter `urlModifier` im Feld Modifier-Katalog veröffentlicht und vor allen Befehlen angewendet, die in der Anforderungs-URL angegeben sind. Befehle in `urlPostApplyModifier` werden im Katalogfeld `PostModifier` veröffentlicht und überschreiben alle Befehle in der Anforderungs-URL oder in `urlModifier`. Beim Image Rendering werden die Befehle in `urlModifier` und `urlPostApplyModifier` verkettet und im Feld Modifier-Katalog veröffentlicht.

## Autorisierte Benutzertypen {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Input (setUrlModifierParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| `*`assetHandle`*` | `xsd:string` | Ja | Asset-Handle. |
| `*`urlModifier`*` | `xsd:string` | Nein | Image Serving- oder Image Rendering-Protokollbefehle, die vor der Anforderung oder den Befehlen `urlPostApplyModifier` angewendet werden sollen. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Nein | Image Serving- oder Image Rendering-Protokollbefehle, die nach `urlModifier` angewendet werden, und Anforderungsbefehle. |

**Output (setUrlModifierReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Anforderung**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**Antwort**

Keine.

---
description: Legt die Protokollbefehle für Image Serving oder Image Rendering für das angegebene Asset fest. Diese Befehle ändern die Darstellung des Assets, ohne es zu zerstören.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 6%

---

# setUrlModifier{#seturlmodifier}

Legt die Protokollbefehle für Image Serving oder Image Rendering für das angegebene Asset fest. Diese Befehle ändern die Darstellung des Assets, ohne es zu zerstören.

Für Image Serving werden Befehle im Parameter `urlModifier` im Feld Modifier-Katalog veröffentlicht und vor allen Befehlen angewendet, die in der Anfrage-URL angegeben sind. Befehle in `urlPostApplyModifier` werden im Katalogfeld `PostModifier` veröffentlicht und überschreiben alle Befehle in der Anforderungs-URL oder in `urlModifier`. Beim Rendern von Bildern werden die Befehle in `urlModifier` und `urlPostApplyModifier` verkettet und im Feld Modifikatorkatalog veröffentlicht.

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
| companyHandle | `xsd:string` | Ja | Handle des Unternehmens. |
| assetHandle | `xsd:string` | Ja | Asset-Handle. |
| urlModifier | `xsd:string` | Nein | Image Serving- oder Image Rendering-Protokollbefehle, die vor der Anforderung oder vor den Befehlen `urlPostApplyModifier` angewendet werden. |
| urlPostApplyModifier | `xsd:string` | Nein | Image Serving - oder Image Rendering -Protokollbefehle, die nach `urlModifier` angewendet werden und Befehle anfordern. |

**Output (setUrlModifierReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Anfrage**

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

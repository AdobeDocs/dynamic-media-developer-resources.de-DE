---
description: Legt die Befehle des Image Serving- oder Image Rendering-Protokolls für das angegebene Asset fest. Diese Befehle ändern die Darstellung des Assets, ohne ihn zu zerstören.
seo-description: Legt die Befehle des Image Serving- oder Image Rendering-Protokolls für das angegebene Asset fest. Diese Befehle ändern die Darstellung des Assets, ohne ihn zu zerstören.
seo-title: setUrlModifier
solution: Experience Manager
title: setUrlModifier
topic: Scene7 Image Production System API
uuid: ec423e57-338b-4a32-be5a-a73fa96712ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUrlModifier{#seturlmodifier}

Legt die Befehle des Image Serving- oder Image Rendering-Protokolls für das angegebene Asset fest. Diese Befehle ändern die Darstellung des Assets, ohne ihn zu zerstören.

Für Image Serving werden Befehle im `urlModifier` Parameter im Feld Modifier-Katalog veröffentlicht und vor allen Befehlen angewendet, die in der Anforderungs-URL angegeben sind. Befehle in `urlPostApplyModifier` werden im Katalogfeld veröffentlicht und überschreiben alle Befehle in der Anforderungs-URL oder in `PostModifier` `urlModifier`. Beim Image Rendering werden die Befehle im Feld Modifier-Katalog verkettet `urlModifier` und im Feld Modifier veröffentlicht, und `urlPostApplyModifier` werden miteinander verkettet.

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Asset-Handle. |
| ` *`urlModifier`*` | `xsd:string` | Nein | Protokollbefehle für Image Serving oder Image Rendering, die vor Anforderung oder `urlPostApplyModifier` Befehlen angewendet werden sollen. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Nein | Protokollbefehle für Image Serving oder Image Rendering, die nach `urlModifier` und nach Befehlen angewendet werden sollen. |

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

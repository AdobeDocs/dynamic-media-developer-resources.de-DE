---
description: Legt die Protokollbefehle für Image Serving oder Image Rendering für das angegebene Asset fest. Diese Befehle ändern die Darstellung des Assets, ohne es zu zerstören.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 7%

---

# setUrlModifier{#seturlmodifier}

Legt die Protokollbefehle für Image Serving oder Image Rendering für das angegebene Asset fest. Diese Befehle ändern die Darstellung des Assets, ohne es zu zerstören.

Für die Bildbereitstellung, Befehle im `urlModifier` -Parameter werden im Feld Modifikatorkatalog veröffentlicht und vor allen Befehlen angewendet, die in der Anfrage-URL angegeben sind. Befehle in `urlPostApplyModifier` werden in der `PostModifier` Katalogfeld und überschreibt alle Befehle auf der Anforderungs-URL oder in `urlModifier`. Für das Rendern von Bildern werden die Befehle in `urlModifier` und `urlPostApplyModifier` werden verkettet und im Feld Modifikatorkatalog veröffentlicht.

## Autorisierte Benutzertypen {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Eingabe (setUrlModifierParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handle des Unternehmens. |
| `*`assetHandle`*` | `xsd:string` | Ja | Asset-Handle. |
| `*`urlModifier`*` | `xsd:string` | Nein | Image Serving- oder Image Rendering-Protokollbefehle, die vor der Anforderung angewendet werden sollen, oder `urlPostApplyModifier` Befehle. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Nein | Protokollbefehle für Image Serving oder Image Rendering, die nach angewendet werden sollen `urlModifier` und fordern Sie Befehle an. |

**Ausgabe (setUrlModifierReturn)**

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

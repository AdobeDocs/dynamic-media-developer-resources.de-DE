---
description: Gibt 2 verschiedene Arten von Informationen basierend auf den weitergeleiteten Parametern zurück. originatorHandle gibt Informationen zu Assets zurück, die aus dem angegebenen Asset generiert wurden. generateHandle gibt Informationen zu Schritten zurück, die zum Generieren des angegebenen Assets oder der angegebenen Datei verwendet werden.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 9%

---


# getGenerationInfo{#getgenerationinfo}

Gibt 2 verschiedene Arten von Informationen basierend auf den weitergeleiteten Parametern zurück. originatorHandle gibt Informationen zu Assets zurück, die aus dem angegebenen Asset generiert wurden. generateHandle gibt Informationen zu Schritten zurück, die zum Generieren des angegebenen Assets oder der angegebenen Datei verwendet werden.

Syntax

## Autorisierte Benutzertypen {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-b7fa94c82147455888e8469fa5f6922b}

**Input (getGenerationInfoParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`Codebegriff`*` | `xsd:string` | Ja | Der Griff zur Firma. |
| `*`Codebegriff`*` | `xsd:string` | Nein | Der Motor, der bei der Generierung verwendet wurde. Siehe Schriftschnitte. |
| `*`Codebegriff`*` | `xsd:string` | Nein | Das Handle des Assets zur Abfrage für generierte Assets. |
| `*`Codebegriff`*` | `xsd:string` | Nein | Das Handle des Assets zur Abfrage für Assets und Motoren, die bei seiner Erstellung verwendet werden. |
| `*`Codebegriff`*` | `xsd:StringArray` | Nein | Eigenschaften, die im Vorgang enthalten sind. |
| `*`Codebegriff`*` | `xsd:StringArray` | Nein | Eigenschaften, die vom Vorgang ausgeschlossen sind. |

**Output (getGenerationInfoReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`generationArray`*` | `types:GenerationInfoArray` | Ja | Array von Generierungsinformationen. |

## Beispiele {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Dieses Codebeispiel gibt Informationen zu Assets zurück, die aus einem bestimmten Asset generiert wurden. Es werden keine Informationen zu den Schritten abgerufen, die zum Generieren des angegebenen Assets verwendet werden. Die Antwort wird wegen ihrer Kürze abgeschnitten.

**Anforderung**

```java
<getGenerationInfoParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <originatorHandle>a|716|25|160</originatorHandle>
</getGenerationInfoParam>
```

**Antwort**

```java
<getGenerationInfoReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <generationArray>
      <items>
         <engine>PostScriptRip</engine>
         <originator>
         ...
         </generated>
         <attributeArray/>
      </items>
   </generationArray>
</getGenerationInfoReturn>
```


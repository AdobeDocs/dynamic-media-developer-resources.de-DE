---
description: Gibt basierend auf den übergebenen Parametern zwei verschiedene Arten von Informationen zurück. originatorHandle gibt Informationen zu Assets zurück, die aus dem angegebenen Asset generiert wurden. generateHandle gibt Informationen zu den Schritten zurück, die zum Generieren des angegebenen Assets oder der angegebenen Datei verwendet wurden.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 9%

---

# getGenerationInfo{#getgenerationinfo}

Gibt basierend auf den übergebenen Parametern zwei verschiedene Arten von Informationen zurück. originatorHandle gibt Informationen zu Assets zurück, die aus dem angegebenen Asset generiert wurden. generateHandle gibt Informationen zu den Schritten zurück, die zum Generieren des angegebenen Assets oder der angegebenen Datei verwendet wurden.

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
| Codeausdruck | `xsd:string` | Ja | Der Handle für das Unternehmen. |
| Codeausdruck | `xsd:string` | Nein | Der Motor, der bei der Generierung verwendet wurde. Siehe Schriftstile. |
| Codeausdruck | `xsd:string` | Nein | Das Handle des Assets, das nach generierten Assets abgefragt werden soll. |
| Codeausdruck | `xsd:string` | Nein | Der Handle des Assets, mit dem nach Assets und Engines abgefragt werden soll, die bei seiner Generierung verwendet werden. |
| Codeausdruck | `xsd:StringArray` | Nein | Im Vorgang enthaltene Eigenschaften. |
| Codeausdruck | `xsd:StringArray` | Nein | Eigenschaften, die vom Vorgang ausgeschlossen sind. |

**Output (getGenerationInfoReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| generationArray | `types:GenerationInfoArray` | Ja | Array von Generierungsinformationen. |

## Beispiele {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Dieses Codebeispiel gibt Informationen zu Assets zurück, die aus einem bestimmten Asset generiert wurden. Es werden keine Informationen zu den Schritten abgerufen, die zum Generieren des angegebenen Assets verwendet werden. Die Antwort wird aus Gründen der Kürze abgeschnitten.

**Anfrage**

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

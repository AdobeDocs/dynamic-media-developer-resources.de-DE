---
description: Gibt zwei verschiedene Arten von Informationen zurück, die auf den übergebenen Parametern basieren. originatorHandle gibt Informationen über Assets zurück, die aus dem angegebenen Asset generiert wurden. generateHandle gibt Informationen über die Schritte zurück, die zum Generieren des angegebenen Assets oder der angegebenen Datei verwendet werden.
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

Gibt zwei verschiedene Arten von Informationen zurück, die auf den übergebenen Parametern basieren. originatorHandle gibt Informationen über Assets zurück, die aus dem angegebenen Asset generiert wurden. generateHandle gibt Informationen über die Schritte zurück, die zum Generieren des angegebenen Assets oder der angegebenen Datei verwendet werden.

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
| Code-Satz | `xsd:string` | Ja | Der Griff zum Unternehmen. |
| Code-Satz | `xsd:string` | Nein | Die Engine, die in der Generation verwendet wurde. Siehe Schriftstile. |
| Code-Satz | `xsd:string` | Nein | Das Handle des Assets, das nach generierten Assets abgefragt werden soll. |
| Code-Satz | `xsd:string` | Nein | Das Handle des Assets, das nach Assets und Engines abgefragt werden soll, die bei seiner Generierung verwendet werden. |
| Code-Satz | `xsd:StringArray` | Nein | Im Vorgang enthaltene Eigenschaften. |
| Code-Satz | `xsd:StringArray` | Nein | Aus dem Vorgang ausgeschlossene Eigenschaften. |

**Ausgabe (getGenerationInfoReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| generationArray | `types:GenerationInfoArray` | Ja | Array von Erzeugungsinformationen. |

## Beispiele {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Dieses Code-Beispiel gibt Informationen über Assets zurück, die aus einem bestimmten Asset generiert wurden. Es werden keine Informationen über die Schritte abgerufen, die zum Generieren des angegebenen Assets verwendet werden. Die Antwort wird zur Vereinfachung gekürzt.

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

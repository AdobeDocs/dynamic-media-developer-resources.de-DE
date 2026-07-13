---
description: Gibt zwei verschiedene Arten von Informationen zurück, die auf den übergebenen Parametern basieren. originatorHandle gibt Informationen über Assets zurück, die aus dem angegebenen Asset generiert wurden. generateHandle gibt Informationen über die Schritte zurück, die zum Generieren des angegebenen Assets oder der angegebenen Datei verwendet werden.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
TQID: 'https://experienceleague.adobe.com/MA0SJinQzPjDFkSXVRhH2e7A3Ry6HXoW--K-elv028M'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 198
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


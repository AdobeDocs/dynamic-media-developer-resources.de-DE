---
description: Ruft Projekte für eine Gruppe verwandter Assets ab.
solution: Experience Manager
title: getProjects
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7262ed7-7419-4d6b-86ed-f3ad4657d654
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 19%

---

# getProjects{#getprojects}

Ruft Projekte für eine Gruppe verwandter Assets ab.

Syntax

## Autorisierte Benutzertypen {#section-337649866b1f4098844d1974ed7ab5d0}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-8d549237b8c440b4872a0a086ddc00a1}

**Input (getProjectsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handle für das Unternehmen. |

**Output (getProjectsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| projectArray | `types:ProjectArray` | Ja | Die mit dem Unternehmen verknüpfte Gruppe von Projekten. |

## Beispiele {#section-8b12d0b948f644f68bf9a16060d3849a}

Dieses Codebeispiel gibt alle Projekt-Handles in einem Projekt-Array zurück.

**Anfrage**

```java
<ns1:getProjectsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getProjectsParam>
```

**Antwort**

```java
<getProjectsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <projectArray>
      <items>
         <projectHandle>47|My Project 1</projectHandle>
         <name>My Project 1</name>
      </items>
      <items>
         <projectHandle>47|My Project 2</projectHandle>
         <name>My Project 2</name>
      </items>
   </projectArray>
</getProjectsReturn>
```

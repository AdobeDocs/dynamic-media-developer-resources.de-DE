---
description: Ruft Projekte für eine Gruppe verwandter Assets ab.
seo-description: Ruft Projekte für eine Gruppe verwandter Assets ab.
seo-title: getProjects
solution: Experience Manager
title: getProjects
uuid: 46ec9a5d-4414-4c9c-aaf2-0db654204b61
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 18%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma. |

**Output (getProjectsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`projectArray`*` | `types:ProjectArray` | Ja | Das Array der mit der Firma verknüpften Projekte. |

## Beispiele {#section-8b12d0b948f644f68bf9a16060d3849a}

Dieses Codebeispiel gibt alle Projektprozeduren in einem Projektarchiv zurück.

**Anforderung**

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


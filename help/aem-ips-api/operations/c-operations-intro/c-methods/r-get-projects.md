---
description: Ruft Projekte für eine Gruppe verwandter Assets ab.
solution: Experience Manager
title: getProjects
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7262ed7-7419-4d6b-86ed-f3ad4657d654
TQID: 'https://experienceleague.adobe.com/8qz891-cE1hkh1ui-mY2AZIyBO7IWoklEmPXNXmUoUU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 66
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

**Eingabe (getProjectsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Griff zum Unternehmen. |

**Ausgabe (getProjectsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| projectArray | `types:ProjectArray` | Ja | Die Reihe der mit dem Unternehmen verknüpften Projekte. |

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

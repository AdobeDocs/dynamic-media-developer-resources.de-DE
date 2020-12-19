---
description: Erstellt ein neues Projekt.
seo-description: Erstellt ein neues Projekt.
seo-title: createProject
solution: Experience Manager
title: createProject
topic: Scene7 Image Production System API
uuid: e011b7ba-6c15-47ef-9ea1-6189c37e7719
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 18%

---


# createProject{#createproject}

Erstellt ein neues Projekt.

Syntax

## Autorisierte Benutzertypen {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-8c741884eb54489bbaad0c444fee80b6}

**Input (createProjectParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Handle der Firma, die mit dem neuen Projekt verknüpft ist. |
| ` *`projectName`*` | `xsd:string` | Ja | Neuer Projektname. |

**Output (createProjectParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`projectHandle`*` | `xsd:string` | Ja | Der Griff zum neuen Projekt. |

## Beispiele {#section-a0cd532b67e346d088fbec141231a0e5}

Dieses Codebeispiel erstellt ein Projekt mit dem Namen `ApiTestProject` in einer vom Handle angegebenen Firma. Die Antwort gibt den Handle an das Projekt zurück.

**Anforderung**

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>
```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```


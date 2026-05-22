---
description: Erstellt ein neues Projekt.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
TQID: 'https://experienceleague.adobe.com/GKNImvhmX1bOepsV0-6QzgZr5jskJQlaqXCMIT5ue5M'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
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

**Eingabe (createProjectParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handle der Firma, die mit dem neuen Projekt verknüpft ist. |
| projectName | `xsd:string` | Ja | Neuer Projektname. |

**Ausgabe (createProjectParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| projectHandle | `xsd:string` | Ja | Der Handler zum neuen Projekt. |

## Beispiele {#section-a0cd532b67e346d088fbec141231a0e5}

Dieses Codebeispiel erstellt ein Projekt mit dem Namen `ApiTestProject` in einem Unternehmen, das durch sein Handle angegeben wird. Die Antwort gibt das Handle an das Projekt zurück.

**Anfrage**

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

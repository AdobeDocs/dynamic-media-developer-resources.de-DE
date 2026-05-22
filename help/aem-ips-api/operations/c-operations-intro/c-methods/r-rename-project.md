---
description: Benennt ein Projekt um.
solution: Experience Manager
title: Projekt umbenennen
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
TQID: 'https://experienceleague.adobe.com/FjPL1Xn4QAYYCdyeYKA1MiQVay988g-sbuiHpazhcMM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 21%

---

# Projekt umbenennen{#renameproject}

Benennt ein Projekt um.

Syntax

## Autorisierte Benutzertypen {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-43ccd77648784be4a259a723c3e1db40}

**Eingabe (renameProjectParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyName | `xsd:string` | Ja | Verarbeiten Sie das Unternehmen mit dem Projekt, das Sie umbenennen möchten. |
| projectHandle | `xsd:string` | Ja | Übernehmen Sie das Projekt. |
| projectName | `xsd:string` | Ja | Neuer Projektname. |

**Ausgabe (renameProjectParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| projectHandle | `xsd:string` | Ja | Der Handle des umbenannten Projekts. |

## Beispiele {#section-a0a06d9244774795b695a10b92b2a5e7}

Dieses Codebeispiel benennt ein Projekt um und gibt das Projekt-Handle zurück.

**Anfrage**

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**Antwort**

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```

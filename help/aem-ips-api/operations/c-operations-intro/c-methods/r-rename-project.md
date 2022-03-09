---
description: Benennt ein Projekt um.
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 23%

---

# renameProject{#renameproject}

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
| projectHandle | `xsd:string` | Ja | Verarbeiten Sie das Projekt. |
| projectName | `xsd:string` | Ja | Neuer Projektname. |

**Ausgabe (renameProjectParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| projectHandle | `xsd:string` | Ja | Der Handle des umbenannten Projekts. |

## Beispiele {#section-a0a06d9244774795b695a10b92b2a5e7}

Mit diesem Codebeispiel wird ein Projekt umbenannt und der Projekthandle zurückgegeben.

**Anforderung**

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

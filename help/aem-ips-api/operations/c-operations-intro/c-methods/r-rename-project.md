---
description: Benennt ein Projekt um.
seo-description: Benennt ein Projekt um.
seo-title: renameProject
solution: Experience Manager
title: renameProject
uuid: 6303c493-a6fe-4b32-80c3-947aba4190f7
feature: Dynamic Media Classic, SDK/API, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 20%

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
| `*`companyName`*` | `xsd:string` | Ja | Behandeln Sie die Firma mit dem Projekt, das Sie umbenennen möchten. |
| `*`projectHandle`*` | `xsd:string` | Ja | Nehmen Sie Kontakt zum Projekt auf. |
| `*`projectName`*` | `xsd:string` | Ja | Neuer Projektname. |

**Output (renameProjectParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | Ja | Der Handle des umbenannten Projekts. |

## Beispiele {#section-a0a06d9244774795b695a10b92b2a5e7}

Dieses Codebeispiel benennt ein Projekt um und gibt den Projektgriff zurück.

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


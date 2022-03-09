---
description: Erstellt ein neues Projekt.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 19%

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
| companyHandle | `xsd:string` | Ja | Der Handle des mit dem neuen Projekt verknüpften Unternehmens. |
| projectName | `xsd:string` | Ja | Neuer Projektname. |

**Ausgabe (createProjectParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| projectHandle | `xsd:string` | Ja | Der Handle für das neue Projekt. |

## Beispiele {#section-a0cd532b67e346d088fbec141231a0e5}

Dieses Codebeispiel erstellt ein Projekt mit dem Namen `ApiTestProject` in einem von seinem Handle angegebenen Unternehmen. Die Antwort gibt das Handle an das Projekt zurück.

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

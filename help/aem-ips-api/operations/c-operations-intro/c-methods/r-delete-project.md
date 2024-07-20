---
description: Löscht ein Projekt aus einem Unternehmen. Die Verknüpfungen zwischen den Assets und dem Projekt sind fehlerhaft, die Assets werden jedoch nicht aus dem IPS gelöscht.
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 7%

---

# deleteProject{#deleteproject}

Löscht ein Projekt aus einem Unternehmen. Die Verknüpfungen zwischen den Assets und dem Projekt sind fehlerhaft, die Assets werden jedoch nicht aus dem IPS gelöscht.

Syntax

## Autorisierte Benutzertypen {#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-00d1e00dd5014513a52b4e6b4f61de62}

**Input (deleteProjectParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyName | `xsd:string` | Ja | Der Name des mit dem Projekt verknüpften Unternehmens. |
| projectHandle | `xsd:string` | Ja | Der Handle für das zu löschende Projekt. |

**Output (deleteProjectReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-e38507f1f7ec41b9a625f47390490254}

In diesem Codebeispiel werden das Unternehmens-Handle und das Projekt-Handle als Felder im deleteProjectParam verwendet, die an den IPS-Webdienstserver gesendet werden, um das Projekt zu löschen.

**Anfrage**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Antwort**

Keine.

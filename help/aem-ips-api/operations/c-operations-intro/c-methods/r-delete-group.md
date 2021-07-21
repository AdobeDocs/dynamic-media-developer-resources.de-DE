---
description: Löscht eine Gruppe.
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 13%

---

# deleteGroup{#deletegroup}

Löscht eine Gruppe.

Syntax

## Autorisierte Benutzertypen {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-42775102ec724c36ae5241eea1a00b8e}

**Eingabe (deleteGroupParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Handle des Unternehmens, das zu der Gruppe gehört, die Sie löschen möchten. |
| `*`groupHandle`*` | `xsd:string` | Ja | Der Handle für die Gruppe, die Sie löschen möchten. |

**Ausgabe (deleteGroupParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Mit diesem Beispielcode wird eine Gruppe aus einem Unternehmen gelöscht. Dazu ist ein Gruppenhandle erforderlich, den Sie von einem anderen Vorgang abrufen müssen.

**Anforderung**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Antwort**

Keine.

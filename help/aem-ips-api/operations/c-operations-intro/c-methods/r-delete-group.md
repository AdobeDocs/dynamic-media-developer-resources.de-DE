---
description: Löscht eine Gruppe.
seo-description: Löscht eine Gruppe.
seo-title: deleteGroup
solution: Experience Manager
title: deleteGroup
topic: Scene7 Image Production System API
uuid: 04934b16-b7ef-4657-9f63-c91fcc741ca4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
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
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, die der zu löschenden Gruppe angehört. |
| ` *`groupHandle`*` | `xsd:string` | Ja | Das Handle der Gruppe, die Sie löschen möchten. |

**Output (deleteGroupParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Dieser Beispielcode löscht eine Gruppe aus einer Firma. Es ist ein Gruppengriff erforderlich, den Sie von einem anderen Vorgang abrufen müssen.

**Anforderung**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Antwort**

Keine.

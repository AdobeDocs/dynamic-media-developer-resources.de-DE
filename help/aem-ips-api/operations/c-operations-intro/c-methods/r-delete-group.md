---
description: Löscht eine Gruppe.
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 12%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, die zur zu löschenden Gruppe gehört. |
| `*`groupHandle`*` | `xsd:string` | Ja | Das Handle der Gruppe, die Sie löschen möchten. |

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

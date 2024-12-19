---
description: Erstellen oder Bearbeiten einer Gruppe.
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 18%

---

# saveGroup{#savegroup}

Erstellen oder Bearbeiten einer Gruppe.

Syntax

## Autorisierte Benutzertypen {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-743610e98dd5494baffcbad6401038eb}

**Eingabe (saveGroupParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für die Firma mit der Gruppe, die Sie speichern möchten. |
| groupHandle | `xsd:string` | Nein | Der -Handle für die Gruppe. |
| name | `xsd:string` | Ja | Gruppenname. |
| isSystemDefined | `xsd:boolean` | Ja | `false` ist Standard. |

**Ausgabe (saveGroupReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| groupHandle | `xsd:string` | Ja | Gruppen-Handle. |

## Beispiele {#section-26eee227ff1f4edabb7fa1240b4d9999}

Dieses Codebeispiel erstellt eine Gruppe, die zu einer bestimmten Firma gehört. Wenn die Gruppe bereits vorhanden ist, wird sie mit den angegebenen Parameterwerten gespeichert.

**Anfrage**

```java
<ns1:saveGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:name>My Other Group</ns1:name>
   <ns1:isSystemDefined>false</ns1:isSystemDefined>
</ns1:saveGroupParam>
```

**Antwort**

```java
<saveGroupReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupHandle>281</groupHandle>
</saveGroupReturn>
```

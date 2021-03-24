---
description: Erstellen oder bearbeiten Sie eine Gruppe.
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 19%

---


# saveGroup{#savegroup}

Erstellen oder bearbeiten Sie eine Gruppe.

Syntax

## Autorisierte Benutzertypen {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-743610e98dd5494baffcbad6401038eb}

**Input (saveGroupParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma mit der zu speichernden Gruppe. |
| `*`groupHandle`*` | `xsd:string` | Nein | Der Griff zur Gruppe. |
| `*`name`*` | `xsd:string` | Ja | Gruppenname. |
| `*`isSystemDefined`*` | `xsd:boolean` | Ja | `false` ist Standard. |

**Output (saveGroupReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`groupHandle`*` | `xsd:string` | Ja | Gruppengriff. |

## Beispiele {#section-26eee227ff1f4edabb7fa1240b4d9999}

Dieses Codebeispiel erstellt eine Gruppe, die zu einer bestimmten Firma gehört. Wenn die Gruppe bereits vorhanden ist, wird sie mit den angegebenen Parameterwerten gespeichert.

**Anforderung**

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


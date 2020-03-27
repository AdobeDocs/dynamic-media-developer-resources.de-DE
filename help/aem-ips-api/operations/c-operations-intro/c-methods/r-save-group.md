---
description: Erstellen oder bearbeiten Sie eine Gruppe.
seo-description: Erstellen oder bearbeiten Sie eine Gruppe.
seo-title: saveGroup
solution: Experience Manager
title: saveGroup
topic: Scene7 Image Production System API
uuid: d1631a55-7f1d-48b4-8b35-fd5a05277219
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma mit der zu speichernden Gruppe. |
| ` *`groupHandle`*` | `xsd:string` | Nein | Der Griff zur Gruppe. |
| ` *`name`*` | `xsd:string` | Ja | Gruppenname. |
| ` *`isSystemDefined`*` | `xsd:boolean` | Ja | `false` ist Standard. |

**Output (saveGroupReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`groupHandle`*` | `xsd:string` | Ja | Gruppengriff. |

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


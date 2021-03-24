---
description: Gibt Firmen zurück.
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 20%

---


# getGroups{#getgroups}

Gibt Firmen zurück.

Syntax

## Autorisierte Benutzertypen {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-0e06195f23dd4c69922df210f566dd18}

**Eingabe (getGroupsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma. |

**Ausgabe (getGroupsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | Ja | Array von Gruppen. |

## Beispiele {#section-ed0708f611574354bf0c6ea83912b531}

Dieser Code gibt ein Array zurück, das alle Gruppen enthält, die zu einer bestimmten Firma gehören, sowie spezifische Informationen zu jeder Gruppe.

**Anforderung**

```java
<ns1:getGroupsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupsParam>
```

```java
<getGroupsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle>
         <companyHandle>47</companyHandle>
         <name>MyGroup</name>
         <isSystemDefined>false</isSystemDefined>
      </items>
   </groupArray>
</getGroupsReturn>
```


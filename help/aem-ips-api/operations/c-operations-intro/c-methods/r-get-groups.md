---
description: Gibt Firmen zurück.
seo-description: Gibt Firmen zurück.
seo-title: getGroups
solution: Experience Manager
title: getGroups
uuid: d6e1542d-83a2-4b25-a986-2465e9e5a145
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 19%

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


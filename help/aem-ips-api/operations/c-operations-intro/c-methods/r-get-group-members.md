---
description: Ruft die Benutzer ab, die zu einer bestimmten Firma und Gruppe gehören.
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
TQID: 'https://experienceleague.adobe.com/30uti0zOBWTPoFORCa3fTaGznpYjTcSO7oV7M3E-A1c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 16%

---

# getGroupMembers{#getgroupmembers}

Ruft die Benutzer ab, die zu einer bestimmten Firma und Gruppe gehören.

Syntax

## Autorisierte Benutzertypen {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-b798b06354c946abbb90fa72cc9c67fd}

**Eingabe (getGroupMembersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Griff zum Unternehmen. |
| groupHandle | `xsd:string` |  | Der -Handle für die Gruppe. |

**Ausgabe (getGroupMembersReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| userHandleArray | `type:HandleArray` | Ja | Ein Array von Benutzerhandles. |

## Beispiele {#section-aaa340dba6b64cce9bcd8303cf999166}

Dieses Code-Beispiel gibt ein Benutzer-Handle-Array zurück, das alle Benutzer enthält, die zu einer bestimmten Gruppe gehören.

**Anfrage**

```java
<ns1:getGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
</ns1:getGroupMembersParam>
```

**Antwort**

```java
<getGroupMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userHandleArray>
      <items>70|kmagnusson@adobe.com</items>
   </userHandleArray>
</getGroupMembersReturn>
```

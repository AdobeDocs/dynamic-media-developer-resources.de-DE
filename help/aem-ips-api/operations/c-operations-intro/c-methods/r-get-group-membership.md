---
description: Gibt die Mitglieder einer Gruppe zurück.
solution: Experience Manager
title: getGroupMitgliedschaft
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 847e4982-219d-47fd-b94c-f7d520ba1367
TQID: 'https://experienceleague.adobe.com/V-LNnM0C56dTOos0qky91nxTLyBJMFxLt4VOD99nTN0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 17%

---

# getGroupMitgliedschaft{#getgroupmembership}

Gibt die Mitglieder einer Gruppe zurück.

Syntax

## Autorisierte Benutzertypen {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-2e92f850254e46e48403acaa215341a5}

**Eingabe (getGroupMembershipParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| userHandle | `xsd:string` | Nein | Der Handle für den Benutzer. |
| companyHandle | `xsd:string` | Nein | Der Griff zum Unternehmen. |

**Ausgabe (getGroupMembershipReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| groupArray | `types:GroupArray` | Ja | Array von Gruppen. |

## Beispiele {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Dieses Codebeispiel gibt alle Mitglieder einer Gruppe zurück. Da die Unternehmens- und Benutzerhandles optional sind, kann der Vorgang alle Mitglieder aller Gruppen zurückgeben.

**Anfrage**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**Antwort**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```

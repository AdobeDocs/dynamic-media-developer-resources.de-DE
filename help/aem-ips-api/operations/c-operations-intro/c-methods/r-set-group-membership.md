---
description: Legt die Gruppenmitgliedschaft für einen Benutzer fest.
solution: Experience Manager
title: setGroupMitgliedschaft
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 11%

---

# setGroupMitgliedschaft{#setgroupmembership}

Legt die Gruppenmitgliedschaft für einen Benutzer fest.

Syntax

## Autorisierte Benutzertypen {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Input (setGroupMembershipParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| userHandle | `xsd:string` | Nein | Das -Handle für den Benutzer, dessen Gruppenmitgliedschaft Sie festlegen möchten. |
| companyHandle | `xsd:string` | Nein | Firmengriff. |
| groupHandleArray | `types:HandleArray` | Ja | Das Array von Handles, zu denen die Benutzerin oder der Benutzer gehört. |

**Ausgabe (setGroupMembershipReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-67b86d259df24938896fe19061845811}

Dieses Codebeispiel macht den Benutzer zum Mitglied einer Gruppe. Fügen Sie einen Benutzer mit dem Gruppenhandle-Array mehreren Gruppen hinzu.

**Anfrage**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**Antwort**

Keine.

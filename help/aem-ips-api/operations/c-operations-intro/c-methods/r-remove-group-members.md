---
description: Entfernt Firmenbenutzer aus einer bestimmten Gruppe.
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 8%

---

# removeGroupMembers{#removegroupmembers}

Entfernt Firmenbenutzer aus einer bestimmten Gruppe.

**Unterschiede zwischen &quot;Befehle entfernen&quot;**

* 0: Entfernt mehrere Benutzer aus einer Gruppe.`removeGroupMembers`
* `removeGroupMembership`: Entfernt einen einzelnen Benutzer aus einem Array von Gruppen.

## Autorisierte Benutzertypen {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-b5596614a3be4ce5962455884e4636af}

**Input (removeGroupMembersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen mit den Benutzern, mit denen Sie arbeiten möchten. |
| groupHandle | `xsd:string` | Ja | Gruppieren. |
| userHandleArray | `types:HandleArray` | Ja | Ein Array von Handles für Benutzer, deren Gruppenmitgliedschaften Sie entfernen möchten. |

**Output (removeGroupMembersParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-9eedac852cea46ec80de6a6928bf97ac}

Dieses Codebeispiel entfernt einen Benutzer aus dem angegebenen Unternehmen. Entfernen Sie mehrere Benutzer aus einer Gruppe mit dem Benutzerhandle-Array.

**Anfrage**

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**Antwort**

Keine.

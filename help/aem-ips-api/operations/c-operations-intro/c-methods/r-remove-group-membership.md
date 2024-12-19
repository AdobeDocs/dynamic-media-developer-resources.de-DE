---
description: Entfernt Benutzer aus einem Array von Gruppen.
solution: Experience Manager
title: removeGroupMitgliedschaft
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 892ee01c-e07b-4321-b0b7-5bb606036340
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 8%

---

# removeGroupMitgliedschaft{#removegroupmembership}

Entfernt Benutzer aus einem Array von Gruppen.

**Unterschiede zwischen Entfernen-Befehlen**

* `removeGroupMembers`: Entfernt mehrere Benutzer aus einer Gruppe.
* `removeGroupMembership`: Entfernt einen einzelnen Benutzer aus einem Array von Gruppen.

## Autorisierte Benutzertypen {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Eingabe (removeGroupMembershipParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| userHandle | `xsd:string` | Nein | Das Handle für die Firma, deren Gruppenmitgliedschaft Sie entfernen möchten. |
| groupHandleArray | `types:HandleArray` | Ja | Das Array von Handles für Gruppen, aus denen die Firma entfernt werden soll. |

**Ausgabe (removeGroupMembershipReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-f8d4181170a243efb9faf5824ae96197}

Dieses Codebeispiel entfernt einen Benutzer aus einer Gruppe.

**Anfrage**

```java
<ns1:removeGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>47</ns1:userHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:removeGroupMembershipParam>
```

**Antwort**

Keine.

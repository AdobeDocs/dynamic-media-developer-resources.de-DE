---
description: Entfernt Benutzer aus einem Array von Gruppen.
seo-description: Entfernt Benutzer aus einem Array von Gruppen.
seo-title: removeGroupMembership
solution: Experience Manager
title: removeGroupMembership
uuid: 553d91a3-73d6-4323-9436-a3ba13260a6c
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 9%

---


# removeGroupMembership{#removegroupmembership}

Entfernt Benutzer aus einem Array von Gruppen.

**Unterschiede zwischen Entfernen-Befehlen**

* `removeGroupMembers`: Entfernt mehrere Benutzer aus einer Gruppe.
* `removeGroupMembership`: Entfernt einen einzelnen Benutzer aus einem Array von Gruppen.

## Autorisierte Benutzertypen {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Input (removeGroupMembershipParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nein | Das Handle der Firma, deren Gruppenmitgliedschaft Sie entfernen möchten. |
| `*`groupHandleArray`*` | `types:HandleArray` | Ja | Das Array der Griffe zu Gruppen, aus denen die Firma entfernt werden soll. |

**Output (removeGroupMembershipReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-f8d4181170a243efb9faf5824ae96197}

Mit diesem Codebeispiel wird ein Benutzer aus einer Gruppe entfernt.

**Anforderung**

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

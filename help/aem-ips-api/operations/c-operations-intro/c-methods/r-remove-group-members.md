---
description: Entfernt Firma-Benutzer aus einer bestimmten Gruppe.
seo-description: Entfernt Firma-Benutzer aus einer bestimmten Gruppe.
seo-title: removeGroupMembers
solution: Experience Manager
title: removeGroupMembers
topic: Scene7 Image Production System API
uuid: dd0ea335-bbd0-43b1-830b-77f32dc39b12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeGroupMembers{#removegroupmembers}

Entfernt Firma-Benutzer aus einer bestimmten Gruppe.

**Unterschiede zwischen Entfernen-Befehlen**

* `removeGroupMembers`: Entfernt mehrere Benutzer aus einer Gruppe.
* `removeGroupMembership`: Entfernt einen einzelnen Benutzer aus einem Array von Gruppen.

## Autorisierte Benutzertypen {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-b5596614a3be4ce5962455884e4636af}

**Input (removeGroupMembersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma mit den Benutzern, mit denen Sie arbeiten möchten. |
| ` *`groupHandle`*` | `xsd:string` | Ja | Gruppengriff. |
| ` *`userHandleArray`*` | `types:HandleArray` | Ja | Ein Array von Handles für Benutzer, deren Gruppenmitgliedschaften Sie entfernen möchten. |

**Output (removeGroupMembersParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-9eedac852cea46ec80de6a6928bf97ac}

Mit diesem Codebeispiel wird ein Benutzer aus der angegebenen Firma entfernt. Entfernen Sie mehrere Benutzer aus einer Gruppe mit dem Benutzerhandle-Array.

**Anforderung**

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

---
description: Entfernt Firmen aus einer bestimmten Gruppe.
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 9%

---


# removeGroupMembers{#removegroupmembers}

Entfernt Firmen aus einer bestimmten Gruppe.

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
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma mit den Benutzern, mit denen Sie arbeiten möchten. |
| `*`groupHandle`*` | `xsd:string` | Ja | Gruppengriff. |
| `*`userHandleArray`*` | `types:HandleArray` | Ja | Ein Array von Handles für Benutzer, deren Gruppenmitgliedschaften Sie entfernen möchten. |

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

---
description: Entfernt einen Benutzer aus einem oder mehreren Unternehmen.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 11%

---

# removeCompanyMembership{#removecompanymembership}

Entfernt einen Benutzer aus einem oder mehreren Unternehmen.

Syntax

## Autorisierte Benutzertypen {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-6dfce5e44d8a4799afd0c231a0b10463}

**Eingabe (removeCompanyMembershipParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nein | Das Handle für den Benutzer mit der Mitgliedschaft, die Sie entfernen möchten. |
| `*`companyHandleArray`*` | `types:HandleArray` | Ja | Das Handle für das Unternehmen, aus dem Sie den Benutzer entfernen. |

**Ausgabe (removeCompanyMembershipReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-6b7903195e8647a1bd0502f87387ca62}

Mit diesem Codebeispiel wird ein Benutzer aus einem Unternehmen entfernt. Lassen Sie den optionalen Benutzer-Handle weg, um alle Benutzer aus den im Handle-Array des Unternehmens angegebenen Unternehmen zu entfernen.

**Anforderung**

```java
<ns1:removeCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:removeCompanyMembershipParam>
```

**Antwort**

Keine.

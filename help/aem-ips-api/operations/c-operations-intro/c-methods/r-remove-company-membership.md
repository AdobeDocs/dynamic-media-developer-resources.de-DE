---
description: Entfernt einen Benutzer aus einem oder mehreren Unternehmen.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
TQID: 'https://experienceleague.adobe.com/5jjL8MnUtL046oSej3HErZB9hrD-ueEBC5-h9vD92HM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 10%

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
| userHandle | `xsd:string` | Nein | Das -Handle an den Benutzer mit der Mitgliedschaft, die Sie entfernen möchten. |
| companyHandleArray | `types:HandleArray` | Ja | Der Handle für das Unternehmen, aus dem Sie den Benutzer entfernen. |

**Ausgabe (removeCompanyMembershipReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-6b7903195e8647a1bd0502f87387ca62}

Dieses Codebeispiel entfernt einen Benutzer aus einer Firma. Lassen Sie das optionale Benutzer-Handle weg, um alle Benutzer aus den im Unternehmens-Handle-Array angegebenen Unternehmen zu entfernen.

**Anfrage**

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

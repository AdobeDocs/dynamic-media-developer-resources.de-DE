---
description: Entfernt einen Benutzer aus einer oder mehreren Firmen.
seo-description: Entfernt einen Benutzer aus einer oder mehreren Firmen.
seo-title: removeCompanyMembership
solution: Experience Manager
title: removeCompanyMembership
topic: Scene7 Image Production System API
uuid: af57fde0-2297-41da-87bf-f063fc313264
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 11%

---


# removeCompanyMembership{#removecompanymembership}

Entfernt einen Benutzer aus einer oder mehreren Firmen.

Syntax

## Autorisierte Benutzertypen {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-6dfce5e44d8a4799afd0c231a0b10463}

**Input (removeCompanyMembershipParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Nein | Das Handle für den Benutzer mit der Mitgliedschaft, die Sie entfernen möchten. |
| ` *`companyHandleArray`*` | `types:HandleArray` | Ja | Der Griff zu der Firma, von der Sie den Benutzer entfernen. |

**Output (removeCompanyMembershipReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-6b7903195e8647a1bd0502f87387ca62}

Mit diesem Codebeispiel wird ein Benutzer aus einer Firma entfernt. Lassen Sie den optionalen Benutzerhandle weg, um alle Benutzer aus den im Firmen-Handle-Array angegebenen Firmen zu entfernen.

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

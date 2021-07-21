---
description: Löscht ein Zoomziel.
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 12%

---

# deleteZoomTarget{#deletezoomtarget}

Löscht ein Zoomziel.

## Autorisierte Benutzertypen {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss Lese- und Schreibzugriff auf das Asset haben.

## Parameter {#section-225330a45e7a408f8375e084677d9cb1}

**Eingabe (deleteZoomTargetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle des Unternehmens, zu dem das Zoomziel gehört. |
| `*`zoomTargetHandle`*` | `xsd:string` | Ja | Der Handle zum zu löschenden Zoomziel. |

**Ausgabe (deleteZoomTargetParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiel {#section-a35857a5ca884357a879f7ba6cf985fe}

Mit diesem Codebeispiel wird ein Zoomziel aus einem Unternehmen gelöscht.

**Anforderung**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Antwort**

Keine.

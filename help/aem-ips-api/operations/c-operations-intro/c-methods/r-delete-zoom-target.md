---
description: Löscht ein Zoom-Ziel.
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
TQID: 'https://experienceleague.adobe.com/dAO3kI0G4UM6HHSwWTqJLb0cS4gkfZi-pR-CAbknUe4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 11%

---

# deleteZoomTarget{#deletezoomtarget}

Löscht ein Zoom-Ziel.

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
| companyHandle | `xsd:string` | Ja | Der Ziehgriff zu dem Unternehmen, zu dem das Zoom-Ziel gehört. |
| zoomTargetHandle | `xsd:string` | Ja | Der Ziehgriff auf das zu löschende Zoom-Ziel. |

**Ausgabe (deleteZoomTargetParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiel {#section-a35857a5ca884357a879f7ba6cf985fe}

Dieses Codebeispiel löscht ein Zoom-Ziel aus einem Unternehmen.

**Anfrage**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Antwort**

Keine.

---
description: Löscht eine Zoom-Zielgruppe.
seo-description: Löscht eine Zoom-Zielgruppe.
seo-title: deleteZoomTarget
solution: Experience Manager
title: deleteZoomTarget
topic: Scene7 Image Production System API
uuid: 01a9321f-89a9-4263-937b-b0b49fe2fb81
translation-type: tm+mt
source-git-commit: d3766bba78cd1051538ff6a94f61ba61e989f1a5

---


# deleteZoomTarget{#deletezoomtarget}

Löscht eine Zoom-Zielgruppe.

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff zu der Firma, zu der die Zoom-Zielgruppe gehört. |
| ` *`zoomTargetHandle`*` | `xsd:string` | Ja | Der Griff zur zu löschenden Zoom-Zielgruppe. |

**Output (deleteZoomTargetParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiel {#section-a35857a5ca884357a879f7ba6cf985fe}

Dieses Codebeispiel löscht eine Zoom-Zielgruppe aus einer Firma.

**Anforderung**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Antwort**

Keine.

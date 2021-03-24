---
description: Löscht eine Zoom-Zielgruppe.
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 12%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zu der Firma, zu der die Zoom-Zielgruppe gehört. |
| `*`zoomTargetHandle`*` | `xsd:string` | Ja | Der Griff zur zu löschenden Zoom-Zielgruppe. |

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

---
description: Legt verschiedene firmenspezifische Konfigurationswerte fest.
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
TQID: 'https://experienceleague.adobe.com/df-NUZDApA-q0a-A3oxM6PUQUoVmGy8gqS4HU8lhfvc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 11%

---

# setCompanySettings{#setcompanysettings}

Legt verschiedene firmenspezifische Konfigurationswerte fest.

Syntax

## Autorisierte Benutzertypen {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-a472da6c57c74a94a179dda081004888}

**Eingabe (setCompanySettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Firmengriff. |
| overwriteMode | `xsd:string` | Nein | Asset-Überschreibungsmodus. |
| retainPublishState | `xsd:boolean` | Nein | Legen Sie dies auf `true` fest, um den Veröffentlichungsstatus beim erneuten Hochladen eines Assets beizubehalten. |
| defaultSourceProfileHandle | `xsd:string` | Nein | IccProfile-Asset, das als standardmäßiges Quellfarbprofil verwendet werden soll. |
| defaultDisplayProfileHandle | `xsd:string` | Nein | IccProfile-Asset, das als standardmäßiges Anzeigefarbprofil verwendet werden soll. |
| iptcExifMappingXsltHandle | `xsd:string` | Nein | XSL-Asset für die Zuordnung von IPTC- und EXIF-Metadaten zu IPS-Metadatenfeldern. |
| xmpMappingXsltHandle | `xsd:string` | Nein | XSL-Asset, das zum Zuordnen von XMP-Metadaten zu IPS-Metadatenfeldern verwendet wird. |
| diskSpaceWarningMin | `xsd:int` | Nein | Mindestverfügbarer freier Speicherplatz (in KB), bevor eine Warnmeldung gesendet wird. |
| emailTrashCleanupWarning | `xsd:boolean` | Nein | Wenn auf `true` eingestellt, erhalten Unternehmensadministratoren eine Benachrichtigung, wenn Assets aus dem Papierkorb geleert werden. |

**Ausgabe (setCompanySettingsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

Dieses Code-Beispiel legt die Konfiguration einer Firma fest.

**Anfrage**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**Antwort**

Keine.

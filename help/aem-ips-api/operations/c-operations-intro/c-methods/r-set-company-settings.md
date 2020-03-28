---
description: Legt verschiedene Konfigurationswerte für die Firma fest.
seo-description: Legt verschiedene Konfigurationswerte für die Firma fest.
seo-title: setCompanySettings
solution: Experience Manager
title: setCompanySettings
topic: Scene7 Image Production System API
uuid: 5908082f-6743-4444-ba73-757ad4664890
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setCompanySettings{#setcompanysettings}

Legt verschiedene Konfigurationswerte für die Firma fest.

Syntax

## Autorisierte Benutzertypen {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-a472da6c57c74a94a179dda081004888}

**Input (setCompanySettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| ` *`overwriteMode`*` | `xsd:string` | Nein | Asset-Überschreibungsmodus. |
| ` *`preservePublishState`*` | `xsd:boolean` | Nein | Wird so eingestellt, dass der Veröffentlichungsstatus beim erneuten Hochladen eines Assets beibehalten `true` wird. |
| ` *`defaultSourceProfileHandle`*` | `xsd:string` | Nein | IccProfile-Asset, das als Standard-Quellfarben-Profil verwendet wird. |
| ` *`defaultDisplayProfileHandle`*` | `xsd:string` | Nein | IccProfile-Asset, das als standardmäßiges Profil für die Anzeigefarbe verwendet wird. |
| ` *`iptcExifMappingXsltHandle`*` | `xsd:string` | Nein | XSL-Asset, das zum Zuordnen von IPTC- und EXIF-Metadaten zu IPS-Metadatenfeldern verwendet wird. |
| ` *`xmpMappingXsltHandle`*` | `xsd:string` | Nein | XSL-Asset, das zur Zuordnung von XMP-Metadaten zu IPS-Metadatenfeldern verwendet wird. |
| ` *`diskSpaceWarningMin`*` | `xsd:int` | Nein | Minimaler freier Speicherplatz (in KB), der verfügbar ist, bevor eine Warnmeldung gesendet wird. |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | Nein | Damit `true` senden Sie Firmen-Administratoren eine Benachrichtigung, wenn Assets aus dem Papierkorb geleert werden. |

**Output (setCompanySettingsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

In diesem Codebeispiel wird eine Firma konfiguriert.

**Anforderung**

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

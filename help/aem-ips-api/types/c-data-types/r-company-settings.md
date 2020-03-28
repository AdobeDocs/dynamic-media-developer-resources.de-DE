---
description: Konfigurationseinstellungen für Firmen.
seo-description: Konfigurationseinstellungen für Firmen.
seo-title: CompanySettings
solution: Experience Manager
title: CompanySettings
topic: Scene7 Image Production System API
uuid: a807d5c1-058d-4313-b4f8-6ee203284003
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CompanySettings{#companysettings}

Konfigurationseinstellungen für Firmen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`overwriteMode`*` | `xsd:string` | Legt fest, ob Bilder im aktuellen Ordner mit demselben Namen und derselben Erweiterung des Basisbilds überschrieben werden sollen. |
| ` *`preservePublishState`*` | `xsd:boolean` | Gibt an, ob bei einem in IPS hochgeladenen Ersatzbild die vorhandene Einstellung &quot;Veröffentlichungsbereit&quot;beibehalten werden soll oder ob es den Vorgaben des Uploads entsprechen soll. |
| ` *`defaultSourceProfile`*` | `types:Asset` | Gibt das Standard-Profil für die Quellfarbe (Coated FOGRA27 (ISO 126472:2004)) an, das beim Hinzufügen von CMYK-Bilddateien automatisch als Teil des &quot;Use default Color Behavior&quot;angewendet wird. |
| ` *`defaultDisplayProfile`*` | `types:Asset` | Gibt das standardmäßige interne Farbschema (U.S. Web Coated (SWOP) v2) an, das beim Hinzufügen von CMYK-Bilddateien automatisch als Teil des Profils &quot;Use default Color Behavior&quot;angewendet wird. |
| ` *`iptcExifMappingXslt`*` | `types:Asset` | Die Extraktion von IPTC- und EXIF-Bildkopfzeilendaten in IPS erfordert eine Konvertierung von internen Feldnamen in benutzerdefinierte Feldnamen für die Firma. Bestimmt eine XSL-Translationstabelle (Standard ist &quot;Keine IPTC- oder EXIF-Felder extrahieren&quot;) für hochgeladene Bilder. |
| ` *`xmpMappingXslt`*` | `types:Asset` | Die Extraktion von XMP-Bildkopfzeilendaten in IPS erfordert eine Konvertierung von internen Feldnamen in benutzerdefinierte Feldnamen für die Firma. Bestimmt eine XSL-Translationstabelle (Standard ist &quot;XMP-Felder nicht extrahieren&quot;) für hochgeladene Bilder. |
| ` *`diskSpaceWarningMin`*` | `xsd:int` | Minimaler freier Speicherplatz im Bildverzeichnis, bevor eine Warnung gesendet wird. |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | Legt fest, ob E-Mails gesendet werden sollen, bevor Elemente, die in den Papierkorb gelegt werden, automatisch gelöscht werden können. |
| ` *`javascriptUploadEnabled`*` | `types:Asset` | Legt fest, ob JavaScript-Dateien hochgeladen werden sollen. Dies ist ein potenzielles Sicherheitsrisiko, also nutzen Sie diese Option mit Vorsicht. |


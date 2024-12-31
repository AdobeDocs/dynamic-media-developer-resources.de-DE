---
description: Firmenspezifische Konfigurationseinstellungen.
solution: Experience Manager
title: Unternehmenseinstellungen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# [!DNL CompanySettings]{#companysettings}

Firmenspezifische Konfigurationseinstellungen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| overwriteMode | `xsd:string` | Legt fest, ob Bilder im aktuellen Ordner mit demselben Namen und derselben Erweiterung für das Basisbild überschrieben werden. |
| retainPublishState | `xsd:boolean` | Gibt an, ob ein in IPS hochgeladenes Ersatzbild die vorhandene Einstellung „Bereit für Publish&quot; beibehalten soll oder ob es wie vom Upload angegeben sein soll. |
| defaultSourceProfile | `types:Asset` | Gibt das standardmäßige Quellfarbprofil (Coated FOGRA27 (ISO 126472:2004)) an, das beim Hinzufügen von CMYK-Bilddateien automatisch als Teil von „Standardfarbverhalten verwenden“ angewendet wird. |
| defaultDisplayProfile | `types:Asset` | Legt das standardmäßige interne Farbprofil (U.S. Web Coated (SWOP) v2) fest, das automatisch als Teil des „Use default color behavior“ (Standardfarbverhalten verwenden) beim Hinzufügen von CMYK-Bilddateien angewendet wird. |
| iptcExifMappingXslt | `types:Asset` | Die Extraktion von IPTC- und EXIF-Bildkopfzeilendaten in IPS erfordert eine Konvertierung von internen Feldnamen in benutzerdefinierte Feldnamen für das Unternehmen. Bestimmt eine XSL-Übersetzungstabelle (der Standardwert lautet „Keine IPTC- oder EXIF-Felder extrahieren„) für hochgeladene Bilder. |
| xmpMappingXslt | `types:Asset` | Die Extraktion von XMP-Bildkopfzeilendaten in IPS erfordert eine Konvertierung von internen Feldnamen in benutzerdefinierte Feldnamen für das Unternehmen. Bestimmt eine XSL-Übersetzungstabelle für hochgeladene Bilder (der Standardwert lautet „Keine XMP-Felder extrahieren„). |
| diskSpaceWarningMin | `xsd:int` | Mindestmenge an freiem Speicherplatz im Image-Verzeichnis, bevor eine Warnung gesendet wird. |
| emailTrashCleanupWarning | `xsd:boolean` | Bestimmt, ob E-Mails gesendet werden, bevor Papierkorb-Elemente automatisch gelöscht werden. |
| javascriptUploadEnabled | `types:Asset` | Legt fest, ob JavaScript-Dateien hochgeladen werden. Diese Option stellt ein potenzielles Sicherheitsrisiko dar. Seien Sie daher vorsichtig. |

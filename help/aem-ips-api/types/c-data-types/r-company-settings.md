---
description: Unternehmenspezifische Konfigurationseinstellungen.
solution: Experience Manager
title: CompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# [!DNL CompanySettings]{#companysettings}

Unternehmenspezifische Konfigurationseinstellungen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| overwriteMode | `xsd:string` | Bestimmt, ob Bilder im aktuellen Ordner mit demselben Basisbildnamen und derselben Erweiterung überschrieben werden. |
| keepPublishState | `xsd:boolean` | Gibt an, ob bei einem in IPS hochgeladenen Ersatzbild die vorhandene Einstellung &quot;Bereit für Publish&quot;beibehalten werden soll oder ob es gemäß den Vorgaben des Uploads sein soll. |
| defaultSourceProfile | `types:Asset` | Gibt das standardmäßige Quellfarbprofil (Coated FOGRA27 (ISO 126472:2004) an, das beim Hinzufügen von CMYK-Bilddateien automatisch als Teil von &quot;Use default Color Behavior&quot;angewendet wird. |
| defaultDisplayProfile | `types:Asset` | Gibt das standardmäßige interne Farbprofil (U.S. Web Coated (SWOP) v2) an, das automatisch als Teil des &quot;Use default Color Behavior&quot;angewendet wird, wenn CMYK-Bilddateien hinzugefügt werden. |
| iptcExifMappingXslt | `types:Asset` | Die Extraktion von IPTC- und EXIF-Bildkopfzeilendaten in IPS erfordert eine Konvertierung von internen Feldnamen in benutzerdefinierte Feldnamen für das Unternehmen. Bestimmt eine XSL-Übersetzungstabelle (standardmäßig &quot;Keine IPTC- oder EXIF-Felder extrahieren&quot;) für hochgeladene Bilder. |
| xmpMappingXslt | `types:Asset` | Die Extraktion XMP Bildkopfzeilendaten in IPS erfordert eine Konvertierung von internen Feldnamen in benutzerdefinierte Feldnamen für das Unternehmen. Bestimmt eine XSL-Übersetzungstabelle (standardmäßig &quot;XMP Felder nicht extrahieren&quot;) für hochgeladene Bilder. |
| diskSpaceWarningMin | `xsd:int` | Mindestens freier Speicherplatz im Bildverzeichnis, bevor eine Warnung gesendet wird. |
| emailTrashCleanupWarning | `xsd:boolean` | Bestimmt, ob E-Mails gesendet werden sollen, bevor Elemente aus dem Papierkorb automatisch gelöscht werden. |
| javascriptUploadEnabled | `types:Asset` | Bestimmt, ob JavaScript-Dateien hochgeladen werden. Diese Option stellt ein potenzielles Sicherheitsrisiko dar, daher sollten Sie mit Vorsicht vorgehen. |

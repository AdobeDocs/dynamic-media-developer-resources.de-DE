---
description: Unternehmenspezifische Konfigurationseinstellungen.
solution: Experience Manager
title: CompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 2%

---

# [!DNL CompanySettings]{#companysettings}

Unternehmenspezifische Konfigurationseinstellungen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| overwriteMode | `xsd:string` | Bestimmt, ob Bilder im aktuellen Ordner mit demselben Basisbildnamen und derselben Erweiterung überschrieben werden. |
| keepPublishState | `xsd:boolean` | Gibt an, ob bei einem in IPS hochgeladenen Ersatzbild die vorhandene Einstellung &quot;Veröffentlichungsbereit&quot;beibehalten werden soll oder ob es gemäß den Vorgaben des Uploads sein soll. |
| defaultSourceProfile | `types:Asset` | Gibt das standardmäßige Quellfarbprofil (Coated FOGRA27 (ISO 126472:2004) an, das beim Hinzufügen von CMYK-Bilddateien automatisch als Teil von &quot;Use default Color Behavior&quot;angewendet wird. |
| defaultDisplayProfile | `types:Asset` | Gibt das standardmäßige interne Farbprofil (U.S. Web Coated (SWOP) v2) an, das automatisch als Teil des &quot;Use default Color Behavior&quot;angewendet wird, wenn CMYK-Bilddateien hinzugefügt werden. |
| iptcExifMappingXslt | `types:Asset` | Die Extraktion von IPTC- und EXIF-Bildkopfzeilendaten in IPS erfordert eine Konvertierung von internen Feldnamen in benutzerdefinierte Feldnamen für das Unternehmen. Bestimmt eine XSL-Übersetzungstabelle (standardmäßig &quot;Keine IPTC- oder EXIF-Felder extrahieren&quot;) für hochgeladene Bilder. |
| xmpMappingXslt | `types:Asset` | Die Extraktion XMP Bildkopfzeilendaten in IPS erfordert eine Konvertierung von internen Feldnamen in benutzerdefinierte Feldnamen für das Unternehmen. Bestimmt eine XSL-Übersetzungstabelle (standardmäßig &quot;XMP Felder nicht extrahieren&quot;) für hochgeladene Bilder. |
| diskSpaceWarningMin | `xsd:int` | Mindestens freier Speicherplatz im Bildverzeichnis, bevor ein Warnhinweis gesendet wird. |
| emailTrashCleanupWarning | `xsd:boolean` | Bestimmt, ob E-Mails gesendet werden sollen, bevor im Papierkorb platzierte Elemente automatisch gelöscht werden können. |
| javascriptUploadEnabled | `types:Asset` | Bestimmt, ob JavaScript-Dateien hochgeladen werden. Dies ist ein potenzielles Sicherheitsrisiko. Verwenden Sie daher diese Option mit Vorsicht. |

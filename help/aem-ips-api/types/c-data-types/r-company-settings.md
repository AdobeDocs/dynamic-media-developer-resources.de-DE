---
description: Firmenspezifische Konfigurationseinstellungen.
solution: Experience Manager
title: Unternehmenseinstellungen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
TQID: 'https://experienceleague.adobe.com/iGc-AwCFbpkATjLjvSBtx4vsP0-OUDSkH2dFHZ-j2rg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 244
ht-degree: 2%

---

# [!DNL CompanySettings]{#companysettings}

Firmenspezifische Konfigurationseinstellungen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| overwriteMode | `xsd:string` | Legt fest, ob Bilder im aktuellen Ordner mit demselben Namen und derselben Erweiterung für das Basisbild überschrieben werden. |
| retainPublishState | `xsd:boolean` | Gibt an, ob ein in IPS hochgeladenes Ersatzbild die vorhandene Einstellung „Veröffentlichungsbereit“ beibehalten soll oder ob es wie vom Upload angegeben veröffentlicht werden soll. |
| defaultSourceProfile | `types:Asset` | Gibt das standardmäßige Quellfarbprofil (Coated FOGRA27 (ISO 126472:2004)) an, das beim Hinzufügen von CMYK-Bilddateien automatisch als Teil des „Use default color behavior“ (Standardfarbverhalten verwenden) angewendet wird. |
| defaultDisplayProfile | `types:Asset` | Legt das standardmäßige interne Farbprofil (U.S. Web Coated (SWOP) v2) fest, das automatisch als Teil des „Use default color behavior“ (Standardfarbverhalten verwenden) beim Hinzufügen von CMYK-Bilddateien angewendet wird. |
| iptcExifMappingXslt | `types:Asset` | Die Extraktion von IPTC- und EXIF-Bildkopfzeilendaten in IPS erfordert eine Konvertierung von internen Feldnamen in benutzerdefinierte Feldnamen für das Unternehmen. Bestimmt eine XSL-Übersetzungstabelle (der Standardwert lautet „Keine IPTC- oder EXIF-Felder extrahieren„) für hochgeladene Bilder. |
| xmpMappingXslt | `types:Asset` | Die Extraktion von XMP-Bildkopfzeilendaten in IPS erfordert eine Konvertierung von internen Feldnamen in benutzerdefinierte Feldnamen für das Unternehmen. Bestimmt eine XSL-Übersetzungstabelle für hochgeladene Bilder (der Standardwert lautet „Keine XMP-Felder extrahieren„). |
| diskSpaceWarningMin | `xsd:int` | Mindestmenge an freiem Speicherplatz im Image-Verzeichnis, bevor eine Warnung gesendet wird. |
| emailTrashCleanupWarning | `xsd:boolean` | Bestimmt, ob E-Mails gesendet werden, bevor Papierkorb-Elemente automatisch gelöscht werden. |
| javascriptUploadEnabled | `types:Asset` | Legt fest, ob JavaScript-Dateien hochgeladen werden. Diese Option stellt ein potenzielles Sicherheitsrisiko dar. Seien Sie daher vorsichtig. |


---
description: Vignette Converter (vntc) ist ein Befehlszeilendienstprogramm, mit dem mit Image Authoring erstellte Inhalte für die Bereitstellung mit Image Rendering vorbereitet werden.
solution: Experience Manager
title: Vignette Converter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Vignette Converter{#vignette-converter}

Vignette Converter (vntc) ist ein Befehlszeilendienstprogramm, mit dem mit Image Authoring erstellte Inhalte für die Bereitstellung mit Image Rendering vorbereitet werden.

[!DNL vntc] befindet sich unter [!DNL  *[!DNL install_root]*\ImageServing\bin]. Er verfügt über die folgenden Funktionen:

* Konvertiert primäre Vignetten in Vignetten mit einfacher Auflösung, mit mehreren Auflösungen oder Pyramid-Produktion (siehe [Vignettenskalierung](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produktions-Schrank und Fenster für Stildateien (siehe `-resolution` und `-jpegquality`).

* Kann verschiedene Dateiversionen von Vignetten-, Cabinets- und Fensterbeläge-Stildateien für die Verwendung mit älteren Versionen des Image Rendering erstellen.
* Extrahiert Ansichtsbilder aus Vignetten, entweder mit voller Auflösung oder Miniaturansichten (siehe `-thumbwidth` und `-image`).
* Extrahiert relevante Eigenschaften aus der Quelldatei (siehe `-info`) und sendet sie an `stdout` oder eine optionale Protokolldatei (siehe `-log`).

Auch wenn die Verwendung von [!DNL vntc] optional ist, wird die optimale Serverleistung dringend empfohlen. [!DNL vntc] implementiert außerdem eine umfassende Fehlerprüfung und kann bei sorgfältiger Verwendung schwerwiegende Serverprobleme, einschließlich Abstürzen, verhindern.

Beim Generieren von Produktionsvignetten wird die Pixelbreite der Ausgabemignette (bzw. 0 bei Pyramid- oder Mehrauflösungs-Vignetten) an den Namen der generierten Vignettendatei angehängt. Bei der Verarbeitung von Kabinett-Stildateien wird die Ausgabeauflösung an den Namen der Ausgabedatei angehängt. Alle Ausgabedateien, einschließlich der optionalen Miniatur-, Bild- und Protokolldateien sowie der Produktions-Vignette- oder Kabinenstil-Datei, werden im selben Verzeichnis abgelegt, in dem sich *[!DNL sourceFile]* befindet (sofern nicht `-destPath` angegeben ist).

[!DNL vntc] begrenzt sich standardmäßig auf maximal 3 GB Arbeitsspeicher. Wenn Vntc diese Grenze erreicht, wird die Verarbeitung beendet und ein Fehler ausgegeben. Diese Beschränkung kann mit `-maxmem` geändert werden.

>[!NOTE]
>
>Das Vignette-Update-Tool in der Image-Authoring kann auch verwendet werden, um Vignetten für die Verwendung zum Image-Rendering vorzubereiten. Ebenso ist das Content Authoring Tool in der Lage, Kabinettsstil-Dateien für die Verwendung mit Image Rendering zu generieren. Verwenden Sie [!DNL vntc] , wenn die Verarbeitung automatisiert werden soll. Die Tools in der Bildbearbeitung enthalten eine grafische Benutzeroberfläche, die in der Regel einfacher interaktiv zu verwenden ist.

## Verwandte Themen {#section-3c756bf17b634543904fdd928adeafb2}

Dokumentation zur Bildbearbeitung

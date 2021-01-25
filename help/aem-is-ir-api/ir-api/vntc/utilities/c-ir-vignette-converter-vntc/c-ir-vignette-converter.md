---
description: Der Vignette Converter (vntc) ist ein Befehlszeilenprogramm, mit dem mit Image Authoring erstellte Inhalte für die Bereitstellung mit Image Rendering vorbereitet werden.
seo-description: Der Vignette Converter (vntc) ist ein Befehlszeilenprogramm, mit dem mit Image Authoring erstellte Inhalte für die Bereitstellung mit Image Rendering vorbereitet werden.
seo-title: Vignette Converter
solution: Experience Manager
title: Vignette Converter
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b32a30d6-ae4a-406f-88a9-e8b0eec394c9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# Vignettenkonverter{#vignette-converter}

Der Vignette Converter (vntc) ist ein Befehlszeilenprogramm, mit dem mit Image Authoring erstellte Inhalte für die Bereitstellung mit Image Rendering vorbereitet werden.

[!DNL vntc] befindet sich in [!DNL  *[!DNL install_root]*\ImageServing\bin]. Es verfügt über die folgenden Funktionen:

* Konvertiert primäre Vignetten in Vignetten mit einer Auflösung, mit mehreren Auflösungen oder in Pyramidenvignetten (siehe [Vignettenskalierung](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Erzeugt Stildateien mit Produktionsschränken und Fenstern (siehe `-resolution` und `-jpegquality`).

* Kann verschiedene Dateiversionen von Vignetten-, Cabinets- und Fensterumschlagsformaten für die Verwendung mit älteren Versionen des Image Rendering erstellen.
* Extrahiert Ansichten aus Vignetten, entweder mit voller Auflösung oder mit Miniaturansichten (siehe `-thumbwidth` und `-image`).
* Extrahiert relevante Eigenschaften aus der Quelldatei (siehe `-info`) und sendet sie an `stdout` oder eine optionale Protokolldatei (siehe `-log`).

Die Verwendung von [!DNL vntc] ist zwar optional, wird jedoch für eine optimale Serverleistung dringend empfohlen. [!DNL vntc] implementiert außerdem eine umfassende Fehlerprüfung und kann schwerwiegende Serverprobleme, einschließlich Abstürzen, bei sorgfältiger Verwendung verhindern.

Beim Generieren von Produktionsvignetten wird die Pixelbreite der Ausgabevignette (bzw. 0 bei Pyramide oder Vignetten mit mehreren Auflösungen) an den Namen der generierten Vignettendatei angehängt. Bei der Verarbeitung von Möbelstil-Dateien wird die Ausgabeauflösung an den Namen der Ausgabedatei angehängt. Alle Ausgabedateien, einschließlich der optionalen Miniaturansicht-, Bild- und Protokolldateien sowie der Produktions-Vignetten- oder Schaltflächenstil-Datei, werden in demselben Ordner abgelegt, in dem sich *[!DNL sourceFile]* befindet (es sei denn, `-destPath` ist angegeben).

[!DNL vntc] begrenzt sich standardmäßig auf maximal 3 GB Arbeitsspeicher. Wenn Vntc diese Beschränkung erreicht, wird die Verarbeitung beendet und es wird ein Fehler ausgegeben. Diese Beschränkung kann mit `-maxmem` geändert werden.

>[!NOTE]
>
>Das Vignette-Aktualisierungstool in Image Authoring kann auch verwendet werden, um Vignetten für die Verwendung als Image Rendering vorzubereiten. Das Content Authoring-Tool ist in der Lage, Mögliche Dateien mit Schaltflächenstil für die Verwendung mit dem Image Rendering zu generieren. Verwenden Sie [!DNL vntc], wenn die Verarbeitung automatisiert werden soll. Die Werkzeuge im Image Authoring beinhalten eine grafische Benutzeroberfläche, die in der Regel einfacher interaktiv zu verwenden ist.

## Verwandte Themen {#section-3c756bf17b634543904fdd928adeafb2}

Dokumentation zum Erstellen von Bildern

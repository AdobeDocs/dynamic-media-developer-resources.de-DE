---
title: Vignettenkonverter
description: Vignette Converter (vntc) ist ein Befehlszeilenprogramm, mit dem mit Image Authoring erstellte Inhalte für die Bereitstellung mit Image Rendering vorbereitet werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Vignettenkonverter{#vignette-converter}

Vignette Converter (vntc) ist ein Befehlszeilenprogramm, mit dem mit Image Authoring erstellte Inhalte für die Bereitstellung mit Image Rendering vorbereitet werden.

[!DNL vntc] befindet sich in [!DNL *[!DNL install_root]*\ImageServing\bin]. Es bietet die folgenden Funktionen:

* Konvertiert primäre Vignetten in Vignetten mit einfacher Auflösung, mehrfacher Auflösung oder Pyramidenproduktion (siehe [Vignettenskalierung](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Erstellt Produktionsschrank- und Fensterabdeckungsstildateien (siehe `-resolution` und `-jpegquality`).

* Erstellen Sie verschiedene Dateiversionen von Vignetten, Schränken und Fensterabdeckungen mit Stildateien für die Verwendung mit älteren Versionen des Bild-Renderings.
* Extrahiert Ansichtsbilder aus Vignetten, entweder in voller Auflösung oder Miniaturen (siehe `-thumbwidth` und `-image`).
* Extrahiert relevante Eigenschaften aus der Quelldatei (siehe `-info`) und sendet sie an `stdout` oder eine optionale Protokolldatei (siehe `-log`).

Obwohl die Verwendung von [!DNL vntc] optional ist, empfiehlt Adobe die Verwendung von für eine optimale Server-Leistung. Der Vignette Converter führt außerdem umfangreiche Fehlerprüfungen durch und kann bei sorgfältigem Einsatz schwerwiegende Serverprobleme wie Abstürze verhindern.

Beim Generieren von Produktionsvignetten wird die Pixelbreite der Ausgangsvignette (bzw. 0 bei Pyramiden- oder Vignetten mit mehreren Auflösungen) an den Namen der generierten Ausgangsvignettendatei angehängt. Bei der Verarbeitung von CAB-Style-Dateien wird die Ausgabedateiauflösung an den Namen der Ausgabedatei angehängt. Alle Ausgabedateien, einschließlich der optionalen Miniatur-, Bild- und Protokolldateien sowie der Produktionsvignetten- oder Kabinettstil-Datei, werden im selben Verzeichnis abgelegt, in dem sich *[!DNL sourceFile]* befindet (sofern nicht `-destPath` angegeben ist).

Der Vignette Converter beschränkt sich standardmäßig auf maximal 3 GB Arbeitsspeicher. Wenn diese Grenze erreicht ist, wird die Verarbeitung gestoppt und ein Fehler ausgegeben. Diese Beschränkung kann mithilfe von `-maxmem` geändert werden.

>[!NOTE]
>
>Mit dem Vignetten-Aktualisierungs-Tool in der Bildbearbeitung können Sie auch Vignetten für die Verwendung zum Rendern von Bildern vorbereiten. Ebenso kann das Inhaltserstellungs-Tool Ablagen-Stildateien für die Verwendung mit dem Bild-Rendering generieren. [!DNL vntc] verwenden, wenn die Verarbeitung automatisiert werden soll. Die Tools in der Bildbearbeitung umfassen eine grafische Benutzeroberfläche, wodurch die Verwendung interaktiv in der Regel einfacher wird.

## Verwandte Themen {#section-3c756bf17b634543904fdd928adeafb2}

Dokumentation zur Bildbearbeitung

---
title: Vignettenkonverter
description: Vignette Converter (vntc) ist ein Befehlszeilenprogramm, mit dem mit Image Authoring erstellte Inhalte für die Bereitstellung mit Image Rendering vorbereitet werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
TQID: 'https://experienceleague.adobe.com/NZsbUGCd25rHyvrmt-Rh3XN0p3pHqEtGZrXLp-7JBsc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 337
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

Auch wenn die Verwendung von [!DNL vntc] optional ist, empfiehlt Adobe seine Verwendung für eine optimale Server-Leistung. Der Vignette Converter führt außerdem umfangreiche Fehlerprüfungen durch und kann bei sorgfältigem Einsatz schwerwiegende Serverprobleme wie Abstürze verhindern.

Beim Generieren von Produktionsvignetten wird die Pixelbreite der Ausgangsvignette (bzw. 0 bei Pyramiden- oder Vignetten mit mehreren Auflösungen) an den Namen der generierten Ausgangsvignettendatei angehängt. Bei der Verarbeitung von CAB-Style-Dateien wird die Ausgabedateiauflösung an den Namen der Ausgabedatei angehängt. Alle Ausgabedateien, einschließlich der optionalen Miniatur-, Bild- und Protokolldateien sowie der Produktionsvignetten- oder Kabinettstil-Datei, werden im selben Verzeichnis abgelegt, in dem sich *[!DNL sourceFile]* befindet (sofern nicht `-destPath` angegeben ist).

Der Vignette Converter beschränkt sich standardmäßig auf maximal 3 GB Arbeitsspeicher. Wenn diese Grenze erreicht ist, wird die Verarbeitung gestoppt und ein Fehler ausgegeben. Diese Beschränkung kann mithilfe von `-maxmem` geändert werden.

>[!NOTE]
>
>Mit dem Vignetten-Aktualisierungs-Tool in der Bildbearbeitung können Sie auch Vignetten für die Verwendung zum Rendern von Bildern vorbereiten. Ebenso kann das Inhaltserstellungs-Tool Ablagen-Stildateien für die Verwendung mit dem Bild-Rendering generieren. [!DNL vntc] verwenden, wenn die Verarbeitung automatisiert werden soll. Die Tools in der Bildbearbeitung umfassen eine grafische Benutzeroberfläche, wodurch die Verwendung interaktiv in der Regel einfacher wird.

## Verwandte Themen {#section-3c756bf17b634543904fdd928adeafb2}

Dokumentation zur Bildbearbeitung


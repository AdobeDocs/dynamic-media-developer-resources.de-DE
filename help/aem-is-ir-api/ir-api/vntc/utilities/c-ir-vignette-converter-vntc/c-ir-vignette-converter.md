---
title: Vignette Converter
description: Der Vignette Converter (vntc) ist ein Befehlszeilendienstprogramm, mit dem mit Image Authoring erstellte Inhalte für die Bereitstellung mit Image Rendering vorbereitet werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# Vignette Converter{#vignette-converter}

Der Vignette Converter (vntc) ist ein Befehlszeilendienstprogramm, mit dem mit Image Authoring erstellte Inhalte für die Bereitstellung mit Image Rendering vorbereitet werden.

[!DNL vntc] befindet sich in [!DNL *[!DNL install_root]*\ImageServing\bin]. Er verfügt über die folgenden Funktionen:

* Konvertiert primäre Vignetten in Vignetten mit einer Auflösung, mit mehreren Auflösungen oder in Pyramiden (siehe [Vignette-Skalierung](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produktions-Schrank und Fensterbedeckungen für Stildateien (siehe `-resolution` und `-jpegquality`).

* Erstellen Sie verschiedene Dateiversionen von Vignetten-, Cabinets- und Fensterbeläge-Stildateien für die Verwendung mit älteren Versionen des Image Rendering.
* Extrahiert Ansichtsbilder aus Vignetten, entweder mit voller Auflösung oder Miniaturansichten (siehe `-thumbwidth` und `-image`).
* Extrahiert relevante Eigenschaften aus der Quelldatei (siehe `-info`) und sendet sie an `stdout` oder eine optionale Protokolldatei (siehe `-log`).

Während die Verwendung von [!DNL vntc] optional ist, empfiehlt Adobe seine Verwendung für die beste Serverleistung. Der Vignette Converter implementiert außerdem eine umfangreiche Fehlerprüfung und kann schwerwiegende Serverprobleme, einschließlich Abstürzen, bei sorgfältiger Verwendung verhindern.

Beim Generieren von Produktionsvignetten wird die Pixelbreite der Ausgabemignette (bzw. 0 bei Pyramid- oder Mehrauflösungs-Vignetten) an den Namen der generierten Vignettendatei angehängt. Bei der Verarbeitung von Kabinett-Stildateien wird die Ausgabeauflösung an den Namen der Ausgabedatei angehängt. Alle Ausgabedateien, einschließlich der optionalen Miniaturansichten-, Bild- und Protokolldateien sowie der Produktions-Vignetten- oder Kabinenstil-Datei, werden im selben Verzeichnis abgelegt, in dem *[!DNL sourceFile]* befindet (sofern `-destPath` angegeben ist).

Der Vignette Converter beschränkt sich standardmäßig auf maximal 3 GB Arbeitsspeicher. Wenn vntc diese Beschränkung erreicht, wird die Verarbeitung beendet und ein Fehler erzeugt. Diese Beschränkung kann mithilfe von `-maxmem`.

>[!NOTE]
>
>Das Vignette-Update-Tool in der Image-Authoring kann auch verwendet werden, um Vignetten für die Verwendung zum Image-Rendering vorzubereiten. Auf ähnliche Weise kann das Content Authoring-Tool Kabinettsstildateien für die Verwendung mit dem Image Rendering generieren. Verwendung [!DNL vntc] , wenn die Verarbeitung automatisiert werden soll. Die Tools in der Bildbearbeitung enthalten eine grafische Benutzeroberfläche, die in der Regel einfacher interaktiv zu verwenden ist.

## Verwandte Themen {#section-3c756bf17b634543904fdd928adeafb2}

Dokumentation zur Bildbearbeitung

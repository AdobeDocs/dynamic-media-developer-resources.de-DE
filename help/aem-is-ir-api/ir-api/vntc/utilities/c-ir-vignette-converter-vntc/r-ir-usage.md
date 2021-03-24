---
description: In diesem Thema wird die vntc-Nutzungssyntax beschrieben.
solution: Experience Manager
title: Nutzung
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# Nutzung{#usage}

In diesem Thema wird die vntc-Nutzungssyntax beschrieben.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* ist der Pfad und der Name der zu verarbeitenden Datei. Kann ein Pfad relativ zum aktuellen Arbeitsverzeichnis oder ein absoluter Pfad sein. Muss eine gültige Vignetten-, Schrank- oder Fensterbedeckungsstil-Datei sein und eines der folgenden Suffixe haben: [!DNL .vnt], [!DNL .vnc] oder [!DNL .vnw]. Erforderlich.

*[!DNL destFile]* ist der Pfad und der Name der Vignettenausgabedatei. Wenn nicht angegeben, wird die Ausgabedatei in dem Ordner abgelegt, der mit `-destpath` angegeben wurde. In diesem Szenario wird der Dateiname automatisch aus dem Namen der Eingabedatei und einem Suffix der Größe generiert, wobei die Zeichenfolge mit `-separator` getrennt wird. Bei Vignetten ist das Suffix &quot;Größe&quot;die Pixelbreite der Ausgabe-Vignette mit einer Auflösung, die Breite der ersten Ansicht einer Ausgabe-Vignette mit mehreren Auflösungen oder &quot;0&quot;bei einer Pyramidenvignette. Bei Möbeldateien wird die Ausgabeauflösung als Dateisuffix verwendet. *[!DNL destFile]* wird ignoriert, wenn angegeben  `-info` wird.

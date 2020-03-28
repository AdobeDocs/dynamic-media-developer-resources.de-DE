---
description: In diesem Thema wird die vntc-Nutzungssyntax beschrieben.
seo-description: In diesem Thema wird die vntc-Nutzungssyntax beschrieben.
seo-title: Nutzung
solution: Experience Manager
title: Nutzung
topic: Scene7 Image Serving - Image Rendering API
uuid: 251aa1a0-5f19-42ab-b237-3e3b53fe8320
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Nutzung{#usage}

In diesem Thema wird die vntc-Nutzungssyntax beschrieben.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* ist der Pfad und der Name der zu verarbeitenden Datei. Kann ein Pfad relativ zum aktuellen Arbeitsverzeichnis oder ein absoluter Pfad sein. Muss eine gültige Vignetten-, Schrank- oder Fensterbedeckungsstil-Datei sein und eines der folgenden Suffixe haben: [!DNL .vnt], [!DNL .vnc]oder [!DNL .vnw]. Erforderlich.

*[!DNL destFile]* ist der Pfad und der Name der Vignettenausgabedatei. Wenn keine Angabe gemacht wird, wird die Ausgabedatei in dem Ordner abgelegt, der mit `-destpath`angegeben wurde. In diesem Szenario wird der Dateiname automatisch aus dem Namen der Eingabedatei und einem Suffix der Größe generiert, getrennt durch die mit `-separator`angegebene Zeichenfolge. Bei Vignetten ist das Suffix &quot;Größe&quot;die Pixelbreite der Ausgabe-Vignette mit einer Auflösung, die Breite der ersten Ansicht einer Ausgabe-Vignette mit mehreren Auflösungen oder &quot;0&quot;bei einer Pyramidenvignette. Bei Möbeldateien wird die Ausgabeauflösung als Dateisuffix verwendet. *[!DNL destFile]* wird ignoriert, wenn angegeben `-info` wird.

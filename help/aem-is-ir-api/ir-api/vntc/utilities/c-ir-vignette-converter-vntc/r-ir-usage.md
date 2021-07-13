---
description: Hier wird die VNTC-Nutzungssyntax beschrieben.
solution: Experience Manager
title: Nutzung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# Nutzung{#usage}

Hier wird die VNTC-Nutzungssyntax beschrieben.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* ist der Pfad und der Name der zu verarbeitenden Datei. Kann ein Pfad relativ zum aktuellen Arbeitsverzeichnis oder ein absoluter Pfad sein. Muss eine gültige Vignetten-, Schrank- oder Fensterbedeckungsdatei sein und eines der folgenden Suffixe aufweisen: [!DNL .vnt], [!DNL .vnc] oder [!DNL .vnw]. Erforderlich.

*[!DNL destFile]* ist der Pfad und der Name der Vignettendatei für die Ausgabe. Wenn nicht angegeben, wird die Ausgabedatei in dem Ordner abgelegt, der mit `-destpath` angegeben ist. In diesem Szenario wird der Dateiname automatisch aus dem Namen der Eingabedatei und einem Größensuffix generiert, getrennt durch die Zeichenfolge, die mit `-separator` angegeben wird. Bei Vignetten ist das Suffix der Größe die Pixelbreite der Ausgabedateien-Vignette mit einer Auflösung, die Breite der ersten Ansicht einer AusgabVignette mit mehreren Auflösungen oder &quot;0&quot;bei einer Pyramid-Vignette. Bei Kabinenstil-Dateien wird die Ausgabeauflösung als Dateisuffix verwendet. *[!DNL destFile]* wird ignoriert, wenn angegeben  `-info` ist.

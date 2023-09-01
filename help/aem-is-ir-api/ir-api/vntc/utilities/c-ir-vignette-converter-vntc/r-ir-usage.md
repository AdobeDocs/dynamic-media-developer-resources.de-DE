---
title: Nutzung
description: Hier wird die VNTC-Nutzungssyntax beschrieben.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---

# Nutzung{#usage}

Hier wird die VNTC-Nutzungssyntax beschrieben.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* ist der Pfad und der Name der zu verarbeitenden Datei. Dies kann ein Pfad relativ zum aktuellen Arbeitsverzeichnis oder ein absoluter Pfad sein. Es muss sich um eine gültige Vignette, einen gültigen Kabinettstil oder ein Fenster handeln, das eine Stildatei umfasst und eines der folgenden Suffixe aufweist:

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

Erforderlich.

*[!DNL destFile]* ist der Pfad und der Name der Vignettendatei für die Ausgabe. Wenn nicht angegeben, wird die Ausgabedatei in dem Ordner abgelegt, der mit `-destpath`. In diesem Szenario wird der Dateiname automatisch aus dem Namen der Eingabedatei und einem Suffix der Größe generiert, getrennt durch die Zeichenfolge, die mit `-separator`. Bei Vignetten ist das Suffix der Größe die Pixelbreite der Ausgabedateien-Vignette mit einer Auflösung, die Breite der ersten Ansicht einer AusgabVignette mit mehreren Auflösungen oder &quot;0&quot;, wenn eine Pyramidenvignette vorhanden ist. Bei Kabinenstil-Dateien wird die Ausgabeauflösung als Dateisuffix verwendet. *[!DNL destFile]* wird ignoriert, wenn `-info` festgelegt ist.

---
title: Nutzung
description: In diesem Thema wird die Syntax der vntc-Verwendung beschrieben.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---

# Nutzung{#usage}

In diesem Thema wird die Syntax der vntc-Verwendung beschrieben.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* ist der Pfad und der Name der zu verarbeitenden Datei. Dies kann ein Pfad relativ zum aktuellen Arbeitsverzeichnis oder ein absoluter Pfad sein. Es muss sich um eine gültige Vignette, einen Schrankstil oder eine Fensterabdeckungsstildatei handeln und eines der folgenden Suffixe aufweisen:

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

Erforderlich.

*[!DNL destFile]* ist der Pfad und der Name der Vignettenausgabedatei. Wenn nicht anders angegeben, wird die Ausgabedatei in dem Ordner abgelegt, der mit `-destpath` angegeben wurde. In diesem Szenario wird der Dateiname automatisch aus dem Namen der Eingabedatei und einem Größensuffix generiert, getrennt durch die mit `-separator` angegebene Zeichenfolge. Bei Vignetten ist das Größensuffix die Pixelbreite der Ausgabevignette mit einfacher Auflösung, die Breite der ersten Ansicht einer Ausgabevignette mit mehreren Auflösungen oder „0“, wenn eine Pyramidenvignette vorhanden ist. Bei Dateien im Kabinettstil wird die Ausgabeauflösung als Dateisuffix verwendet. *[!DNL destFile]* wird ignoriert, wenn `-info` angegeben wird.

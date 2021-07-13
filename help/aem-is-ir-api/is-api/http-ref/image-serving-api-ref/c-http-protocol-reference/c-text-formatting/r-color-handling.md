---
description: Die RTF-Spezifikation lässt die mit &bsol;colortbl angegebenen RGB-Farbwerte zu. Jede Komponente wird separat mit den Befehlen &bsol;red, &bsol;green und &bsol;blue bereitgestellt.
solution: Experience Manager
title: Farbhandhabung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Farbhandhabung{#color-handling}

Die RTF-Spezifikation lässt RGB-Farbwerte zu, die mit `\colortbl` angegeben werden. Jede Komponente wird separat mit den Befehlen `\red`, `\green` und `\blue` bereitgestellt.

Der proprietäre RTF-Erweiterungsbefehl `\cmykcolortbl` ermöglicht die Angabe von CMYK-Farben, wobei jede Farbkomponente mit den Befehlen `\cyan`, `\magenta`, `\yellow` und `\black` bereitgestellt wird.

Farbkomponentenwerte für `\colortbl` liegen im Bereich von 0 bis 255. Komponentenwerte für `\cmykcolortbl` liegen im Bereich von 0 bis 100.

Der RTF-Erweiterungsbefehl `\*\iscolortbl`, der von `textPs=` unterstützt wird, bietet eine Möglichkeit, eine Farbtabelle mit standardmäßigen Image Serving-Farbwerten mit voller RGB-, Grau-, CMYK- und Alpha-Unterstützung anzugeben. Sie hat die folgende Syntax:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* einen oder mehrere IS-Farbwerte, durch &#39;;&#39; getrennt

In derselben `text=`- oder `textPs=`-RTF-Zeichenfolge können mehrere Arten von Farbtabellen angegeben werden. Jede Farbtabelle kann eine andere Anzahl von Einträgen aufweisen. Image Serving versucht, Farben in dieser Reihenfolge zu finden: `\iscolortbl` vor `\cmykcolortbl` (nur wenn der Pixeltyp der Textebene CMYK ist) vor `\colortbl`. Nur für `textPs=` werden Farben bei Bedarf genau zwischen CMYK und RGB konvertiert (z. B. wenn RGB-Farben angegeben, aber eine CMYK-Ausgabe erforderlich ist). Wenn keine Farbe für einen bestimmten Indexwert gefunden wird, wird die Standardfarbe (schwarz) verwendet.

Eine Beschreibung der Syntax von IS-Farbwerten finden Sie unter [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) .

## Einschränkungen {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` unterstützt nicht  `\*\iscolortbl`. `textPs=` unterstützt nicht  `\cmykcolortbl`.

Farbauswahlen werden beim Rendern von Fotofonts ignoriert.

## Beispiel {#section-0f166bb72bd44479be01131077851142}

Lassen Sie die Steuerung von drei Textfarben mit Variablen zu, während der Standardwert für die Farbe weiterhin angezeigt wird, wenn die RTF-Zeichenfolge in einem Standard-RTF-Texteditor geöffnet wird.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`

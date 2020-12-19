---
description: Die RTF-Spezifikation erlaubt die Angabe von RGB-Farbwerten mit &bsol;colortbl. Jede Komponente wird separat mit den Befehlen &bsol;red, &bsol;green und &bsol;blue bereitgestellt.
solution: Experience Manager
title: Farbhandhabung
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 925fb4b0a9018d711ea9a1db248dc2ddc803c9fb
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# Farbbehandlung{#color-handling}

Die RTF-Spezifikation erlaubt RGB-Farbwerte, die mit `\colortbl` angegeben werden. Jede Komponente wird separat mit den Befehlen `\red`, `\green` und `\blue` bereitgestellt.

Der proprietäre Befehl für die RTF-Erweiterung `\cmykcolortbl` ermöglicht die Angabe von CMYK-Farben, wobei jede Farbkomponente mit den Befehlen `\cyan`, `\magenta`, `\yellow` und `\black` bereitgestellt wird.

Farbkomponentenwerte für `\colortbl` liegen im Bereich von 0 bis 255. Komponentenwerte für `\cmykcolortbl` liegen im Bereich von 0 bis 100.

Der Befehl für die RTF-Erweiterung `\*\iscolortbl`, unterstützt von `textPs=`, bietet eine Möglichkeit, eine Farbtabelle mit standardmäßigen Image Serving-Farbwerten mit voller RGB-, Grau-, CMYK- und Alpha-Unterstützung anzugeben. Es hat folgende Syntax:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* ein oder mehrere IS-Farbwerte, durch &#39;;&#39; getrennt

In derselben `text=`- oder `textPs=`-RTF-Zeichenfolge können mehrere Arten von Farbtabellen angegeben werden. Jede Farbtabelle kann eine andere Anzahl von Einträgen haben. Image Serving versucht, Farben in der folgenden Reihenfolge zu finden: `\iscolortbl` vor `\cmykcolortbl` (nur wenn der Pixeltyp der Textebene CMYK ist) vor `\colortbl` Nur für `textPs=` werden Farben bei Bedarf genau zwischen CMYK und RGB konvertiert (z. B. wenn RGB-Farben angegeben sind, aber CMYK-Ausgabe erforderlich ist). Wenn für einen bestimmten Indexwert keine Farbe gefunden wird, wird die Standardfarbe (schwarz) verwendet.

Eine Beschreibung der Syntax von IS-Farbwerten finden Sie unter [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md).

## Einschränkungen {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` wird nicht unterstützt  `\*\iscolortbl`. `textPs=` wird nicht unterstützt  `\cmykcolortbl`.

Farbauswahlen werden beim Rendern von Fotofonts ignoriert.

## Beispiel {#section-0f166bb72bd44479be01131077851142}

Zulassen, dass drei Textfarben mit Variablen gesteuert werden, während der Standardwert für Farbe angezeigt wird, wenn die RTF-Zeichenfolge in einem Standard-RTF-Texteditor geöffnet wird.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`

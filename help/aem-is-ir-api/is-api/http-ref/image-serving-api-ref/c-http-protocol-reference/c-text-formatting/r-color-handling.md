---
description: Die RTF-Spezifikation erlaubt RGB-Farbwerte, die mit \colortbl angegeben werden. Jede Komponente wird separat mit den Befehlen \red, \green und \blue bereitgestellt.
seo-description: Die RTF-Spezifikation erlaubt RGB-Farbwerte, die mit \colortbl angegeben werden. Jede Komponente wird separat mit den Befehlen \red, \green und \blue bereitgestellt.
seo-title: Farbhandhabung
solution: Experience Manager
title: Farbhandhabung
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 341693d69fc414dacf984d66e2eaeba2418e663b

---


# Farbhandhabung{#color-handling}

Die RTF-Spezifikation erlaubt die Angabe von RGB-Farbwerten mit `\colortbl`. Jede Komponente wird separat mit den Befehlen `\red`, `\green`und `\blue` bereitgestellt.

Der proprietäre Befehl für die RTF-Erweiterung `\cmykcolortbl` ermöglicht die Angabe von CMYK-Farben, wobei jede Farbkomponente mit den Befehlen `\cyan`, `\magenta`, `\yellow`und `\black` versehen ist.

Farbkomponentenwerte für `\colortbl` liegen im Bereich von 0 bis 255. Komponentenwerte für `\cmykcolortbl` liegen im Bereich von 0 bis 100.

Der Befehl RTF Extension `\*\iscolortbl`unterstützt `textPs=`die Auswahl einer Farbtabelle mit standardmäßigen Image Serving-Farbwerten mit voller RGB-, Grau-, CMYK- und Alpha-Unterstützung. Es hat folgende Syntax:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* ein oder mehrere IS-Farbwerte, durch &#39;;&#39; getrennt

Es kann mehr als ein Farbtabellentyp in derselben `text=` oder derselben `textPs=` RTF-Zeichenfolge angegeben werden. Jede Farbtabelle kann eine andere Anzahl von Einträgen haben. Image Serving versucht, Farben in der folgenden Reihenfolge zu finden: Vor `\iscolortbl``\cmykcolortbl` (nur, wenn der Pixeltyp der Textebene CMYK ist) `\colortbl`. Nur `textPs=` bei Bedarf werden Farben genau zwischen CMYK und RGB konvertiert (z. B. wenn RGB-Farben angegeben sind, aber CMYK-Ausgabe erforderlich ist). Wenn für einen bestimmten Indexwert keine Farbe gefunden wird, wird die Standardfarbe (schwarz) verwendet.

Eine Beschreibung der Syntax von IS-Farbwerten finden Sie unter [Farbe](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) .

## Restrictions {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` wird nicht unterstützt `\*\iscolortbl`. `textPs=` wird nicht unterstützt `\cmykcolortbl`.

Farbauswahlen werden beim Rendern von Fotofonts ignoriert.

## Beispiel {#section-0f166bb72bd44479be01131077851142}

Zulassen, dass drei Textfarben mit Variablen gesteuert werden, während der Standardwert für Farbe angezeigt wird, wenn die RTF-Zeichenfolge in einem Standard-RTF-Texteditor geöffnet wird.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`

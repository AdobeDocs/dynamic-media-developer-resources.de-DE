---
title: Farbhandhabung
description: Die RTF-Spezifikation ermöglicht RGB-Farbwerte, die mit &bsol;colortbl angegeben werden. Jede Komponente wird separat mit den Befehlen &bsol;red, &bsol;green und &bsol;blue bereitgestellt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Farbhandhabung{#color-handling}

Die RTF-Spezifikation ermöglicht RGB-Farbwerte, die mit `\colortbl` angegeben werden. Jede Komponente wird separat mit den Befehlen `\red`, `\green` und `\blue` bereitgestellt.

Der proprietäre RTF-Erweiterungsbefehl `\cmykcolortbl` ermöglicht die Angabe von CMYK-Farben, wobei jede Farbkomponente mit den Befehlen `\cyan`, `\magenta`, `\yellow` und `\black` bereitgestellt wird.

Farbkomponentenwerte für `\colortbl` liegen im Bereich von 0-255. Die Komponentenwerte für `\cmykcolortbl` liegen im Bereich von 0 bis 100.

Der RTF-Erweiterungsbefehl `\*\iscolortbl`, der von `textPs=` unterstützt wird, bietet eine Möglichkeit, eine Farbtabelle mit standardmäßigen Image Serving-Farbwerten mit voller RGB-, Grau-, CMYK- und Alpha-Unterstützung anzugeben. Sie hat die folgende Syntax:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* Ein oder mehrere IS-Farbwerte, getrennt durch &#39;;&#39;

In derselben RTF-Zeichenfolge für `text=` oder `textPs=` kann mehr als ein Farbtabellentyp angegeben werden. Jede Farbtabelle kann eine andere Anzahl von Einträgen aufweisen. Image Serving versucht, Farben in dieser Reihenfolge zu finden: `\iscolortbl` vor `\cmykcolortbl` (nur wenn der Pixeltyp der Textebene CMYK ist) vor `\colortbl`. Nur für `textPs=` werden Farben bei Bedarf genau zwischen CMYK und RGB konvertiert (z. B. wenn RGB-Farben angegeben, aber eine CMYK-Ausgabe erforderlich ist). Wenn keine Farbe für einen bestimmten Indexwert gefunden wird, wird die Standardfarbe (schwarz) verwendet.

Eine Beschreibung der Syntax der IS-Farbwerte finden Sie unter [Farbe](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) .

## Einschränkungen {#section-c5173e672d854e4aa9656844f7fc4d0e}

Der Modifikator `text=` unterstützt `\*\iscolortbl` nicht. Der Modifikator `textPs=` unterstützt `\cmykcolortbl` nicht.

Farbauswahlen werden beim Rendern von Fotofonts ignoriert.

## Beispiel {#section-0f166bb72bd44479be01131077851142}

Lassen Sie die Steuerung von drei Textfarben mit Variablen zu, während der Standardwert für die Farbe weiterhin angezeigt wird, wenn die RTF-Zeichenfolge in einem Standard-RTF-Texteditor geöffnet wird.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`

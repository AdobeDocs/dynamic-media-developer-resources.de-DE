---
title: Farbhandhabung
description: Die RTF-Spezifikation ermöglicht RGB-Farbwerte, die mit &bsol;colortbl angegeben werden. Jede Komponente wird separat mit den Befehlen &bsol;red, &bsol;green und &bsol;blue bereitgestellt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# Farbhandhabung{#color-handling}

Die RTF-Spezifikation ermöglicht RGB-Farbwerte, die mit `\colortbl`. Jede Komponente wird separat mit der `\red`, `\green`, und `\blue` Befehle.

Der proprietäre Befehl der RTF-Erweiterung `\cmykcolortbl` ermöglicht die Angabe von CMYK-Farben, wobei jede Farbkomponente mit der `\cyan`, `\magenta`, `\yellow`, und `\black` Befehle.

Farbkomponentenwerte für `\colortbl` liegen im Bereich von 0-255. Komponentenwerte für `\cmykcolortbl` liegen im Bereich von 0-100.

RTF-Erweiterung, Befehl `\*\iscolortbl`, unterstützt von `textPs=`bietet eine Möglichkeit, eine Farbtabelle mit standardmäßigen Image Serving-Farbwerten mit voller RGB-, Grau-, CMYK- und Alpha-Unterstützung anzugeben. Sie hat die folgende Syntax:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* einen oder mehrere IS-Farbwerte, durch &#39;;&#39; getrennt

Es kann mehr als ein Farbtabellentyp in derselben `text=` oder `textPs=` RTF-Zeichenfolge. Jede Farbtabelle kann eine andere Anzahl von Einträgen aufweisen. Image Serving versucht, Farben in dieser Reihenfolge zu finden: `\iscolortbl` before `\cmykcolortbl` (nur wenn der Pixeltyp der Textebene CMYK ist) vor `\colortbl`. Für `textPs=` Nur Farben werden bei Bedarf zwischen CMYK und RGB genau konvertiert (z. B. wenn RGB-Farben angegeben, aber eine CMYK-Ausgabe erforderlich ist). Wenn keine Farbe für einen bestimmten Indexwert gefunden wird, wird die Standardfarbe (schwarz) verwendet.

Siehe Abschnitt [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) für eine Beschreibung der Syntax der IS-Farbwerte.

## Einschränkungen {#section-c5173e672d854e4aa9656844f7fc4d0e}

Der Modifikator `text=` unterstützt nicht `\*\iscolortbl`. Der Modifikator `textPs=` unterstützt nicht `\cmykcolortbl`.

Farbauswahlen werden beim Rendern von Fotofonts ignoriert.

## Beispiel {#section-0f166bb72bd44479be01131077851142}

Lassen Sie die Steuerung von drei Textfarben mit Variablen zu, während der Standardwert für die Farbe weiterhin angezeigt wird, wenn die RTF-Zeichenfolge in einem Standard-RTF-Texteditor geöffnet wird.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`

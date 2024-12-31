---
title: Farbverarbeitung
description: Die RTF-Spezifikation ermöglicht das RGB von Farbwerten, die mit &bsol;colorTbl angegeben wurden. Jede Komponente wird separat mit den Befehlen &bsol;rot, &bsol;grün und &bsol;blau bereitgestellt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Farbverarbeitung{#color-handling}

Die RTF-Spezifikation ermöglicht das RGB von Farbwerten, die mit `\colortbl` spezifiziert wurden. Jede Komponente wird separat mit den Befehlen `\red`, `\green` und `\blue` bereitgestellt.

Der proprietäre RTF-Erweiterungsbefehl `\cmykcolortbl` die Angabe von CMYK-Farben, wobei jede Farbkomponente mit den Befehlen `\cyan`, `\magenta`, `\yellow` und `\black` versehen ist.

Die Werte der Farbkomponenten für `\colortbl` liegen im Bereich von 0 bis 255. Die Komponentenwerte für `\cmykcolortbl` liegen im Bereich von 0 bis 100.

Der von `textPs=` unterstützte RTF-Erweiterungsbefehl `\*\iscolortbl` bietet die Möglichkeit, eine Farbtabelle mit standardmäßigen Bildbereitstellungsfarbwerten anzugeben, mit vollständiger RGB-, Grau-, CMYK- und Alpha-Unterstützung. Sie weist die folgende Syntax auf:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* einen oder mehrere IS-Farbwerte, getrennt durch &quot;;“

In derselben `text=` oder `textPs=` RTF-Zeichenfolge können mehrere Arten von Farbtabellen angegeben werden. Jede Farbtabelle kann eine andere Anzahl von Einträgen aufweisen. Die Bildbereitstellung versucht, Farben in dieser Reihenfolge zu finden: `\iscolortbl` vor dem `\cmykcolortbl` (nur wenn der Pixeltyp der Textebene CMYK ist) vor dem `\colortbl`. Nur für `textPs=` werden die Farben bei Bedarf genau zwischen CMYK und RGB konvertiert (z. B. wenn RGB-Farben angegeben werden, aber eine CMYK-Ausgabe erforderlich ist). Wenn für einen bestimmten Indexwert keine Farbe gefunden wird, wird die Standardfarbe (Schwarz) verwendet.

Unter [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) finden Sie eine Beschreibung der Syntax von IS-Farbwerten.

## Einschränkungen {#section-c5173e672d854e4aa9656844f7fc4d0e}

Der Modifikator `text=` unterstützt keine `\*\iscolortbl`. Der Modifikator `textPs=` unterstützt keine `\cmykcolortbl`.

Farbauswahl wird beim Rendern von Fotofonts ignoriert.

## Beispiel {#section-0f166bb72bd44479be01131077851142}

Lassen Sie die Steuerung von drei Textfarben mit Variablen zu, während weiterhin der Standardwert für die Farbe angezeigt wird, wenn die RTF-Zeichenfolge in einem standardmäßigen RTF-Texteditor geöffnet wird.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`

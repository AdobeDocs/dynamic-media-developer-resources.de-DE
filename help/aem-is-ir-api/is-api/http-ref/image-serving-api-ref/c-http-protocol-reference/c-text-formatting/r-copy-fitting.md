---
description: textPs= implementiert einen proprietären Kopiereinpassungsalgorithmus, mit dem die Schriftgröße(n) automatisch angepasst wird, um den Textbereich optimal mit Text zu füllen, wodurch zusätzlicher Platz am unteren Rand minimiert wird und ein Überlauf vermieden wird.
seo-description: textPs= implementiert einen proprietären Kopiereinpassungsalgorithmus, mit dem die Schriftgröße(n) automatisch angepasst wird, um den Textbereich optimal mit Text zu füllen, wodurch zusätzlicher Platz am unteren Rand minimiert wird und ein Überlauf vermieden wird.
seo-title: Kopiereinpassung
solution: Experience Manager
title: Kopiereinpassung
topic: Scene7 Image Serving - Image Rendering API
uuid: c3ddbf1f-c724-4436-96ff-2c616dfd355d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---


# Copy-fit{#copy-fitting}

textPs= implementiert einen proprietären Kopiereinpassungsalgorithmus, mit dem die Schriftgröße(n) automatisch angepasst wird, um den Textbereich optimal mit Text zu füllen, wodurch zusätzlicher Platz am unteren Rand minimiert wird und ein Überlauf vermieden wird.

Die Kopiereinfügung kann für die gesamte Textebene einzeln, auch für einen einzelnen Textbereich, einzeln aktiviert und gesteuert werden.

Geben Sie die minimale Schriftgröße mit `\fs` und die maximale Schriftgröße mit `\copyfit` an. In derselben RTF-Zeichenfolge ist eine beliebige Anzahl von Bereichen zulässig. Die Schriftgrößen für alle Bereiche werden proportional variiert, sodass das gewünschte Schriftgrößenverhältnis erhalten bleibt.

`\copyfit` wird als Zeichenformatierungsbefehl betrachtet und hat Scope-Regeln wie  `\fs` und  `\b`.

Die Kopiereinpassung ist deaktiviert, indem `\copyfit` mit einer Größe, die kleiner oder gleich der mit `\fs` angegebenen Größe ist, angegeben wird.

## Begrenzung der Zeilenanzahl {#section-e5aee0f039e04842afc3d6884ed681ac}

Neben der Angabe des Schriftartumfangs kann das Verhalten des Kopiereinpassungsalgorithmus mit den Befehlen `\copyfitlines` oder `\copyfitmaxlines` weiter gesteuert werden, wodurch die Anzahl der Zeilen begrenzt wird, die der Algorithmus generieren soll. Beide Befehle akzeptieren einen Zeilenzählungsparameter oder 0, um die Anzahl der Zeilen im kopierten Bereich nicht zu begrenzen.

`\copyfitlines` ermöglicht den Überlauf von Text in zusätzliche Zeilen, wenn er nicht in die angegebene Zeilenanzahl passt. Explizite Zeilenumbrüche im zu kopierenden Textsegment werden immer berücksichtigt.

`\copyfitmaxlines` schneidet immer zusätzliche Ausgabelinien ab, die den angegebenen Grenzwert überschreiten. Die angegebene Zeilenanzahl wird nie überschritten, selbst wenn explizite Zeilenumbrüche vorhanden sind. Für diese Version von Image Serving dürfen im kopierten Textbereich höchstens N-1 `\line`-Markierungen vorhanden sein. Verhalten ist nicht definiert, wenn dieser Grenzwert überschritten wird.

## Beispiele {#section-f4ddbbfade444560be30a813d90c2c1b}

Die folgenden Beispiele gehen davon aus, dass Textkörper mit Variablen namens *[!DNL $A$]*, *[!DNL $B$]* und *[!DNL $C$]* bereitgestellt werden.

**Beibehalten des gleichen Verhältnisses zwischen Schriftgrößen im gesamten Bereich:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* wird immer doppelt so groß gerendert wie der Rest des Textes. Wenn viel Text angegeben ist, werden *[!DNL $A$]* und *[!DNL $C$]* mit `\fs10` und *[!DNL $B$]* mit `\fs20` gerendert. Bei wenig Text verwenden *[!DNL $A$]* und *[!DNL $C$]* `\fs100` und *[!DNL $B$]* `\fs200`.

**In eine allgemeine Schriftgröße mit großer Schriftgröße konvertieren, wenn nur eine kleine Textmenge gezeichnet wird:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

Am kleinsten Ende des Bereichs wird *[!DNL $B$]* mit `\fs20`, doppelt so groß wie *[!DNL $A$]* und *[!DNL $C$]* bei `\fs10` gerendert. Der gesamte Text wird am gegenüberliegenden Ende des Bereichs mit `\fs100` (50 pts) gezeichnet.

**Konvertieren Sie den Text in eine häufig verwendete kleine Schriftgröße, wenn viel Text gerendert werden soll:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Der gesamte Text wird mit \fs10 am kleinen Ende des Bereichs gezeichnet, während *[!DNL $A$]* und *[!DNL $C$]* am größten mit `\fs100` und *[!DNL $B$]* mit `\fs200` gerendert werden.

**Deaktivieren Sie die Texteinpassung für einen inneren Textbereich:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

Die Schriftgröße für *[!DNL $A$]* und *[!DNL $C$]* kann zwischen 10 und 100 variieren, während *[!DNL $B$]* immer mit `\fs50` gerendert wird.

**Die Ausgabe auf eine einzelne Zeile begrenzen, selbst wenn mehr vertikaler Abstand verfügbar ist, sie jedoch auf zusätzliche Zeilen überlaufen lassen darf, wenn zu viel Text angegeben ist, um in eine Zeile einzupassen  `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Beschränken Sie die Ausgabe auf eine einzelne Zeile, selbst wenn mehr vertikaler Abstand verfügbar ist. Wenn zu viel Text angegeben wurde, um in eine einzelne Zeile unter `\fs10` einzupassen, wird er abgeschnitten:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`

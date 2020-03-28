---
description: $var$-Verweise können an einer beliebigen Stelle innerhalb der geschweiften Klammern einer verschachtelten Image Serving- oder Image Rendering-Anforderung auftreten, auch links neben dem "?" Trennen des Pfads von der Abfrage.
seo-description: $var$-Verweise können an einer beliebigen Stelle innerhalb der geschweiften Klammern einer verschachtelten Image Serving- oder Image Rendering-Anforderung auftreten, auch links neben dem "?" Trennen des Pfads von der Abfrage.
seo-title: Variablenverarbeitung in verschachtelten Anforderungen
solution: Experience Manager
title: Variablenverarbeitung in verschachtelten Anforderungen
topic: Scene7 Image Serving - Image Rendering API
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Variablenverarbeitung in verschachtelten Anforderungen{#variable-processing-in-nested-requests}

$var$-Verweise können an einer beliebigen Stelle innerhalb der geschweiften Klammern einer verschachtelten Image Serving- oder Image Rendering-Anforderung auftreten, auch links neben dem &quot;?&quot; Trennen des Pfads von der Abfrage.

Der Server ersetzt diese Referenzen durch Werte (entweder aus der URL oder aus `catalog::Modifier` dem Hauptbildkatalog), bevor die verschachtelte Anforderung weiter analysiert und verarbeitet wird.

Darüber hinaus werden alle `$ *[!DNL var]*=` `catalog::Modifier` Definitionen aus der URL weitergeleitet und an alle verschachtelten Image Serving- und Image Rendering-Anforderungen weitergeleitet. Dadurch wird sichergestellt, dass alle Variablendefinitionen unabhängig von der Verschachtelungsebene für alle Vorlagen verfügbar sind.

Unabhängig von der Verschachtelungsstufe muss nur eine HTTP-Kodierung mit einem Durchgang auf Variablenwerte angewendet werden, die an einer beliebigen Stelle in verschachtelten Image Rendering- oder Image Serving-Anforderungen ersetzt werden sollen.

---
description: $var$-Verweise können an einer beliebigen Stelle innerhalb der geschweiften Klammern einer verschachtelten Image Serving- oder Image Rendering-Anforderung auftreten, auch links neben dem "?" Trennen des Pfads von der Abfrage.
solution: Experience Manager
title: Variablenverarbeitung in verschachtelten Anforderungen
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# Variablenverarbeitung in verschachtelten Anforderungen{#variable-processing-in-nested-requests}

$var$-Verweise können an einer beliebigen Stelle innerhalb der geschweiften Klammern einer verschachtelten Image Serving- oder Image Rendering-Anforderung auftreten, auch links neben dem &quot;?&quot; Trennen des Pfads von der Abfrage.

Der Server ersetzt diese Referenzen durch Werte (entweder aus der URL oder aus `catalog::Modifier` des Hauptbildkatalogs), bevor die verschachtelte Anforderung weiter analysiert und verarbeitet wird.

Darüber hinaus werden alle `$ *[!DNL var]*=`-Definitionen aus der URL und `catalog::Modifier` an alle verschachtelten Image Serving- und Image Rendering-Anforderungen weitergeleitet. Dadurch wird sichergestellt, dass alle Variablendefinitionen unabhängig von der Verschachtelungsebene für alle Vorlagen verfügbar sind.

Unabhängig von der Verschachtelungsstufe muss nur eine HTTP-Kodierung mit einem Durchgang auf Variablenwerte angewendet werden, die an einer beliebigen Stelle in verschachtelten Image Rendering- oder Image Serving-Anforderungen ersetzt werden sollen.

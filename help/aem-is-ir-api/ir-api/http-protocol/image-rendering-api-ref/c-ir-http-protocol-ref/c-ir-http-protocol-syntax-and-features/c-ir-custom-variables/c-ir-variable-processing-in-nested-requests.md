---
title: Variablenverarbeitung in verschachtelten Anforderungen
description: $var$-Verweise können an einer beliebigen Stelle in den geschweiften Klammern einer verschachtelten Image Serving- oder Image Rendering-Anforderung auftreten, auch links neben "?" Trennen Sie den Pfad von der Abfrage.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Variablenverarbeitung in verschachtelten Anforderungen{#variable-processing-in-nested-requests}

$var$-Verweise können an einer beliebigen Stelle in den geschweiften Klammern einer verschachtelten Image Serving- oder Image Rendering-Anforderung auftreten, auch links neben &quot;?&quot; Trennen Sie den Pfad von der Abfrage.

Der Server ersetzt diese Verweise durch Werte (entweder aus der URL oder aus `catalog::Modifier` des Hauptbildkatalogs), bevor die verschachtelte Anforderung weiter analysiert und verarbeitet wird.

Darüber hinaus werden alle `$ *[!DNL var]*=` -Definitionen aus der URL und `catalog::Modifier` an alle verschachtelten Image Serving- und Image Rendering-Anforderungen weitergeleitet. Dadurch wird sichergestellt, dass alle Variablendefinitionen unabhängig von der Verschachtelungsebene für alle Vorlagen verfügbar sind.

Unabhängig von der Verschachtelungsstufe darf nur eine einmalige HTTP-Kodierung auf Variablenwerte angewendet werden, die an einer beliebigen Stelle in verschachtelten Image Rendering- oder Image Serving-Anforderungen ersetzt werden sollen.

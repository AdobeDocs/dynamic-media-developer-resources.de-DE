---
title: Variablenverarbeitung in verschachtelten Anfragen
description: $var$-Verweise können überall in den geschweiften Klammern einer verschachtelten Bildbereitstellungs- oder Bildrendering-Anfrage auftreten, einschließlich links neben "?“ Trennen des Pfads von der Abfrage
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Variablenverarbeitung in verschachtelten Anfragen{#variable-processing-in-nested-requests}

$var$-Verweise können überall in den geschweiften Klammern einer verschachtelten Bildbereitstellungs- oder Bildrendering-Anfrage auftreten, einschließlich links neben &quot;?“ Trennen des Pfads von der Abfrage

Der Server ersetzt diese Verweise durch Werte (entweder aus der URL oder aus `catalog::Modifier` des Hauptbildkatalogs), bevor die verschachtelte Anfrage weiter analysiert und verarbeitet wird.

Darüber hinaus werden alle `$ *[!DNL var]*=` Definitionen aus der URL und den `catalog::Modifier` an alle verschachtelten Bildbereitstellungs- und Bildrendering-Anfragen weitergeleitet. Dadurch wird sichergestellt, dass alle Variablendefinitionen für alle Vorlagen verfügbar sind, unabhängig von der Verschachtelungsebene.

Unabhängig von der Verschachtelungsebene muss bei Variablenwerten, die in verschachtelten Bildrendering- oder Bildbereitstellungsanfragen an einer beliebigen Stelle ersetzt werden sollen, nur eine HTTP-Kodierung mit einem Durchgang angewendet werden.

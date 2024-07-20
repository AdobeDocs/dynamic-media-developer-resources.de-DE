---
title: Beispiele
description: In diesem Beispiel wird das Image Serving verwendet, um ein Objekt zu kolorisieren und einen Decal anzuwenden, der benutzerdefinierten Text in einem Satz von Vignetten enthält.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 1%

---

# Beispiele{#examples}

In diesem Beispiel wird das Image Serving verwendet, um ein Objekt zu kolorisieren und einen Decal anzuwenden, der benutzerdefinierten Text in einem Satz von Vignetten enthält.

IR -Variablen werden verwendet, um die Vignette, das Logo-Bild und den benutzerdefinierten Text zu identifizieren.

Das Feld `vignette::Modifier` im Datensatz mit dem Namen *template* in der Vignettenkarte des Materialkatalogs `myCat` enthält Folgendes:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Alle verwendeten Vignetten sind in der Vignettenkarte des Materialkatalogs `myCat` aufgeführt.

Der Client kann nun die folgende Anfrage zum Abrufen des Standardbilds stellen (verwendet die am Anfang der Vorlage definierten Variablen):

[!DNL `https://server/myCat/template`]

Die folgende Anfrage gibt bestimmte Inhalte an, die gerendert werden sollen:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Weitere Informationen zum Image Serving-Befehl `text=` finden Sie in der Dokumentation zum Image Serving .

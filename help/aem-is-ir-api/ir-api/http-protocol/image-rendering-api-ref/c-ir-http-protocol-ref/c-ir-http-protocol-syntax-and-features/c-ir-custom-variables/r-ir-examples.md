---
description: In diesem Beispiel wird das Image Serving verwendet, um ein Objekt zu kolorisieren und einen Decal anzuwenden, der benutzerdefinierten Text in einem Satz von Vignetten enthält.
solution: Experience Manager
title: Beispiele
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 1%

---

# Beispiele{#examples}

In diesem Beispiel wird das Image Serving verwendet, um ein Objekt zu kolorisieren und einen Decal anzuwenden, der benutzerdefinierten Text in einem Satz von Vignetten enthält.

IR -Variablen werden verwendet, um die Vignette, das Logo-Bild und den benutzerdefinierten Text zu identifizieren.

Das Feld `vignette::Modifier` im Datensatz *template* in der Vignettenkarte des Materialkatalogs `myCat` enthält Folgendes:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Alle verwendeten Vignetten werden in der Vignettenkarte des Materialkatalogs `myCat` aufgelistet.

Der Client kann nun die folgende Anfrage zum Abrufen des Standardbilds stellen (dabei werden die am Anfang der Vorlage definierten Variablen verwendet):

[!DNL `https://server/myCat/template`]

Die folgende Anfrage gibt bestimmte Inhalte an, die gerendert werden sollen:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Weitere Informationen zum Image-Serving-Befehl `text=` finden Sie in der Image Serving-Dokumentation .

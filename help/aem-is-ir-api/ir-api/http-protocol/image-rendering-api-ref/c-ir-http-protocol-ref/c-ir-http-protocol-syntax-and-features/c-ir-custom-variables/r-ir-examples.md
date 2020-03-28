---
description: In diesem Beispiel wird Image Serving verwendet, um ein Objekt zu färben und einen Ausdruck mit benutzerdefiniertem Text in einem Satz Vignetten anzuwenden.
seo-description: In diesem Beispiel wird Image Serving verwendet, um ein Objekt zu färben und einen Ausdruck mit benutzerdefiniertem Text in einem Satz Vignetten anzuwenden.
seo-title: Beispiele
solution: Experience Manager
title: Beispiele
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f8e4346-6efe-4f21-982d-613328bd708d
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# Beispiele{#examples}

In diesem Beispiel wird Image Serving verwendet, um ein Objekt zu färben und einen Ausdruck mit benutzerdefiniertem Text in einem Satz Vignetten anzuwenden.

Mit IR-Variablen werden die Vignette, das Logo-Bild und der benutzerdefinierte Text identifiziert.

Das `vignette::Modifier` Feld im Datensatz mit dem Namen *template* in der Vignettenzuordnung des Materialkatalogs `myCat` enthält Folgendes:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Alle verwendeten Vignetten werden in der Vignettenkarte des Materialkatalogs aufgeführt `myCat`.

Der Client kann jetzt die folgende Anforderung zum Abrufen des Standardbilds ausführen (dabei werden die am Anfang der Vorlage definierten Variablen verwendet):

[!DNL `https://server/myCat/template`]

Die folgende Anforderung gibt bestimmte Inhalte an, die gerendert werden sollen:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Weitere Informationen zum Image Serving- `text=` Befehl finden Sie in der Dokumentation zum Image Serving.

---
description: In diesem Beispiel wird Image Serving verwendet, um ein Objekt zu färben und einen Ausdruck mit benutzerdefiniertem Text in einem Satz Vignetten anzuwenden.
solution: Experience Manager
title: Beispiele
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---


# Beispiele{#examples}

In diesem Beispiel wird Image Serving verwendet, um ein Objekt zu färben und einen Ausdruck mit benutzerdefiniertem Text in einem Satz Vignetten anzuwenden.

Mit IR-Variablen werden die Vignette, das Logo-Bild und der benutzerdefinierte Text identifiziert.

Das Feld `vignette::Modifier` im Datensatz *template* in der Vignettenzuordnung des Materialkatalogs `myCat` enthält Folgendes:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Alle verwendeten Vignetten werden in der Vignettenkarte des Materialkatalogs `myCat` aufgeführt.

Der Client kann jetzt die folgende Anforderung zum Abrufen des Standardbilds ausführen (dabei werden die am Anfang der Vorlage definierten Variablen verwendet):

[!DNL `https://server/myCat/template`]

Die folgende Anforderung gibt bestimmte Inhalte an, die gerendert werden sollen:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Weitere Informationen zum Befehl Image Serving `text=` finden Sie in der Dokumentation zum Image-Server.

---
title: Beispiele
description: In diesem Beispiel wird die Bildbereitstellung verwendet, um ein Objekt einzufärben und ein Abziehbild mit benutzerdefiniertem Text in einer Gruppe von Vignetten anzuwenden.
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

In diesem Beispiel wird die Bildbereitstellung verwendet, um ein Objekt einzufärben und ein Abziehbild mit benutzerdefiniertem Text in einer Gruppe von Vignetten anzuwenden.

IR-Variablen werden verwendet, um die Vignette, das Logo-Bild und den benutzerdefinierten Text zu identifizieren.

Das `vignette::Modifier` im Datensatz namens *template* in der Vignettenkarte des `myCat` enthält Folgendes:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Alle verwendeten Vignetten sind in der Vignettenkarte des `myCat` aufgeführt.

Der Client kann jetzt die folgende Anfrage stellen, um das Standardbild abzurufen (verwendet die Variablen, die am Anfang der Vorlage definiert sind):

[!DNL `https://server/myCat/template`]

Die folgende Anfrage gibt bestimmte Inhalte an, die gerendert werden sollen:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Weitere Informationen zum Befehl Image-Serving-`text=` finden Sie in der Dokumentation zu Image-Serving .

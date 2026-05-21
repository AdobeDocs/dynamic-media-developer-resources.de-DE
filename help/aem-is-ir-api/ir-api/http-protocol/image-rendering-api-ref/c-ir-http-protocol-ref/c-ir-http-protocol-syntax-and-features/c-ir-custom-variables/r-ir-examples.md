---
title: Beispiele
description: In diesem Beispiel wird die Bildbereitstellung verwendet, um ein Objekt einzufärben und ein Abziehbild mit benutzerdefiniertem Text in einer Gruppe von Vignetten anzuwenden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
TQID: 'https://experienceleague.adobe.com/GMzKDuP-wzTrPJQbxpXc0M08BjCQdWCkGo5jOUiWipU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
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

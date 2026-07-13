---
title: Variablenverarbeitung in verschachtelten Anfragen
description: $var$-Verweise können überall in den geschweiften Klammern einer verschachtelten Bildbereitstellungs- oder Bildrendering-Anfrage auftreten, einschließlich links neben "?“, wodurch der Pfad von der Abfrage getrennt wird.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
TQID: 'https://experienceleague.adobe.com/m7BlSGU8gSozgp8fvNcWuMz5uvpUrfMi4fV5yCYH5bs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 0%

---

# Variablenverarbeitung in verschachtelten Anfragen{#variable-processing-in-nested-requests}

$var$-Verweise können überall in den geschweiften Klammern einer verschachtelten Bildbereitstellungs- oder Bildrendering-Anfrage auftreten, einschließlich links neben &quot;?“, wodurch der Pfad von der Abfrage getrennt wird.

Der Server ersetzt diese Verweise durch Werte (entweder aus der URL oder aus `catalog::Modifier` des Hauptbildkatalogs), bevor die verschachtelte Anfrage weiter analysiert und verarbeitet wird.

Darüber hinaus werden alle `$ *[!DNL var]*=` Definitionen aus der URL und den `catalog::Modifier` an alle verschachtelten Bildbereitstellungs- und Bildrendering-Anfragen weitergeleitet. Dadurch wird sichergestellt, dass alle Variablendefinitionen für alle Vorlagen verfügbar sind, unabhängig von der Verschachtelungsebene.

Unabhängig von der Verschachtelungsebene muss bei Variablenwerten, die in verschachtelten Bildrendering- oder Bildbereitstellungsanfragen an einer beliebigen Stelle ersetzt werden sollen, nur eine HTTP-Kodierung mit einem Durchgang angewendet werden.


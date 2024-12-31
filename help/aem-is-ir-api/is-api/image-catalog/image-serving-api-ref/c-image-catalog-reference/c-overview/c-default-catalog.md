---
description: Der Standardkatalog stellt Standardwerte für alle Katalogattribute für alle Bildkataloge bereit.
solution: Experience Manager
title: Standardkatalog
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Standardkatalog{#default-catalog}

Der Standardkatalog stellt Standardwerte für alle Katalogattribute für alle Bildkataloge bereit.

Wenn ein bestimmtes Attribut in einem bestimmten Bildkatalog nicht gefunden werden kann, verwendet der Server stattdessen den entsprechenden Wert aus dem Standardkatalog. Ebenso kann der Standardkatalog verwendet werden, um Standardwerte für bestimmte Katalogdatensätze (Bilder, Makrodefinitionen, Schriftarten und ICC-Profile) bereitzustellen. Wenn ein bestimmter Datensatz nicht in einem bestimmten Bildkatalog gefunden werden kann, versucht der Server stattdessen, ihn im Standardkatalog zu finden. Dadurch können Bildkataloge spärlich gefüllt werden und die Verwaltung globaler Attribute und Daten, wie freigegebene Vorlagen, Makros, Schriftarten usw. wird vereinfacht.

Darüber hinaus stellt der Standardkatalog alle Attribute und Datensätze bereit (Makros, Schriftarten, ICC-Profile, Regeln für die Anfragevorverarbeitung), wenn an einem Vorgang kein bestimmter Bildkatalog beteiligt ist.

Damit die [!DNL Platform Server] ordnungsgemäß funktioniert, muss die Katalogattributdatei für den Standardkatalog [!DNL default.ini] benannt sein, immer im Katalogordner vorhanden sein und vollständig mit allen erforderlichen Attributen gefüllt sein, mit Ausnahme von `attribute::RootId` und den Verweisen auf die verschiedenen Katalogdatendateien, die alle optional sind.

>[!NOTE]
>
>Alle Katalogattributdateien außer [!DNL default.ini] müssen einen eindeutigen `attribute::RootId` enthalten. `attribute::RootId` in [!DNL default.ini] muss leer sein.

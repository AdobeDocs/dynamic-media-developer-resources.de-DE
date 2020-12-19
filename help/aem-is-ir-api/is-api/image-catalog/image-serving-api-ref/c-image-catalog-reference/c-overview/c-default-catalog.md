---
description: Der Standardkatalog enthält Standardwerte für alle Katalogattribute für alle Bildkataloge.
seo-description: Der Standardkatalog enthält Standardwerte für alle Katalogattribute für alle Bildkataloge.
seo-title: Standardkatalog
solution: Experience Manager
title: Standardkatalog
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f0c967e-a2fa-4ef0-bacb-3dcfb06a8027
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---


# Standardkatalog{#default-catalog}

Der Standardkatalog enthält Standardwerte für alle Katalogattribute für alle Bildkataloge.

Wenn ein bestimmtes Attribut nicht in einem bestimmten Bildkatalog gefunden werden kann, verwendet der Server stattdessen den entsprechenden Wert aus dem Standardkatalog. Gleichermaßen kann der Standardkatalog verwendet werden, um Standardwerte für bestimmte Katalogdatensätze (Bilder, Makrodefinitionen, Schriftarten und ICC-Profile) bereitzustellen. Wenn ein bestimmter Datensatz nicht in einem bestimmten Bildkatalog gefunden werden kann, versucht der Server, ihn stattdessen im Standardkatalog zu finden. Dadurch können Bildkataloge dünn gefüllt werden und die Verwaltung globaler Attribute und Daten wie freigegebene Vorlagen, Makros, Schriftarten usw. wird vereinfacht.

Darüber hinaus stellt der Standardkatalog alle Attribute und Datensätze (Makros, Schriftarten, ICC-Profil, Vorverarbeitungsregeln anfordern) bereit, wenn kein bestimmter Bildkatalog an einem Vorgang beteiligt ist.

Damit der Plattformserver ordnungsgemäß funktioniert, muss die Katalogattributdatei für den Standardkatalog den Namen [!DNL default.ini] haben, muss sich immer im Katalogordner befinden und muss mit allen erforderlichen Attributen gefüllt werden, mit Ausnahme von `attribute::RootId` und der Verweise auf die verschiedenen Katalogdatendateien, die alle optional sind.

>[!NOTE]
>
>Alle Katalogattributdateien mit Ausnahme von [!DNL default.ini] müssen einen eindeutigen `attribute::RootId`-Wert enthalten. `attribute::RootId` in  [!DNL default.ini] muss leer sein.


---
description: Der Standardkatalog stellt Standardwerte für alle Katalogattribute für alle Bildkataloge bereit.
solution: Experience Manager
title: Standardkatalog
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
TQID: 'https://experienceleague.adobe.com/qbfEwBJ-eQmCbBR0MJQhP7x3ZEd30nfLJHWjBVoXIjc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 215
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

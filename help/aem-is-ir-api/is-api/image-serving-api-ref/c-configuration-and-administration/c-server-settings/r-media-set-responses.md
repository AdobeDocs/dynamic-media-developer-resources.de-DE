---
title: Antworten auf Mediensets
description: Die Einstellungen in diesem Abschnitt gelten für die Mediensatzantworten, die vom Modifikator „req=set“ abgerufen werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
TQID: 'https://experienceleague.adobe.com/FNUguOqf8f5FnIeGTzheZU-8zCXqwRMU3YGyvYDA0uM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 0%

---

# Antworten auf Mediensets{#media-set-responses}

Die Einstellungen in diesem Abschnitt gelten für die Medienset-Antworten, die vom Modifikator `req=set` abgerufen werden.

## PS:fvctx.useCatalogRecordValidation - Caching-Richtlinie {#section-9accb087d16548a988993bb30395a6f6}

Diese Eigenschaft steuert die Caching-Richtlinie, wenn bestimmt wird, ob eine aus einem Cache abgerufene Antwort neu generiert werden muss. Wenn die Eigenschaft deaktiviert ist, wird der Zeitstempel der [!DNL catalog.ini] für die Validierung verwendet. Wenn die Eigenschaft aktiviert ist, wird der letzte `catalog::LastModified` Zeitstempel aus allen referenzierten Datensätzen für die Validierung verwendet.

## PS:fvctx.nestingLimit - Schachtelungslimit {#section-280210341f1647fea02590e7069934d2}

Die maximale Verschachtelungstiefe einer `req=set` Antwort. Wenn diese Tiefe überschritten wird, wird ein Fehler zurückgegeben.

## PS::fvctx.brochureLimit - Broschüren-Limit {#section-fe36e47db49244cea7f07e9dd3639440}

Die maximale Anzahl an E-Katalog-Broschüren in der `req=set`-Antwort, die alle zugehörigen Metadaten enthält. Sobald dieses Limit überschritten wird, werden alle privaten Zuordnungen und Benutzerdaten, die mit dem Broschürenelement verknüpft sind, unterdrückt.

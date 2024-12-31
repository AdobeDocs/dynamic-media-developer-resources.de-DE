---
title: Antworten auf Mediensets
description: Die Einstellungen in diesem Abschnitt gelten für die Mediensatzantworten, die vom Modifikator „req=set“ abgerufen werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '146'
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

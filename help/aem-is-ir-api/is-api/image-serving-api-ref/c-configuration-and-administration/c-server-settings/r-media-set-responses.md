---
title: Medienset-Antworten
description: Die Einstellungen in diesem Abschnitt gelten für die Mediensatzantworten, die vom Modifikator req=set abgerufen werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Medienset-Antworten{#media-set-responses}

Die Einstellungen in diesem Abschnitt gelten für die vom Modifikator `req=set` abgerufenen Medienset-Antworten.

## PS::fvctx.useCatalogRecordValidation - Caching-Richtlinie {#section-9accb087d16548a988993bb30395a6f6}

Diese Eigenschaft steuert die Cacherichtlinie, wenn festgestellt wird, ob eine aus einem Cache abgerufene Set-Antwort neu generiert werden muss. Wenn die Eigenschaft deaktiviert ist, wird der Zeitstempel der Datei [!DNL catalog.ini] zur Validierung verwendet. Wenn die -Eigenschaft aktiviert ist, wird zur Überprüfung der aktuelle `catalog::LastModified`-Zeitstempel aller referenzierten Datensätze verwendet.

## PS::fvctx.nestingLimit - Verschachtelungsgrenze {#section-280210341f1647fea02590e7069934d2}

Die maximale Verschachtelungstiefe einer `req=set` -Antwort. Wenn diese Tiefe überschritten wird, wird ein Fehler zurückgegeben.

## PS::fvctx.brochureLimit - Broschürenlimit {#section-fe36e47db49244cea7f07e9dd3639440}

Die maximale Anzahl von E-Katalog-Broschüren in der Antwort &quot;`req=set`&quot;, die alle zugehörigen Metadaten enthält. Sobald diese Grenze überschritten wird, werden alle privaten Karten und Benutzerdaten unterdrückt, die mit dem Prospekt verknüpft sind.

---
description: Die Einstellungen in diesem Abschnitt gelten für die Mediensatzantworten, die vom Modifikator req=set abgerufen werden.
solution: Experience Manager
title: Medienset-Antworten
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Medienset-Antworten{#media-set-responses}

Die Einstellungen in diesem Abschnitt gelten für die Mediensatzantworten, die vom Modifikator req=set abgerufen werden.

## PS::fvctx.useCatalogRecordValidation - Caching-Richtlinie {#section-9accb087d16548a988993bb30395a6f6}

Diese Eigenschaft steuert die Cacherichtlinie, wenn festgestellt wird, ob die aus dem Cache abgerufene Antwort neu generiert werden muss oder nicht. Wenn die -Eigenschaft deaktiviert ist, wird der Zeitstempel der [!DNL catalog.ini]-Datei zur Validierung verwendet. Wenn die -Eigenschaft aktiviert ist, wird zur Validierung der neueste Zeitstempel von `catalog::LastModified` aus allen referenzierten Datensätzen verwendet.

## PS::fvctx.nestingLimit - Verschachtelungsgrenze {#section-280210341f1647fea02590e7069934d2}

Die maximale Verschachtelungstiefe einer `req=set`-Antwort. Wenn diese Tiefe überschritten wird, wird ein Fehler zurückgegeben.

## PS::fvctx.brochureLimit - Broschürenlimit {#section-fe36e47db49244cea7f07e9dd3639440}

Die maximale Anzahl von E-Katalog-Broschüren in der `req=set`-Antwort, die alle zugehörigen Metadaten enthält. Sobald diese Grenze überschritten wird, werden alle privaten Karten und Benutzerdaten unterdrückt, die mit dem Prospekt verknüpft sind.

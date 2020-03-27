---
description: Die Einstellungen in diesem Abschnitt gelten für die Medienset-Antworten, die mit dem Modifikator req=set abgerufen werden.
seo-description: Die Einstellungen in diesem Abschnitt gelten für die Medienset-Antworten, die mit dem Modifikator req=set abgerufen werden.
seo-title: Medienset-Antworten
solution: Experience Manager
title: Medienset-Antworten
topic: Scene7 Image Serving - Image Rendering API
uuid: 9fa6a38a-cd1f-499b-a2b6-e1a9a6c69ed0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Medienset-Antworten{#media-set-responses}

Die Einstellungen in diesem Abschnitt gelten für die Medienset-Antworten, die mit dem Modifikator req=set abgerufen werden.

## PS::fvctx.useCatalogRecordValidation - Cacherichtlinie {#section-9accb087d16548a988993bb30395a6f6}

Diese Eigenschaft steuert die Cacherichtlinie, wenn festgestellt wird, ob die aus dem Cache abgerufene Antwort neu generiert werden muss oder nicht. Wenn die Eigenschaft deaktiviert ist, wird der Zeitstempel der [!DNL catalog.ini] Datei für die Überprüfung verwendet. Wenn die Eigenschaft aktiviert ist, wird der neueste `catalog::LastModified` Zeitstempel aller referenzierten Datensätze zur Überprüfung verwendet.

## PS::fvctx.nestingLimit - Verschachtelungsgrenze {#section-280210341f1647fea02590e7069934d2}

Die maximale Verschachtelungstiefe einer beliebigen `req=set` Antwort. Wenn diese Tiefe überschritten wird, wird ein Fehler zurückgegeben.

## PS::fvctx.brochureLimit - Prospektbeschränkung {#section-fe36e47db49244cea7f07e9dd3639440}

Die maximale Anzahl an E-Katalog-Prospekten in der `req=set` Antwort, die alle zugehörigen Metadaten enthalten. Sobald dieser Grenzwert überschritten wird, werden alle mit dem Prospektelement verknüpften privaten Maps und Benutzerdaten unterdrückt.

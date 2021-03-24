---
description: Die Einstellungen in diesem Abschnitt gelten für die Medienset-Antworten, die mit dem Modifikator req=set abgerufen werden.
solution: Experience Manager
title: Medienset-Antworten
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# Medienset-Antworten{#media-set-responses}

Die Einstellungen in diesem Abschnitt gelten für die Medienset-Antworten, die mit dem Modifikator req=set abgerufen werden.

## PS::fvctx.useCatalogRecordValidation - Cache-Richtlinie {#section-9accb087d16548a988993bb30395a6f6}

Diese Eigenschaft steuert die Cacherichtlinie, wenn festgestellt wird, ob die aus dem Cache abgerufene Antwort neu generiert werden muss oder nicht. Wenn die Eigenschaft deaktiviert ist, wird der Zeitstempel der [!DNL catalog.ini]-Datei für die Überprüfung verwendet. Wenn die Eigenschaft aktiviert ist, wird der neueste `catalog::LastModified`-Zeitstempel aller referenzierten Datensätze für die Überprüfung verwendet.

## PS::fvctx.nestingLimit - Verschachtelungsgrenze {#section-280210341f1647fea02590e7069934d2}

Die maximale Verschachtelungstiefe einer `req=set`-Antwort. Wenn diese Tiefe überschritten wird, wird ein Fehler zurückgegeben.

## PS::fvctx.brochureLimit - Prospektbeschränkung {#section-fe36e47db49244cea7f07e9dd3639440}

Die maximale Anzahl von E-Katalog-Prospekten in der Antwort `req=set`, die alle zugehörigen Metadaten enthält. Sobald dieser Grenzwert überschritten wird, werden alle mit dem Prospektelement verknüpften privaten Maps und Benutzerdaten unterdrückt.

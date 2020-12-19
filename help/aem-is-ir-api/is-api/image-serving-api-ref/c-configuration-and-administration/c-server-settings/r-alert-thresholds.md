---
description: Verwenden Sie diese Servereinstellungen, um Warnschwellenwerte zu konfigurieren.
seo-description: Verwenden Sie diese Servereinstellungen, um Warnschwellenwerte zu konfigurieren.
seo-title: Warnschwellenwerte
solution: Experience Manager
title: Warnschwellenwerte
topic: Scene7 Image Serving - Image Rendering API
uuid: 032cb396-1a03-4ba9-82d6-ed2cb06e8cf2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---


# Warnschwellenwerte{#alert-thresholds}

Verwenden Sie diese Servereinstellungen, um Warnschwellenwerte zu konfigurieren.

## AS: monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS: monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

Eine Warnungsmeldung zur Antwortzeit wird ausgegeben, wenn die durchschnittliche Verarbeitungszeit einer Anforderung während des Stichprobenintervalls den hier festgelegten Schwellenwert überschreitet. ausgedrückt in msec; Ganzzahl 0 oder größer. Typische Werte liegen je nach Komplexität der Vorgänge zwischen 100 und 1000 msec.

>[!NOTE]
>
>Anforderungen, die zu einem 4xx- oder 5xx-Antwortstatus führen, werden für diesen Warnhinweis nicht berücksichtigt.

## AS::monitorAlertGenerator.maxErrorRate - Error Response Rate ThresholdAS::monitorAlertGenerator.maxErrorRate - Error Response Rate {#section-76ba77fd3102419395e0f86719a1f3ec}

Eine Fehlerwarnung wird ausgegeben, wenn das Verhältnis der HTTP-Fehlerantworten zu den Gesamtantworten während des Stichprobenintervalls den angegebenen Schwellenwert überschreitet.

Der reale Wert liegt zwischen 0,0 und 1,0. Normalerweise zwischen 0,005 und 0,1. Auf 1 setzen, um Fehlerwarnungen zu deaktivieren.

## AS::monitorAlertGenerator.minRequestRate - Low Traffic Threshold {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Eine minimale Traffic-Warnung wird gesendet, wenn die durchschnittliche Anzahl der während des aktuellen Stichprobenintervalls eingegangenen Anfragen pro Sekunde unter diesen Schwellenwert fällt. Deaktivieren Sie die Warnung, indem Sie diesen Wert auf 0 setzen. In Anforderungen pro Sekunde ausgedrückt. Realer Wert 0 oder größer.

## AS::monitorAlertGenerator.minFreeHeapSpace -Free Heap Space Threshold {#section-ce6705045f6842769030ccb1894594cc}

Gibt den minimalen freien Java-Heap-Speicherplatz an. Unmittelbar nach einem Java-Garbage Collection-Zyklus wird eine Warnung mit Priorität gesendet, wenn der freie Heap-Speicher unter diesem Schwellenwert liegt. 50 MB werden für den sicheren Betrieb des Plattformservers empfohlen. Durch die Beibehaltung des freien Heap-Speichers über diesem Wert wird die Häufigkeit von Garbage Collection-Zyklen reduziert, was die Serverleistung insgesamt verbessern kann. Ganzzahlwert in Byte, 0 oder größer.

## AS::monitorAlertGenerator.maxOverlap - Maximale Anzahl gleichzeitiger Anfragen {#section-ddc6925bff944758ab19bcc9cf3f2589}

Eine Überschneidungswarnung wird ausgelöst, wenn die durchschnittliche Anzahl der gleichzeitig verarbeiteten Anforderungen während des Durchschnitts diesen Schwellenwert überschreitet. Eine hohe Überschneidung kann auf eine mögliche Serverüberlastung hindeuten.

Ganzzahlwert 1 oder höher. Der typische Bereich liegt zwischen 20 und 50, abhängig von der Cache-Trefferrate und der Anforderungskomplexität.

## AS::monitorAlertGenerator.lockedThreshold - Gesperrter Anforderungsschwellenwert {#section-012a1c9937d445708380339279c62d80}

Gibt die Anzahl der Sekunden an, die eine Anforderung ausstehen muss, bevor sie als gesperrt oder hängend gilt. Eine gesperrte Anforderungswarnung wird ausgegeben, wenn am Ende eines Durchschnitts mindestens eine Anforderung länger als der angegebene Zeitraum aussteht. Positiver ganzzahliger Wert in msec.

Zur Berücksichtigung komplexer Render-Anfragen und -Anfragen, bei denen Daten von ausländischen HTTP-Servern abgerufen werden, wird empfohlen, diesen Wert auf mindestens 30 Sekunden festzulegen (es sei denn, eine solche Bedingung wird durch diesen Warnhinweis erkannt).

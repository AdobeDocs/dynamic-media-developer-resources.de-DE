---
description: Verwenden Sie diese Servereinstellungen, um Warnschwellen zu konfigurieren.
solution: Experience Manager
title: Warnschwellen
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Warnschwellen{#alert-thresholds}

Verwenden Sie diese Servereinstellungen, um Warnschwellen zu konfigurieren.

## AS: monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS: monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

Eine Warnungen zur Antwortzeit wird ausgegeben, wenn die durchschnittliche Verarbeitungszeit für eine Anforderung während des Sampling-Intervalls den hier festgelegten Schwellenwert überschreitet. in ms ausgedrückt; Ganzzahl 0 oder größer. Je nach Komplexität der Vorgänge liegen die typischen Werte zwischen 100 und 1000 ms.

>[!NOTE]
>
>Anforderungen, die zu einem 4xx- oder 5xx-Antwortstatus führen, werden für diesen Warnhinweis nicht berücksichtigt.

## AS::monitorAlertGenerator.maxErrorRate - Error Response Rate ThresholdAS::monitorAlertGenerator.maxErrorRate - Error Response Rate {#section-76ba77fd3102419395e0f86719a1f3ec}

Es wird ein Fehler-Warnhinweis ausgegeben, wenn das Verhältnis der HTTP-Fehlerantworten zu den Gesamtantworten während des Sampling-Intervalls den festgelegten Schwellenwert überschreitet.

Realer Wert zwischen 0,0 und 1,0. In der Regel auf 0,005 bis 0,1 gesetzt. Auf 1 setzen, um Fehlerwarnungen zu deaktivieren.

## AS::monitorAlertGenerator.minRequestRate - Low Traffic Threshold {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Eine minimale Traffic-Warnung wird gesendet, wenn die durchschnittliche Anzahl der Anfragen pro Sekunde, die im aktuellen Stichprobenintervall empfangen werden, unter diesen Schwellenwert fällt. Deaktivieren Sie den Warnhinweis, indem Sie diesen Wert auf 0 setzen. Wird in Anforderungen pro Sekunde ausgedrückt. Realer Wert 0 oder größer.

## AS::monitorAlertGenerator.minFreeHeapSpace -Free Heap Space Threshold {#section-ce6705045f6842769030ccb1894594cc}

Gibt den minimalen freien Java-Heap-Speicherplatz an. Ein Warnhinweis mit Priorität wird unmittelbar nach einem Java-Speicherbereinigungszyklus gesendet, wenn der freie Heap-Speicher unter diesem Schwellenwert liegt. Für den sicheren Betrieb des Platform-Servers wird eine Größe von 50 MB empfohlen. Wenn Sie den freien Heap-Speicher über diesem Wert belassen, wird die Häufigkeit der Speicherbereinigungszyklen reduziert, was die Gesamtleistung des Servers verbessern kann. Ganzzahlwert in Byte, 0 oder größer.

## AS::monitorAlertGenerator.maxOverlap - Maximale Anzahl gleichzeitiger Anforderungen {#section-ddc6925bff944758ab19bcc9cf3f2589}

Es wird ein Warnhinweis zur Überschneidung ausgelöst, wenn die durchschnittliche Anzahl der gleichzeitig verarbeiteten Anforderungen im Durchschnitts-Intervall diesen Schwellenwert überschreitet. Eine hohe Überschneidung kann auf eine mögliche Überlastungsbedingung des Servers hinweisen.

Ganzzahlwert 1 oder größer. Je nach Cache-Trefferrate und Anforderungskomplexität liegt der typische Bereich zwischen 20 und 50.

## AS::monitorAlertGenerator.lockedThreshold - Locked Request Threshold {#section-012a1c9937d445708380339279c62d80}

Gibt die Anzahl der Sekunden an, die eine Anforderung ausstehen muss, bevor sie als gesperrt oder hängengeblieben gilt. Es wird ein Warnhinweis mit gesperrten Anfragen ausgegeben, wenn am Ende eines Durchschnitts mindestens eine Anfrage länger als den angegebenen Zeitraum ausstand. Positiver ganzzahliger Wert in msec.

Um komplexe Render-Anfragen und -Anfragen zu berücksichtigen, bei denen Daten von ausländischen HTTP-Servern abgerufen werden, wird empfohlen, diesen Wert auf mindestens 30 Sekunden festzulegen (es sei denn, diese Bedingung wird von diesem Warnhinweis erkannt).

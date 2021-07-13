---
description: Verwenden Sie diese Servereinstellungen, um das Überwachungs- und Warnsystem zu konfigurieren.
solution: Experience Manager
title: Überwachungs- und Warnsystem
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# Überwachungs- und Warnsystem{#monitoring-and-alerting-system}

Verwenden Sie diese Servereinstellungen, um das Überwachungs- und Warnsystem zu konfigurieren.

## AS::monitorAlertGenerator.enableGlobalAlerting - Warnsystem aktivieren {#section-612f8ea61794426ab205e22e5f665fa9}

Aktivieren Sie die E-Mail-Benachrichtigung, indem Sie auf &quot;true&quot;setzen und die E-Mail-Benachrichtigungseinstellungen konfigurieren. Durch die Einstellung von `false` werden alle E-Mail-Warnungen deaktiviert. Dies kann nützlich sein, wenn ein Server für die Wartung offline geschaltet wird. Boolesch.

## AS::mailSender.host - SMTP Host {#section-151df07e7b44446581339bb7abeeba7a}

Die IP-Adresse des SMTP-E-Mail-Servers.

## AS::mailSender.port- SMTP Port {#section-4b25efca8fd84d5c92dafacd0555e99d}

Der Listening-Anschluss für den SMTP-E-Mail-Server.

## AS::monitorAlertGenerator.messageTo - Message Recipient {#section-0017bbaa15434117a70900c3f1163960}

Eine oder mehrere E-Mail-Adressen, an die Warnhinweise gesendet werden sollen. Verwenden Sie Semikolons als Trennzeichen.

## AS::monitorAlertGenerator.messageFrom - Message Sender {#section-db320cba4ac2438ca1cfe6abce4aed87}

Die E-Mail-Adresse, die im E-Mail-Feld **[!UICONTROL From]** verwendet werden soll.

## AS::monitorAlertGenerator.alertInterval - Monitoring Interval {#section-99cb2e3380c1499e9d5aec3671ed73c7}

Das Überwachungssystem akkumuliert Warnungsbedingungen im Warnungsintervall und sendet am Ende jedes Intervalls eine Warn-E-Mail mit allen gesammelten Warnungen. Millisekunden, ganzzahliger Wert, 60000 oder höher. In der Regel auf 5 oder 10 Minuten eingestellt.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Warnungsintervall für Heap Space {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Mindestzeit nach einem Heap-Space-Warnhinweis, bevor ein anderer ausgegeben wird. Intervallzeit in ms. Ganzzahlwert, 0 oder größer.

## AS::monitorAlertGenerator.minTrafficForAlerts - Minimaler Traffic zur Aktivierung der Warnmeldung {#section-8b4db2d6f96642309ca35c49eb3ab230}

Anforderungen pro Sekunde. Wenn der Traffic unter diesen Schwellenwert fällt, werden keine Warnungen zu Antwortzeiten und Fehlern ausgegeben. Auf 0 setzen, um Antwortzeiten und Fehlerwarnungen unabhängig vom Traffic-Volumen zu senden. Realer Wert 0 oder größer.

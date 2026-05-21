---
description: Verwenden Sie diese Server-Einstellungen, um das Überwachungs- und Warnsystem zu konfigurieren.
solution: Experience Manager
title: Überwachungs- und Warnsystem
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
TQID: 'https://experienceleague.adobe.com/n8Xw2xwdJNYlTVQusHBqP0aEpMYyPuE135TR30FLZKQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 240
ht-degree: 0%

---

# Überwachungs- und Warnsystem{#monitoring-and-alerting-system}

Verwenden Sie diese Server-Einstellungen, um das Überwachungs- und Warnsystem zu konfigurieren.

## AS::monitorAlertGenerator.enableGlobalAlerting - Alerting System Enable {#section-612f8ea61794426ab205e22e5f665fa9}

Aktivieren Sie die E-Mail-Benachrichtigung, indem Sie auf „true“ setzen und die Einstellungen für die E-Mail-Benachrichtigung konfigurieren. Wenn Sie auf `false` setzen, werden alle E-Mail-Warnhinweise deaktiviert. Dies kann nützlich sein, wenn ein Server zur Wartung offline geschaltet wird. Boolesch.

## AS::mailSender.host - SMTP-Host {#section-151df07e7b44446581339bb7abeeba7a}

Die IP-Adresse des SMTP-E-Mail-Servers.

## AS::mailSender.port- SMTP-Port {#section-4b25efca8fd84d5c92dafacd0555e99d}

Der Überwachungs-Port für den SMTP-E-Mail-Server.

## AS::monitorAlertGenerator.messageTo - Nachrichtenempfänger {#section-0017bbaa15434117a70900c3f1163960}

Eine oder mehrere E-Mail-Adressen, an die Warnhinweise gesendet werden sollen. Verwenden Sie Semikolons als Trennzeichen.

## AS::monitorAlertGenerator.messageFrom - Nachrichtenabsender {#section-db320cba4ac2438ca1cfe6abce4aed87}

Die E-Mail-Adresse, die im E-Mail **[!UICONTROL Feld &quot;]**&quot; verwendet werden soll.

## AS::monitorAlertGenerator.alertInterval - Überwachungsintervall {#section-99cb2e3380c1499e9d5aec3671ed73c7}

Das Überwachungssystem sammelt die Warnbedingungen während des Warnintervalls und sendet am Ende jedes Intervalls eine E-Mail mit allen gesammelten Warnhinweisen. Millisekunden, ganzzahliger Wert, 60000 oder größer. Normalerweise auf 5 oder 10 Minuten eingestellt.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Heap-Speicherwarnungsintervall {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Minimale Zeit nach Ausgabe eines Heap-Speicherplatzwarnungssignals, bevor ein anderer ausgegeben wird. Intervallzeit in ms. Ganzzahliger Wert, 0 oder größer.

## AS::monitorAlertGenerator.minTrafficForAlerts - Mindestanzahl an Traffic zum Aktivieren von Warnhinweisen {#section-8b4db2d6f96642309ca35c49eb3ab230}

Anfragen pro Sekunde. Wenn der Traffic unter diesen Grenzwert fällt, werden keine Reaktionszeiten und Fehlermeldungen ausgegeben. Auf 0 gesetzt, um die Antwortzeit und Fehler-Warnhinweise unabhängig vom Traffic-Volumen zu senden. Realer Wert 0 oder höher.

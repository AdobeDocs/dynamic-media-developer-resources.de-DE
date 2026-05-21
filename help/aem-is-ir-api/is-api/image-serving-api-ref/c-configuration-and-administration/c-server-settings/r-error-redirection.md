---
description: Verwenden Sie diese Server-Einstellungen, um Fehler umzuleiten.
solution: Experience Manager
title: Fehlerumleitung
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
TQID: 'https://experienceleague.adobe.com/3fcob7pfE-bMms-4PtD5MKkcolKHmXEWdzEL7vgzLhc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# Fehlerumleitung{#error-redirection}

Verwenden Sie diese Server-Einstellungen, um Fehler umzuleiten.

>[!NOTE]
>
>Pipe-Zeichen (|) im nächsten Pfad werden für die Fehlerumleitung nicht unterstützt.

## PS::errorRedirect.rootUrl - Umleitungs-Server {#section-85f22e48d68842a490b0e1191543b558}

Die Stamm-URL ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]]) für die sekundäre Image-Serving-Bereitstellung, an die lokal fehlgeschlagene Anforderungen umgeleitet werden sollen. Die Fehlerumleitung ist deaktiviert (Standard), wenn diese Einstellung leer oder nicht definiert ist.

## PS::errorRedirect.connectTimeout - Zeitüberschreitung der Umleitungsverbindung {#section-3971be8f720d4b32a2cc7860b4085971}

Maximale Wartezeit (in ms), bis der Server eine Verbindung mit dem sekundären Server hergestellt hat, bevor ein Fehler an den Client zurückgegeben wird.

## PS::errorRedirect.socketTimeout - Zeitüberschreitung bei Umleitungsantwort {#section-69d8579f748d4044bca99dfb64dd523c}

Maximale Wartezeit (in ms), bevor der Server die Umleitungsanfrage abbricht und einen Fehler an den Client zurückgibt, bis der sekundäre Server Daten zurückgibt.

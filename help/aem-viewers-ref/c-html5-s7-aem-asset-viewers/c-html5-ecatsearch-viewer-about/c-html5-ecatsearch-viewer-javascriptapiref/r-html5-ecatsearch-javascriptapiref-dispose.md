---
title: dispose
description: JavaScript-API-Referenz für den E-Katalog-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fda6d50f-0e1b-436c-af2e-1ccc9cd51c39
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# dispose{#dispose}

JavaScript-API-Referenz für den E-Katalog-Viewer.

[!DNL `dispose()`]

Stellt diese Viewer-Instanz bereit, indem alle von der Viewer-Logik verwendeten Ressourcen freigegeben und alle inneren Objekte und Komponenten gelöscht werden, die vom Viewer zur Laufzeit erstellt wurden.

Der Webseitencode sollte auch die Viewer-Instanzvariable löschen, um den Viewer vollständig aus dem Webbrowser-Speicher zu entfernen.

Wenn im Webseitencode Ereignis-Listener direkt auf vom Viewer verwendeten Viewer-SDK-Komponenten registriert sind oder externe Verweise auf solche Komponenten gespeichert sind, müssen diese Listener explizit vom Webseitencode abgemeldet werden. Und diese externen Komponentenverweise müssen vor dem Aufruf von [!DNL `dispose()`].

Rufen Sie die Viewer-API nicht mehr auf, nachdem [!DNL `dispose()`] aufgerufen wird.

## Parameter {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Keine.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

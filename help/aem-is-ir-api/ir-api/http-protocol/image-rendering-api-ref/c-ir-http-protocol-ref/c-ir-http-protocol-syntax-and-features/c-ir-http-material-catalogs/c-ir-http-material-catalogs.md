---
description: Materialkataloge bieten verschiedene Funktionen.
solution: Experience Manager
title: Materialkataloge *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Materialkataloge *{#material-catalogs}

Materialkataloge bieten verschiedene Funktionen.

* Persistente Definition von Materialien, einschließlich aller Materialeigenschaften.

   Im Materialkatalog definierte Materialien können mit einer einfachen ID referenziert werden, anstatt mit einer Reihe von Materialeigenschaften.
* Stellen Sie Standardwerte für bestimmte Anforderungsattribute bereit, z. B. die JPEG-Qualität oder eine standardmäßige Antwortbildgröße.
* Verwalten Sie Vignetten, ICC-Profile und Anforderungsvorlagen.

Selbst wenn keine spezifischen Materialkataloge definiert sind, sind alle Funktionen von Materialkatalogen über den Standardkatalog ( [!DNL default.ini]) verfügbar.

Rendermaterial kann zwar explizit in Anfragen unter Verwendung von Materialattributen angegeben werden, doch ist es in vielen Fällen wünschenswert, die Details von Materialien auf der Website mithilfe von Materialkatalogen zu verbergen. src= -Befehle akzeptieren Katalogverweise anstelle expliziter Dateipfade. Ein Katalogeintrag besteht aus ` [ *[!DNL catId]*/] *[!DNL itemId]*`, wobei ` *[!DNL catId]*` einen Materialkatalog bezeichnet und ` *[!DNL itemId]*` einen Datensatz im Katalog angibt. Wenn ` *[!DNL catId]*` nicht angegeben ist, wird der Sitzungskatalog verwendet (siehe unten).

Ein Katalogdatensatz wird erfolgreich abgeglichen, wenn (a) ` *[!DNL catId]*` mit dem `attribute::RootId`-Wert eines Materialkatalogs übereinstimmt und (b) ` *[!DNL recId]*` mit dem Wert catalog::Id im selben Katalog übereinstimmt. Bei erfolgreicher Übereinstimmung werden die Attribute des Materials (einschließlich `src=`) auf die Daten aus dem Katalogdatensatz eingestellt. Wenn das MSS neben src= zusätzliche Attribute für dieses Material enthält, überschreiben sie die Werte aus dem Katalogdatensatz.

Wenn ` *[!DNL recId]*` nicht mit einem Katalogeintrag übereinstimmen kann, wird ` *[!DNL catId]*` aus dem Katalog durch `attribute::RootPath` ersetzt und der resultierende Pfad wird dann als einfacher Dateipfad betrachtet. Andere Standardattribute (z. B. `attribute::Resolution`) auch aus dem Materialkatalog übernommen werden.

Vignetten und ICC-Profile können in Materialkatalogen, ähnlich den Materialien selbst, und in bestimmten Eigenschaften eingeschlossen werden. Darüber hinaus stellt die Vignettenzuordnung auch den Container für Vorlagen bereit.

**Verwandte Themen**

Materialkatalog-Referenz, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`

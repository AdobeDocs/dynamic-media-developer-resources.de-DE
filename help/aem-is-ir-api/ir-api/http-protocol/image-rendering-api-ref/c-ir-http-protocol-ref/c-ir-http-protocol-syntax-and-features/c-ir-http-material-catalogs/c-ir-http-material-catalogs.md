---
description: Materialkataloge bieten verschiedene Angebote.
solution: Experience Manager
title: Materialkataloge *
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---


# Materialkataloge *{#material-catalogs}

Materialkataloge bieten verschiedene Angebote.

* Standardisierte Definition von Materialien, einschließlich aller Materialeigenschaften.

   Im Materialkatalog definierte Materialien können mit einer einfachen ID anstelle einer Reihe von Materialeigenschaften referenziert werden.
* Geben Sie Standardwerte für bestimmte Anforderungsattribute an, z. B. die JPEG-Qualität oder eine standardmäßige Antwortbildgröße.
* Verwalten Sie Vignetten, ICC-Profile und Anforderungsvorlagen.

Auch wenn keine spezifischen Materialkataloge definiert sind, stehen alle Funktionen von Materialkatalogen über den Standardkatalog ( [!DNL default.ini]) zur Verfügung.

Während Render-Materialien explizit in Anforderungen mit Materialattributen spezifiziert werden können, ist es in vielen Fällen wünschenswerter, die Details von Materialien auf der Website mithilfe von Materialkatalogen auszublenden. src=-Befehle akzeptieren Katalogverweise anstelle expliziter Dateipfade. Ein Katalogeintrag besteht aus ` [ *[!DNL catId]*/] *[!DNL itemId]*`, wobei ` *[!DNL catId]*` einen Materialkatalog identifiziert und ` *[!DNL itemId]*` einen Datensatz im Katalog identifiziert. Wenn ` *[!DNL catId]*` nicht angegeben ist, wird der Sitzungskatalog verwendet (siehe unten).

Ein Katalogdatensatz wird erfolgreich abgeglichen, wenn (a) ` *[!DNL catId]*` mit dem `attribute::RootId`-Wert eines Materialkatalogs übereinstimmt und (b) ` *[!DNL recId]*` mit dem Katalog::Id-Wert im selben Katalog übereinstimmt. Bei erfolgreicher Übereinstimmung werden die Attribute des Materials (einschließlich `src=`) auf die Daten aus dem Katalogdatensatz eingestellt. Wenn das MSS neben src= weitere Attribute für dieses Material enthält, setzen sie die Werte aus dem Katalogdatensatz außer Kraft.

Wenn ` *[!DNL recId]*` nicht mit einem Katalogeintrag übereinstimmen kann, wird ` *[!DNL catId]*` durch `attribute::RootPath` aus dem Katalog ersetzt und der resultierende Pfad wird dann als einfacher Dateipfad angenommen. Andere Standardattribute (z. B. `attribute::Resolution`) kann auch aus dem Materialkatalog übernommen werden.

Vignetten und ICC-Profil können in Materialkatalogen ähnlich wie die Materialien selbst und mit Eigenschaften gegliedert werden. Darüber hinaus bietet die Vignettenzuordnung auch den Container für Vorlagen.

**Verwandte Themen**

Materialkatalog-Referenz, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`

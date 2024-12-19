---
title: Materialkataloge
description: Materialkataloge bieten mehrere Funktionen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Materialkataloge {#material-catalogs}

Materialkataloge bieten mehrere Funktionen.

* Persistente Definition von Materialien einschließlich aller Materialeigenschaften zulassen.

  Im Materialkatalog definierte Materialien können mit einer einfachen ID referenziert werden, anstatt mit einer Reihe von Materialeigenschaften.
* Geben Sie Standardwerte für bestimmte Anforderungsattribute an, z. B. die JPEG-Qualität oder eine standardmäßige Größe des Antwortbildes.
* Verwalten von Vignetten, ICC-Profilen und Anfragevorlagen.

Auch wenn keine spezifischen Materialkataloge definiert sind, stehen alle Features der Materialkataloge über den Standardkatalog zur Verfügung ( [!DNL default.ini]).

Während Render-Materialien in Anfragen mithilfe von Materialattributen explizit angegeben werden können, ist es oft wünschenswerter, die Details von Materialien auf der Website mithilfe von Materialkatalogen auszublenden. src= -Befehle akzeptieren Katalogverweise anstelle von expliziten Dateipfaden. Ein Katalogeintrag besteht aus ` [ *[!DNL catId]*/] *[!DNL itemId]*`, wobei ` *[!DNL catId]*` einen Materialkatalog und ` *[!DNL itemId]*` einen Datensatz im Katalog identifiziert. Wenn ` *[!DNL catId]*` nicht angegeben ist, wird der Sitzungskatalog verwendet (siehe unten).

Ein Katalogdatensatz wird erfolgreich abgeglichen, wenn (a) ` *[!DNL catId]*` mit dem `attribute::RootId` eines Materialkatalogs übereinstimmt und (b) ` *[!DNL recId]*` mit dem Wert catalog::id im selben Katalog übereinstimmt. Bei einer erfolgreichen Übereinstimmung werden die Attribute des Materials (einschließlich `src=`) auf die Daten aus dem Katalogdatensatz festgelegt. Wenn die MSS neben src= zusätzliche Attribute für dieses Material enthält, überschreiben sie die Werte aus dem Katalogdatensatz.

Wenn ` *[!DNL recId]*` nicht mit einem Katalogeintrag abgeglichen werden können, wird ` *[!DNL catId]*` durch `attribute::RootPath` aus dem Katalog ersetzt und der resultierende Pfad wird dann als einfacher Dateipfad angenommen. Andere Standardattribute (z. B. `attribute::Resolution`) können ebenfalls aus dem Materialkatalog übernommen werden.

Vignetten und ICC-Profile können in Materialkatalogen ähnlich den Materialien selbst und mit bestimmten Eigenschaften eingeordnet werden. Darüber hinaus stellt die Vignettenkarte auch den Container für Vorlagen bereit.

**Siehe auch**

Materialkatalogreferenz, [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`

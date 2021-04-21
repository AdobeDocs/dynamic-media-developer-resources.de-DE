---
description: Vorlagen können verwendet werden, um die Länge und Komplexität von Anforderungen zu reduzieren, die mehrere Bildebenen zusammenführen oder die RTF-formatierten Text enthalten.
solution: Experience Manager
title: Vorlagen
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# Vorlagen{#templates}

Vorlagen können verwendet werden, um die Länge und Komplexität von Anforderungen zu reduzieren, die mehrere Bildebenen zusammenführen oder die RTF-formatierten Text enthalten.

Benutzerdefinierte Variablen können verwendet werden, um die Verwendung von Vorlagen weiter zu vereinfachen. Vorlagen werden häufig so eingerichtet, dass Bilder oder Text leicht ausgetauscht oder andere Optionen zur Laufzeit festgelegt werden können.

Vorlagen werden als Datensätze in Bildkatalogen gespeichert, wobei der Vorlagentext im Feld `catalog::Modifier` und das Feld `catalog::Path` leer sind oder ein statisches Hintergrundbild angeben, das nicht dynamisch geändert werden kann.

Vorlagen werden mit dem Befehl `template=` oder in der Pfadkomponente der Anforderungs-URL angegeben. Für die meisten Anwendungen wird empfohlen, Vorlagen mit dem Befehl `template=` anzugeben. Der Befehl `template=`darf nicht im Feld `catalog::PostModifier` auftreten und darf nur im Feld `catalog::Modifier` in einer verschachtelten IS-Anforderung (d.h. in einem `src=is{...}`-Konstrukt) auftreten. Vorlagendatensätze werden möglicherweise nicht in den Befehlen `src=` oder `mask=`referenziert.

Alle in die Vorlage eingebetteten `src=`- oder `mask=`Befehle können in den Hauptkatalog der Anforderung oder in einen anderen Bildkatalog aufgelöst werden. Wenn kein `rootId` explizit angegeben ist, wird der Hauptkatalog angenommen. Die mit `template=` angegebene Vorlage befindet sich möglicherweise auch im Hauptkatalog oder in einem anderen Bildkatalog.

Es wird dringend empfohlen, immer Standarddefinitionen für alle Variablen einzubeziehen, die in einer Vorlage verwendet werden. Auf diese Weise kann die Bildausgabe der Vorlage immer angezeigt werden, indem einfach `attribute::RootId` und `catalog::Id` angegeben werden, ohne dass Sie wissen müssen, welche Variablen in der Vorlage verwendet werden.

Die vordefinierte Pfadsetzungsvariable `$object$` kann verwendet werden, um das im URL-Pfad angegebene Bildobjekt auf eine beliebige Ebenenquelle oder -maske ( `src=` oder `mask=`) anzuwenden, auch in verschachtelten oder eingebetteten Anforderungen.

* [Beispiel A](r-example-a.md)
* [Beispiel B](r-example-b.md)
* [Beispiel C](r-example-c.md)

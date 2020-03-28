---
description: Vorlagen können verwendet werden, um die Länge und Komplexität von Anforderungen zu reduzieren, die mehrere Bildebenen zusammenführen oder die RTF-formatierten Text enthalten.
seo-description: Vorlagen können verwendet werden, um die Länge und Komplexität von Anforderungen zu reduzieren, die mehrere Bildebenen zusammenführen oder die RTF-formatierten Text enthalten.
seo-title: Vorlagen
solution: Experience Manager
title: Vorlagen
topic: Scene7 Image Serving - Image Rendering API
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# Vorlagen{#templates}

Vorlagen können verwendet werden, um die Länge und Komplexität von Anforderungen zu reduzieren, die mehrere Bildebenen zusammenführen oder die RTF-formatierten Text enthalten.

Benutzerdefinierte Variablen können verwendet werden, um die Verwendung von Vorlagen weiter zu vereinfachen. Vorlagen werden häufig so eingerichtet, dass Bilder oder Text leicht ausgetauscht oder andere Optionen zur Laufzeit festgelegt werden können.

Vorlagen werden als Datensätze in Bildkatalogen gespeichert, wobei der Vorlagentext im `catalog::Modifier` Feld und das `catalog::Path` Feld leer sind oder ein statisches Hintergrundbild angeben, das nicht dynamisch geändert werden kann.

Vorlagen werden mit dem `template=` Befehl oder in der Pfadkomponente der Anforderungs-URL angegeben. Bei den meisten Anwendungen wird empfohlen, Vorlagen mit dem `template=` Befehl anzugeben. Der `template=`Befehl darf nicht im `catalog::PostModifier` Feld auftreten und darf nur im Feld einer verschachtelten IS-Anforderung (d. h. in einem `catalog::Modifier` `src=is{...}` Konstrukt) auftreten. Vorlagendatensätze können in `src=` oder `mask=`Befehlen nicht referenziert werden.

Alle `src=` oder in die Vorlage eingebetteten `mask=`Befehle können in den Hauptkatalog der Anforderung oder in einen anderen Bildkatalog aufgelöst werden. Wenn keine explizite Angabe erfolgt, wird der Hauptkatalog angenommen. `rootId` Die mit angegebene Vorlage `template=` befindet sich möglicherweise auch im Hauptkatalog oder in einem anderen Bildkatalog.

Es wird dringend empfohlen, immer Standarddefinitionen für alle Variablen einzubeziehen, die in einer Vorlage verwendet werden. Auf diese Weise kann die Bildausgabe der Vorlage immer einfach angezeigt werden, indem deren `attribute::RootId` und `catalog::Id`ohne zu wissen, welche Variablen in der Vorlage verwendet werden.

Die vordefinierte Pfadsetzungsvariable `$object$` kann verwendet werden, um das im URL-Pfad angegebene Bildobjekt auf eine beliebige Ebenenquelle oder -maske ( `src=` oder `mask=`) anzuwenden, auch in verschachtelten oder eingebetteten Anforderungen.

* [Beispiel A](r-example-a.md)
* [Beispiel B](r-example-b.md)
* [Beispiel C](r-example-c.md)

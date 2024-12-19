---
title: Benutzerdefinierte Variablen
description: Der Abfrageteil von Anfragen und Vignettenmodifikator-Zeichenfolgen kann benutzerdefinierte Variablen enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Benutzerdefinierte Variablen{#custom-variables}

Der Abfrageteil von Anfragen und „vignette:Modifier“-Zeichenfolgen kann benutzerdefinierte Variablen enthalten.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Variablenname. Kann aus einer beliebigen Kombination von Buchstaben, Ziffern und sicheren Zeichen bestehen, mit Ausnahme von `$`.

`[!DNL value]` - Wert, auf den die Variable gesetzt werden soll (Zeichenfolge).

Variablen werden ähnlich wie andere Server-Befehle unter Verwendung der obigen Syntax definiert. Variablen müssen definiert werden, bevor sie referenziert werden können. Variablen, die in `vignette::Modifier` definiert sind, können in der URL-Anfrage referenziert werden und umgekehrt.

>[!NOTE]
>
>`[!DNL value]` muss für eine sichere HTTP-Übertragung URL-kodiert sein. Doppelte Kodierung ist erforderlich, wenn `[!DNL value]` erneut über HTTP übertragen wird. Dies ist der Fall, wenn `[!DNL value]` durch eine verschachtelte Fremdanforderung ersetzt wird.

Variablen werden durch Einbetten des Variablennamens (eingeschlossen von einem führenden und einem nachfolgenden `$`) an einer beliebigen Stelle in Befehlswerten referenziert. Beispielsweise zwischen dem `=`, der dem Befehlsnamen folgt, und dem nachfolgenden `&` oder dem Ende der Anfrage. Der Server ersetzt jedes Vorkommen von `$ [!DNL name]$` durch `[!DNL string]`. Es finden keine Ersetzungen statt bei `$ [!DNL name]$` in Befehlsnamen (vor dem Gleichheitszeichen eines Befehls) und im Pfadteil der Anfrage.

Benutzerdefinierte Variablen dürfen nicht verschachtelt sein. Alle Vorkommen von `$ [!DNL name]$` in `[!DNL string]` werden nicht ersetzt. Beispielsweise wird das Anfragefragment `$var2=apple&$var1=my$var2$tree&text=$var1$` zu `text=my$var2$tree` aufgelöst.

`$` ist kein reserviertes Zeichen; es kann auch anders in der Anfrage vorkommen. `src=my$texture$file.tif` ist beispielsweise ein gültiger Befehl (vorausgesetzt, dass ein Materialkatalogeintrag oder eine Strukturdatei mit dem Namen `[!DNL my$texture$file.tif]` vorhanden ist), `wid=$number$` ist dies jedoch nicht, da `wid=` ein numerisches Argument erfordert.

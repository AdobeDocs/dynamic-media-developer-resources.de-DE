---
title: Benutzerdefinierte Variablen
description: Der Abfrageteil von Anfragen und Vignettenmodifikator-Zeichenfolgen kann benutzerdefinierte Variablen enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
TQID: 'https://experienceleague.adobe.com/1-o3GqgzwvPYV8UDBuZu5udOiG-p8Tue3Fo-ft8-QhI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 251
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


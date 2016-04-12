# af3
<h1>AutoFOCUS 3 traffic light example</h1><br>
Nyissuk meg az autofocust<br>
Kattintsunk a File-> New AF3-Project-ra<br>
<div align="center">
  <img src="1.png" align="center">
</div>
Majd hozzuk létre a projektünk legfontosabb részeit: követelmények, Komponsek és adatok<br>


A létrejött projekt részeket könnyedén átnevezhetjük, ha jobb egérrel kattintunk rájuk és a rename-re kattintunk. Legalábbis elméletben. Ez a követelmények résznél még működött, de a Component-Architecture-t sehogy sem engedte átnevezni, bármit is írtam be.<br>
Most foglalkozzunk a követelmények résszel, hozzáadunk az előbb is működő jobb gombos módszerrel egy Glossaryt, Requirement Sources-t és egy Requirements-et.<br>

Glossary Entry-k felvétele:<br>


Át is nevezhetőek<br>
Most töltsük meg a glossaryt tartalommal.<br>
Kitöltjük a Controller definíciját<br>


A Traffic entry definícióját is kitöltjük<br>

Ha minden igaz, akkor ezzel meg is vagyunk az entrykkel.<br>
Most adjuk meg a requirement sources-nál a követelmények forrásait<br>
A követelmények forrásai lehetnek:<br>
•	érdekelt felektől (stakeholders)<br>
•	külső rendszerekből (external system)<br>
•	dokumentumokból (document)<br>

Esetünkben három külső rendszer van:<br>
•	gyalogos lámpa(pedestrian light)<br>
•	kijelző(Indicator)<br>
•	közlekedési lámpa (traffic light)<br>
Az ISO 26262 szabvány adja a funkcionális követelményeinket, ezt document típussal vesszük fel.<br>
A general fülön el tudjuk nevezni és megadjuk a leírását<br>

A Files fülön akár csatolhatjuk is a dokumentumot, én most be fogom linkelni a szabványt:<br>

A leírását és a verzióját is megadhatjuk<br>

Mivel a szabvány három részben van fent a weben, ezért mindhárom linket megadjuk:<br>
A link utólag is szerkeszthető, viszont akkor írhatjuk újra a description és a version részt is, mert a program automatán<br> kitörli ezeket.<br>
Most következzenek az érdekelt felek:<br>
•	A gyalogosok(pedestrian)<br>
•	és a rendszer építői(System Architect)<br>
Stakeholder típussal hozom őket létre:<br>
Kitöltjük a definíció részeket. Szinonimákat is adhatunk meg egyes dolgokra, a gyalogosra adtunk is<br>

Ezzel megvannak a követelmények forrásai is<br>

A követelmények:<br>
Létrehozhatunk package-eket, hogy egységbe zárjunk egyes követelményeket. Megadhatunk use-case-eket is, amelyek felhasználói esetek<br>

Létre is hozunk két package-et, egyet a követelményeknek, egyet a use case-eknek:<br>

Először a Use Cases Package-ben dolgozzuk ki a use case-t<br>
A use case tulajdonságainak nagy része egyszerűen beírható Az actor felvitelét mutatja az alábbi kép:<br>

Észrevesszük, hogy Inputokat outputokat nem lehet még a modell nélkül ide beírni, ezekre még visszatérek.<br>
A use case-hez felvehetünk scenariokat is, ezek különféle lefutásai ugyanannak a use case-nek, itt definiálhatjuk, hogy mi egy hibás lefutás vagy egy sikeres.<br>
felvettem a Failure scenario-t a use case-ek között, itt adjuk meg, hogy mit kell tenni vészhelyzet esetén<br>

Készítek még egy use case-et „ Activate traffic light to 'red' and pedestrian light to 'go'” néven, ez sikeres scenario<br>


Actort véletlenül se próbáljunk meg dupla kattintással adni a use case-hez, az kiveszi az actorok listájából.<br>
A Branch részben meg tudjuk adni, hogy az adott jelenséget produkálja a rendszer, akkor az előző use case-ekből hova is ugorjon a végrehajtás.<br>


Menjünk tovább az előzőleg létrehozott MSC specification-re, eddig nem tudtuk átnevezni, de ha adunk hozzá MSC-ket erre is képesek leszünk<br>

Itt UML szekvencia diagramra hasonlító módon készíthetünk modellt. Itt ismét gondom akadt az inputok és outputok esztétikus elhelyezésével, mindegyik fordítva áll, mint ahogy akartam.<br>

Átmenetet úgy lehet behúzni, hogy nyomva tartjuk a Ctrl gombot, belekattintunk az egyik objektumba, majd húzzuk az egeret a másikhoz és végül elengedjük az egér gombját, eddigi észrevételem szerint teljesen véletlen, hogy melyik input/output melyik oldalra kerül, áthelyezni nem tudok őket. <br>
A többi követelmény felvétele<br>


Ezzel néhány apróságot eltekintve elkészültünk a követelményekkel, most térjünk át a Data dictionary-re.<br>
Adatszerkezetek és függvények hozzáadása (Data dictionary)<br>
A Data dictonary-be az oldalsó eszköztárról tudunk elemeket behúzni<br>

Nem is időzünk itt sokat, a Properties-ben lehet módosítani a függvények visszatérési értékét/paramétereit és minden egyebet. Figyelem a void kulcsszó itt nem használható. Csak visszatérési értékkel rendelkező, állapotváltozót nem módosító függvényeket hozhatunk létre.<br>

Elkészítjük a modellt, ügyelünk a konzisztens elnevezésekre, hogy tudjunk mindenre hivatkozni.<br>
Miután a modell elkészült a use case-hez köthetünk egyes modellelemeket, ezt a use case beállításai között tehetjük meg:<br>



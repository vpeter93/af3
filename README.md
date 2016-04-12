# af3
<h1 align="center">AutoFOCUS 3 traffic light example</h1><br>
Nyissuk meg az autofocust<br>
Kattintsunk a File-> New AF3-Project-ra<br>
<div><img src="images/1.png" ></div>
Majd hozzuk létre a projektünk legfontosabb részeit: követelmények, Komponsek és adatok<br>
<div><img src="2.png" ></div>
<div><img src="3.png" ></div>
<div><img src="4.png" ></div>
A létrejött projekt részeket könnyedén átnevezhetjük, ha jobb egérrel kattintunk rájuk és a rename-re kattintunk. Legalábbis elméletben. Ez a követelmények résznél még működött, de a Component-Architecture-t sehogy sem engedte átnevezni, bármit is írtam be.<br>
<h2>Követelmények</h2><br>
Most foglalkozzunk a követelmények résszel, hozzáadunk az előbb is működő jobb gombos módszerrel egy Glossaryt, Requirement Sources-t és egy Requirements-et.<br>
<div><img src="5.png" ></div>
Glossary Entry-k felvétele:<br>
<div><img src="6.png" ></div>
Át is nevezhetőek a létrehozott dolgok.<br>
Most töltsük meg a glossaryt tartalommal.<br>
Kitöltjük a Controller definíciját<br>
<div><img src="7.png" ></div>
A Traffic entry definícióját is kitöltjük<br>
<div><img src="8.png" ></div>
Ha minden igaz, akkor ezzel meg is vagyunk az entrykkel.<br>
Most adjuk meg a requirement sources-nál a követelmények forrásait<br>
A követelmények forrásai lehetnek:<br>
<ul>
    <li>érdekelt felektől (stakeholders)</li>
    <li>külső rendszerekből (external system)</li>
    <li>dokumentumokból (document)</li>
</ul>
<div><img src="9.png" ></div>
Esetünkben három külső rendszer van:<br>
<ul>
    <li>gyalogos lámpa(pedestrian light)</li>
    <li>kijelző(Indicator)</li>
    <li>közlekedési lámpa (traffic light)</li>
</ul>
Az ISO 26262 szabvány adja a funkcionális követelményeinket, ezt document típussal vesszük fel.<br>
A general fülön el tudjuk nevezni és megadjuk a leírását<br>
<div><img src="10.png" ></div>
A Files fülön akár csatolhatjuk is a dokumentumot, én most be fogom linkelni a szabványt:<br>
<div><img src="11.png" ></div>
A leírását és a verzióját is megadhatjuk<br>
<div><img src="12.png" ></div>
Mivel a szabvány három részben van fent a weben, ezért mindhárom linket megadjuk:<br>
A link utólag is szerkeszthető, viszont akkor írhatjuk újra a description és a version részt is, mert a program automatán<br> kitörli ezeket.<br>
Most következzenek az érdekelt felek:<br>
<ul>
    <li>A gyalogosok(pedestrian)</li>
    <li>és a rendszer építői(System Architect)</li>
</ul>
Stakeholder típussal hozom őket létre:<br>
Kitöltjük a definíció részeket. Szinonimákat is adhatunk meg egyes dolgokra, a gyalogosra adtunk is<br>
<div><img src="13.png" ></div>
Ezzel megvannak a követelmények forrásai is<br>
<div><img src="14.png" ></div>
A követelmények:<br>
Létrehozhatunk package-eket, hogy egységbe zárjunk egyes követelményeket. Megadhatunk use-case-eket is, amelyek felhasználói esetek<br>
<div><img src="15.png" ></div>
Létre is hozunk két package-et, egyet a követelményeknek, egyet a use case-eknek:<br>
<div><img src="16.png" ></div>
Először a Use Cases Package-ben dolgozzuk ki a use case-t<br>
A use case tulajdonságainak nagy része egyszerűen beírható Az actor felvitelét mutatja az alábbi kép:<br>
<div><img src="17.png" ></div>
Észrevesszük, hogy Inputokat outputokat nem lehet még a modell nélkül ide beírni, ezekre még visszatérek.<br>
A use case-hez felvehetünk scenariokat is, ezek különféle lefutásai ugyanannak a use case-nek, itt definiálhatjuk, hogy mi egy hibás lefutás vagy egy sikeres.<br>
felvettem a Failure scenario-t a use case-ek között, itt adjuk meg, hogy mit kell tenni vészhelyzet esetén<br>
<div><img src="18.png" ></div>
Készítek még egy use case-et „ Activate traffic light to 'red' and pedestrian light to 'go'” néven, ez sikeres scenario<br>
<div><img src="19.png" ></div>
<div><img src="20.png" ></div>
Actort véletlenül se próbáljunk meg dupla kattintással adni a use case-hez, az kiveszi az actorok listájából.<br>
A Branch részben meg tudjuk adni, hogy az adott jelenséget produkálja a rendszer, akkor az előző use case-ekből hova is ugorjon a végrehajtás.<br>
<div><img src="21.png" ></div>
<div><img src="22.png" ></div>
Menjünk tovább az előzőleg létrehozott MSC specification-re, eddig nem tudtuk átnevezni, de ha adunk hozzá MSC-ket erre is képesek leszünk<br>
<div><img src="23.png" ></div>
Itt UML szekvencia diagramra hasonlító módon készíthetünk modellt. Itt ismét gondom akadt az inputok és outputok esztétikus elhelyezésével, mindegyik fordítva áll, mint ahogy akartam.<br>
<div><img src="24.png" ></div>
Átmenetet úgy lehet behúzni, hogy nyomva tartjuk a Ctrl gombot, belekattintunk az egyik objektumba, majd húzzuk az egeret a másikhoz és végül elengedjük az egér gombját, eddigi észrevételem szerint teljesen véletlen, hogy melyik input/output melyik oldalra kerül, áthelyezni nem tudok őket. <br>
A többi követelmény felvétele<br>
<div><img src="25.png" ></div>
<div><img src="26.png" ></div>
Ezzel néhány apróságot eltekintve elkészültünk a követelményekkel, most térjünk át a Data dictionary-re.<br>
Adatszerkezetek és függvények hozzáadása (Data dictionary)<br>
A Data dictonary-be az oldalsó eszköztárról tudunk elemeket behúzni<br>
<div><img src="27.png" ></div>
Nem is időzünk itt sokat, a Properties-ben lehet módosítani a függvények visszatérési értékét/paramétereit és minden egyebet. Figyelem a void kulcsszó itt nem használható. Csak visszatérési értékkel rendelkező, állapotváltozót nem módosító függvényeket hozhatunk létre.<br>
<div><img src="28.png" ></div>
Elkészítjük a modellt, ügyelünk a konzisztens elnevezésekre, hogy tudjunk mindenre hivatkozni.<br>
Miután a modell elkészült a use case-hez köthetünk egyes modellelemeket, ezt a use case beállításai között tehetjük meg:<br>
<div><img src="29.png" ></div>
<div><img src="30.png" ></div>


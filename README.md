# autofocus3 használatának bemutatása a közelekedési lámpa példáján keresztül.
<h1 align="center">AutoFOCUS 3 traffic light example</h1><br>
Nyissuk meg az autofocust<br>
Kattintsunk a File-> New AF3-Project-ra<br>
<div><img src="images/1.png" ></div>
Majd hozzuk létre a projektünk legfontosabb részeit: követelmények, Komponsek és adatok<br>
<div><img src="images/2.png" ></div>
<div><img src="images/3.png" ></div>
<div><img src="images/4.png" ></div>
A létrejött projekt részeket könnyedén átnevezhetjük, ha jobb egérrel kattintunk rájuk és a rename-re kattintunk. Legalábbis elméletben. Ez a követelmények résznél még működött, de a Component-Architecture-t sehogy sem engedte átnevezni, bármit is írtam be.<br>
<h2>Követelmények</h2><br>
Most foglalkozzunk a követelmények résszel, hozzáadunk az előbb is működő jobb gombos módszerrel egy Glossaryt, Requirement Sources-t és egy Requirements-et.<br>
<div><img src="images/5.png" ></div>
Glossary Entry-k felvétele:<br>
<div><img src="images/6.png" ></div>
Át is nevezhetőek a létrehozott dolgok.<br>
Most töltsük meg a glossaryt tartalommal.<br>
Kitöltjük a Controller definíciját<br>
<div><img src="images/7.png" ></div>
A Traffic entry definícióját is kitöltjük<br>
<div><img src="images/8.png" ></div>
Ha minden igaz, akkor ezzel meg is vagyunk az entrykkel.<br>
Most adjuk meg a requirement sources-nál a követelmények forrásait<br>
A követelmények forrásai lehetnek:<br>
<ul>
    <li>érdekelt felektől (stakeholders)</li>
    <li>külső rendszerekből (external system)</li>
    <li>dokumentumokból (document)</li>
</ul>
<div><img src="images/9.png" ></div>
Esetünkben három külső rendszer van:<br>
<ul>
    <li>gyalogos lámpa(pedestrian light)</li>
    <li>kijelző(Indicator)</li>
    <li>közlekedési lámpa (traffic light)</li>
</ul>
Az ISO 26262 szabvány adja a funkcionális követelményeinket, ezt document típussal vesszük fel.<br>
A general fülön el tudjuk nevezni és megadjuk a leírását<br>
<div><img src="images/10.png" ></div>
A Files fülön akár csatolhatjuk is a dokumentumot, én most be fogom linkelni a szabványt:<br>
<div><img src="images/11.png" ></div>
A leírását és a verzióját is megadhatjuk<br>
<div><img src="images/12.png" ></div>
Mivel a szabvány három részben van fent a weben, ezért mindhárom linket megadjuk:<br>
A link utólag is szerkeszthető, viszont akkor írhatjuk újra a description és a version részt is, mert a program automatán<br> kitörli ezeket.<br>
Most következzenek az érdekelt felek:<br>
<ul>
    <li>A gyalogosok(pedestrian)</li>
    <li>és a rendszer építői(System Architect)</li>
</ul>
Stakeholder típussal hozom őket létre:<br>
Kitöltjük a definíció részeket. Szinonimákat is adhatunk meg egyes dolgokra, a gyalogosra adtunk is<br>
<div><img src="images/13.png" ></div>
Ezzel megvannak a követelmények forrásai is<br>
<div><img src="images/14.png" ></div>
A követelmények:<br>
Létrehozhatunk package-eket, hogy egységbe zárjunk egyes követelményeket. Megadhatunk use-case-eket is, amelyek felhasználói esetek<br>
<div><img src="images/15.png" ></div>
Létre is hozunk két package-et, egyet a követelményeknek, egyet a use case-eknek:<br>
<div><img src="images/16.png" ></div>
Először a Use Cases Package-ben dolgozzuk ki a use case-t<br>
A use case tulajdonságainak nagy része egyszerűen beírható Az actor felvitelét mutatja az alábbi kép:<br>
<div><img src="images/17.png" ></div>
Észrevesszük, hogy Inputokat outputokat nem lehet még a modell nélkül ide beírni, ezekre még visszatérek.<br>
A use case-hez felvehetünk scenariokat is, ezek különféle lefutásai ugyanannak a use case-nek, itt definiálhatjuk, hogy mi egy hibás lefutás vagy egy sikeres.<br>
felvettem a Failure scenario-t a use case-ek között, itt adjuk meg, hogy mit kell tenni vészhelyzet esetén<br>
<div><img src="images/18.png" ></div>
Készítek még egy use case-et „ Activate traffic light to 'red' and pedestrian light to 'go'” néven, ez sikeres scenario<br>
<div><img src="images/19.png" ></div>
<div><img src="images/20.png" ></div>
Actort véletlenül se próbáljunk meg dupla kattintással adni a use case-hez, az kiveszi az actorok listájából.<br>
A Branch részben meg tudjuk adni, hogy az adott jelenséget produkálja a rendszer, akkor az előző use case-ekből hova is ugorjon a végrehajtás.<br>
<div><img src="images/21.png" ></div>
<div><img src="images/22.png" ></div>
Menjünk tovább az előzőleg létrehozott MSC specification-re, eddig nem tudtuk átnevezni, de ha adunk hozzá MSC-ket erre is képesek leszünk<br>
<div><img src="images/23.png" ></div>
Itt UML szekvencia diagramra hasonlító módon készíthetünk modellt. Itt ismét gondom akadt az inputok és outputok esztétikus elhelyezésével, mindegyik fordítva áll, mint ahogy akartam.<br>
<div><img src="images/24.png" ></div>
Átmenetet úgy lehet behúzni, hogy nyomva tartjuk a Ctrl gombot, belekattintunk az egyik objektumba, majd húzzuk az egeret a másikhoz és végül elengedjük az egér gombját, eddigi észrevételem szerint teljesen véletlen, hogy melyik input/output melyik oldalra kerül, áthelyezni nem tudok őket. <br>
A többi követelmény felvétele<br>
<div><img src="images/25.png" ></div>
<div><img src="images/26.png" ></div>
Ezzel néhány apróságot eltekintve elkészültünk a követelményekkel, most térjünk át a Data dictionary-re.<br>
Adatszerkezetek és függvények hozzáadása (Data dictionary)<br>
A Data dictonary-be az oldalsó eszköztárról tudunk elemeket behúzni<br>
<div><img src="images/27.png" ></div>
Nem is időzünk itt sokat, a Properties-ben lehet módosítani a függvények visszatérési értékét/paramétereit és minden egyebet. Figyelem a void kulcsszó itt nem használható. Csak visszatérési értékkel rendelkező, állapotváltozót nem módosító függvényeket hozhatunk létre.<br>
<div><img src="images/28.png" ></div>
Elkészítjük a modellt, ügyelünk a konzisztens elnevezésekre, hogy tudjunk mindenre hivatkozni.<br>

<h2>A modell elkészítése</h2><br>
Három komponensből építkezünk:<br>
<ul>
<li>Controller</li>
<li>Merge</li>
<li>Panel</li>
</ul>
Hozzuk ezeket létre a Component Architecture-ben, új komponensek hozzáadásával:<br>
<div><img src="images/m1.png" ></div>
A properties fülön ezek a komponensek átnevezhetőek, ahogy már a többi modellelemnél is megszokhattuk.<br>
<div><img src="images/m2.png" ></div>
Először elkészítjük a komponensek egymáshoz való viszonyát leíró legfelsőbb komponens diagramot.<br>
Inputok hozzáadása a modellhez az input karika diagramterületre való behúzásával történik:<br>
<div><img src="images/m3.png" ></div>
Az input properties menüjében be tudjuk állítani a típusát és megadhatjuk a nevét is. Típusokból azokat tudjuk használni, amelyeket megadtunk a Data dictionary-ban, vagy választhatunk az int, boolean, double primitív típusok közül.<br>
<div><img src="images/m4.png" ></div>
Ahhoz, hogy az inputból átmenetet húzzunk egy komponensbe, le kell nyomni a Ctrl billentyűt és az egér gombját nyomva tartva tudunk nyilat húzni. Ha nem tetszik az input elhelyezkedése a komponensen, akkor egyszerűen arrébb húzhatjuk fogd és vidd módszerrel:<br>
<div><img src="images/m5.png" ></div>
Az átmenetnek is tudunk nevet adni a properties részben:
<div><img src="images/m6.png" ></div>
Összeraktuk a legfelsőbb komponens diagramot, ne ijedjünk meg az alábbi hibaüzenetttől, az eszköznek igaza van, teddig tényleg gyengén kauzális rendszerünk van, de majd a végén visszatérünk erre:<br>
<div><img src="images/m7.png" ></div>
Csináljuk meg a komponensek belsejét is, a Merge komponensben egy állapotdiagram lesz. Húzzuk is be az eszköztárról:<br>
<div><img src="images/m8.png" ></div>
Az átmentek őrfeltételeiben hivatkozhatunk a ki és bemeneteinkre és használhatjuk a Data dictionary-ben definiált értékéket is egy-egy enumeration típushoz. Ezek furcsamód függvényhívásszerűen vannak jelölve, alább a Present( ) egy lehetséges értéke a Signal típusnak.<br>
<div><img src="images/m9.png" ></div>
A megfelelő átmenetek behúzása után a modell ezen részével nincs több dolgunk, specifikáltuk a Merge komponens működését:<br>
<div><img src="images/m10.png" ></div>
A Contoller komponensbe egy újabb komponenst teszünk Behavior néven, melynek a belsejében majd egy állapotgép lesz.
Elkészült a Behavior, még mindig megkapjuk ugyanazt a hibaüzenetet, ne foglalkozzunk vele:<br>
<div><img src="images/m11.png" ></div>
Húzzunk be az eszköztárról egy újabb state automaton-t a Behavioron belülre. Vegyük fel a közlekedési lámpánk állapotait:<br>
<ul>
    <li>Red</li>
    <li>Yellow</li>
    <li>RedYellow</li></li>
    <li>Green</li>
    <li>Init</li>
</ul>
Majd menjünk a Data State fülre
<div><img src="images/m12.png" ></div>
Itt belső változókat lehet a modellhez hozzáadni. Adjunk is hozzá egy idő(time) int változót az oldalsó Add gombbal:<br>
<div><img src="images/m13.png" ></div>
Váltsunk vissza State automaton nézetre, ott ahol a Data State fület választottuk és hozzuk létre a modellt. A time változóra innentől hivatkozhatunk őrfeltételekben és akciókban is.<br>
<div><img src="images/m14.png" ></div>
Ügyeljünk az eggyel felsőbb szint elnevezéseire, hogy valóban azokat használjuk-e, az én esetemben elfeledtem egy Outputot átnevezni a Behaviornál és most ezért ír hibát. Ügyeljünk a szóközökre is, ha mindent jól elneveztünk és csak arra hivatkozunk, ami valóban létezik, akkor nem kapunk ilyen hibákat.<br>
<div><img src="images/m15.png" ></div>
Ügyeljünk rá, hogy elsőre jó helyre kerüljenek a nyilak és rögtön esztétikus legyen a modell, mert a state automaton-nál hiába próbáljuk átpakolni az elcsúszott inputokat/outputokat a program kissé öntörvényűen értelmezi, hogy hova is tennénk ezeket:<br>
<div><img src="images/m16.png" ></div>
<div><img src="images/m17.png" ></div>
A program készítői az állapotgép kezdőállapotát +1 kimenetnek látszó karikával jelölték meg, amiből nem jön ki semmi és nem is megy be.<br>
<div><img src="images/m18.png" ></div>
Ezzel meg is van a sajnálatosan nem túl szép állapotgép. A ki/bemenetek és átmenete pozícionálásra még nem sikerült rájönni.<br>
<div><img src="images/m19.png" ></div>
A következő rész a Panel komponens, ez két külön komponensből fog állni:<br>
<ul>
    <li>A megjelenítő (Display)</li>
    <li>A HAL(Hardware Abstration Layer)</li>
</ul>
Először a komponensek egymáshoz való viszonyát modellezzük le. A hibaüzenetünk még mindig ugyanaz.<br>
<div><img src="images/m20.png" ></div>
A HAL belül egy újabb állapotgép lesz, amiben ismét belső változókra lesz szükségünk, amiket a Data State fülön definiálhatunk:<br>
<div><img src="images/m21.png" ></div>
<div><img src="images/m22.png" ></div>
<div><img src="images/m23.png" ></div>
<div><img src="images/m24.png" ></div>
Ha az eggyel feljebbi szinten mindent tisztességesen elneveztünk, akkor itt semmi hibát nem kaphatunk.
Csináljuk most meg a megjelenítésért felelős Display komponenst. Ennek a belsejében egy operator panel lesz.<br>
<div><img src="images/m25.png" ></div>
Helyezhetünk bele nyomógombot:
<div><img src="images/m26.png" ></div>
És címkéket is:
<div><img src="images/m27.png" ></div>
És persze lámpákat:
<div><img src="images/m28.png" ></div>
<div><img src="images/m29.png" ></div>
Végül kezdjünk valamit a hibaüzenettel, ami végig velünk volt modellezés közben:
<div><img src="images/m30.png" ></div>
A hibaüzenetre a megoldás annyi, hogy a Controller Behavior-jánál beállítjuk erősen kauzálisra rendszert és utána már nem szól, hogy gyengén kauzális.
<div><img src="images/m31.png" ></div>
Ezzel el is készült a modell.<br>
Miután a modell elkészült a use case-hez köthetünk egyes modellelemeket, ezt a use case beállításai között tehetjük meg:<br>
<div><img src="images/29.png" ></div>
<div><img src="images/30.png" ></div>
Ennek segítségével később ellenőrzhetjük, hogy a modellünk megfelel-e az előzetesen felállított követelményeknek.

<h2>A generátormodell</h2><br>
Az eddigiekben bemutatott modell természetesen azért készült, hogy később ellenőrzött programkód legyen belőle. Ehhez nyújt segítséget nekünk a generátormodell.<br>
Először készítsünk egy új projektet.<br>



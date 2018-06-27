# SML
SML Handbook

SeemoreLabs

Vállalatirányítási szoftver

Kézikönyv


Bevezetés

Az SML megalkotásával egy, a vállalatok mindennapi életét nagyban megkönnyítő megoldást szerettünk volna nyújtani. Egyik legfontosabb tulajdonsága, hogy minden platformon - Windows/Mac/Linux/iOS/Android, illetve ezeken belül az összes böngészőt ideértve - kiválóan üzemel, nincs szüksége telepítésre, új eszköz bevonása esetén pedig elegendő csak a tartomány cím beírása és máris a bejelentkezési felületen találjuk magunkat. Használatának elsajátításához nem kell szakértőt bevonni, a világ bármely pontjáról és bármilyen eszközről elérhető, felhasználó-barát, teljesen egyénre szabható felülettel és menürendszerrel, megfelelő méretezhetőséggel, és nem utolsó sorban kedvező árral rendelkezik. A program fő aspektusai a költség és erőforrás menedzsment, a termelésirányítás, valamint a raktárkezelés. Az SML az alapvető vállalatirányítási részegységeket egy rendszerbe integrálja, ennek köszönhetően a vállalat összes alkalmazottja azonos szoftverrel dolgozik - így például egy raktáros és egy bérszámfejtő is ugyanazt a rendszert használva képes mindennapi munkáját elvégezni. Ez azt jelenti, hogy nincs szükség külön számlázó-, raktárkezelő-, és könyvelőszoftver beszerzésére, az SML ezeket is magába foglalja. A programnak saját beléptető rendszere van, mely nyomon követi a dolgozók jelenlétét/távollétét, a felvett/leadott műszakokat és az eltöltött pihenőidőket. Ezen kívül az SML belső kommunikációs lehetőséget is biztosít a dolgozók számára, mely lehetővé teszi a hatékonyabb együttműködést és nem utolsó sorban költségcsökkentő hatással bír. Egy szoftver, egy felület, egy adatbázis: egyetlen információ forrás, melyre a program összes funkciója épül, és amely azonnal hozzáférhető, pontos és valós idejű adatokat szolgáltat, ezzel elősegítve az értékesítési lehetőségek kiaknázását és növekedését, az egyszerűbb és gyorsabb döntéshozatalt az érintettek számára, illetve leegyszerűsíti a könyvelők munkáját is - nincs szükség máshonnan származó adatok kinyerésére, sem adategyeztetésre. Az SML két, és egyben egyik legfontosabb alappillére a termékek és a megrendelések: a rendszer tárol és nyomon követ minden rájuk vonatkozó és hozzájuk kapcsolt információt, legyen az számla, mennyiség függő ár, gyártási folyamat vagy nyomóforma, ezzel segítve a megfelelő minőség folyamatos fenntartását, illetve az alapanyaghasználat optimalizálását és nyomonkövetését.


A programfelület struktúrája

a, Bejelentkezés

A szoftver egyszerű és letisztult bejelentkezési felülettel rendelkezik, mely nem csak a rendszerbe való bejelentkezést, hanem a “Beléptető kapu” menüpont révén adott műszak megkezdését is lehetővé teszi. Bejelentkezés után minden felhasználót a saját jogosultsági köre szerinti funkciókkal rendelkező SML felület fogadja - pl.: egy gépkezelő nem fér(het) hozzá a bérszámfejtő modulhoz. A felhasználócsoportokról és a jogosultsági körökről a későbbiekben ejtünk majd szót.

beszúrás: bejelentkezés.png

↳ Beléptető kapu:

A beléptető kapu - belépőkártyán szereplő vonalkód, QR kód, vagy akár NFC stb. - kód alapú belépést biztosít a dolgozók számára. Ez lehetővé teszi a műszak felvételt/leadást, illetve a dolgozók pihenőidejének regisztrálását a rendszerbe. Az SML listázza, hogy melyik dolgozó és mióta van jelen, illetve megjeleníti a pihenőidejüket töltő kollégák nevét is.
Műszak kezdés: csak a dolgozói kód beolvasása - és műszakleadás - után lehetséges. 
Pihenő kezdés: csak a műszakfelvételt követően lehetséges.
Pihenő vége: csak a pihenőidő megkezdését követően lehetséges.
Műszak vége: csak a már megkezdett műszak esetén lehetséges.

(Megjegyzés: a beléptető kapu az SML-en belül az Alkalmazások menüpontból is elérhető!)

beszúrás: belép.kapu_felület.png

b, Kezdőképernyő

Az SML-ben az alapértelmezettként megjelenő kezdőképernyő struktúrája egyénileg testreszabható, így az a megjelenítési beállításoktól függően felhasználónként teljesen különböző lehet.

beszúrás: kezdőképernyő_v2.png

(Megjegyzés: az illusztrációként szolgáló kép az alapértelmezett beállításokat tükrözi.)

c, Felhasználók és jogosultsági köreik

Az SML a felhasználók és jogaik kezeléséhez hozzáférés ellenőrző listát - ACL (Access Control List) - használ, mely a felhasználócsoportok, engedélyek és objektumok közti kapcsolatot felügyeli. Ez azt jelenti, hogy minden egyes felhasználót valamely csoporthoz kell hozzárendelni, mely az annak megfelelő hozzáférést biztosítja a különböző objektumokhoz.
A rendszer által használt csoportok a következők:

-Gépkezelő

-Raktáros

-Irodista

-Termelésirányító

-Üzletkötő

-Adminisztrátor

1. Gépkezelő: a legszűkebb jogkörrel rendelkező felhasználó. Az egyetlen dolga, hogy rögzítse a ráosztott munka részleteit és csatolja/változtassa a gyártáshoz szükséges - pl.: rákel, klisé, recept stb. - elemeket.
2. Raktáros: jogköre magába foglalja a raktárkezelő alkalmazásokhoz való hozzáférést, illetve az alapanyag menedzsmentet.
3. Irodista: ő tartja a kapcsolatot a cég üzleti partnereivel és ő felelős az SML termékekhez és rendelésekhez kapcsolódó kezdeti adatokkal való feltöltéséért. Hozzáfér az ügyletekhez - pl.: számlát állíthat ki, kiegyenlítéseket rögzíthet -, viszont a gyártásba nem szólhat bele.
4. Termelésirányító: az ő jogköre ott kezdődik, ahol az irodistáé véget ér: joga van belenyúlni a termelési folyamatokba, kezelni az árucikkeket és raktárkészletet.
5. Üzletkötő: jogköre hasonló az irodistáéhoz, viszont ő csak saját partnereihez és az azokhoz kapcsolódó objektumokhoz férhet hozzá.
6. Adminisztrátor: az SML minden részéhez van hozzáférése.

d, Értesítések

A program értesítéseket küld számunkra különböző műveletek - be/kijelentkezés, objektum létrehozás/szerkesztés/törlés - végrehajtásakor, ide értve a jogosultsági körünkön kívül eső programrészek megnyitására tett próbálkozást is. Példaként: a bejelentkezést követően a “Sikeres bejelentkezés” című értesítést kapjuk a rendszertől, mely a felület jobb felső sarkában jelenik meg zöld színnel és nagyjából 7 másodpercig marad látható. Ha az értesítésre visszük az egeret/ujjunkat annak megjelenésekor, akkor az egészen addig a képernyőn marad, míg le nem vesszük róla az egeret/ujjunkat. Manuálisan is eltűntethetők az értesítés jobb szélén található ‘X’ megnyomásával, illetve az értesítésre való kattintással. Kivételként meg kell említenünk a “Hozzáférés megtagadva” és “A keresett elem nem található” című értesítéseket, melyek piros színnel és méretes felkiáltójellel figyelmeztetnek jogkörön kívüli vagy sikertelen művelet végrehajtáskor.

e, Felület tartalma

Ez az alfejezet taglalja a programfelületet alkotó legfontosabb elemeket: a fejléc, a menürendszer, és a táblázat formátumú, kilistázott objektumok tartalmát, illetve felépítését.

↳ Fejléc:


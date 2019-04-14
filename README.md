# Feladatok
## 7
A kliens kapcsolódjon a `12345` porton futó szerverhez. Ez egy fájlból portszámokat olvas fel, és sorban átküldi őket a kliensnek. Amikor a kliens megkap egy portszámot, csatlakozik az azon a porton futó szerverhez (közben megtartja a kapcsolatát az első szerverrel). Ez a szerver egy fájlból néhány számot olvas fel, ezeket átküldi a kliensnek, majd bontja vele a kapcsolatot. A kliens minden megkapott szám fogadása után kiírja egy fájlba az összes eddig megkapott szám összegét.

fájlok:`7/`

## 8
A szerverhez kapcsolódjon két kliens egymás után (ugyanazon a porton) úgy, hogy a szerver mindkét kapcsolatot egyszerre tartja nyitva. A kliensek először egy-egy sorban a saját nevüket küldik át, majd felváltva írhatnak be egy-egy sornyi szöveget. A beírt üzeneteket küldje át a szerver a másik kliensnek ilyen alakban: `<másik kliens neve>: <másik kliens üzenete>`. Ha valamelyik kliens bontja a kapcsolatot, akkor a szerver zárja be a másik klienssel a kapcsolatot, és lépjen ki.
- Ha az egyik kliens bontja a kapcsolatot, akkor a szerver várakozzon egy újabb kliensre, aki kapcsolódás után átveszi az előző helyét. Természetesen az új kliens is először a saját nevét küldi át.
- A porton tetszőlegesen sok kliens kapcsolódhat, és bármikor ki is léphetnek. A szerver sorban engedi szóhoz jutni a klienseket, azonban az üzeneteket nem azonnal küldi el mindegyik másik kliensnek. Ehelyett a szerver összegyűjti az üzeneteket, és csak akkor küldi el az adott kliens számára szóló üzeneteket, amikor az éppen szóhoz jut.

fájlok: `sajatmegoldas/` és `8/`

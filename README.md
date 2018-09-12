# Párhuzamos programozás témalabor BME AUT

A témalabor során kisfeladatok megoldásán keresztül ismerhető meg a párhuzamos programozás világa, a gyakori problémák és lehetséges megoldásaik.

## Ajánlott irodalom

Maurice Herlihy & Nir Shavit – The art of multiprocessor programming

Developing Parallel Programs - A discussion of popular models http://www.oracle.com/technetwork/server-storage/solarisstudio/documentation/oss-parallel-programs-170709.pdf

C++ Intel Threading Building Blocks https://www.threadingbuildingblocks.org, Parallel Patterns Library https://msdn.microsoft.com/en-us/library/dd492418.aspx

Java: Runnable-ök és Executor service

.NET: Task Parallel Library https://docs.microsoft.com/en-us/dotnet/standard/parallel-programming/task-parallel-library-tpl

## Feladatokkal kapcsolatos általános tanácsok

* Mindig kapcsoljuk be a fordító optimalizációkat a teljesítmény méréshez
  * Visual Studio-ban ez a "release" build configuráció használatát jelenti
* Teljesítmény alatt a program lényegi részének futási idejét értjük
* Amikor teljesítményt mérünk, kellően nagy méretű feladatokat hasonlítsunk össze (pl. 15 és 18 millisec nem elég nagy különbség, hogy következtetést lehessen levonni)
* Az időmérést mindig ismételjük meg legalább 5-ször, és az átlagot használjuk
  * Ha nagy a szórás a mért időkben, vizsgáljuk meg, miért
  * Szofisztikáltabb megoldás: 10-szer mértünk, 2-2 legnagyobb és legkisebb értékel eldobjuk, és a maradék átlagát vesszük
* A idő mérést mindig a program maga végezze és írja ki konzolra az eredményt, így könnyen lehet CSV fájlokat gyártani úgy, hogy egy bat fájlból / valamilyen scriptből futtatva a programot a >> operátorral átirányítod a kimenetet egy CSV fájlba

## Feladatok beadása

Összes feladat megoldása, forráskódokkal, eredményekkel, diagramokkal együtt egy publikusan elérhető GitHub repository-ban. A beadás az adott feladat pusholását jelenti a megadott nap végéig.

Határidők 2018 őszi félév:

1. feladat: szeptember 30.
2. feladat: október 14.
3. feladat: október 28.
4. feladat: november 11.
5. feladat: december 2.
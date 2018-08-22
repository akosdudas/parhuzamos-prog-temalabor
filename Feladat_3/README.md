# 3. feladat: tömb rendezés parallel merge sort alrogitmussal C# nyelven

## Ajánlott olvasnivaló

Divide and conquer ("oszd meg, és uralkodj elv"): http://reedcopsey.com/2010/02/26/parallelism-in-net-part-11-divide-and-conquer-via-parallel-invoke/
Parallel merge sort algoritmus: http://www.drdobbs.com/parallel/parallel-merge-sort/229400239, https://stanford.edu/~rezab/classes/cme323/S16/notes/Lecture04/cme323_lec4.pdf

## Feladat

### Készíts egy C# nyelvű programot, amely

* Konzol alkalmazás
* Parancssori argumentumban kap egy számot, amely a rendezendő tömb mérete
* Inicializál véletlen integer számokkal egy megadott méretű tömböt
* Elkezd időt mérni
* Lefuttatja a rendezést
* Konzolja kiírja a pontos futási időt

### Algoritmusok

* Quicksort rendezés
  * Fontos, hogy NE használd a .NET rendező függvényét, hanem fog egy egyszerzű, egyszálú quicksort algoritmust
  * Ez az összehasonlítási alap a párhuzamos implementációhoz
* Párhuzamos implementáció parallel merge sort algoritmussal
  * Használd a Task Parallel Library képességeit, mind a Parallel.Invoke vagy a Task.Run; ne használj explicit szálakat
  * Megvizsgálandó feladat, hogy meddig érdemes darabolni a feladatot párhuzamos részekre, és mikortól már nem érdemes további, kisebb egységekre osztani, hanem már végre kell hajtani a rendezést az adott szálon/taszban

### Elvárt eredmény

* Lemérni és összehasonlítani az egyszálú és a párhuzamos futási időt
  * Diagram formájában ábrázolva
* Megvizsgálni azt a paramétert, aminél kisebb feladatot már nem darabolunk tovább (vagyis, mekkora az a legkisebb tömb, amit már egy szálon rendezünk?)
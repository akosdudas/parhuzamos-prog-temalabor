# 1. feladat: mátrix szorzás C# nyelven

## Ajánlott olvasnivaló

Daan Leijen, Wolfram Schulte, and Sebastian Burckhardt: The Design of a Task Parallel Library https://www.microsoft.com/en-us/research/wp-content/uploads/2009/09/TheDesignOfATaskParallelLibraryoopsla2009.pdf

## Feladat

### Készíts egy C# nyelvű programot, amely

* Konzol alkalmazás
* Parancssori argumentumban kap egy számot, amely az összeszorzandó mátrixok mérete (négyzetes mátrix)
* Parancssori argumentumban megadható neki, hogy melyik algoritmust (lásd alább) használja
* Inicializál véletlen integer számokkal két megadott méretű négyzetes mátrixot
* Elkezd időt mérni
* Lefuttatja a választott algoritmussal a szorzást
* Konzolja kiírja a pontos futási időt

### Algoritmusok

* Naív, egyszálú algoritmus, 3 egymásba ágyazott for ciklussal
* Naív algoritmus belső két for ciklusának megcserélése azért, hogy az összeszorzandó mátrixokat sorfolytonosan olvassuk
* Párhuzamos implementáció Thread / ThreadPool használatával, ahol a szálak együtt dolgoznak a feladaton
  * A szálak száma változtatható legyen
  * Minden szál egy jól meghatározott régiót (pl. egy sort, egy oszlopot, n*n-es darabot) készít el
* Párhuzamos implementáció Task Parallel Library segítségével
  * Használd a Parallel.Foreach-et a párhuzamosításhoz (ne használj se Thread-et, se ThreadPool-t)

### Elvárt eredmény

* Lemérni és összehasonlítani a futási időket változó mátrix méretekkel
* Megtalálni, mely mátrix méretek esetén jobb a párhuzamos algoritmus
* Diagram formájában ábrázolt futási idők (pl. Excel)
  * Első diagramon a vízszintes tengelyen a mátrix méretének hatása az egyes algoritmusokra (vonal diagram)
  * Másik diagramon egy választott mátrix méret, ahol láthatóak a különbségek, oszlop diagram formájában összegezve a teljesítményt
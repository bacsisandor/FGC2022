# FGC2022 - Bevezető

Oldd meg az alábbi programozási feladatokat Java nyelven!

Miért fontos a Java az FGC szempontjából? A Java-ra azért van szükség, mert a versenyen használt REV-es [Control HUB-ot](http://www.revrobotics.com/rev-31-1595/) Java-ban lehet a leghatékonyabban programozni. A feladatok kezdő szintűek, így annak sem kell aggódnia, aki még nem programozott korábban Java-ban. Az interneten számos oktatási anyag található a témakörben angolul és magyarul is. Ezek közül néhány:

* https://www.codecademy.com/learn/learn-java
*	https://www.w3schools.com/java/
*	http://nagygusztav.hu/sites/default/files/csatol/java_programozas_1.3.pdf

A feladatok megoldásához természetesen bármilyen IDE használható. A legelterjedtebb és legnépszerűbb IDE-k Java fejlesztéshez:

* [IntelliJ IDEA](https://www.jetbrains.com/idea/)
* [Eclipse](https://www.eclipse.org/ide/)
* [NetBeans](https://netbeans.apache.org/)

Sok sikert! :blush: Bármilyen kérdés esetén keress minket bizalommal az alábbi email címen: fgc@kjbkinfinity.com

# 1. Feladat - Robot Controller

Egy robot controller működését fogjuk modellezni, ahol a controlleren található gombok állapotát vizsgáljuk. Az osztályok leírása az alábbi:

## Button class:

### Tagváltozók:
```Java
private String ID
```

Privát láthatóság, megadja a controlleren található gomb azonostóját

```Java
private boolean pressed
```
Privát láthatóság, megadja, hogy az adott gomb megvan-e nyomva. True, ha meg van nyomva, false, ha nincs.

### Konstruktor:
```Java
public Button(String ID, boolean pressed) 
```
Beállítja az ID-t és a pressed tagváltozók értékeit a paraméterül kapott értékekre. 

### Műveletek:

```Java
public String getID()
```
Visszatér az adott gomb ID-jával. 


```Java
public void setState(boolean pressed)
```
Beállítja az adott gomb állapotát a paraméterül kapott értékre. 


```Java
public boolean getState()
```
Visszatér az adott gomb pressed értékével. 


## Controller class: 

### Tagváltozók:

```Java
private ArrayList<Button> buttons
```
Privát láthatóság, tárolja a Button objektumokat egy ArrayList-ben.

### Konstruktor:
```Java
public Controller()
```
Példányosítja a buttons ArrayList-et. 

### Műveletek:
```Java
public void addButton(Button b)
```
Hozzáadja a paraméterül kapott Button objektumot az ArrayList-hez.

```Java
public void pressAll()
```

Az összes gomb állapotát beállítja megnyomottra.

```Java
public void releaseAll()
```
Az összes gomb állapotát beállítja elengedett állapotúra. 

```Java
public int getNumOfPressedBtns()
```
Visszatér a lenyomott gombok számával.

## Main class:

A main függvényben az alábbi műveleteket végezzük el:
```Java
Controller ctrl = new Controller();
```
Példányosítsunk egy Controller-t, amihez majd a gombokat adjuk hozzá.

Adjunk hozzá 4 gombot a Controller-hez:

ID: "A" Pressed: true

ID: "B" Pressed: false

ID: "X" Pressed: false

ID: "Y" Pressed: true

Írjuk ki a nyomva tartott gombok számát. (Elvárt kimenet: 2)
Pl. Így:
```Java
System.out.println("Number of pressed buttons:" + ctrl.getNumOfPressedBtns());
```

Hívjuk meg a Controller objektumon a pressAll() metódust. 

Írjuk ki most a nyomva tartott gombok számát. (Elvárt kimenet: 4)

Hívjuk meg a Controller objektumon a releaseAll() metódust. 

Írjuk ki most a nyomva tartott gombok számát. (Elvárt kimenet: 0)

 # 2. feladat - Iker-majdnem-prímek

Egy természetes számot "majdnem prímnek" nevezünk, ha felírható két (nem feltétlenül különböző) prímszám szorzataként. Ha két szomszédos természetes szám is "majdnem prím", akkor nevezzük ezeket "iker-majdnem-prímeknek". Ilyen például a 9 és a 10, hiszen 9=3×3, illetve 10=2×5, azaz mindketten "majdnem prímek", és szomszédosak. A feladat olyan program írása, mely egy megadott határig (n) előállítja az összes "iker-majdnem-prím" párokat.

# 3. feladat - Feltöltés Github repository-ba

Készíts egy új reposiroty-t GitHub-on, ahova fel tudod tölteni a megoldásaidat. A két feladat lehetőleg két külön mappába kerüljön. Ezután a repository linkjét küldd el a fgc@kjbkinfinity.com e-mail címre. 

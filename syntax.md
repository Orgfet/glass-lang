# The Glass Lang Documentation

## Kapitel 1 Variablen

### 1.1 Datentypen in Glass:

Glass hat folgende Datentypen:
```
Integer,   //Für Ganzzahlen
String,    //Für Zeichenketten
Character, //Für ein Zeichem
Boolean.   //Für Boolische werte
Float,     //Für Komma zahlen
```

Sie werden folgendermaßen deklariert:

``Integer = int x = Wert;``

``String = str x = "Inhalt";``

``Character = char x = "Buchstabe";``

``Boolean = bool x = true/false; oder 1/0;``

### 1.2 Konstanten in Glass:


Um eine Konstante zu deklarieren musst du folgendes Tun:

In Glass nutzen wir 'final'.

Beispiel:
```
final datentyp = wert;
```

## Kapitel 2 Operatoren

### 2.1 Unäre Operatoren

```
!  //Die Negation mit dem ! Operator wird die Variable negiert.
++ //Inkrementiert die Variable um 1
-- //Dekrementiert die Variable um 1
```

### 2.2 Arithmetische Operatoren

```
+ //Addition
- //Subtraktion
/ //Multiplikation
* //Division
```
### 2.3 Bit-Shift Operatoren

```
<< //Verschiebt nach Links (Füllt von Rechts mit 0en auf)
>> //Verschiebt nach Rechts (Füllt von Link mit 0en auf)
```

### 2.4 Vergleichs Operatoren

```
<  //Weniger als
<= //Weniger oder gleich als
>  //Mehr als
>= //Mehr oder gleich als
== //Gleich
!= //Nicht Gleich
```

### 2.5 Logische und Bitwise Operatoren

```
&&, & //Logisches(&&) und Bitwise(&) Und
||, | //Logisches(||) und Bitwise(|) Oder
```

### 2.6 Abweichende Möglichkeiten

```
+= //Erhöht den wert x um y
-= //Veringert den wert x um y
```

## Kapitel 3 Arrays

Ein Array wird in Glass mit den [] klammern deklariert.

### 3.1 1D Arrays
Beispiel:

```
int x [] = {1,2,3,4};
str x [] = {"Hi", "Hello"};
char x [] = {"a", "b"};
```

### 3.2 2D Arrays
Beispiel:
```
int x [][] = {
    {1,2,3}
    {4,5,6}
    {7,8,9]
};
```

### 3.3 3D Arrays
Beispiel:
```
int x [][][] = {
    {
        {1,2,3}
        {4,5,6}
    }
    {  
        {7,8,9}
        {10,11,12}
    }
};
```

## Kapitel 4 Strings

### 4.1 Strings Deklarieren
```
str vname = "Marc";
str nname = "Zweiler";
```

### 4.2 Formatierte Strings:
```
str fname = f"{nname}, {vname}";
```

### 4.3 Strings verbinden:
```
str cname = "nname+ ' ,' + vname";
```

### 4.4 String indexierung
```
char vInitial = vname[0];
char nInitial = nname[0];


print(toLowercase(nname));
print(toUppercase(vname));
```

## Kapitel 5 Kommentare

### 5.1 Normaler Kommentar
```
 //Kommentar
```

### 5.2 Mehrzeiliger Kommentar
```
//*
    Doku
    @parameter
    @return
*/
```

## Kapitel 6 Konditionen

### 6.1 If anweisungen
```
if (condition) {
    print("hehe");
}
```

### 6.2 If-Else anweisung
```
if (condition) {
    print("hehe");
} else {
    print("haha");
}
```

### 6.3 else if anweisung
```
if (condition) {
    print("hehe");
} else if (condition2) {
    print("haha");
} else {
    print("hoho");
}
```

### 6.4 Case
```
func str dailyMood(Weekday w) {
    return case(w) {
        SATURDAY, SUNDAY: "Yippi, Weekebd!";
        Monday: "ugh...";
        default: ":)";
    };
}
```
## Kapitel 7 Loops

### 7.1 For schleifen

Die for schleife in Glass funktioniert folgender maßen:
```
int x = 10;
for (int i = 0; i < x; i++) {

    print("hehe");

}
```
### 7.2 While schleifen

Die while schleife in Glass funktioniert folgender maßen:
```
while(condition) {

    print("hehe");
    
}
```
### 7.3 Do While schleifen

Die do while schleife in Glass funktioniert folgender maßen:
```
do {

    print("hehe");

} while (condition);
```

## Kapitel 8 Funktionen und Voids

```
func int myFunction (int a, int b) { 

    return a + b;

}
```
```
func int myFunction2 (int a,b) {//Wenn man mehrere 
//parameter des sleben typen übergibt kann man sie zusammenfassen.

    return a+b;

}
```
```
Void myVoid(void) { //Wenn man keine parameter 
//übergibt muss man "void als parameter eintragen auch bei Fuctions

    print("Hallo Welt!");

}
```
```
func int noParameters(void) {//Beispiel für den paramter void

    str name = "Marc";

    return name;
}
```
```
//Aufrufen von funktionen
func int main() {//main ist die ausnahme des Void parameters
    int x = 25;
    int y = 5;
    
    myFunction(x,y);    //Hier kommt 30 raus a+b
    myFunction2(x,y);   //Hier kommt 30 raus a+b
    myVoid();           //Hier wird "Hallo Welt" ausgegeben
    noParameters();     //Hier wird "Marc" zurückgegeben
    
    return 0;
}
```

## Kapitel 9 Strukturierte Daten
```
struct Person {
    str vname;      //Vorname
    str nname;      //Nachname
    int age;        //Alter
    float height;   //Größe
}
```
Anwendung:
```
Person p1 = {"Mattes", "Kania", 20, 1.75};
```

## Kapitel 10 Sub und Supertypen

### 10.1 Supertyp
```
struct Person {
    string name;
    int age;
}

```

### 10.2 Subtyp
```
struct Student : Person {
float grade;
}
```
```
Student s1 = {"Mattes", 20, 4.6}; //Stundenten erstellen
print("s1.name");                 //Ausgeben vom Name (Mattes)
s1.age = 21;                      //Alter von 20 auf 21 setzen
```

## Kapitel 11 Enums
```
define Enum as Weekday {
    MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY;
} 

func int Main() {
    Weekday w = MONDAY; 

    print(w);               //MONDAY
    print(asOrdinal(w));    //0
        
    return 0;

}
```

## Kapitel 12 Interfaces .gli (Glass Interface)
```
@interface "Interface1" //Namen des Interfaces festlegen

struct Person {
    str name;
    int age;
}

void eat (void);

void sleep(void) {
    print("zzz");
}


// In der Glass file:

#import Interface1.gli;


@Overide
void eat(void) {
    print("Lecker!"); //Gibt jetzt lecker aus
}


int main() {
    
    eat(); //Gibt die überschiebene Methode aus "Lecker!"
    sleep(); //Gibt wie im Interface definiert "zzz" aus
    
    Person p1 = {"Mattes", 21};
    return 0;
}
```

## Kapitel 13 Importe/Projekte mir mehreren Dateien
```
#import dateiname.gli/glass //mit "#import" werden .gli (Glass Interface) oder .glass (Glass Code datein) importiert.
//*Mann kann in Interfaces und in Code datein importieren man muss aber aufpassen eine datei nicht 2mal zu importieren!
   Wenn man eine .glass datei importiert mann kan die funktionen aufrufen aber man kann die nicht mit @Overide 
   Überschreiben. 
*/
```
```
Projekt Struktur:
[root]
 ├─[src]
 │  │
 │  └─ Interface.gli
 │  └─ Main.glass
 │ 
 │
 └─[test]
      └─ test.glf //(= Glass Forge)
```
``Interface.gli:``
```
@Interface "Interface"

#import glassio.gll //(= Glass Library)

final int NUM = 20;

void hello (void) {
    print("hello");
}
```
``Main.glass:``
```
#import Interface.gli; //Importiert "Interface.gli" und "glassio.gll"

int Main () {
    hello(); //printed "Hello"
    print(NUM); //printed "20"
}
```

## Kapitel 14 Type Casting
```
float fnum = 1.5;
str words = "2";
int nnum;
int wordsnum;

wordsnum = word: int; //da kommt 2 raus

nnum = fnum: int; // Da kommt 1 raus
nnum = fnum: round(int); //Da kommt dann 2 raus er rundet auf
```
### Das schema ist:
``newvar = orgvar: newtype;``
### ``:`` Muss sich direkt an der orgvar befinden.


## Kapitel 15 Macros
```
//*
    Macros funkten wie in c
    mit "#define" gibt man an das man ein Macro erstellen möchte
    danach kommt der Name des Macros und der wert. Bei Macros braucht mein kein ";" am ende
*/
#define NAMEDESMARCROS = wert
```

## Kapitel 16 Type-aliases
```
//*
    Um einen Typ Alias zu erstellen muss man ähnlich wie bei Enums "define" benutzen
    dann gibt man an das es sich um einen "aliass" handelt und danach den Namen des "aliass" und was ihn ausmacht.
*/
define aliass as Name char[20];

// Aliasse für Aliasse sind möglich
define aliass as Vorname Name;
```

## Kapitel 17 Operant Grouping

``Rangliste und  Assoziativität``
```
# 1 höheste Priorität
    Postfix: expr++, expr-- (Increment/Decrement
    L zur R

# 2 Unäre Operatoren
    Präsix: ++expr, --expr, +, -, ~, !, TypeCast
    R zur L

# 3 Muliplikation/Division/Modulo
    *, /, %
    L zu R

# 4 Bit Shifting
    << , >>
    R zu R

# 5 Vergleich
    <, <=, > ,>=, ==, !=
    L zu R

# 6 Bitwise AND
    &
    L zu R

# 7 Bitwise OR
    |
    L zu R

# 8 Logic AND
    &&
    L zu R

# 9 Logic OR
    ||
    L zu R

# 10 Tenär
    ? :
    R zu L

# 11 Zuweisungen
    =, +=, -=. *=. /=. %=
    L zu R

# 12 Komma
    ,
    L zu R
```

## Kapitel 18 Listen und Sets
```
int liste[10];

add_to_list(10);
print_list(); // Gibt 10 aus

int set[10];
add_to_set(40);
add_to_set(40); //Duplikat wird ignoriert
if(contains_in_set(40) {
    print(hehe);
}
print_set(); //Gibt 40 aus
```

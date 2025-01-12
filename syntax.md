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


## Datentypen
### Primitive Datentypen

| **Datentyp** | **Beschreibung**                                       |
| ------------ | ------------------------------------------------------ |
| byte         | Ganze Zahlen, 8 Bit groß                               |
| char         | Ein beliebiges Zeichen in '' angegeben. NICHT ""!      |
| short        | Ganze Zahlen, 16 Bit groß                              |
| int          | Ganze Zahlen, 32 Bit groß                              |
| long         | Ganze Zahlen, 64 Bit groß                              |
| float        | Gleitkommazahlen, 32 Bit groß, f an die Zahl schreiben |
| double       | Gleitkommazahlen, 64 Bit groß                          |
| boolean      | false or true                                          |
### Komplexe Datentypen
| **Datentyp**                               | **Beschreibung**                  |
| ------------------------------------------ | --------------------------------- |
| String                                     | Eine beliebige Zeichenkette       |
| Jede Klasse oder z.B. Integer, Boolean ... | "Alles was groß geschrieben wird" |

## Variablen
### Deklarierung
**Beispiel:**
```java
byte alter;
String name;
...
```
Es werden die Variablen nur angelegt (also deklariert), jedoch noch keine Werte zugewiesen.

### Initialisierung
**Beispiel**
```java
alter = 123;
name = abc;
```
Den Variablen werden konkrete Werte zugewiesen.

### Deklarieren und Initialisieren
**Beispiel**
```java
char zeichen = '@';
float pi = 3,14f;
...
```
Es werden die Variablen in einem Schritt deklariert und initialisiert.


## Einfache Operatoren
### Arithmetische Operatoren

| **Operator** | **Beschreibung**                                                            |
| ------------ | --------------------------------------------------------------------------- |
| +            | Addition zweier Zahlen (funktioniert auch zum Zusammenfügen zweier Strings) |
| -            | Suptraktion zweier Zahlen                                                   |
| *            | Multiplikation zweier Zahlen                                                |
| /            | Division zweier Zahlen                                                      |
| %            | Modulo                                                                      |
| ++           | Inkrementieren einer Variable z.B. i++ (i = i + 1)                          |
| --           | Dekrementieren einer Variable z.B. i-- (i = i - 1)                          |

### Vergleiche

| **Operator** | **Beschreibung**                 |
| ------------ | -------------------------------- |
| <            | Zahl 1 ist kleiner Zahl 2        |
| <=           | Zahl 1 ist kleiner gleich Zahl 2 |
| >            | Zahl 1 ist größer Zahl 2         |
| >=           | Zahl 1 ist größer gleich Zahl 2  |
| ==           | Zahl 1 ist gleich Zahl 2         |
| !=           | Zahl 1 ist ungleich Zahl 2       |

### Logische Operatoren

| **Operator** | **Beschreibung** |
| ------------ | ---------------- |
| !            | Negation         |
| &&           | logisches und    |
| \|\|         | logisches oder   |
| ^            | logisches xor    |

### Bitweise Operatoren
| **Operator** | **Beschreibung** |
| ------------ | ---------------- |
|              |                  |

## Bedingungen
**Beispiele**
```java
...
if(a > b){
	System.out.println("Zahl 1 ist größer Zahl 2");
}
else if (a < b){
	System.outprintln("Zahl 1 ist kleiner Zahl 2");
}
else{
	System.out.println("Zahl 1 ist gleich Zahl 2");
}
```
Bedingungen evaluieren zu true or false.

## Schleifen 
### for-Schleife
**Beispiel**
```java
for (int i = 0; i < 10; i++){
	System.out.println(i);
}
```

### while-Schleife
**Beispiel**
```java
int zaehler = 0;
while (zaehler < 10){
	System.out.println(zaehler);
	zaehler++;
}
System.out.println(zaehler);
```

### do-while-Schleife
**Beispiel**
```java
int zaehler = 0;
do{
	System.out.println(zaehler);
	zaehler++;
}while (zaehler < 10);
System.out.println(zaehler);
```

## Zufallszahlen
**Beispiel** 
```java
Random random = new Random();
int zufallszahl = random.nextInt(6);
System.out.println(zufallszahl);
```
Bei dem Beispiel werden Zahlen von 0 bis einschließlich 5 zufällig ausgeben. Die Obergrenze 6 ist nicht bei den zufälligen Zahlen enthalten!

Für Zufallszahlen von (untereGrenze) ... bis (obereGrenze) ... zu erhalten gilt folgende Regel:
```java
Random random = new Random();
int zufallszahl = random.nextInt(obereGrenze - untereGrenze + 1) + untereGrenze;
System.out.println(zufallszahl);
```

## Ein- und Ausgabe
**Beispiel**
```java
Scanner scanner = new Scanner(System.in);

System.out.println("Bitte geben sie was ein: ");
// Eingabe
String eingabe = scanner.nextLine();

// Ausgabe
System.out.println("Ihre Eingabe war: \n" + eingabe);
```


## Aufgaben Teil 1
[[Einfache Aufgaben]]
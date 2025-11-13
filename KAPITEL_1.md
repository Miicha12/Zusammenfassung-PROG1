# 📘 Zusammenfassung: Klassen & Objekte (Java)
### 🔹 1. Klassen & Objekte

**Klasse** = Bauplan für Objekte

`→ Definiert Datenfelder (Zustand) und Methoden (Verhalten).`

**Objekt** = konkrete Instanz einer Klasse

`→ Einzelnes Exemplar mit eigenem Zustand.`

Beispiel:
```java
class Person {
    String name;   // Datenfeld
    int alter;

    void begruessen() {  // Methode
        System.out.println("Hallo, ich bin " + name);
    }
}
```

### 🔹 2. Zustand

Der Zustand eines Objekts wird durch die Werte seiner Datenfelder beschrieben.

Beispiel:
```java
Person p = new Person();
p.name = "Anna";
p.alter = 20;   // Zustand des Objekts p
```

### 🔹 3. Methoden & Kommunikation

Objekte können über Methodenaufrufe miteinander kommunizieren.

**Methoden** haben:

`Parameter` (Informationen für den Aufruf)

`Typen` (welche Werte zulässig sind)

`Ergebnistyp` (z. B. int, String, void)

<br><br>

Beispiel:
```java
class Rechner {
    int addiere(int a, int b) {  // Parameter mit Typen
    return a + b;           // Ergebniswert
    }
}

Rechner r = new Rechner();
int summe = r.addiere(5, 3);    // Methodenaufruf
```

### 🔹 4. Signatur einer Methode

Eine Signatur besteht aus:

`Methodenname`

`Parametertypen`

Beispiel:
```java
int addiere(int a, int b)   // Signatur: addiere(int, int)
```

### 🔹 5. Ergebniswerte

Methoden können einen Wert zurückgeben `return`.

Wenn der Typ `void` ist, kommt kein Wert zurück.

Beispiel:
```java
void druckeName(String name) {   // void-Methode
    System.out.println(name);
}
```

### 🔹 6. Erstellung von Objekten

Objekte werden mit dem `new`-Operator erzeugt.

Beispiel:
```java
Auto meinAuto = new Auto();
```

<br>

### 🔹 7. Quelltext & Struktur

Der Quelltext einer Klasse definiert:

welche Daten die Objekte halten `Datenfelder`,
welche Aktionen sie ausführen können `Methoden`.

Ein Java-Programm besteht aus vielen Klassen, die sich gegenseitig aufrufen.

📘 Ein kompaktes Lernbeispiel:
```java
class Auto {
String farbe;     // Zustand
int geschwindigkeit;

    void beschleunigen(int wert) {  // Methode mit Parameter
        geschwindigkeit += wert;
    }

    int getSpeed() {  // Methode mit Ergebniswert
        return geschwindigkeit;
    }
}

class Main {
public static void main(String[] args) {
Auto a = new Auto();   // Instanz erzeugen
a.farbe = "Rot";
a.beschleunigen(30);

        System.out.println(a.getSpeed());  // -> 30
    }
}
```


#### 🧠 Merksätze fürs Lernen

`Klassen` sind *Baupläne*, `Objekte` sind *konkrete Dinge*.

Objekte haben Zustand `Datenfelder` und Verhalten `Methoden`.

`Methoden` definieren *Aktionen*; `Parameter` geben zusätzliche *Infos* mit.

Java-Programme bestehen aus vielen zusammenarbeitenden `Klassen`.
# 🏗️ Clase și Obiecte — Teorie și Exemple

## 📘 Teorie

- **Clasă**: tip definit de utilizator care descrie o entitate (stare + comportament).
  - **Stare (câmpuri/atribute)**: variabile ale obiectului (ex.: `nume`, `puncte`).
  - **Comportament (metode)**: acțiuni pe starea obiectului (ex.: `adaugaPuncte`).
- **Obiect**: instanță a unei clase, creată cu `new`.
- **Constructor**: metodă specială cu același nume ca al clasei, fără tip de retur.
  - Implicit există un constructor fără argumente dacă nu definim noi altul.
  - Când definim un constructor propriu, cel implicit nu mai este generat automat.
- **this**: referință la obiectul curent. Folosită pentru a diferenția câmpurile de parametri (`this.puncte = puncte`).
- **Referințe**: variabilele de tip clasă rețin adrese către obiecte (nu obiectul în sine).
  - Atribuirea copiază referința: două variabile pot indica același obiect.
- **Valori implicite pentru câmpuri**: numerice `0`, `boolean false`, referințe `null`.
- **`null`**: absența unei referințe. Orice acces la membru pe `null` produce `NullPointerException`.
- **Afișare**: putem scrie o metodă `afisare()` sau suprascrie `toString()` pentru formatare.
- Deocamdată folosim câmpuri `public` pentru simplitate; în lecția de **Încapsulare** le vom proteja.

## 🔎 Exemple

### Exemplul 1: Primii pași — clasă cu câmpuri și obiecte

```java
public class ExCls1CardHarryFields {
    // Clasă simplă cu câmpuri publice
    public static class CardHarry {
        public String nume;
        public String casa;
        public int puncte;
    }

    public static void main(String[] args) {
        CardHarry c1 = new CardHarry();
        c1.nume = "Harry";
        c1.casa = "Gryffindor";
        c1.puncte = 150;

        System.out.println(c1.nume + " | " + c1.casa + " | " + c1.puncte + "p");
    }
}
```

### Exemplul 2: Constructor, `this` și metode care modifică starea

```java
public class ExCls2ConstructorSiMetode {
    public static class CardHarry {
        public String nume;
        public String casa;
        public int puncte;

        // Constructor cu parametri
        public CardHarry(String nume, String casa, int puncte) {
            this.nume = nume;
            this.casa = casa;
            this.puncte = puncte;
        }

        public void adaugaPuncte(int p) {
            this.puncte += p;
        }

        public void scadePuncte(int p) {
            this.puncte -= p;
        }

        public void afisare() {
            System.out.println("👤 Nume: " + nume);
            System.out.println("🏰 Casa: " + casa);
            System.out.println("⭐ Puncte: " + puncte);
        }
    }

    public static void main(String[] args) {
        CardHarry h = new CardHarry("Hermione", "Gryffindor", 100);
        h.adaugaPuncte(30);
        h.scadePuncte(10);
        h.afisare(); // 120 puncte
    }
}
```

### Exemplul 3: Colecție de obiecte — array și parcurgere

```java
public class ExCls3ArrayDeObiecte {
    public static class CardHarry {
        public String nume;
        public int puncte;

        public CardHarry(String nume, int puncte) {
            this.nume = nume;
            this.puncte = puncte;
        }
    }

    public static void main(String[] args) {
        CardHarry[] arr = new CardHarry[] {
            new CardHarry("Harry", 150),
            new CardHarry("Ron", 90),
            new CardHarry("Hermione", 120)
        };

        for (int i = 0; i < arr.length; i++) {
            System.out.println(arr[i].nume + " - " + arr[i].puncte + "p");
        }
    }
}
```

### Exemplul 4: Referințe la același obiect (`aliasing`)

```java
public class ExCls4Referinte {
    public static class CardHarry {
        public String nume;
        public int puncte;

        public CardHarry(String nume, int puncte) {
            this.nume = nume;
            this.puncte = puncte;
        }
    }

    public static void main(String[] args) {
        CardHarry a = new CardHarry("Harry", 150);
        CardHarry b = a; // b referă același obiect ca a

        b.puncte += 10;
        System.out.println(a.puncte); // 160 — s-a modificat și prin a

        a = null; // a nu mai referă obiectul
        // b încă referă obiectul existent
        System.out.println(b.puncte); // 160
    }
}
```

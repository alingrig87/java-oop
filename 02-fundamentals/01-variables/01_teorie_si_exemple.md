# 🧩 Variabile — Teorie și Exemple

## 📘 Teorie

- Ce este o variabilă: o zonă de memorie etichetată printr-un nume, ce reține valori. Tipul stabilește ce valori poate conține și ce operații sunt permise.
- Tipuri primitive: `byte`, `short`, `int`, `long`, `float`, `double`, `char`, `boolean`.
- Tipuri de referință: toate clasele (ex.: `String`). `String` este imutabil.
- Literali:
  - Întregi: `42`, `1_000`, sufix `L` pentru `long`.
  - Zecimale: `3.14`, sufix `f` pentru `float`.
  - Caracter: `'A'`, escapări: `\n`, Unicode: `\u2764`.
  - String: "Ana".
- Inițializare: `int puncte = 100;` sau declarare apoi atribuiri.
- Constante: `final double VALOARE_PUNCT = 0.05;`
- Domeniu de vizibilitate (scope): definit în blocul `{}` în care este declarată.
- Conversii de tip:
  - Lărgire implicită: `int -> long -> float -> double`.
  - Îngustare explicită: `double -> int` cu `(int)` (trunchiere).
- Întregi vs. zecimale: `5/2 == 2`; `5/2.0 == 2.5`.
- Memorie: primitivele pe stivă, obiectele pe heap (prin referințe). Colectorul de gunoi eliberează memorie.
- Stil: `camelCase`, nume descriptive: `numeClient`, `puncteAcumulate`.

## 🔎 Exemple

### Exemplul 1: Card cafenea

```java
public class Ex1CardCafea {
    public static void main(String[] args) {
        String numeClient = "Ana";
        int puncte = 12;
        double valoarePunct = 0.3;
        boolean activ = true;
        System.out.println("Client: " + numeClient);
        System.out.println("Puncte: " + puncte);
        System.out.println("Valoare: " + (puncte * valoarePunct) + " lei");
        System.out.println("Activ: " + activ);
    }
}
```

### Exemplul 2: Card hotel

```java
public class Ex2CardHotel {
    public static void main(String[] args) {
        String hotel = "Sunrise";
        int nopti = 3;
        double punctePeNoapte = 25.5;
        double total = nopti * punctePeNoapte;
        System.out.println("Hotel: " + hotel + ", Total puncte: " + total);
    }
}
```

### Exemplul 3: Casting explicit

```java
public class Ex3Casting {
    public static void main(String[] args) {
        double d = 7.8;
        int i = (int) d; // 7
        System.out.println(i);
    }
}
```

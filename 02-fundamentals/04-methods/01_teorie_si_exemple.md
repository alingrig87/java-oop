# 🧮 Metode — Teorie și Exemple

## 📘 Teorie

- Semnătură metodă: `modificatori tipReturn nume(par1Tip par1, ...)`.
- `static` vs instanță: `static` aparține clasei; instanță cere obiect (`this`).
- Parametri: Java e „pass‑by‑value”. La obiecte se copiază referința; poți modifica starea, nu referința originală.
- `return`: obligatoriul pentru metode non-`void`; acoperă toate ramurile.
- Overloading: același nume, liste de parametri diferite (tip/număr/ordine).
- Varargs: `metoda(T... xs)` — convenabil pentru număr variabil de argumente.
- Metode pure vs cu efecte secundare: preferă pure pentru testabilitate.

## 🔎 Exemple

### Exemplul 1: metodă de calcul valoare

```java
public class ExMet1Valoare {
    static double calculeazaValoare(int puncte, double valoarePunct) {
        return puncte * valoarePunct;
    }
    public static void main(String[] args) {
        System.out.println(calculeazaValoare(120, 0.05));
    }
}
```

### Exemplul 2: metodă instanță cu `this`

```java
public class ExMet2Card {
    String nume;
    int puncte;
    ExMet2Card(String nume) { this.nume = nume; }
    void adauga(int p) { this.puncte += p; }
}
```

### Exemplul 3: overloading

```java
public class ExMet3Overload {
    static void printCard(String nume, int puncte) {
        System.out.println(nume + ": " + puncte + "p");
    }
    static void printCard(String nume, int puncte, double valPunct) {
        System.out.println(nume + ": " + puncte + "p (" + puncte * valPunct + " lei)");
    }
}
```

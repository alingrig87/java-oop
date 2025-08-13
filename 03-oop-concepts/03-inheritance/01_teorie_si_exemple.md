# 🌳 Moștenire — Teorie și Exemple

## 📘 Teorie

- Relația „is‑a”: o clasă copil extinde o clasă părinte în mod natural și stabil.
- `extends`: moștenește câmpuri/metode non-`private` și metode `public/protected`.
- `super(...)`: apel al constructorului părinte; trebuie să fie primul în constructor.
- `protected`: acces în același pachet și în subclase.
- `final` la clasă: nu poate fi extinsă; la metodă: nu poate fi suprascrisă.
- Overriding: aceeași semnătură; respectă regulile de acces și aruncare excepții; folosește `@Override`.
- Ordine inițializare: întâi părinte, apoi copil.
- Preferă compoziția când ierarhiile devin fragile („composition over inheritance”).

## 🔎 Exemple

### Exemplul 1: Bază + copil simplu

```java
class CardFidelitate {
    protected int puncte;
    public void adauga(int p) { puncte += p; }
}
class CardCinema extends CardFidelitate {
    String cinema;
    CardCinema(String cinema) { this.cinema = cinema; }
}
```

### Exemplul 2: Overriding + super

```java
class Card {
    String tip() { return "generic"; }
}
class CardHotel extends Card {
    @Override String tip() { return "hotel"; }
}
```

### Exemplul 3: Constructor copil cu `super`

```java
class Baza {
    int puncte;
    Baza(int p) { this.puncte = p; }
}
class Derivat extends Baza {
    Derivat(int p) { super(p); }
}
```

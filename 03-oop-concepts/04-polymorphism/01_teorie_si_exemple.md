# 🎭 Polimorfism — Teorie și Exemple

## 📘 Teorie

- Upcasting: referință de tip părinte poate indica un obiect copil.
- Downcasting: conversie spre tipul copil după verificare `instanceof`.
- Dynamic dispatch: metoda apelată la runtime e cea a tipului real al obiectului.
- Clasă abstractă: nu poate fi instanțiată; poate conține implementări parțiale.
- Interfață: definește contracte; poate avea `default`/`static` methods.
- `instanceof` (pattern matching modern): `if (c instanceof CardCinema cc) { cc.play(); }`.

## 🔎 Exemple

### Exemplul 1: Upcasting + overriding

```java
abstract class Card { abstract String tip(); }
class CardCinema extends Card { String tip() { return "cinema"; } }
class CardHotel extends Card { String tip() { return "hotel"; } }
public class Demo {
    public static void main(String[] args) {
        Card c = new CardCinema(); // upcast
        System.out.println(c.tip()); // "cinema" (dispatch dinamic)
    }
}
```

### Exemplul 2: Interfață + implementări

```java
interface Recompensabil { int calculeazaBonus(int puncte); }
class BonusStandard implements Recompensabil {
    public int calculeazaBonus(int puncte) { return puncte >= 100 ? 20 : 0; }
}
class BonusVip implements Recompensabil {
    public int calculeazaBonus(int puncte) { return (int)(puncte * 0.2); }
}
```

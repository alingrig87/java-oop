# 🔀 Structuri de Control — Teorie și Exemple

## 📘 Teorie

- Condiții în Java: strict `boolean`; nu există „truthy/falsy”.
- `if / else if / else`: evaluează prima condiție adevărată, restul se ignoră.
- `switch` pe `int`, `String`, `enum`: fiecare `case` necesită `break`, `default` opțional.
- Bucle:
  - `for (init; conditie; pas)` pentru iterații cu număr cunoscut.
  - `while (conditie)` pentru iterații condiționale.
  - `do { } while (conditie);` execută cel puțin o dată.
- Controlul buclei: `break` (iese), `continue` (sare la următoarea iterație).
- Evită bucle infinite; asigură-te că variabilele din condiție se modifică.

## 🔎 Exemple

### Exemplul 1: if/else — bonus după puncte

```java
public class ExCtrl1If {
    public static void main(String[] args) {
        int puncte = 120;
        if (puncte >= 100) {
            System.out.println("Bonus activat");
        } else {
            System.out.println("Fără bonus încă");
        }
    }
}
```

### Exemplul 2: switch — beneficii după tip card

```java
public class ExCtrl2Switch {
    public static void main(String[] args) {
        String tip = "cinema";
        switch (tip) {
            case "cinema":
                System.out.println("Reducere popcorn");
                break;
            case "hotel":
                System.out.println("Late checkout");
                break;
            default:
                System.out.println("Bonus standard");
        }
    }
}
```

### Exemplul 3: for — simulare acumulare pe zile

```java
public class ExCtrl3For {
    public static void main(String[] args) {
        int total = 0;
        for (int zi = 1; zi <= 7; zi++) {
            total += 10; // 10 puncte/zi
        }
        System.out.println("Total: " + total);
    }
}
```

### Exemplul 4: while — caută primul card activ

```java
public class ExCtrl4While {
    public static void main(String[] args) {
        boolean[] active = {false, false, true, true};
        int i = 0;
        while (i < active.length && !active[i]) {
            i++;
        }
        System.out.println("Primul activ la index: " + i);
    }
}
```

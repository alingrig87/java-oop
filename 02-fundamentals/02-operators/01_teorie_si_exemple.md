# ➕ Operatori — Teorie și Exemple

## 📘 Teorie

- Aritmetici: `+ - * / %`
- Unari: `+ - ++ -- !`
- Comparație: `== != > >= < <=` (rezultatul e `boolean`)
- Logici: `&& || !` (short-circuit)
- Atribuire compusă: `+= -= *= /= %=`
- Ternar: `cond ? a : b`
- Precedență: `()` > unari > `* / %` > `+ -` > comparații > `&&` > `||` > `?:` > atribuiri
- Pitfall: `double` are erori de reprezentare binară; pentru bani folosește `BigDecimal`.

## 🔎 Exemple

### Exemplul 1: Total puncte cu `+=`

```java
public class ExOp1TotalPuncte {
    public static void main(String[] args) {
        int puncte = 10;
        puncte += 5; // 15
        System.out.println(puncte);
    }
}
```

### Exemplul 2: Comparare pentru bonus

```java
public class ExOp2Comparare {
    public static void main(String[] args) {
        int puncte = 120;
        boolean eligibil = puncte >= 100;
        System.out.println("Eligibil: " + eligibil);
    }
}
```

### Exemplul 3: Ternar pentru mesaj

```java
public class ExOp3Ternar {
    public static void main(String[] args) {
        boolean activ = true;
        String mesaj = activ ? "Card activ" : "Card inactiv";
        System.out.println(mesaj);
    }
}
```

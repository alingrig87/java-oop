# 🧱 Proiectel — Simulare discounturi festival (operatori)

Obiectiv: Construiește un mini-program care calculează prețul final al biletelor la un festival în funcție de puncte, tipul biletului și starea cardului.

Cerințe:

1. Fișier/clasă `Proiectel_Operatori_Festival` cu `main`.
2. Variabile:
   - `String numeClient` (ex. "Radu Ionescu")
   - `String tipBilet` (valori: "standard", "vip", "student")
   - `double pretBaza` (ex. 200.0)
   - `int puncte` (ex. 180)
   - `boolean activ` (ex. true)
3. Reguli de discount (folosește operatori, fără `switch` sau colecții):
   - Dacă `!activ` => discount final = 0.
   - Altfel, `discountPuncte` = `puncte >= 200 ? 0.15 : (puncte >= 100 ? 0.1 : 0.0)`
   - `discountTip`:
     - `vip` => 0.2
     - `student` => 0.1
     - altfel => 0.0
   - `discountFinal` = `discountPuncte + discountTip`, plafonat la maxim 0.4.
   - `pretFinal = pretBaza * (1 - discountFinal)`.
4. Output exact (exemplu):

```
🎟️ FESTIVAL — CALCUL BILET
Client: Radu Ionescu | Tip: vip | Activ: true
Puncte: 180 | Discount puncte: 0.10 | Discount tip: 0.20
Discount final: 0.30
Preț final: 140.00 lei
```

5. Commit:

- `git add Proiectel_Operatori_Festival.java`
- `git commit -m "feat: add proiectel operatori - discounturi festival"`

# 🧱 Proiectel — Meniu interactiv cafenea (control flow)

Obiectiv: Creează un meniu textual care permite utilizatorului să aleagă opțiuni și simulează acumularea de puncte pe zile. Folosește `if/else`, `switch`, `for/while` și `break/continue` într-un singur program.

Cerințe:

1. Fișier/clasă `Proiectel_Control_MeniuCafea` cu `main`.
2. Fără biblioteci externe; input-ul poate fi simulat prin variabile (nu e obligatoriu să citești din consolă).
3. Variabile inițiale:
   - `int puncte = 0;`
   - `String tipCard = "standard"; // standard/vip`
4. Meniu (simulat prin `int optiune = 1;` apoi schimbă la 2, 3 etc. pentru a testa ramurile):
   - 1: "Setează tip card" (`switch` pe `tipCard` pentru mesaj dedicat)
   - 2: "Simulează acumulare 7 zile" (`for` adaugă 10 puncte/zi)
   - 3: "Verifică bonus" (`if` => dacă `puncte >= 50`, afișează "Bonus activat")
   - 4: "Ieșire" (afișează un mesaj și finalizează)
5. Output exemplu (doar idee, nu fix):

```
☕ MENIU CAFENEA
1) Setează tip card
2) Simulează 7 zile
3) Verifică bonus
4) Ieșire
Tip card: vip
-> Tip setat: vip (beneficii extinse)
-> Simulare: +70 puncte (total: 70)
-> Bonus: activat
La revedere!
```

6. Commit:

- `git add Proiectel_Control_MeniuCafea.java`
- `git commit -m "feat: add proiectel control - meniu interactiv cafenea"`

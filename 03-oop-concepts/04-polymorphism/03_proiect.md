# 🧱 Proiectel — Procesator recompense (polimorfism)

Obiectiv: Calculează bonusuri pentru carduri diferite folosind o interfață comună și dispatch dinamic.

De ce acest proiect:

- Arată puterea polimorfismului: un singur cod (procesator) operează pe tipuri diferite prin același contract.

Cerințe:

1. Interfață `Recompensabil { int calculeazaBonus(int puncte); }`.
2. Tipuri care implementează interfața:
   - `CardCinema` — bonus fix: `puncte >= 100 ? 20 : 0`
   - `CardHotel` — bonus procent: `10%` din `puncte`
   - `CardRetail` — bonus mixt: `5%` + `10` dacă `puncte >= 200`
3. Clasă `ProcesatorBonus` cu metodă:
   - `static int totalBonus(Recompensabil[] xs, int puncte)` care însumează bonusurile tuturor.
4. În `main` (`Proiectel_Polimorfism_Procesator`):
   - Creează un array cu toate tipurile, calculează totalul pentru `puncte = 240` și afișează EXACT:

```
Total bonus: 74
```

(Ex.: cinema=20, hotel=24, retail=30)

5. Commit:

- `git add Proiectel_Polimorfism_Procesator.java`
- `git commit -m "feat: add proiectel polimorfism - procesator recompense"`

Pași recomandați:

1. Definește interfața `Recompensabil`.
2. Implementează cele 3 tipuri concrete conform regulilor bonus.
3. Scrie `ProcesatorBonus.totalBonus` care parcurge array-ul și însumează rezultatele apelând `calculeazaBonus` pe fiecare element.
4. În `main`, creează array-ul, apelează metoda și afișează formatul EXACT.

Teste recomandate:

- `puncte` sub și peste pragurile folosite de implementări pentru a vedea variația rezultatului.

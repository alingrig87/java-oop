# 🧱 Proiectel — Procesator recompense (polimorfism)

Obiectiv: Calculează bonusuri pentru carduri diferite folosind o interfață comună și dispatch dinamic.

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

(Ex.: cinema=20, hotel=24, retail=30) 5. Commit:

- `git add Proiectel_Polimorfism_Procesator.java`
- `git commit -m "feat: add proiectel polimorfism - procesator recompense"`

# 🧱 Proiectel — Card fidelitate sigur pentru hotel (încapsulare)

Obiectiv: Implementează un card de fidelitate pentru hotel cu câmpuri private, validări în setteri și metode derivate de stare.

Cerințe:

1. Clasă `CardHotelSecure` cu câmpuri `private`:
   - `String nume;`
   - `int noptiAcumulate;`
   - `boolean activ;`
2. Constructor: `CardHotelSecure(String nume, int noptiAcumulate, boolean activ)` aplică normalizări:
   - `nume`: `trim()`; dacă null/blank => `"Anonim"`
   - `noptiAcumulate`: clamp `[0, 1000]`
3. Setteri validați:
   - `setNume(String n)` — ca la constructor
   - `setNoptiAcumulate(int n)` — clamp `[0, 1000]`
   - `setActiv(boolean a)`
4. Getteri: pentru toate câmpurile + `boolean isVip()` returnează `noptiAcumulate >= 50`.
5. Metodă de afișare:

```
👤 Nume: <nume> | 🛏️ Nopți: <noptiAcumulate> | 🔓 Activ: <activ>
VIP? <true/false>
```

6. În `main` (clasa `Proiectel_Encapsulare_CardHotel`), demonstrează 3 seturi de modificări și afișări.
7. Commit:

- `git add Proiectel_Encapsulare_CardHotel.java`
- `git commit -m "feat: add proiectel incapsulare - card hotel secure"`

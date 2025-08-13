# 🧱 Proiectel — Catalog carduri turism (moștenire)

Obiectiv: Realizează o mini-aplicație cu o clasă de bază și mai multe subclase care modelează carduri pentru turism.

Cerințe:

1. Bază `CardFidelitate` (ca la ex. 31) cu `protected int puncte`, `adauga/scade` și `String descriere()` generic.
2. Subclase:
   - `CardHotel` (câmp `hotel`), `CardCinema` (câmp `cinema`), `CardRetail` (câmp `magazin`).
   - Fiecare suprascrie `descriere()` pentru a include specificul.
3. În `main` (`Proiectel_Mostenire_CatalogTurism`):
   - Creează câte o instanță din fiecare, adaugă puncte diferit, pune-le într-un array `CardFidelitate[]`.
   - Parcurge și printează `descriere()` și `Puncte: <puncte>`.
4. Commit:

- `git add Proiectel_Mostenire_CatalogTurism.java`
- `git commit -m "feat: add proiectel mostenire - catalog carduri turism"`

# 🧱 Proiectel — Catalog carduri turism (moștenire)

Obiectiv: Realizează o mini-aplicație cu o clasă de bază și mai multe subclase care modelează carduri pentru turism.

De ce acest proiect:

- Exersezi proiectarea unei ierarhii și beneficiile moștenirii: reutilizare de cod, specializare prin override.

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

Pași recomandați:

1. Definește baza `CardFidelitate` cu câmp `protected` și metode comune.
2. Creează subclasele și suprascrie `descriere()` pentru fiecare.
3. În `main`, construiește array-ul de bază și adaugă instanțe diverse.
4. Parcurge cu `for` și afișează `descriere()` + puncte pentru fiecare.

Acceptance criteria:

- Fiecare subclasă adaugă câte un câmp specific și `descriere()` personalizată.
- Output-ul pentru toate elementele din array este coerent și în format clar.

Greșeli frecvente:

- Lipsa `@Override` => metoda nu este recunoscută ca suprascrisă (ai grijă la semnătura exactă).

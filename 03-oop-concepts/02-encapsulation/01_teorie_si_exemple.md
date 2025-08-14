# 🔒 Încapsulare — Teorie și Exemple

## 📘 Teorie

- **Încapsulare**: ascunderea stării interne și expunerea unui API sigur.
  - Câmpuri `private`, acces prin `getteri/setteri` sau metode dedicate.
  - Menține „invariantele” clasei (reguli care trebuie să fie mereu adevărate).
- **Modificatori de acces** (pe scurt):
  - `private` — acces doar din aceeași clasă (implicit pentru datele interne).
  - „package-private” — fără cuvânt cheie; acces în același pachet.
  - `protected` — ca package + subclase.
  - `public` — acces de oriunde (pentru API-ul clasei).
- **Constructori validați**: normalizează valorile la creare; evită stări invalide.
- **Setteri validați**: aplică aceleași reguli ca în constructor (nu rupe invarianta).
- **Imutabilitate**: toate câmpurile `final`, fără setteri. Siguranță și simplitate.
- **Câmpuri mutabile** (ex.: `List`, `Date`): folosește „defensive copies” la intrare/ieșire.
- **Afișare/toString**: nu expune internals sensibile; păstrează format clar.

Notă: în lecția precedentă câmpurile au fost `public` pentru simplitate. De acum, folosim `private` + API controlat.

## 🔎 Exemple

### Exemplul 1: Câmpuri private + getteri/setteri

```java
public class ExEnc1BasicGetSet {
    public static class CardCinemaSecure {
        private String numeClient;
        private int puncte;

        public String getNumeClient() {
            return numeClient;
        }

        public void setNumeClient(String numeClient) {
            this.numeClient = numeClient;
        }

        public int getPuncte() {
            return puncte;
        }

        public void setPuncte(int puncte) {
            this.puncte = puncte;
        }
    }

    public static void main(String[] args) {
        CardCinemaSecure c = new CardCinemaSecure();
        c.setNumeClient("Ana");
        c.setPuncte(120);
        System.out.println(c.getNumeClient() + " | " + c.getPuncte() + "p");
    }
}
```

### Exemplul 2: Validare/normalizare în constructor și setteri

```java
public class ExEnc2Validari {
    public static class CardHotelSecure {
        private String nume;         // niciodată null/blank
        private int noptiAcumulate;  // interval 0..1000
        private boolean activ;

        public CardHotelSecure(String nume, int noptiAcumulate, boolean activ) {
            setNume(nume);
            setNoptiAcumulate(noptiAcumulate);
            setActiv(activ);
        }

        public String getNume() { return nume; }
        public int getNoptiAcumulate() { return noptiAcumulate; }
        public boolean isActiv() { return activ; }

        public void setNume(String n) {
            if (n == null) { n = ""; }
            n = n.trim();
            this.nume = n.isEmpty() ? "Anonim" : n;
        }

        public void setNoptiAcumulate(int n) {
            if (n < 0) n = 0;
            if (n > 1000) n = 1000;
            this.noptiAcumulate = n;
        }

        public void setActiv(boolean a) {
            this.activ = a;
        }

        public boolean isVip() {
            return this.noptiAcumulate >= 50;
        }

        public void afisare() {
            System.out.println("👤 Nume: " + nume + " | 🛏️ Nopți: " + noptiAcumulate + " | 🔓 Activ: " + activ);
            System.out.println("VIP? " + isVip());
        }
    }

    public static void main(String[] args) {
        CardHotelSecure c = new CardHotelSecure("  ", -10, true);
        c.afisare();
        c.setNume("  Maria ");
        c.setNoptiAcumulate(1200);
        c.afisare();
    }
}
```

### Exemplul 3: Clasă imutabilă (fără setteri, câmpuri final)

```java
public class ExEnc3Immutable {
    public static class CardNetflixImmutable {
        private final String numeProfil;
        private final int minuteVizionate;

        public CardNetflixImmutable(String numeProfil, int minuteVizionate) {
            this.numeProfil = (numeProfil == null || numeProfil.trim().isEmpty()) ? "Profil" : numeProfil.trim();
            this.minuteVizionate = Math.max(0, minuteVizionate);
        }

        public String getNumeProfil() { return numeProfil; }
        public int getMinuteVizionate() { return minuteVizionate; }

        // "cuX" — creează un nou obiect cu modificarea dorită
        public CardNetflixImmutable cuMinuteVizionate(int minuteNoi) {
            return new CardNetflixImmutable(this.numeProfil, minuteNoi);
        }
    }

    public static void main(String[] args) {
        CardNetflixImmutable p1 = new CardNetflixImmutable("Kids", 90);
        CardNetflixImmutable p2 = p1.cuMinuteVizionate(120); // p1 rămâne neschimbat
        System.out.println(p1.getMinuteVizionate()); // 90
        System.out.println(p2.getMinuteVizionate()); // 120
    }
}
```

### Exemplul 4: Defensive copy pentru câmpuri mutabile

```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

public class ExEnc4DefensiveCopy {
    public static class CardCafeneaPerks {
        private final String nume;
        private final List<String> beneficii; // listă internă protejată

        public CardCafeneaPerks(String nume, List<String> beneficii) {
            this.nume = (nume == null || nume.trim().isEmpty()) ? "Anonim" : nume.trim();
            // Copie la intrare
            this.beneficii = new ArrayList<>(beneficii == null ? List.of() : beneficii);
        }

        public String getNume() { return nume; }

        public List<String> getBeneficii() {
            // Copie imuabilă la ieșire
            return Collections.unmodifiableList(new ArrayList<>(beneficii));
        }
    }

    public static void main(String[] args) {
        List<String> initial = new ArrayList<>();
        initial.add("1x cafea gratis");
        CardCafeneaPerks c = new CardCafeneaPerks("Ana", initial);

        // Modific lista originală — obiectul rămâne protejat
        initial.add("10% reducere");

        // Încerc să modific lista returnată — aruncă excepție dacă încercăm să facem add
        List<String> laExterior = c.getBeneficii();
        System.out.println(laExterior); // [1x cafea gratis]
    }
}
```

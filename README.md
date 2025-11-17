# Flask-prosjekt -- Dokumentasjon

## 1. Forside

**SovSmart:**\
**Arda:**\
**IMI:**\
**17.11.2025:**

**Kort beskrivelse av prosjektet:**\
Applikasjonen vil hjelpe og assistere med søvn for hvilke som helst målgruppe med problemer. Siden dette er et universell problem tenker jeg at vi burde derimot løse problemet sammen med eget tempo. Applikasjonen utfører kalkulasjoner og koder som vil best passe deltakere.



## 2. Systembeskrivelse

**Formål med applikasjonen:**\
Jeg ønsker å løse et helseproblem som er universell for veldig mange folk. Omtrent mere enn en tredje-del av voksne rapporterer at to-tredjedel har søvn forstyrrelse og problemer. Jeg selv har opplevd slike problemer og vet mange ungdommer og voksne føler det samme. 


**Brukerflyt:**\
*Beskriv hvordan brukeren bruker løsningen -- fra startside til lagring
av data.*

Før testen starter så må deltakeren registrere med Navn og Alder. Så skal applikasjonen tilpasse søvn anbefalingne så godt det kan.


**Teknologier brukt:**

-   Python / Flask\
-   MariaDB\
-   HTML / CSS / JS\
-   


## 3. Server-, infrastruktur- og nettverksoppsett

### Servermiljø

*F.eks.: Ubuntu VM, Docker, fysisk server.*

### Nettverksoppsett

-   Nettverksdiagram
-   IP-adresser\
-   Porter\
-   Brannmurregler

Eksempel:

    Klient → Waitress → MariaDB

### Tjenestekonfigurasjon

-   systemctl / Supervisor\
-   Filrettigheter\
-   Miljøvariabler

------------------------------------------------------------------------

## 4. Prosjektstyring -- GitHub Projects (Kanban)

-   To Do / In Progress / Done\
-   Issues\
-   Skjermbilde (valgfritt)

Refleksjon: Hvordan hjalp Kanban arbeidet?

------------------------------------------------------------------------

## 5. Databasebeskrivelse

**Databasenavn:**

**Tabeller:**\
\| Tabell \| Felt \| Datatype \| Beskrivelse \|
\|--------\|-------\|-----------\|--------------\| \| customers \| id \|
INT \| Primærnøkkel \| \| customers \| name \| VARCHAR(255) \| Navn \|
\| customers \| address \| VARCHAR(255) \| Adresse \|

**SQL-eksempel:**

``` sql
CREATE TABLE customers (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(255),
  address VARCHAR(255)
);
```

------------------------------------------------------------------------

## 6. Programstruktur

    projectnavn/
     ├── app.py
     ├── templates/
     ├── static/
     └── .env

Databasestrøm:

    HTML → Flask → MariaDB → Flask → HTML-tabell

------------------------------------------------------------------------

## 7. Kodeforklaring

Forklar ruter og funksjoner (kort).

------------------------------------------------------------------------

## 8. Sikkerhet og pålitelighet

-   .env\
-   Miljøvariabler\
-   Parameteriserte spørringer\
-   Validering\
-   Feilhåndtering

------------------------------------------------------------------------

## 9. Feilsøking og testing

-   Typiske feil\
-   Hvordan du løste dem\
-   Testmetoder

------------------------------------------------------------------------

## 10. Konklusjon og refleksjon

-   Hva lærte du?\
-   Hva fungerte bra?\
-   Hva ville du gjort annerledes?\
-   Hva var utfordrende?

------------------------------------------------------------------------

## 11. Kildeliste

-   w3schools\
-   flask.palletsprojects.com

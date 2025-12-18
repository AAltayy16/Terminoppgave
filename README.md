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
Før testen starter så må deltakeren registrere med Navn og Alder. Så skal applikasjonen tilpasse søvn anbefalingne så godt det kan.


**Teknologier brukt:**

-   Python / Flask\
-   MariaDB\
-   HTML / CSS / JS\



## 3. Server-, infrastruktur- og nettverksoppsett

### Servermiljø

Ubuntu

### Nettverksoppsett

-   Nettverksdiagram
-   IP-adresser\
-   Porter\
-   Brannmurregler


## 4. Prosjektstyring -- GitHub Projects (Kanban)

-   To Do / In Progress / Done\

Refleksjon: Hvordan hjalp Kanban arbeidet?

Det hjalp meg ha en liten oversikt over planen min for prosjektet var ikke det beste men hadde selvagt hjulpet.

## 5. Databasebeskrivelse

**Databasenavn:**

**Tabeller:**\
\| Tabell \| Felt \| Datatype \| Beskrivelse \|
\|--------\|-------\|-----------\|--------------\| \| customers \| id \|
INT \| Primærnøkkel \| \| customers \| name \| VARCHAR(255) \| Navn \|
\| customers \| address \| VARCHAR(255) \| Adresse \|


con = get_db()
        cur = con.cursor()
        cur.execute(
            "INSERT INTO sleep_data (user_id, start_time, end_time, hours) VALUES (%s, %s, %s, %s)",
            (user_id, start_time_str, end_time_str, hours)


 6. Programstruktur

    SovSmart/
     ├── app.py
     ├── templates/
     ├── sleep.html
     └── register.html

Databasestrøm:

    HTML → Flask → MariaDB → Flask → HTML-tabell


## 7. Kodeforklaring

Forklar ruter og funksjoner (kort).

Programmet starter en Flask-app. get_db() kobler til databasen. sleep() viser en nettside der brukeren kan legge inn søvntider. calculate_sleep() tar imot tidene, regner ut hvor mange timer brukeren har sovet (og håndterer hvis man sover over midnatt), lagrer dataene i databasen og viser resultatet på en ny side.

 8. Sikkerhet og pålitelighet

Koden bruker parameteriserte spørringer for å hindre SQL-injection og enkel validering for å håndtere søvn over midnatt. .env, miljøvariabler og feilhåndtering er ikke implementert i denne koden.

## 9. Feilsøking og testing

-   Typiske feil\
-   Hvordan du løste dem\
-   Testmetoder

  Jeg trengte mere oversikt over planen, hadde en god del feil med å føre in data fra registreringen, det førte ikke inn noe data til databasen. Metoden jeg brukte var å gå tilbake til kode kilden fra forrige oppgaver og lese hva de kodene gjør og bruke dem. Fikk også litt hjelp fra w3schools og noen ganger så spurte jeg lærer eller kunstig intelligens om hva som er feil i koden jeg ikke klarte å se.



## 10. Konklusjon og refleksjon

-   Hva lærte du?\
-   Hva fungerte bra?\
-   Hva ville du gjort annerledes?\
-   Hva var utfordrende?

Jeg har lært svært mye gjennom dette arbeidet, men ser samtidig at jeg fortsatt trenger mer øvelse for å få bedre forståelse og flyt i koden. Jeg har fått innsikt i hvor viktig en database er for å kunne lagre og håndtere brukerdata på en nettside, noe jeg opplevde som både nyttig og lærerikt. Det som fungerte godt var oppsettet av nettsiden og databasen hver for seg, men det var mer utfordrende å skrive all koden som skulle til for å koble dem sammen på en riktig måte. Jeg testet og eksperimenterte med ulike løsninger for å se hvordan koden reagerte, og prøvde forskjellige tilnærminger for å forstå sammenhengen mellom de ulike delene av programmet. Det mest krevende var å få alle komponentene til å fungere samlet, slik at koden faktisk kjørte som den skulle og data ble sendt, lagret og brukt korrekt. Samlet sett har dette gitt meg verdifull erfaring og en bedre forståelse av hvordan backend, database og nettside samarbeider.

## 11. Kildeliste


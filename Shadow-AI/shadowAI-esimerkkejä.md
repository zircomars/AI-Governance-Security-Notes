<img width="466" height="19" alt="image" src="https://github.com/user-attachments/assets/580cb48e-3926-4381-b820-5a3984a7a188" /># Shadow AI – käytännön esimerkit ja tietoturvapolut

Tässä osiossa esitetään kokonaisia esimerkkejä siitä, miten shadow AI ‑tilanteet syntyvät, miten tietovuoto tapahtuu teknisesti ja milloin tekoälyn käyttö on turvallista. Kaikki esimerkit on säilytetty alkuperäisessä muodossaan ja esitetään passiivisesti.

---

## 1. Pieni esimerkki: Onko “Hello World” ‑koodin lähettäminen vuotamista?

Ei. Tavallinen Hello World ‑koodi ei sisällä mitään luottamuksellista, joten sitä ei voida pitää tietovuotona.

Se on täysin harmiton esimerkki, koska:

- se ei sisällä yrityksen omaa koodia  
- se ei sisällä henkilötietoja  
- se ei sisällä API‑avaimia, konfiguraatioita tai sisäisiä rakenteita  
- se on yleisesti tunnettu ja kaikkialla käytetty esimerkki  

Eli ei synny vuotoa, eikä siitä muodostu shadow AI ‑tilannetta.

### Minne se menisi?

Kun Hello World ‑koodi lähetetään tekoälylle:

- se käsitellään chatissa  
- sitä ei lähetetä ulkopuoliseen palveluun käyttäjän toimesta  
- se ei sisällä mitään, mikä voisi vaarantaa käyttäjää tai organisaatiota  

Eli riskiä ei synny, koska sisältö on täysin julkista ja vaaratonta.

## Milloin koodin lähettäminen olisi vuotoa?

Vain jos koodi sisältää jotain seuraavista:

- yrityksen sisäistä logiikkaa  
- integraatioita  
- API‑avaimia  
- konfiguraatioita  
- tietokantarakenteita  
- asiakkaiden dataa  
- sisäisiä URL‑osoitteita  
- liiketoimintakriittistä logiikkaa  

Silloin kyseessä olisi tietovuoto ja shadow AI ‑tilanne.

---

## 2. esimerkki: Miten tietovuoto tapahtuisi tekoälyn kautta?

Alla kuvataan tekninen “juna‑rata” eli polku vaihe vaiheelta.

### 🔵 1. Tekoälypalvelun avaaminen

- Palvelu voi olla ChatGPT, Copilot, VS Code ‑laajennus, selainpohjainen botti tai mobiilisovellus.  
- Kirjautuminen tehdään henkilökohtaisella tilillä.  
→ IT ei näe mitään.

### 🔵 2. Datan syöttäminen palveluun

Esimerkiksi:

- 100 nimeä  
- osoitteita  
- asiakkuustietoja  
- sisäisiä muistiinpanoja  

→ Data lähetetään palveluntarjoajan palvelimille.

### 🔵 3. Datan kulku internetin yli

- Salaus suojaa siirron, mutta data poistuu organisaation hallinnasta.  
- IT ei voi enää valvoa tapahtumia.

### 🔵 4. Palveluntarjoajan vastaanotto

Data voi päätyä:

- lokitiedostoihin  
- mallin optimointiin  
- kehittäjien tarkasteltavaksi  
- diagnostiikkajärjestelmiin  

→ Tässä vaiheessa tapahtuu varsinainen tietovuoto.

### 🔵 5. Datan säilytys

Retention‑politiikka voi olla:

- 30 päivää  
- 90 päivää  
- 1 vuosi  
- “kunnes poistetaan”  
- “ei poisteta koskaan”  

Käyttäjä ei voi tarkistaa tätä.

### 🔵 6. Datan päätyminen mallin koulutukseen

Joissain palveluissa syötteitä käytetään mallien parantamiseen:

- data voi päätyä mallin painoihin  
- sitä ei voi poistaa  
- sitä ei voi yksilöidä  
- sitä ei voi jäljittää  

→ GDPR:n “oikeus tulla unohdetuksi” ei toteudu.

### 🔵 7. Epäsuora vuoto

Malli voi:

- tuottaa samankaltaisia nimiä  
- paljastaa rakenteita  
- antaa osia tekstistä  

Tämä on harvinaista, mutta dokumentoitu riski.

### 🔵 8. Organisaatiolla ei ole näkyvyyttä

Koska:

- ei ole lokitusta  
- ei ole valvontaa  
- ei ole näkyvyyttä  
- ei ole sopimusta  

→ Tämä on shadow AI.

### 🟦 Koskeeko tämä kaikkia tiedostoja?

Kyllä. Kaikki tiedostotyypit voivat vuotaa:

- PDF  
- TXT  
- DOCX  
- Excel  
- Kuvakaappaukset  
- Kooditiedostot  
- Konfiguraatiot  
- JSON / YAML  
- Logit  
- Sopimukset  

Tiedostomuoto ei suojaa mitään.

### 🟦 Entä allekirjoitetut tai leimatut tiedostot?

Ei vaikuta mitään.

- Allekirjoitus ei estä vuotoa  
- Leima ei estä vuotoa  
- PDF‑suojaus ei estä vuotoa  

Tekoäly näkee kaiken, minkä käyttäjä näkee.

---

## 3. esimerkki: Työsuhteen päättyminen ja koodin vieminen

### 🟦 Esimerkki

Henkilö irtisanotaan ja ottaa mukaansa:

- muutaman koodin  
- testejä  
- API‑avaimia  
- tokeneita  

Hän jatkaa niiden kehittämistä harrastuksena.

→ Tämä ei ole normaalia.  
→ Tämä on shadow AI + tietovuoto + sopimusrikkomus.

### 🟦 Miksi tämä ei ole normaalia?

Työsuhteen päättyessä kaikki seuraava on työnantajan omaisuutta:

- koodi  
- API‑avaimet  
- tokenit  
- konfiguraatiot  
- testit  
- skriptit  
- dokumentit  
- projektit  

Niitä ei saa käyttää henkilökohtaisesti.

### 🟥 Miksi tämä on shadow AI?

Koska:

- työdataa käytetään henkilökohtaisessa ympäristössä  
- työprojekteja jatketaan ilman lupaa  
- työdataa syötetään henkilökohtaiseen AI‑palveluun  
- API‑avaimia ja tokeneita käytetään luvatta  

### 🟦 Miksi tämä on tietoturvariski?

Koska:

- API‑avaimet voivat antaa pääsyn järjestelmiin  
- tokenit voivat avata palveluita  
- koodi voi paljastaa sisäisiä rakenteita  
- testit voivat sisältää luottamuksellista logiikkaa  
- AI‑palvelu voi tallentaa syötteitä  

### 🟦 Mikä olisi normaalia?

Normaalia on:

- käyttää AI:ta omiin projekteihin  
- käyttää AI:ta omalla koodilla  
- käyttää AI:ta harrastuksiin  
- käyttää AI:ta opiskeluun  

Mutta ei koskaan työperäisellä datalla työsuhteen jälkeen.

### 🟦 Yksi lause, joka kiteyttää kaiken

Jos koodi, API-avaimet tai tokenit ovat peräisin työpaikalta, niitä ei saa käyttää henkilökohtaisissa projekteissa eikä syöttää tekoälyyn — se on shadow AI ja tietovuoto. Työasiat pysyvät työssä. Jos haluaa käyttää niitä henkilökohtaisesti, siitä joutuu maksamaan itse ja varmistamaan, että käyttö on sallittua. Tämä koskee yleensä harrastelijoita tai siviilissä testejä tekeviä henkilöitä.

---

## 🔵 Turvallisin tapa käyttää tekoälyä

### 🟩 Turvallisin = yrityksen hallittu AI‑ympäristö

Tämä tarkoittaa:
- yritystili  
- yrityksen lisenssit  
- hyväksytyt AI‑palvelut  
- hallitut laitteet  
- tietoturvapolitiikat  
- DLP / CASB / SSO / auditointi  

Kun nämä ovat käytössä: 
- Data ei vuoda
- Data ei päädy mallin koulutukseen
- Data pysyy EU:ssa (jos määritelty)
- Käyttö on valvottua

## 🟥 Epäturvallisin = henkilökohtaiset ilmaisversiot

Esim.:

- ChatGPT Free  
- Gemini Free  
- Copilot Free  
- DuckDuck AI Free  
- Discord‑botit  
- WhatsApp‑botit  

Näissä:

- ei ole sopimuksia  
- ei ole DPA:ta  
- dataa voidaan käyttää mallin koulutukseen  
- data voi jäädä palveluun  

→ Suurin shadow AI ‑lähde.

---

## 🔵 Turvalliset käytännöt eri käyttäjäryhmille

Tästä käytöstä on erilaisia työtehtävän tyyppejä, että ei ole oikeeta tai väärää titteliä.

### 🟩 Tavallinen käyttäjä

- käytetään yrityksen AI:ta työasioihin  
- henkilökohtaista AI:ta käytetään vain omiin projekteihin  
- työdataa ei syötetä henkilökohtaiseen AI:hin  

### 🟦 Testaaja

- testataan vain testidatalla  
- ei käytetä oikeaa asiakasdataa  
- käytetään hyväksyttyjä ympäristöjä  

### 🟧 Frontend / backend ‑devaaja

- käytetään yrityksen Copilotia tai Azure OpenAI:ta  
- tuotantokoodia ei syötetä henkilökohtaiseen AI:hin  
- API‑avaimia ja konfiguraatioita ei syötetä  

### 🟪 DevOps / infra / automaatio / robotiikka

- käytetään vain hallittuja AI‑ympäristöjä  
- CI/CD‑konfiguraatioita ei syötetä henkilökohtaiseen AI:hin  
- lokitietoja ei analysoida henkilökohtaisella AI:lla  

### 🟫 Specialist / analyytikko / konsultti

- asiakkaan dataa käytetään vain asiakkaan ympäristössä  
- työnantajan dataa käytetään vain työnantajan ympäristössä  
- tilejä ei sekoiteta  

---

## 🔵 Kolme sääntöä kaikille

Tämä sääntö on koskien miten käyttää tekoälyn kanssa ettei se tieto vuoda ulos.

- 🟩 Sääntö 1: “Työdata → työtili” - (mikäli data liittyy: asiakkaaseen/työnantaja/sisäisen järjestelmiin/koodiin/sopimuksiin/tiketteihin)
- 🟦 Sääntö 2: “Henkilökohtainen data → henkilökohtainen tili” - (Harrasteprojektit, opiskelujutut, omat ideat → henkilökohtainen AI)
- 🟥 Sääntö 3: “Älä syötä tekoälyyn mitään, mitä et saisi lähettää ulkopuoliselle sähköpostilla” 

---

## 🔵 Voiko tekoälyn käyttö vuotaa tietoja, jos henkilö ei ole työssä?

### 🟩 Vain, jos syötetään arkaluonteista dataa.

Tekoäly ei “vuoda itsestään”. Vuoto syntyy vain, jos käyttäjä itse syöttää: 

- omia ideoita  
- omia projekteja  
- omia tekstejä  
- julkista tietoa  
- yleisiä kysymyksiä  
- harrastekoodia  

> Vuotoriski = 0 %
> Jos henkilö ei syötä mitään tällaista → vuotoriski on käytännössä 0 %.


**Paitsi**, jos syötetään:

- henkilötietoja  
- yrityksen dataa  
- asiakkaiden tietoja  
- sisäisiä dokumentteja  
- työperäistä koodia  
- sopimuksia  
- lokitietoja  
- konfiguraatioita  

> Vuotoriski = 100 %
> Vuoto tapahtuu välittömästi, koska data lähtee palveluntarjoajalle.

**Lyhyesti sanottuna:** - Jos henkilö ei ole työssä, shadow AI -vuotoa ei synny itsestään. Käytännössä vuoto tapahtuu vain, jos käyttäjä syöttää arkaluonteista tai salassapidettävää tietoa, kuten henkilö- tai muiden tietoja, sopimuksia tai työn peräisiä koodinpätkiä (vanhoja tai uusia) — tämä on riskitekijä. Sen sijaan omien ideoiden, tekstien, harrastekoodin tai matemaattisten laskujen syöttäminen ei aiheuta vuotoa, eli näissä tapauksissa vuotoriski on käytännössä 0 %.
- Toinen esim. lyhyempi vers: Tekoälyn käyttö ei itsessään aiheuta vuotoa — vuoto syntyy vain, jos käyttäjä syöttää tekoälyyn sellaista dataa, jota ei olisi saanut jakaa alun perinkään.

---

# 🔵 Turvallisin tapa käyttää tekoälyä (lyhyesti ja lunttilappuna)

## 🟩 1) Älä syötä tekoälyyn mitään arkaluonteista  
Tämä koskee kaikkia — työssä tai ei.  
Älä koskaan syötä:  
- henkilötietoja  
- yrityksen tietoja  
- asiakasdataa  
- sopimuksia  
- sisäisiä dokumentteja  
- lähdekoodia, joka ei ole omaa  
- API‑avaimia  
- salasanoja  
- subscription ID:tä  
- konfiguraatioita  
- lokitietoja  

Jos et syötä arkaluonteista dataa → ei ole vuotoriskiä.  

---

## 🟦 2) Käytä esimerkkejä, ei oikeaa dataa  
Jos haluat kysyä tekoälyltä jotain teknistä, mutta et voi näyttää oikeaa dataa, tee näin:  

### 🟩 Turvallinen tapa:  
- Muuta nimet  
- Muuta numerot  
- Muuta rakenteet  
- Käytä “dummy dataa”  
- Käytä pseudokoodia  
- Käytä kuvitteellisia arvoja  

**Esimerkki:**  
Ei näin:  
“Minulla on asiakkaan sopimus, jossa lukee että maksamme 12 500 € kuussa…”  
Vaan näin:  
“Minulla on esimerkkisopimus, jossa on kuukausimaksu X. Miten laskisin vuosikustannuksen?”  

---

## 🟧 3) Jos haluat käyttää numeroita, tee ne epätarkoiksi  
Voit käyttää:  
- pyöristettyjä summia  
- karkeita arvioita  
- satunnaisia lukuja  
- esimerkkilukuja  

**Esimerkki:**  
“Jos minulla olisi vaikka 10 000 € budjetti, miten jakaisin sen neljään osaan?”  
Ei mitään riskiä.  

---

## 🟨 4) Jos kirjoitat kuvauksen tekstinä (txt), tee se neutraaliksi  
Tämä on hyvä tapa, jos haluat selittää ongelman ilman oikeaa dataa.  

**Esimerkki:**  
Sen sijaan että kirjoitat:  
“Tässä on asiakkaan lokitiedosto…”  
Kirjoita:  
“Tässä on esimerkkiloki, joka muistuttaa oikeaa tilannetta. Miten analysoisin tämän?”  

---

## 🟫 5) Sama sääntö pätee kaikkiin käyttäjiin  
Ei väliä oletko:  
- töissä  
- työtön  
- opiskelija  
- harrastaja  
- dev  
- testaaja  
- infra‑asiantuntija  
- palveluhenkilö  
- konsultti  
- tavallinen käyttäjä  

> Turvallisin tapa on aina sama: **Älä syötä tekoälyyn mitään, mitä et saisi lähettää ulkopuoliselle sähköpostilla.**
> Käytä tekoälyä vain esimerkeillä, pseudodatalle ja yleisillä kuvauksilla — älä koskaan syötä oikeita henkilötietoja, yritystietoja tai salaisuuksia.

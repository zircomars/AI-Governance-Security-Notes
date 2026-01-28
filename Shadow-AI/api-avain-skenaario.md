# Shadow AI – mitä tapahtuu, jos API-avain syötetään tekoälylle?

Tämä osio kuvaa simuloidusti, mitä voisi tapahtua, jos toimiva API-avain (esim. `1234-ABCD-SECRET`) syötetään ulkopuoliseen AI-palveluun. Kyseessä ei ole tekninen analyysi, vaan hahmottava riskipolku, joka auttaa ymmärtämään mahdollisia seurauksia.

---

## 1) Syöttöhetki

Käyttäjä liittää API-avaimen AI-chattiin, esimerkiksi:

```
API_KEY = "1234-ABCD-SECRET"
```
→ Tässä vaiheessa data poistuu käyttäjän hallinnasta.

## 2) Mihin API-avain voi päätyä?

Jos API-avain syötetään väärään paikkaan, se voi päätyä esimerkiksi:

**A) Palveluntarjoajan sisäisiin järjestelmiin**

- lokitietoihin  
- mallin sisäiseen kontekstiin  
- telemetriadataan  

**B) Kolmannen osapuolen palvelimille**

- selainlaajennusten kautta  
- automaattisten sovellusten kautta  
- epäluotettavien verkkosivujen kautta  

→ Tällöin avain voi päätyä suoraan hyökkääjän haltuun.

**C) Julkisiin tietokantoihin**

- GitHub  
- Pastebin  
- muut julkiset alustat  

→ Bottiverkot voivat kerätä avaimen minuuteissa.

**D) Skannereihin ja hakukoneisiin**

- Pastebin-skannerit  
- GitHub-skannerit  
- tekoälypohjaiset secret scanners  
- Shodan ja vastaavat työkalut  

---

## 3) Miten hyökkääjä voi tunnistaa avaimen?

Usein avaimen muoto paljastaa sen alkuperän:

- AWS: `AKIA...`  
- Stripe: `sk_live...`  
- OpenAI: `sk-...`  
- Google: `AIza...`  
- GitHub: `ghp_...`  

→ Palvelu voidaan tunnistaa pelkästä rakenteesta.  
→ Avainta voidaan testata automaattisesti.  
→ Avainta voidaan käyttää väärin, jos se on voimassa.

---

## 4) Mitä hyökkääjä voi tehdä vuotaneella avaimella?

Riippuen palvelusta, hyökkääjä voi:

**A) Laskuttaa käyttäjää**

- pilvipalveluissa (AWS, Azure, Google Cloud)  
- aiheuttaa tuhansien eurojen kustannuksia  

**B) Ladata tai muokata dataa**

- ERP-, CRM- tai automaatiojärjestelmissä  

**C) Käyttää palvelua väärin**

- lähettää sähköpostia  
- tehdä API-kutsuja  
- käyttää AI-resursseja  

**D) Varastaa dataa**

- päästä tietokantaan  
- lukea integraatioita  

---

## 5) Voiko avaimen sijaintia jäljittää?

Ei täysin.  
Kun avain on vuotanut, se voi olla:

- lokitiedoissa  
- mallin sisäisessä järjestelmässä  
- palveluntarjoajan infrastruktuurissa  
- julkisessa tietokannassa  
- bottiverkossa  
- hakukoneessa  
- Telegram-kanavassa  
- pimeässä verkossa  

→ Ainoa oikea toimenpide on poistaa avain ja luoda uusi.

---

## 6) Miten Shodan liittyy tähän?

Shodan ei kerää API-avaimia, mutta se:

- etsii avoimia palveluita  
- etsii avoimia portteja  
- etsii vanhoja konfiguraatioita  
- etsii IoT-laitteita  
- etsii haavoittuvuuksia  

→ Jos API-avain liittyy palveluun, joka on avoinna internetissä, Shodan voi paljastaa palvelun, ja hyökkääjä voi testata avaimen.

---

## 7) Mitä järjestelmänvalvoja voi tehdä?

**1️⃣ Rajoittaa oikeuksia**

- annetaan vain minimi-oikeudet  
- estetään pääsy kriittisiin resursseihin  

**2️⃣ Käyttää IP-rajausta**

- API toimii vain tietyistä IP-osoitteista  

**3️⃣ Käyttää lyhytaikaisia avaimia**

- avaimet vanhenevat automaattisesti  

**4️⃣ Käyttää salaisuudenhallintaa**

- Azure Key Vault  
- Google Secret Manager  
- HashiCorp Vault  

**5️⃣ Valvoa käyttöä**

- käyttöpäiväkirjat  
- anomalioiden tunnistus  

---

## 8) Yhteenveto

Jos API-avain vuotaa, sen sijaintia ei voida jäljittää täysin.  
→ Hyökkääjä voi tunnistaa avaimen, testata sen ja käyttää sitä väärin.  
→ Ainoa oikea toimenpide on poistaa avain, luoda uusi ja rajoittaa sen käyttöoikeuksia.

---
---

# Pieni malli skenaario

<img src="./images/API-vuotaminen-malli.png" width="500">

Tämä osio kuvaa lyhyesti, mitä tapahtuu tilanteessa, jossa käyttäjä, testaaja tai ohjelmistokehityksen parissa työskentelevä henkilö syöttää API‑avaimen tekoälyn chattiin. Tällainen toiminta muodostaa käytännössä Shadow AI ‑tilanteen, koska avain voi päätyä ympäristöihin, joita ei hallita.

> 📅 Kirjoitettu tammikuussa 2026. Sisältö voi päivittyä tai muuttua myöhemmin.

Lyhyesti tapahtumaketjusta: 
- Kun API‑avain syötetään tekoälyn chattiin, se voi päätyä ulkopuolisten nähtäväksi.
  - Tekoälypalveluihin jää yleensä lokitusta, ja avain voi tallentua tai vuotaa yhteyksien kautta.
- Hyökkääjien näkökulmasta avainta testataan automaattisesti eri ympäristöissä, ja sitä voidaan hyödyntää AI‑pentestauksessa tai muissa hyökkäysmenetelmissä.
  - Avaimen voimassaolo määrittää, kuinka pitkään sitä voidaan käyttää väärin.
  - Jos avain saadaan toimimaan, sitä voidaan käyttää kiristämiseen, phishing‑hyökkäyksiin tai laskutuksen väärinkäyttöön.
- Jos avain löytyy haavoittuvuusskannauksissa ja palveluntarjoaja (Azure, AWS, Google) tunnistaa sen omakseen, reagointi tapahtuu yleensä viiveellä.




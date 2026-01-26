# Tekoälyyn syötettävän datan turvallisuus

Tässä osiossa käsitellään tekoälylle syötettävän datan turvallisuusperiaatteita. Yleisen kyberturvallisuuden näkökulmasta tekoälypalveluihin ei tule syöttää henkilötietoja, luottamuksellista sisältöä tai yrityksen sisäisiä tietoja.  

Tietoteknisten ohjelmien yhteydessä on huomioitava, että osa koodeista voi olla kertakäyttöisiä tai niillä voi olla määräaikainen elinkaari — esimerkiksi 3–9 kuukauden välillä. Elinkaari määräytyy käytetyn palvelun mukaan, ja se voi vaihdella ohjelmistokehityksen ja tavallisen käyttäjän tarpeiden välillä.

Syötettävän datan turvallisuus riippuu:

- datan luonteesta (julkinen vs. sisäinen)
- palvelun säilytyskäytännöistä (retention policies)
- käyttöoikeuksista ja sopimuksista (esim. DPA, NDA)
- teknisestä kontekstista (esim. API-avaimet, tokenit, konfiguraatiot)

Näiden periaatteiden avulla voidaan varmistaa, että tekoälyn käyttö pysyy hallittuna ja sääntelyn mukaisena.

## ✅ SAA SYÖTTÄÄ (turvallista)

Seuraavat tiedot voidaan syöttää tekoälyyn, koska ne eivät sisällä henkilötietoja, luottamuksellista dataa tai yrityksen sisäisiä salaisuuksia.

### Julkinen tieto

- Julkiset verkkosivut
- Julkiset dokumentit
- Avoimet standardit ja protokollat
- Yleiset tekniset kysymykset

### Oma, ei-luottamuksellinen teksti

- Omat muistiinpanot
- Omat luonnokset
- Omat ideat, jotka eivät sisällä yrityksen sisäistä tietoa

### Koodi, joka ei sisällä yrityksen omaisuutta

- Open-source-koodi
- Koodi, jossa ei ole yrityksen dataa, sisäisiä integraatioita tai salaisuuksia

### Yleiset kysymykset

- ”Miten tämä algoritmi toimii?”
- ”Voiko tätä käyttää koodin suorituskykyyn?”
- ”Mikä on paras tapa toteuttaa shop&spin?”

---

## ❌ EI SAA SYÖTTÄÄ (kiellettyä)

Seuraavat tiedot ovat kyberturvallisuuden ja tietosuojan näkökulmasta riskialttiita. Näiden syöttäminen tekoälyyn muodostaa shadow AI ‑riskin.

### Henkilötiedot

- Henkilöiden nimet, sähköpostit, puhelinnumerot
- Asiakkaiden tiedot
- CV:t, HR-aineistot
- Rekrytointimuistiinpanot

### Yrityksen sisäinen tai luottamuksellinen tieto

- Sopimukset
- Strategiat
- Talousluvut
- Projektisuunnitelmat
- Sisäiset dokumentit
- Turvallisuusarkkitehtuuri

### Koodi, joka sisältää yrityksen omaisuutta

- Sisäiset integraatiot
- API-avaimet
- Tokenit
- Konfiguraatiot
- Tietokantarakenteet
- Liiketoimintalogiikkaa sisältävä koodi

### Asiakasdata

- Lokitiedot
- Tapahtumatiedot
- Käyttäjäprofiilit
- Tilaukset
- Tukipyynnöt

### Sopimuksia rikkova tieto

- NDA-suojattu tieto
- Kumppanien data
- Toimialakohtaisesti säädelty data (esim. terveys, finanssi)

---

## 🔒 Kyberturvallisuuden tekniset näkökohdat

### 1) Data-egress

Kun data syötetään tekoälyyn, se poistuu organisaation hallinnasta. Ei voida tietää:

- Missä maassa data säilytetään
- Kuka dataa käsittelee
- Käytetäänkö dataa mallin koulutukseen

### 2) Retention-politiikat

Jotkut palvelut säilyttävät syötteitä:

- Mallien parantamiseen
- Kehittäjien tarkasteltavaksi
- Virheentunnistuksen tueksi

GDPR:n mukainen “oikeus tulla unohdetuksi” ei voida toteuttaa, koska dataa ei voida yksilöidä.

### 3) Mallivuodot

Syötetty data voi päätyä:

- Mallin painoihin
- Muiden käyttäjien vastauksiin (harvinaista, mutta dokumentoitu riski)

### 4) Auditoinnin puute

Shadow AI ei lokita tapahtumia. Ei voida jäljittää:

- Kuka syötti mitä
- Milloin
- Minne

### 5) Supply-chain-riskit

Epäviralliset työkalut voivat sisältää:

- Haitallisia kirjastoja
- Epäluotettavia malleja
- Datan varastavia komponentteja

### 6) GDPR-rikkomukset

Henkilötietojen syöttäminen julkiseen AI-palveluun ilman sopimusta muodostaa suoran sääntelyrikkomuksen.

---

## 📏 Peukalosääntö

Jos tietoa ei voida lähettää julkiseen Slack-kanavaan, sitä ei voida syöttää tekoälyyn.

Tätä sääntöä käytetään monissa organisaatioissa yksinkertaisena ja toimivana ohjeena.

---

## 🧠 Yhteenveto

Tekoälyyn saa syöttää vain julkista, ei-luottamuksellista ja ei-henkilökohtaista tietoa. Kaikki muu muodostaa tietoturvariskin, sääntelyrikkomuksen tai hallinnan puutteen. Shadow AI:n riskejä voidaan hallita selkeillä ohjeilla ja teknisillä kontrollikeinoilla.

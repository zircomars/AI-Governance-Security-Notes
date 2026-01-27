# Shadow AI – järjestelmänvalvojan rooli ja vastuut tekoälyn hallinnassa

## Johdanto

Tämä osio koskee suoraan järjestelmänvalvojia, IT-tukea ja kaikkia teknisiä rooleja — riippumatta kokemustasosta. Sama pätee myös yrityksen hallintoon, kuten chief-tason vastuuhenkilöihin ja esihenkilöihin. Jokaisessa organisaatiossa tulee olla vähintään yksi osasto, jossa järjestelmänvalvoja ja IT-tuki vastaavat AI-ympäristön hallinnasta ja ohjeistuksesta.

Kaikille käyttäjille — nykyisille ja tuleville työntekijöille — tulee tarjota selkeä dokumentti, joka toimii sekä selitys- että koulutusmateriaalina. Tämän avulla voidaan vastata tilanteisiin, joissa tavallinen käyttäjä kysyy, miksi jokin tekoälytyökalu ei ole sallittu tai mitä riskejä siihen liittyy.

> Shadow AI ‑riskien hallinta ei ole yksittäisen käyttäjän vastuulla, vaan rakenteellinen tehtävä, joka kuuluu järjestelmänvalvojalle ja organisaation tekniselle johdolle.

## 1) Järjestelmänvalvojan ei kuulu kysyä jokaiselta käyttäjältä lupaa käyttää tekoälyä

Tämä ei ole hallittavissa, skaalautuvaa eikä turvallista.

Miksi ei?

- ei voida määrittää, kuka saa käyttää tekoälyä  
- ei voida määrittää, millä perusteella  
- ei voida määrittää, missä tilanteissa  
- järjestelmänvalvoja joutuisi manuaalisesti:  
  - hyväksymään jokaisen pyynnön  
  - seuraamaan tilannetta ja perusteluja  
  - tekemään päätöksiä perustuen käyttäjien jatkuvaan vakuutteluun  

> Tämä pätee myös siihen, että jokaisella työntekijällä on oma työtehtävänkuvansa ja selkeät perehdytyksensä, jotka määrittävät, mitä työssä saa tehdä ja millaisia työkaluja voidaan käyttää.

---

## 2) Järjestelmänvalvojan todellinen tehtävä shadow AI:n suhteen

### A) Luodaan selkeät pelisäännöt (AI-politiikka)

✅ skaalautuvaa  
✅ hallittavissa  
✅ turvallista  

Mitä pitää määrittää:

- missä tilanteissa tekoälyä saa käyttää  
- mitä dataa saa syöttää  
- mitä ei saa tehdä  
- mitä pitää huomioida  
- mitä riskejä on  
- mitä vaihtoehtoja on  

### B) Asetetaan tekniset kontrollit

✅ hallittavissa  
✅ turvallista  

Mitä pitää estää:

- pääsy kiellettyihin AI-sovelluksiin  
- pääsy kiellettyihin datalähteisiin  
- pääsy kiellettyihin verkkosivuihin  
- pääsy kiellettyihin tiedostoihin  
- pääsy kiellettyihin henkilökohtaisiin tietoihin  
- pääsy kiellettyihin API-rajapintoihin  

### C) Tarjotaan turvallinen vaihtoehto

✅ skaalautuvaa  
✅ hallittavissa  
✅ turvallista  

Mitä pitää tarjota:

- virallinen, hyväksytty, turvallinen AI-työkalu  
- virallinen, hyväksytty, turvallinen AI-palvelu  
- virallinen, hyväksytty, turvallinen AI-sovellus  
- virallinen, hyväksytty, turvallinen AI-ympäristö  
- virallinen, hyväksytty, turvallinen AI-data  

### D) Koulutetaan käyttäjiä

✅ skaalautuvaa  
✅ hallittavissa  
✅ turvallista  

Mitä pitää kouluttaa:

- AI-politiikka  
- AI-riskit  
- AI-vaihtoehdot  
- AI-työkalut  
- AI-palvelut  
- AI-sovellukset  
- AI-ympäristöt  
- AI-data  

---

## 3) Pilvipalvelut (AWS, Azure, Google, Oracle jne.)

Tämä kuuluu järjestelmänvalvojan vastuulle.

Mitä pitää estää:

- pääsy kiellettyihin AI-palveluihin  
- pääsy kiellettyihin AI-työkaluihin  
- pääsy kiellettyihin AI-sovelluksiin  
- pääsy kiellettyihin AI-ympäristöihin  
- pääsy kiellettyihin AI-datalähteisiin  
- pääsy kiellettyihin henkilökohtaisiin tietoihin (esim. Gmail, GDrive jne.)

→ Tämä ei ole käyttäjän vastuulla eikä käyttäjän hallittavissa.

---

## 4) Ilmaisversioiden käyttö “turvallisesti”

Tämä ei ole turvallista hallintaa.

Mitä puuttuu:

- GDPR:n mukaisuus  
- DPA  
- riskiarvio  
- datan anonymisointi  
- tekniset kontrollit  
- AI-politiikka  
- koulutus  

→ Tämä ei estä shadow AI:ta.  
→ Tämä ei ole hallittavissa, skaalautuvaa eikä turvallista.

---

## 5) Yhteenveto mustavalkoisesti

**Järjestelmänvalvojan tehtävä ei ole:**

- valvoa jokaisen käyttäjän tekoälyn käyttöä  
- kysyä jokaiselta lupaa  
- seurata jokaista syötettä  
- arvioida jokaista tilannetta  

**Järjestelmänvalvojan tehtävä on:**

- luoda pelisäännöt  
- asettaa tekniset kontrollit  
- tarjota turvallinen vaihtoehto  
- kouluttaa käyttäjiä  

→ Näin toimitaan skaalautuvasti, hallittavasti ja turvallisesti.

---

## 6) Järjestelmänvalvoja ei ole “tekoälypoliisi”

Järjestelmänvalvojan rooli ei ole:

- tapauskäsittelijä  
- tutkija  
- tuomari  

→ Tämä ei ole hallittavissa eikä skaalautuvaa.

---

## 7) Järjestelmänvalvojan tehtävä on luoda rakenne, ei valvoa ihmisiä

**Järjestelmänvalvoja tekee:**

- luo pelisäännöt  
- luo tekniset kontrollit  
- luo turvallisen vaihtoehdon  
- kouluttaa käyttäjiä  

**Järjestelmänvalvoja ei tee:**

- ei valvo käyttäjiä  
- ei arvioi käyttäjiä  
- ei tutki käyttäjiä  
- ei tuomitse käyttäjiä  
- ei tee päätöksiä perustuen yksittäisiin tilanteisiin  

---

## 8) Lupaprosessit ja manuaalinen hyväksyntä

Järjestelmänvalvoja ei tarvitse:

- tekoälyn käyttöön liittyvää lupaprosessia  
- tekoälyn käyttöön liittyvää hyväksymisprosessia  
- tekoälyn käyttöön liittyvää manuaalista arviointia  

---

## 9) Suosittujen AI-työkalujen käyttöpyynnöt

Käyttäjien toiveet eivät muuta AI-politiikkaa.

Mitä pitää tehdä:

- arvioida riskit  
- arvioida sopimukset  
- arvioida GDPR:n mukaisuus  
- tarkistaa mallin koulutuskäyttö  
- päättää, onko palvelu hyväksyttävissä  

→ Tämä ei ole käyttäjän tehtävä.  
→ Tämä ei ole käyttäjän päätös.

---

## 10) Tiukat politiikat – kyllä, mutta järkevästi

Mitä pitää määrittää:

- missä tilanteissa saa käyttää  
- mitä dataa saa syöttää  
- mitä ei saa tehdä  
- mitä pitää huomioida  
- mitä riskejä on  
- mitä vaihtoehtoja on  

→ Tämä on skaalautuvaa, hallittavissa ja turvallista.

---

## 11) Hälytykset kielletyistä AI-sovelluksista

Kyllä, mutta automaattisesti.

Mitä pitää toteuttaa:

- tekninen kontrolli  
- tekninen hälytys  
- tekninen estäminen  
- tekninen valvonta  

→ Esim. Cloud Access Security Broker (CASB)

---

## 12) Uusien AI-työkalujen testaus

Tämä kuuluu järjestelmänvalvojalle.

**Käyttäjän tehtävä:**

- ilmoittaa järjestelmänvalvojalle  
- pyytää arviointia  
- pyytää päätöstä  
- pyytää ohjeistusta  

**Järjestelmänvalvojan tehtävä:**

- arvioida riskit  
- arvioida sopimukset  
- arvioida GDPR:n mukaisuus  
- arvioida mallin koulutuskäyttö  
- päättää, onko palvelu hyväksyttävissä  

---

## 13) Yhteenveto mustavalkoisesti

Järjestelmänvalvojan tehtävä:

- luoda pelisäännöt  
- asettaa tekniset kontrollit  
- tarjota turvallinen vaihtoehto  
- kouluttaa käyttäjiä  

---

## 14) Yksi lause, joka kiteyttää kaiken

Järjestelmänvalvojan ei kuulu valvoa käyttäjiä — vaan rakentaa järjestelmä, jossa tekoälyä voidaan käyttää turvallisesti, selkeiden sääntöjen ja teknisten kontrollien avulla.

## 15) Mahdolliset jatkotoimenpiteet

Jos järjestelmänvalvojan tai IT-tuen oletettaisiin valvovan jokaisen käyttäjän tekoälyn käyttöä, tilanne muuttuisi nopeasti kuormittavaksi ja epärealistiseksi. Jatkuva hälytysten seuraaminen herättäisi väistämättä kysymyksen siitä, kuka niihin vastaa ja millä resursseilla.

Tekniset kontrollit ja selkeät pelisäännöt ovat siksi välttämättömiä. Ilman niitä järjestelmänvalvojan oma työkuorma kasvaisi hallitsemattomaksi, ja ohjeistuksen kehittäminen voisi pysähtyä, kun ideat ja keinot loppuvat. Digitaalinen ympäristö kehittyy nopeasti, ja uusia riskejä syntyy jatkuvasti.

Jos organisaation sisäiset säännöt tai osaaminen eivät riitä, on suositeltavaa hakea lisäohjeistusta suuremmilta toimijoilta, kuten viestintä-, tietoturva- ja tietosuojaviranomaisilta sekä kyberturvallisuuden asiantuntijoilta. Näiltä tahoilta voidaan saada ajantasaisia neuvoja, uutiskirjeitä, koulutuksia ja webinaareja, jotka tukevat organisaation omaa AI-politiikkaa ja riskienhallintaa.

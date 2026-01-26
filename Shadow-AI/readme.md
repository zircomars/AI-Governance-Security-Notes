# Shadow AI: määritelmä, riskit ja tekninen erittely

<img src="../images/Shadow-Ai-image.jpg" width="600">


## 🔍 Mitä shadow AI tarkoittaa?

Shadow AI:lla tarkoitetaan tekoälyn käyttöä organisaatiossa ilman IT-osaston hyväksyntää, valvontaa tai tietoa. Työntekijät voivat käyttää AI-työkaluja (esim. ChatGPT, Copilot, AutoML, kuvan- tai koodingenerointityökalut) työtehtävissä, vaikka niitä ei ole virallisesti sallittu.

> IBM: “unconsented use of an AI tool without IT approval”  
> Varonis: “AI tools used without the knowledge or oversight of IT or security teams”  
> Group-IB: korostaa generatiivisten AI-työkalujen luvattoman käytön riskejä

---

## ❓ Miten shadow AI syntyy?

- AI-palveluja käytetään julkisesti ja helposti saatavilla olevissa sovelluksissa
- Organisaatiossa ei ole selkeitä AI-politiikkoja
- Käyttö tapahtuu ilman ymmärrystä riskeistä tai lupakäytännöistä

---

## ⚠️ Miksi se on ongelma?

- Tietovuotojen ja datan ulosvirtausten riski
- Compliance-rikkomukset (GDPR, sopimukset, toimialasääntely)
- Mallien väärinkäyttö ilman turvallisuustarkastusta

---

## 🤷 Miksi sitä kuitenkin tapahtuu?

- AI-työkalut ovat helposti saatavilla ja nopeita käyttää
- Työntekijät haluavat ratkaista ongelmat heti, eivät odottaa virallisia prosesseja

---

## 📌 Konkreettisia esimerkkejä shadow AI:sta

1. Kehittäjä käyttää generatiivista AI-mallia koodin tuottamiseen  
   → Koodia generoidaan AI-palvelussa ilman tietoa syötteistä tai mallin käytöstä

2. Markkinointitiimi käyttää AI-työkalua ilman IT-hyväksyntää  
   → Dataa käytetään julkaisuun ilman DPA-sopimusta

3. HR käyttää AI-pohjaista CV-analyysityökalua ilman tietoturvatarkastusta  
   → CV-dataa lähetetään kolmannen osapuolen palvelimille

4. Analyytikko kokeilee AutoML-palvelua omalla datalla  
   → Data ladataan pilvipalveluun, jota ei ole hyväksytty

---

## 🧠 Shadow AI:n tekniset riskit

### 1) Data-egress — hallitsematon datan ulosvirtaus

- Data siirtyy tuntemattomiin palveluihin ilman siirtopolitikkaa tai valvontaa
- Ei tiedetä, missä maassa data päätyy tai säilytetäänkö sitä mallin koulutukseen
- Forensiikkaa ei voida tehdä, jos data vuotaa

### 2) Mallien retention-politiikat — mitä mallille syötetty data tekee?

- Data voi päätyä mallin koulutukseen, parantamiseen tai vastauksiin
- Organisaatio menettää kontrollin datan elinkaaresta
- Retention-politiikkaa ei voida yksilöidä (esim. GDPR Art. 17)

### 3) API- ja integraatioriskit

- AI-työkalut voivat käyttää API:a ja DL-suojauksia
- Liikennettä ei voida valvoa tai estää väärinkäyttöä

### 4) Mallien hallitsematon versiointi ja päivitykset

- Mallien versiot vaihtuvat ilman kontrollia
- Tulokset voivat muuttua päivittäin
- Auditointi on mahdotonta

### 5) Haavoittuvuudet ja supply-chain-riskit

- Käytetään epäluotettavia open-source-malleja tai epävakaita komponentteja
- Piilotettuja riippuvuuksia ja haitallisia kirjastoja voi esiintyä

### 6) Compliance-rikkomukset (GDPR, ISO 27001, sopimukset)

- GDPR-sääntelyä ja sopimuksia voidaan rikkoa
- Toimialasääntelyä (esim. finanssi, terveys) ei noudateta

### 7) Hallinnan ja näkyvyyden puute

- Ei tiedetä, mitä työkaluja käytetään
- Ei tiedetä, mitä dataa syötetään tai mitä vastauksia saadaan

---

## 📊 Yhteenveto teknisestä näkökulmasta

| Riski             | Tekninen vaikutus |
|-------------------|-------------------|
| Data-egress       | Data poistuu organisaatiosta ilman valvontaa |
| Retention         | Data voi jäädä malliin pysyvästi |
| API-riskit        | Ei voida valvoa liikennettä, ei DLP-suojaa |
| Versiointi        | Mallien tulokset muuttuvat, auditointi mahdotonta |
| Supply-chain      | AI-mallit voi sisältää haitallisia riippuvuuksia |
| Compliance        | GDPR, sopimukset, sääntely voivat rikkoutua |
| Näkyvyys          | Ei tietoa siitä, mitä AI-työkaluja käytetään |

---

## ✅ Suositus

Shadow AI ‑käyttöä tulisi hallita selkeillä AI-politiikoilla, teknisillä valvontakeinoilla ja roolikohtaisilla käyttöoikeuksilla. Riskit voidaan minimoida, kun näkyvyys, valvonta ja hyväksyntä ovat kunnossa.


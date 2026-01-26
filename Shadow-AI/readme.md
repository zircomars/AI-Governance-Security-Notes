# Shadow AI: määritelmä, riskit ja tekninen erittely

<img src="../images/Shadow-Ai-image.jpg" width="600">
# Copilot Studio, agenttien hallinta ja shadow AI: riskit ja käytännöt

Shadow AI:lla tarkoitetaan tekoälyn käyttöä työtehtävissä ilman organisaation lupaa, ohjeistusta tai valvontaa. Työkalujen käyttö tapahtuu ilman IT-osaston hyväksyntää, eikä tiedetä, mitä dataa syötetään tai mihin se päätyy.

> IBM: “unconsented use of an AI tool without IT approval”  
> Gartner, Forrester, Varonis: korostetaan IT:n ja tietoturvan ulkopuolista käyttöä  
> Group-IB: painotetaan generatiivisten AI-työkalujen riskejä

### Tyypillisiä käyttäjiä

- HR
- Dev / IT / ICT
- Markkinointi
- Myynti
- Testaus
- Johto
- Tuki
- Ulkoiset konsultit

---

## ❓ Miten shadow AI syntyy?

- AI-työkaluja käytetään selaimessa, sovelluksissa tai sähköpostiohjelmissa ilman asennuksia tai tunnuksia
- Organisaatiossa ei ole selkeitä AI-politiikkoja tai hyväksyntäprosesseja
- Työntekijät eivät tiedä, että käyttö on luvanvaraista tai riskialtista

---

## ⚠️ Miksi se on ongelma?

- Tietovuotojen ja datan ulosvirtausten riski
- GDPR:n ja sopimusten rikkominen
- Mallien väärinkäyttö ja hallitsematon versiointi
- Auditoinnin ja näkyvyyden puute

---

## 🧩 Käytännön esimerkkejä

| Rooli | Käyttötilanne | Riskit |
|------|----------------|--------|
| Kehittäjä | Koodia generoidaan ChatGPT:llä | Ei tiedetä, mitä dataa syötetään tai mihin se tallentuu |
| Markkinointi | AI:ta käytetään sisällön luomiseen | Asiakasdataa voidaan syöttää ilman DPA-sopimusta |
| HR | CV-analyysityökalu käytössä | Data voi päätyä kolmannen osapuolen palvelimille |
| Analyytikko | AutoML-palvelua testataan | Data ladataan ei-hyväksyttyyn pilvipalveluun |

---

## 🔐 Tekninen riskierittely

| Riski | Tekninen vaikutus |
|-------|--------------------|
| Data-egress | Data poistuu organisaatiosta ilman valvontaa |
| Retention | Data voi jäädä malliin pysyvästi |
| API-riskit | Liikennettä ei voida valvoa, ei DLP-suojaa |
| Versiointi | Mallien tulokset muuttuvat, auditointi mahdotonta |
| Supply-chain | AI-mallit voivat sisältää haitallisia komponentteja |
| Compliance | GDPR, sopimukset, toimialasääntely voivat rikkoutua |
| Näkyvyys | Ei tietoa siitä, mitä AI-työkaluja käytetään |

---

## ✅ Missä kulkee raja?

### Sallittu ja turvallinen käyttö

- Käytetään organisaation hyväksymää AI-työkalua
- Työkalu on käynyt läpi tietoturvakatsauksen
- Käyttöön on ohjeet, eikä syötetä arkaluonteista dataa

### Shadow AI (kielletty / riskialtis)

- Työkalua käytetään ilman lupaa
- Syötetään yrityksen sisäistä koodia tai dataa julkiseen palveluun
- Palvelulla ei ole DPA-sopimusta tai tietoturvakontrollia

---

## 🧠 Copilot Studio: lisenssivaatimukset ja kokeiluversiot

Copilot Studio ‑työkalun käyttö edellyttää voimassa olevia lisenssejä tai tilausta. Työkalua ei enää tarjota täysin ilmaisena versiona ilman ehtoja.

### Kokeiluversio

- Voidaan kokeilla maksutta rajoitetun ajan (n. 30 päivää)
- Mahdollistaa agenttien luomisen ja testauksen
- Edellyttää Azure-tiliä ja laskutusasetuksia

### Lisenssityypit

- **Käyttäjälisenssi**: teknisesti maksuton, mutta vaatii tenantin aktivoinnin (esim. Copilot Credits)
- **Tenant-lisenssi / Copilot Credit -paketti**: maksullinen, mahdollistaa tuotantokäytön

---

## 🤖 Agenttien hallinta: Block ja Deploy

Agenttien käyttöä hallitaan samalla tavalla kuin sovelluksia:

### ❌ Block

- Agentti ei ole käytettävissä
- Käyttö ei näy Copilotissa
- Estetään myös shadow AI -käyttö

### ✅ Deploy

- Agentti otetaan käyttöön valituille käyttäjille tai ryhmille
- Käyttö näkyy Copilotissa (Teams, M365, Outlook)
- Agenttia voidaan käyttää ja sen tietoja hyödyntää

### Käytännön esimerkki: 5 roolia ja 5 sovellusta

| Käyttäjä | Canva | Adobe Express | Word | Excel | Monday.com |
|----------|-------|----------------|------|--------|-------------|
| Laura (Markkinointi) | ✅ Deploy | ✅ Deploy | ✅ Deploy | ❌ Block | ✅ Deploy |
| Mika (Taloushallinto) | ❌ Block | ❌ Block | ✅ Deploy | ✅ Deploy | ❌ Block |
| Sanna (HR) | ❌ Block | ❌ Block | ✅ Deploy | ✅ Deploy | ✅ Deploy |
| Jari (IT) | ❌ Block | ❌ Block | ✅ Deploy | ✅ Deploy | ✅ Deploy |
| Emilia (Graafinen suunnittelu) | ✅ Deploy | ✅ Deploy | ✅ Deploy | ❌ Block | ❌ Block |

---

## 📊 Copilot Channel ja shadow AI ‑integraatiot

- Sovellus liitetään Copilot Channeliin → käyttö tapahtuu Copilotin kautta
- Copilot voi kutsua sovelluksen agentin ja käsitellä sen tietosisältöä
- Jos sovellusta ei ole liitetty → Copilot ei voi käyttää sitä → ei hallintaa → mahdollinen shadow AI ‑riski

---

## 📌 Yhteenveto

- Shadow AI = tekoälyn käyttö ilman lupaa, ohjeita tai valvontaa
- Copilot Studio = vaatii lisenssin, mutta tarjoaa kokeiluversioita
- Agenttien hallinta = Block/Deploy-malli antaa kontrollin
- Copilot Channel = määrittää, voiko Copilot käyttää sovellusta
- Riskit = datavuoto, compliance-rikkomukset, näkyvyyden puute

---

## ✅ Suositus organisaatioille

- Laaditaan selkeät AI-politiikat ja hyväksyntäprosessit
- Määritellään roolikohtaiset käyttöoikeudet ja tekniset kontrollit
- Valvotaan AI-työkalujen käyttöä ja koulutetaan henkilöstöä


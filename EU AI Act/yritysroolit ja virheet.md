# EU AI Act – roolit, virheelliset tulkinnat ja soveltamisen riskit

Tässä osiossa kuvataan, ketä EU AI Act koskee, mitä rooleja organisaatioilla voi olla, ja mitkä ovat yleisimmät virheet lain soveltamisessa. Sisältö perustuu asiantuntija-arvioihin ja EU AI Actin rakenteeseen.

Kappaleessa käsitellään lyhyesti tehtävien rooleja ja sitä, ketä ne voivat koskea. Vaikka tehtävänimikkeet eivät ole kiveen hakattuja, EU AI Actin velvoitteet voivat koskea laajasti organisaation henkilöstöä – ei vain teknisiä kehittäjiä tai johtoa. Tavoitteena on ymmärtää, että EU AI Act koskee myös yrityksen sisäisiä käyttäjiä, jotka toimivat tekoälyn kanssa osana työtehtäviään.

> 📅 Päivitetty tammikuussa 2026. Sisältö ja vaatimukset voivat muuttua tai tarkentua vaiheittain.


---

## Ketä EU AI Act koskee?

EU AI Act ei koske yksittäisiä kuluttajia tai yksityishenkilöitä lain velvoitteiden tasolla.  
Sen sijaan se koskee organisaatioita ja toimijoita, jotka:

- kehittävät tekoälyjärjestelmiä (provider)  
- ottavat käyttöön tekoälyjärjestelmiä (deployer)  
- tuovat AI-järjestelmiä markkinoille EU:ssa  
- toimivat jakelijoina tai maahantuojina  
- tarjoavat general-purpose AI -malleja (esim. GPT-4, Claude, Llama)

Yksittäinen henkilö, joka käyttää valmista AI-palvelua (esim. ChatGPT, Copilot, Midjourney), ei ole lain kohde.

---

## Organisaation roolit – kaaviomainen jäsennys

| Rooli        | Kuvaus                                                                 | Esimerkki                                               |
|--------------|------------------------------------------------------------------------|----------------------------------------------------------|
| Provider     | Kehittää oman AI-järjestelmän tai mallin                               | Yritys rakentaa oman rekrytointimallin                  |
| Deployer     | Ottaa käyttöön valmiin AI-järjestelmän                                 | Yritys käyttää GPT-pohjaista työkalua rekrytoinnissa    |
| Jakelija     | Välittää AI-järjestelmiä EU-markkinoille                               | Teknologiatoimittaja tuo AI-tuotteen EU:hun             |
| Maahantuoja  | Tuo AI-järjestelmiä EU-alueelle                                         | EU:ssa toimiva yritys tuo ulkomaisen AI-järjestelmän    |
| GPAI-tarjoaja| Kehittää yleiskäyttöisiä malleja (GPT, Claude, Llama)                  | Mallin kehittäjä, joka tarjoaa teknologian EU:ssa       |

---

## Henkilökohtainen käyttö vs. organisaation käyttö

EU AI Act ei tee eroa henkilön statuksen mukaan (työntekijä, opiskelija, harrastaja).  
Ero tehdään sen mukaan, käytetäänkö AI:ta organisaation puolesta vai yksityisesti.

- Jos AI:ta käytetään organisaation puolesta → vastuu on organisaatiolla  
- Jos AI:ta käytetään yksityishenkilönä → laki ei velvoita käyttäjää  

---

## Yleisimmät virheet EU AI Actin soveltamisessa

⚠️ Yleisin virhe: Organisaatio ei tunnista omaa rooliaan (provider vs. deployer).  
Tämä johtaa seuraaviin ongelmiin:

- velvoitteet arvioidaan väärin  
- riskiluokka tulkitaan virheellisesti  
- dokumentaatio jää puutteelliseksi  
- läpinäkyvyysvelvoitteet unohtuvat  
- AI otetaan käyttöön ilman vaikutusarviointia  

Tämä virhe on todennäköisin ja aiheuttaa eniten sanktioita.

---

## Arvio virheiden todennäköisyydestä (asiantuntija-arviot)

📉 Arvioitu virheiden todennäköisyys:

- 60–80 % yrityksistä tekee alkuvaiheessa virheitä roolituksessa  
- 60 % arvioi dokumentaatiovaatimukset väärin  
- 30–50 % ei tee vaikutusarviointia ajoissa  
- 40–60 % ei tiedosta, että käytetty AI kuuluu korkean riskin luokkaan  

Nämä luvut perustuvat asiantuntijakokemukseen ja konsulttitalojen arvioihin (EY, OnSecurity), eivät virallisiin tilastoihin.

---

## Miksi virheitä tapahtuu?

Virheiden taustalla on se, että EU AI Act:

- on laaja ja tekninen  
- sisältää useita rooleja ja velvoitetasoja  
- tuo velvoitteita eri käyttäjäryhmille  
- astuu voimaan vaiheittain  
- tuo velvoitteita pelkästä AI:n käytöstä  

Organisaatiot eivät ole tottuneet siihen, että pelkkä AI:n käyttö voi tuoda sääntelyvelvoitteita.

---

# 🟦 1. Roolikaavio: Provider / Deployer / Distributor / Importer

(EU AI Actin virallisen roolijaon pohjalta)
Roolikaavio (tekstimuotoinen, selkeä ja yksiselitteinen)

 ![alt text](./images/roolikaavio.png)

Roolien selitykset:
- Provider Rakentaa, kehittää tai julkaisee AI-järjestelmän. Vastaa teknisestä dokumentaatiosta, riskienhallinnasta ja vaatimustenmukaisuudesta.
- Distributor Ei kehitä, mutta välittää AI-järjestelmiä eteenpäin (esim. jälleenmyyjä, konsulttitalo, joka myy AI-tuotteita).
- Importer Tuo EU:n ulkopuolelta AI-järjestelmiä EU-markkinoille.
- Deployer Käyttää AI-järjestelmää omassa toiminnassaan (yritys, kunta, oppilaitos, palveluntarjoaja).

## 🔷 Riskiluokitusmatriisi  
*(EU AI Actin virallinen riskiperusteinen malli)*

| Riskitaso         | Esimerkkejä                                               | Velvoitteet                                                                 |
|-------------------|-----------------------------------------------------------|------------------------------------------------------------------------------|
| Kielletty         | Sosiaalinen pisteytys, manipuloiva AI, biometrinen profilointi | Täyskielto                                                                  |
| Korkea riski      | Rekrytointi, luottopäätökset, koulutusarviointi, terveydenhuolto, kriittinen infrastruktuuri | Tiukat vaatimukset: dokumentaatio, riskienhallinta, data governance, lokitus, ihmisen valvonta |
| Rajoitettu riski  | Chatbotit, generatiivinen AI, deepfake-sisältö            | Läpinäkyvyys: kerrottava käyttäjälle, että AI tuottaa sisältöä              |
| Vähäinen riski    | Pelit, suositusalgoritmit, ei-päätöksentekoon vaikuttavat AI:t   | Ei erityisiä velvoitteita                                                   |

---

## 🔶 Checklist: konsultti, admin, palveluntarjoaja  
*(Käytännönläheinen, suoraan käyttöön)*

### Konsultti

- [ ] Asiakkaan rooli tunnistettu (provider / deployer / distributor / importer)  
- [ ] AI-järjestelmän riskiluokka tunnistettu  
- [ ] Vaikutusarviointi tehty (AI Impact Assessment)  
- [ ] Dokumentaatio ja läpinäkyvyyden toteutuminen varmistettu  
- [ ] Tekninen ja organisatorinen henkilöstö koulutettu  
- [ ] Asiakkaan prosessien yhteensopivuus AI Act -vaatimusten kanssa varmistettu  
- [ ] Henkilötiedon rooli huomioitu riskien arvioinnissa  

### Admin (IT / tietoturva / infra)

- [ ] AI-järjestelmät inventoitu  
- [ ] Pääsynhallinta ja lokitus toteutettu  
- [ ] Datan laatu ja datalähteiden hallinta varmistettu  
- [ ] Tekniset kontrollit toteutettu (DLP, CASB, SSO, auditointi)  
- [ ] Järjestelmät ja riskit dokumentoitu  
- [ ] Kiellettyjen toimintojen estäminen varmistettu  

### Palveluntarjoaja (MSP, IT-palvelut, SaaS-toimija)

- [ ] Oma rooli määritelty (usein distributor + deployer)  
- [ ] Asiakkaalle tarjottu AI on vaatimustenmukainen  
- [ ] Asiakkaalle toimitettu dokumentaatio ja läpinäkyvyys  
- [ ] Asiakkaan AI Act -vastuut tunnistettu  
- [ ] Asiakkaan data käsitelty lain mukaisesti  
- [ ] Jatkuva valvonta ja riskienhallinta toteutettu  

---

## 🔷 Esimerkkitapaukset  
*(rekrytointi, asiakaspalvelu, sisäinen assistentti, automaatio)*

### 1) Rekrytointi (High-risk)

- CV-seulonta AI:lla → korkean riskin järjestelmä  
- Velvoitteet: dokumentaatio, ihmisen valvonta, datan laatu, auditointi  
- Rooli: deployer (jos käytetään), provider (jos rakennetaan itse)

### 2) Asiakaspalvelu (Limited risk)

- Chatbot vastaa asiakkaiden kysymyksiin  
- Velvoite: kerrottava, että käyttäjä keskustelee AI:n kanssa  
- Rooli: deployer

### 3) Sisäinen assistentti (Limited risk)

- GPT-pohjainen työkalu  
- Velvoitteet: läpinäkyvyys, datan hallinta  
- Rooli: deployer

### 4) Automaatio (käyttötarkoituksesta riippuen)

- Prosessiautomaatio ilman päätöksentekoa → vähäinen riski  
- Päätöksenteko ihmisiin vaikuttavissa asioissa → korkea riski  
- Rooli: deployer tai provider

---

## 🔶 Organisaatiokohtainen tulkinta

Tulkinta perustuu siihen, että työskentely tapahtuu:

- teknisen asiantuntijan roolissa  
- arkkitehtuurin, automaation ja turvallisuuden parissa  
- konsulttina ja palveluntarjoajien rajapinnassa  
- politiikan ja ohjeistusten laatijana organisaatiolle  

### Tyypilliset roolit organisaatioympäristössä:

#### 1) Deployer

Kun organisaatiossa käytetään AI-ratkaisuja, kuten:

- Copilot  
- GPT-pohjaiset työkalut  
- automaatio  

→ velvoitteet: riskienhallinta, dokumentaatio, läpinäkyvyys, datan hallinta

#### 2) Distributor / Service Provider

Kun AI-ratkaisuja tarjotaan asiakkaille:

- integraatio  
- automaatio  
- AI-avusteiset palvelut  

→ velvoitteet: varmistettava, että asiakkaalle tarjottu AI on vaatimustenmukainen

### Provider-rooli

Tulee sovellettavaksi vain, jos AI-järjestelmä tai malli rakennetaan itse.








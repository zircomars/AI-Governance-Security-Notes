# Shadow AI – tietoturvariskit, tallennus ja henkilökohtainen ympäristö

Tässä osiossa käsitellään lyhyesti työperäisten tiedostojen, koodien ja arkaluonteisten tietojen tallennusta henkilökohtaisessa ympäristössä. Shadow AI ‑tilanne ei synny pelkästä tallennuksesta ulkoiselle levylle tai USB-tikulle, jos dataa ei siirretä eteenpäin. Shadow AI syntyy vasta, kun arkaluonteista tai työperäistä dataa syötetään tekoälypalveluun tai tallennetaan valvomattomaan ympäristöön.

Yritystilin käyttö mahdollistaa datan suojaamisen ja valvonnan. Henkilökohtaisessa tilissä vastaavaa suojaa ei ole, eikä tavallisia käyttäjiä varoiteta automaattisesti. Siksi tallennuspaikalla ja käyttöympäristöllä on ratkaiseva merkitys tietoturvan kannalta.

## 1) Työperäisen datan tallennus omalle koneelle (ilman synkronointia)

Tämä ei vielä itsessään aiheuta shadow AI ‑vuotoa, jos:

- dataa ei poisteta koneelta  
- dataa ei lähetetä mihinkään palveluun  
- dataa ei syötetä tekoälylle  
- dataa ei synkronoida pilveen  
- dataa ei jaeta eteenpäin  

Mutta kyseessä on silti tietoturvariski, koska:

- yritys ei näe dataa  
- yritys ei voi poistaa dataa  
- yritys ei voi auditoida dataa  
- data voi joutua rikotuksi, varastetuksi tai haittaohjelman kohteeksi  

→ Ei ole automaattisesti shadow AI, mutta kyseessä on väärä paikka työdatalle.

> Tämä pätee kaikkiin laitteisiin, kuten Windows- ja Mac-työasemiin, ulkoisiin tikku- ja levyjärjestelmiin, sekä palvelimiin, joita ei hallinnoida yrityksen toimesta.

---

## 2) Milloin tallennuksesta syntyy shadow AI?

Shadow AI syntyy vasta, kun data poistuu koneelta ulos esimerkiksi:

- tekoälypalveluun (HTTP POST)  
- henkilökohtaiseen OneDriveen  
- henkilökohtaiseen Google Driveen  
- WhatsAppiin / Discordiin / Telegramiin  
- henkilökohtaiseen sähköpostiin  
- AI-ikkunaan, jossa ei ole tallennusvalvontaa  

> Shadow AI syntyy vasta, kun tapahtuu eksfiltraatio eli tallennus ulkopuolelle.

---

## 3) Mistä tietää, jos data vuotaa?

Tämä on tärkeä kohta.

🔴 Henkilökohtaisessa ympäristössä (ei yritystiliä):  
→ Vuotoa ei voida havaita täydellisesti.

Miksi?

Koska henkilökohtaisessa ympäristössä ei ole:

- DLP-valvontaa  
- CASB-valvontaa  
- proxy-logeja  
- Entra ID -auditointia  
- yrityksen pääsynhallintaa  
- endpoint-agentteja  
- edistynyttä verkkovalvontaa  

→ Henkilökohtainen kone + henkilökohtainen tili = ei näkyvyyttä.

Jos data lähtee koneelta (esimerkiksi tekoälypalveluun), se:

- lähetetään HTTP POST -pyynnöllä  
- ei ole henkilökohtaisessa selaimessa verkkovalvontaa  
- ei ole jäljitettävissä jälkeenpäin  

→ Siksi shadow AI on niin vaarallinen.

---

## 4) Voiko tietää, jos data vuotaa tekoälyyn?

Teknisesti:

🔴 Ei voida nähdä:

- mitä palvelu tallentaa  
- minne data menee  
- kuinka kauan dataa säilytetään  
- käytetäänkö dataa mallin koulutukseen  
- kuka dataa käsittelee  
- jaetaanko dataa kolmansille osapuolille  

🟢 Vain seuraavat asiat voidaan nähdä:

- että HTTP-linkkejä lähtee  
- mihin domainiin ne menevät  
- milloin pyyntö tehtiin  

→ Sisältöä ei voida nähdä, koska se on TLS-salattua.

---

## 5) Miten estää shadow AI, jos yritystiliä ei ole?

Tämä on tärkeä kysymys, ja vastaus on selkeä:

🟢 A) Työperäistä dataa ei tule syöttää tekoälyyn  
→ Ei sopimuksia  
→ Ei asiakasdataa  
→ Ei koodia  
→ Ei sisäisiä dokumentteja  
→ Ei koulutusmateriaaleja  
→ Ei API-avaimia  
→ Ei konfiguraatioita  

🟢 B) Työdataa ei tule synkronoida henkilökohtaisiin pilvipalveluihin  
→ Ei OneDrive (henkilökohtainen)  
→ Ei Google Drive  
→ Ei Dropbox  
→ Ei iCloud  

🟢 C) Henkilökohtaisia AI-työkaluja ei tule käyttää työasioihin  
→ Ei ChatGPT free  
→ Ei Copilot free  
→ Ei VS Code AI-laajennuksia henkilökohtaisella tilillä  

🟢 D) Työdataa tulee säilyttää vain:

- yrityksen antamissa ympäristöissä  
- yrityksen hallitsemilla laitteilla  
- yrityksen valvomassa ympäristössä  

→ Jos yritystiliä ei ole käytössä → työdataa ei tule käsitellä lainkaan.

---

## 6) Yhteenveto yhdellä lauseella

Shadow AI syntyy vasta, kun työdataa poistuu koneelta väärään paikkaan — ja henkilökohtaisessa ympäristössä ei voida nähdä tai valvoa, minne se menee. Siksi paras suoja on olla siirtämättä työdataa mihinkään ennen kuin käytössä on yritystili ja yrityksen valvoma ympäristö.

> HTTPS-yhteys tarkoittaa, että selaimen ja palvelun välinen liikenne on salattu ja suojattu ulkopuolisilta. Tämä salaus ei kuitenkaan tee palvelusta tekoälyä, eikä se anna tekoälylle oikeutta tai pääsyä käyttäjän henkilökohtaisiin tai arkaluonteisiin tietoihin. Kun käyttäjä tallentaa tietojaan palveluihin, kuten OneDriveen, GitHubiin, sähköpostiin tai viestisovelluksiin, kyse on pelkästä tiedon säilyttämisestä. Tallennuspalvelut eivät analysoi sisältöä tekoälyn avulla, eivätkä ne muodosta Shadow AI -riskiä. Esimerkiksi muistiinpano “osta maito 12.03.2026” tai koodipätkän tallentaminen GitHubin private-repoon eivät ole tekoälyn käsittelemiä tapahtumia.

> Shadow AI syntyy vasta silloin, kun käyttäjä syöttää tietoa tekoälylle analysoitavaksi ilman organisaation lupaa tai valvontaa. Tällaisia tilanteita ovat esimerkiksi ChatGPT:n, Geminin, Copilotin tai minkä tahansa sivuston sisäänrakennetun tekoälychatin käyttö, jos niille annetaan sisältöä käsiteltäväksi. Jos käyttäjä toimii Azure-, AWS- tai GitHub-ympäristössä ja käyttää niiden sisäisiä AI-chatteja, nämä työkalut ovat tarkoitettu kyseisen ympäristön omaan käyttöön. Ne eivät ole Shadow AI:ta, mikäli organisaatio on hyväksynyt ne osaksi virallista työkalupakettia. Pelkkä tekoälyn näkyminen sivun reunassa ei tee siitä Shadow AI:ta — riski syntyy vasta, kun käyttäjä syöttää sille tietoa, jota ei ole tarkoitettu tekoälyn käsiteltäväksi.


---

## Shadow AI – Microsoft-ympäristö, pilvipalvelut ja tallennuksen riskit

### 1) GitHub ja koodin tallennus

**GitHub Public**  
❌ aiheuttaa riskin  
→ AI voi hakea koodia  
→ jos työperäistä koodia ladataan julkisesti, voi syntyä shadow AI ‑tilanne  
→ AI voi käyttää koodia mallien koulutukseen  
→ voi syntyä ei-toivottu lopputulema yritykselle  

**GitHub Private**  
✅ ei aiheuta riskiä, mutta ei automaattisesti turvallinen  
→ AI ei voi hakea private-repojen koodia  
→ riski syntyy, jos työntekijä lataa koodia julkisesti tai jakaa käyttöoikeuksia väärin  

---

### 2) Pilvipalvelut

**Henkilökohtainen OneDrive / Google Drive**  
❌ aiheuttaa riskin  
→ työdataa voidaan tallentaa  
→ AI voi hakea dataa  
→ ei-toivottu lopputulema voi syntyä  

**Yrityksen OneDrive / SharePoint**  
✅ ei aiheuta riskiä  
→ AI ei voi hakea dataa  
→ turvallinen, kun käytetään yritystiliä  

**AWS / Azure / GCP henkilökohtaisilla tileillä**  
❌ aiheuttaa riskin  
→ ei ole yrityksen hallinnassa  
→ AI voi hakea dataa  
→ voi syntyä ei-toivottu lopputulema  

---

### 3) Kassakaapit ja salasanapalvelut

**Oikein käytettynä**  
✅ ei aiheuta riskiä  
→ turvallinen, kun käytetään yritystiliä  
→ esim. Microsoft Purview, Azure Key Vault, AWS Secrets Manager, HashiCorp Vault  
→ AI ei voi hakea dataa yrityksen hallinnoimista kassakaapeista  

---

### 4) Fyysiset työasemat ja palvelimet

**Yrityksen työasema**  
✅ ei aiheuta riskiä  
→ yrityksen hallinnoima  
→ yritys voi poistaa käytöstä  

**Henkilökohtainen työasema**  
❌ aiheuttaa riskin  
→ työdataa voidaan tallentaa omalle koneelle  
→ AI voi hakea dataa  
→ voi syntyä ei-toivottu lopputulema  

---

### 5) Yhteenveto mustavalkoisesti

**Ei shadow AI:ta, kun:**  
✅ käytetään yritystiliä  
✅ käytetään yrityksen hallinnoimia työasemia ja palvelimia  
✅ käytetään yrityksen hallinnoimia pilvipalveluita  
✅ käytetään yrityksen hallinnoimia kassakaappeja  

**Shadow AI syntyy, kun:**  
❌ käytetään henkilökohtaisia tilejä  
❌ käytetään henkilökohtaisia työasemia  
❌ käytetään henkilökohtaisia pilvipalveluita  
❌ käytetään henkilökohtaisia kassakaappeja  

→ Shadow AI ei liity vain työkaluihin — se liittyy kaikkeen tallennukseen.  
→ Jos työdata päätyy väärään paikkaan, AI voi käyttää sitä väärin.

---

### 6) Microsoft-työkalut ja tilien erot

**Microsoftin työkalut itsessään eivät aiheuta shadow AI:ta**  
→ OneNote, OneDrive, Teams, Word, Excel, SharePoint, Entra ID, Outlook jne.  
→ turvallisia, kun käytetään yritystiliä ja yrityksen hallinnoimia palvelimia  

**Shadow AI syntyy, kun:**  
❌ käytetään henkilökohtaisia Microsoft-tilejä työasioihin  
❌ syötetään työdataa Microsoftin AI-ominaisuuksiin henkilökohtaisilla tileillä  
→ esim. Copilot Wordissä, Excelissä, Teamsissä, Outlookissa  
→ AI voi hakea dataa  
→ voi syntyä ei-toivottu lopputulema  

**Turvallinen käyttö edellyttää:**  
✅ yritystiliä (esim. Entra ID for Business)  
✅ SharePoint (yritys), Teams (yritys), OneDrive (yritys), Outlook (yritys)  
✅ Copilot for Microsoft 365 (yritysversio)  
→ AI ei pääse yrityksen hallintaan  

---

### 7) Käyttötiheys ei vaikuta riskiin

→ Shadow AI ei synny, jos dataa ei syötetä, tallenneta tai käytetä väärin  
❌ riski syntyy, jos työdataa syötetään henkilökohtaisiin AI-palveluihin  
❌ riski syntyy, jos henkilökohtainen ja työympäristö sekoitetaan  

---

### 8) Konkreettiset esimerkit Microsoft-ympäristöstä

**Ei shadow AI:**  
✅ käytetään yritystiliä  
✅ käytetään yrityksen hallinnoimia palvelimia  
✅ käytetään yrityksen hallinnoimia työasemia  
✅ käytetään yrityksen hallinnoimia kassakaappeja  

**Shadow AI syntyy, kun:**  
❌ käytetään henkilökohtaisia Microsoft-tilejä  
❌ käytetään henkilökohtaisia palvelimia  
❌ käytetään henkilökohtaisia työasemia  
❌ käytetään henkilökohtaisia kassakaappeja  

---

### 9) Fyysiset työasemat ja palvelimet

**Yrityksen hallinnoima työasema**  
✅ turvallinen  
→ yritys hallinnoi  
→ yritys voi poistaa käytöstä  
→ yritys voi estää datan tallennuksen OneDriveen  
→ yritys voi estää datan tallennuksen Copilotin palvelimiin  

**Henkilökohtainen työasema**  
❌ ei turvallinen  
→ ei ole yrityksen hallinnassa  
→ työdataa voidaan tallentaa  
→ AI voi hakea dataa  
→ voi syntyä ei-toivottu lopputulema  

---

### 10) Yksi lause, joka kiteyttää kaiken

Microsoftin työkalut ovat turvallisia, kun käytetään yritystiliä — mutta jos henkilökohtaisia tilejä käytetään työdataan, syntyy shadow AI ‑riski.

→ Shadow AI syntyy pilvipalveluista, vääristä tileistä, datan syötöstä, datan tallennuksesta ja datan poistosta hallituista ympäristöistä.  
→ Riski ei ole tekninen virhe — vaan käytöksestä johtuva tietoturvapoikkeama.













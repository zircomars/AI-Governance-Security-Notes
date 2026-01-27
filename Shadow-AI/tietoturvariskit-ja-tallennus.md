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





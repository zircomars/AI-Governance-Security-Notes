# Shadow AI: järjestelmänvalvojan vastuu ja toimintamalli

Tässä osiossa kuvataan järjestelmänvalvojan näkökulmaa shadow AI ‑ilmiön hallintaan. IT-tuen ja järjestelmänvalvojien tehtävänä on valvoa organisaation käyttäjiä, järjestelmiä ja koko osaston toimintaa. Käyttöoikeudet on määritettävä selkeästi, ja valvontaa on toteutettava jatkuvasti.

Mahdollisiin väärinkäytöksiin on reagoitava välittömästi, erityisesti tilanteissa, joissa käyttäjä saattaa syöttää tekoälypalveluun arkaluonteista tai virheellistä dataa. Tällaisissa tapauksissa on varmistettava:

- että lokitus toimii ja tapahtumat voidaan jäljittää  
- että käyttäjille on annettu selkeät ohjeet ja koulutus AI-työkalujen käytöstä  
- että työtilit ja henkilökohtaiset tilit pidetään erillään  
- että työhön liittyvä data käsitellään vain työympäristössä

Järjestelmänvalvojan roolissa on huolehdittava siitä, että AI-työkalujen käyttö tapahtuu hallitusti, turvallisesti ja organisaation politiikkojen mukaisesti.

## 🔴 1) Tietoturvariskit

Shadow AI:lla viitataan luvattomien AI-työkalujen käyttöön ilman IT-valvontaa. Tällainen käyttö altistaa organisaation seuraaville riskeille:

- **Data-egress ilman valvontaa**  
  AI-palveluihin on saatettu syöttää sisältöä koodista, dokumenteista tai yritysportaaleista. Esimerkiksi API-tunnuksia on päätynyt pimeään verkkoon järjestelmäkompromissin seurauksena.

- **Lokituksen ja näkyvyyden puute**  
  Organisaatiolla ei ole ollut näkyvyyttä siihen, mitä dataa on syötetty. Varoniksen mukaan jopa 98 % työntekijöistä on käyttänyt luvattomia AI-työkaluja.

- **Credential-vuodot**  
  OAuth-tunnuksia, API-avaimia ja salasanoja on voitu syöttää vahingossa AI-palveluihin, mikä on johtanut järjestelmäkompromisseihin.

- **Haavoittuvuudet ja supply-chain-riskit**  
  AI-koodigeneraattoreissa on havaittu kirjastoja ja komponentteja, jotka sisältävät haavoittuvuuksia. Esimerkiksi GitHub Copilot on avannut uuden hyökkäyspinnan.

---

## 🔴 2) Tietosuojariskit

Shadow AI rikkoo helposti GDPR:n periaatteita, erityisesti seuraavilla tavoilla:

- **Henkilötietojen luvaton siirto kolmansiin maihin**  
  Datan sijaintia, säilytyskäytäntöjä ja automaattisia käsittelylistoja ei ole voitu varmistaa.

- **Datan elinkaaren hallinnan puute**  
  Syötettyä dataa on voitu säilyttää mallien parantamiseen. Poistaminen, sijainnin tarkistus tai koulutuksen estäminen ei ole ollut mahdollista.

- **Rekisteröityjen oikeuksien rikkominen**  
  Henkilötietojen syöttämisen jälkeen rekisteröity ei ole voinut tarkistaa tai poistaa tietoja — tämä on suora GDPR-rikkomus.

---

## 🔴 3) Järjestelmänvalvojan minimivaatimukset

Seuraavat asiat on tiedettävä ja hallittava:

- Missä AI-palveluissa data voi päätyä (USA, EU, Aasia)
- Mitä retention-politiikkaa palvelu käyttää
- Miten credential-vuodot estetään (esim. API-avainten rotatointi)
- Miten shadow AI havaitaan (Proxy, CASB, DLP, DNS-valvonta, SSO-listat)
- Miten datan ulosvirtausta rajoitetaan (vain hyväksytyt työkalut, yrityslistat)
- Miten henkilöstöä koulutetaan (riskitietoisuus, ohjeistus)

---

## 🔴 4) Järjestelmäarkkitehdin jatkopohdinnat

Seuraavat kysymykset on nostettu esiin arkkitehtitasolla:

- Tarvitaanko virallinen AI-politiikka?
- Tarvitaanko hyväksytty, turvallinen AI-ympäristö (esim. Azure OpenAI)?
- Miten AI-liikennettä valvotaan (Proxy, CASB, DLP, DNS, SSO)?
- Miten credential-vuodot estetään (Secret scanning, Vault-ratkaisut)?
- Miten kehittäjien AI-käyttö voidaan toteuttaa turvallisesti (suljettu ympäristö, hyväksymisprosessi)?

---

## 🔴 Yhteenveto järjestelmänvalvojalle

Shadow AI aiheuttaa tietoturvariskejä, jotka yhdistävät datavuodot, credential-vuodot, GDPR-rikkomukset ja supply-chain-riskit. Minimivaatimuksena on varmistaa näkyvyys, valvonta, ohjeistus ja turvallinen vaihtoehto.

AI-palvelut, VS Code ‑laajennukset ja muut sisäänrakennetut AI-chatit voivat muodostaa shadow AI ‑riskin, jos niitä käytetään ilman valvontaa — riippumatta siitä, onko käyttöliittymä osa selainta, Azurea, VS Codea tai erillistä sovellusta.

---

# Pilvipalvelut ja VS Code: shadow AI ‑riskit työkalutasolla

Tässä osiossa kuvataan, miten pilvipalveluihin ja kehitysympäristöihin liittyvät AI-työkalut voivat muodostaa shadow AI ‑riskin, mikäli niitä käytetään ilman organisaation hyväksyntää tai valvontaa.

## ✔️ Milloin VS Code tai Azure AI-chat voi muuttua shadow AI:ksi?

Shadow AI ‑käyttöä on havaittu seuraavissa tilanteissa:

- AI-laajennus on otettu käyttöön ilman IT-osaston hyväksyntää
- Kirjautuminen on tehty henkilökohtaisella Microsoft-tilillä
- AI-chatille on syötetty sisältöä, kuten koodia, konfiguraatioita, API-avaimia tai asiakasdataa
- Laajennus on lähettänyt dataa taustalla ilman käyttäjän tietoisuutta
- Julkisia mallipalveluita on käytetty organisaation hallitun Azure OpenAI ‑instanssin sijaan

## 🧪 Konkreetteja esimerkkejä

- VS Code AI Tools Extension Pack on asennettu itse, ja siihen on syötetty sisäistä koodia → data on voinut päätyä ulkoiseen mallipalveluun
- Azure AI Foundry on käytetty henkilökohtaisella tilillä → ei ole ollut yhteyttä yrityksen Azure-tenanttiin
- VS Code AI-chat on avattu ja siihen on syötetty sisäistä dataa → data on voinut siirtyä Azureen, OpenAI:hin tai muihin palveluihin

## 🔐 Tietoturva- ja tietosuojariskit

- **Data-egress**: koodi, konfiguraatiot, API-avaimet ja lokitiedot voivat siirtyä palveluihin, joiden sijainti ja säilytyskäytännöt ovat tuntemattomia
- **Retention-politiikat**: syötetty data voidaan säilyttää mallien parantamiseen, jolloin organisaatio menettää kontrollin
- **Credential-vuodot**: .env-tiedostot, API-avaimet ja konfiguraatiot voivat vuotaa automaattisesti
- **Näkyvyyden puute**: IT-osasto ei näe, mitä dataa on lähetetty, minne, milloin ja kenen toimesta

## 🛠️ Järjestelmänvalvojan minimitieto

- VS Code ‑laajennukset voivat muodostaa ulkoisia yhteyksiä mallipalveluihin
- Azure-integraatiot voivat toimia henkilökohtaisilla tileillä myös ilman asennuksia
- AI-chatit voivat lähettää dataa automaattisesti editorista käsin
- Shadow AI syntyy, jos työkalua ei ole hyväksytty, DPA-sopimusta ei ole tehty, eikä liikenteestä ole näkyvyyttä

---

Pilvipalveluihin liittyvä AI-työkalujen käyttö on hallittava selkeästi, jotta datan siirtyminen, säilytys ja käyttö tapahtuvat organisaation politiikkojen mukaisesti. Ilman valvontaa syntyy tekninen ja sääntelyyn liittyvä riski, joka voi johtaa tietovuotoihin ja compliance-rikkomuksiin.

---

# Shadow AI: miksi ilmiö yleistyy ja mitä siitä seuraa

## 🔵 Miksi Shadow AI yleistyy?

### 1) Tekoäly on kaikkialla

- VS Code
- Azure
- Canva
- Copilot
- ChatGPT
- selainlaajennukset
- mobiilisovellukset

Tekoälyä on integroitu työkaluihin — käyttöä ei aina havaita tai ymmärretä.

### 2) Ilmaisversiot ovat liian helppoja

- Ei vaadita asennuksia
- Ei vaadita tunnuksia
- Ei vaadita hyväksyntää
- Käyttö onnistuu suoraan selaimessa

Esimerkki: ChatGPT avataan selaimessa → “kirjoita nopeasti”. Mutta ei huomata, että data siirtyy ulos.

### 3) Käyttäjät eivät ymmärrä datan arvoa

- Ei tunnisteta, mikä on sisäistä
- Ei tunnisteta, mikä on luottamuksellista
- Ei tunnisteta, mikä on henkilötietoa
- Ei tunnisteta, mikä on sopimuksilla suojattua

### 4) Organisaatiot eivät ole ehtineet ohjeistaa

- Ei ole AI-politiikkaa
- Ei ole hyväksyntäprosessia
- Ei ole koulutusta
- Ei ole teknistä valvontaa

### 5) Käyttäjät haluavat olla tehokkaita

- Työ halutaan tehdä nopeasti
- AI-työkalu ratkaisee ongelman heti
- Ei haluta odottaa IT:n hyväksyntää

---

## 🟢 Mitä jatkossa pitää ottaa huomioon?

### 1) Tällaisia tilanteita esiintyy

- Kehittäjät, markkinointi, HR, johto, asiakaspalvelu, opiskelijat, harjoittelijat, freelancerit ja ulkoiset
- Käyttö tapahtuu työkalun sisällä, ilman että AI-ikkuna tunnistetaan

### 2) Dataa ei saa siirtää hallitusta ympäristöstä

- Azure-tenantin ulkopuolelle
- VS Code -laajennuksen kautta
- Henkilökohtaiselle tilille
- Ei-hyväksyttyyn palveluun

### 3) Ellei se syötetä nimittäin, mikä ei ole julkista

- Julkinen tieto on sallittua
- Sisäinen tieto, henkilötiedot, sopimustieto, API-avaimet, konfiguraatiot → ei saa syöttää

### 4) Käyttäjän pitää ymmärtää, että AI = ulkopuolinen palvelu

- AI-palvelu ei ole osa organisaation sisäistä järjestelmää
- Data siirtyy ulos, ellei käytetä hallittua instanssia

---

## 🔵 Mitä perehdytyksessä ja koulutuksessa pitäisi opettaa?

### 1) Selkeä peruslähtö

- AI ei ole neutraali
- AI ei ole organisaation sisäinen sovellus
- AI ei ole automaattisesti turvallinen

### 2) Tietoturva- ja ympäristöperustelu

- Data siirtyy ulos
- Dataa ei voida poistaa
- Dataa ei voida jäljittää
- Dataa voidaan käyttää mallin koulutukseen

### 3) Käytännön esimerkit

- Koodin syöttäminen
- CV:n syöttäminen
- Projektisuunnitelman syöttäminen
- API-avaimen syöttäminen
- Konfiguraation syöttäminen

### 4) Turvalliset vaihtoehdot

- Käytetään organisaation hallittua AI-ympäristöä
- Käytetään hyväksyttyjä työkaluja
- Käytetään yritystiliä

---

## 🔴 Mitä tehdä, jos virhe tapahtuu?

### 1) Pitää reagoida

- Lokitus
- Ilmoitus
- Poisto
- Koulutus

### 2) Järjestelmänvalvoja vs. siviili

#### Järjestelmänvalvoja

- Tunnistaa riskin
- Varmistaa lokituksen
- Varmistaa ohjeistuksen
- Varmistaa valvonnan
- Varmistaa teknisen suojauksen

#### Siviili / yksityishenkilö

- Ei tunnista riskiä
- Ei tiedä, mitä tapahtui
- Ei tiedä, mihin data meni
- Ei tiedä, miten AI toimii

---

## 🟣 Yhteenveto yhdellä lauseella

Shadow AI syntyy, kun tekoälyä käytetään ilman valvontaa, ohjeistusta tai organisaation hyväksyntää. Se uhkaa yksityisyyttä, IT- ja tietoturvaa, sääntelyä ja sopimuksia. Käyttö voi tapahtua selaimessa, editorissa, pilvipalvelussa, työkalussa tai mobiilissa.

---

## 🔵 Voiko shadow AI koskea robotiikkaa?

Kyllä, jos:

- Robotti käyttää AI-mallia
- Robotti käyttää ulkoista mallipalvelua
- Robotti käyttää henkilökohtaista tiliä
- Robotti käyttää ei-hyväksyttyä laajennusta

### Missä kohtaa shadow AI syntyy robotiikassa?

- Kun robotti käyttää AI-palvelua, jota ei ole hyväksytty
- Kun robotti käyttää mallia, joka ei ole hallittu
- Kun robotti käyttää dataa, joka ei ole julkista
- Kun robotti käyttää henkilökohtaista tiliä

---

## 🟣 Logistiikka, automaatio ja teollisuus

Shadow AI voi syntyä, kun:

- Käytetään AI-laajennusta ilman hyväksyntää
- Käytetään henkilökohtaista tiliä
- Käytetään ei-hallittua mallipalvelua
- Syötetään sisäistä dataa AI:hin
- Käytetään AI:ta ilman lokitusta tai valvontaa

---

## 🟢 Mobiilimaailma ja shadow AI

Shadow AI syntyy, jos:

- Käytetään AI-sovellusta ilman hyväksyntää
- Käytetään henkilökohtaista tiliä
- Syötetään sisäistä dataa
- Käytetään AI:ta ilman valvontaa

---

## 🔴 Miten tämä liittyy Kiinaan, Pohjois-Koreaan ja muihin rajoitettuihin maihin?

### Kiina ja Pohjois-Korea

- AI-palvelut voivat olla estettyjä
- AI-palvelut voivat olla valvottuja
- Dataa ei voida siirtää vapaasti

Shadow AI on poliittisesti estetty:

- Kaikki AI-palvelut eivät ole sallittuja
- Käyttö voi olla valvonnan alla
- Data pysyy maan sisällä

---

## 🟢 Eurooppa, USA ja muut avoimet markkinat

- AI-palvelut ovat saatavilla
- Käyttö voi tapahtua ilman valvontaa
- Data voi siirtyä ulos
- Shadow AI voi syntyä helposti

---

## 🔵 Yhteenveto mustavalkoisesti

Shadow AI koskee:

- Selaimia
- VS Codea
- Azurea
- ChatGPT:tä
- Copilotia
- mobiilisovelluksia
- laajennuksia
- pilvipalveluita
- robotiikkaa
- logistiikkaa
- teollisuutta

Shadow AI syntyy, kun:

- Käyttö tapahtuu ilman hyväksyntää
- Käyttö tapahtuu ilman valvontaa
- Käyttö tapahtuu ilman ohjeistusta

---

## 🔴 Kiina ja Pohjois-Korea

- Käyttö on estetty
- Käyttö on valvottua
- Dataa ei voida siirtää vapaasti

---

## 🟣 Eurooppa ja USA

- Käyttö on avointa
- Käyttö voi tapahtua ilman valvontaa
- Shadow AI syntyy helposti

---

## 🟢 Yksi lause, joka kiteyttää kaiken

Shadow AI syntyy, kun tekoälyä käytetään ilman hyväksyntää, valvontaa, ohjeistusta, mallipalvelun hallintaa tai sopimuksia. Käyttö voi tapahtua selaimessa, editorissa, mobiilissa, robotiikassa, teollisuudessa tai pilvipalvelussa — ja se voi johtaa datavuotoihin, sääntelyrikkomuksiin ja hallinnan menetykseen.






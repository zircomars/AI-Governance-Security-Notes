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



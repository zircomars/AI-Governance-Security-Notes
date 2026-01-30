# EU AI Act – Oman tekoälyjärjestelmän rakentaminen ja hyväksyntä

Tämä dokumentti kuvaa, mitä EU AI Act edellyttää tilanteissa, joissa organisaatio rakentaa oman tekoälyjärjestelmänsä. Sisältö koskee sekä alusta asti rakennettuja järjestelmiä että ratkaisuja, jotka toteutetaan valmiiden alustojen, kuten Copilot Studion, avulla.

---

## 1. Oman tekoälyjärjestelmän rakentaminen

Kun organisaatio rakentaa oman tekoälyjärjestelmänsä, sen on määriteltävä järjestelmän riskiluokka. EU AI Act sisältää neljä riskitasoa:

- kielletty AI  
- korkean riskin AI  
- rajoitetun riskin AI  
- matalan riskin AI  

Vain korkean riskin AI-järjestelmät edellyttävät virallista hyväksyntää.

## EU AI Act – Riskiluokat ja esimerkit

EU AI Act jakaa tekoälyjärjestelmät neljään riskiluokkaan. Riskiluokka määräytyy käyttötarkoituksen, ei teknologian tai alustan perusteella.

---

### 1. Kielletty AI (Prohibited AI)
Kiellettyjä ovat järjestelmät, jotka aiheuttavat merkittävää haittaa perusoikeuksille tai turvallisuudelle.

**Esimerkkejä:**
- Alitajuntaan vaikuttava manipulaatio  
- Sosiaalinen pisteytys (social scoring)  
- Kasvojentunnistus reaaliaikaisesti julkisissa tiloissa (tietyin poikkeuksin)  
- Haavoittuvien ryhmien manipulointi (lapset, vammaiset)

---

### 2. Korkean riskin AI (High-risk AI)
Korkean riskin AI edellyttää vaatimustenmukaisuuden arviointia, CE-merkintää ja rekisteröintiä.

**Esimerkkejä:**
- Rekrytointipäätöksiä tekevät järjestelmät  
- Pankkien luottokelpoisuusarvioinnit  
- Lääketieteelliset diagnostiikkajärjestelmät  
- Kriittisen infrastruktuurin ohjausjärjestelmät  
- Oppilasarviointia tai pääsykokeita automatisoivat järjestelmät  
- Oikeusjärjestelmän tukijärjestelmät (esim. riskinarviointi)

---

### 3. Rajoitetun riskin AI (Limited-risk AI)
Rajoitetun riskin järjestelmät edellyttävät läpinäkyvyyttä, mutta eivät CE-merkintää.

**Esimerkkejä:**
- Chatbotit, jotka keskustelevat käyttäjän kanssa  
- Sisältöä generoivat järjestelmät (teksti, kuva, ääni), kun käyttäjälle kerrotaan, että sisältö on AI:n tuottamaa  
- Suositusjärjestelmät (esim. verkkokaupan tuotesuositukset)

---

### 4. Matalan riskin AI (Minimal-risk AI)
Valtaosa AI-järjestelmistä kuuluu tähän luokkaan. Velvoitteet ovat kevyitä.

**Esimerkkejä:**
- Koodin generointi (Copilot, ChatGPT, Gemini)  
- Sisäiset automaatiotyökalut  
- Analytiikka ja raportointi  
- Pelien tekoäly  
- Sisäiset chatbotit, jotka eivät tee päätöksiä ihmisten puolesta

---

## Yhteenveto riskiluokista

| Riskiluokka | Hyväksyntä | Dokumentaatio | Esimerkkejä |
|-------------|------------|---------------|-------------|
| Kielletty | Ei sallittu | Ei sovellu | Sosiaalinen pisteytys, manipulaatio |
| Korkea riski | Pakollinen | Laaja | Rekrytointi, diagnostiikka, luottopäätökset |
| Rajoitettu riski | Ei | Läpinäkyvyys | Chatbotit, generatiivinen AI |
| Matala riski | Ei | Kevyt | Koodigenerointi, sisäiset työkalut |











Rakennettavasta järjestelmästä on dokumentoitava:

- mitä järjestelmä tekee  
- miksi järjestelmä on rakennettu  
- miten järjestelmä toimii  
- mitä dataa järjestelmä käyttää  
- mitä riskejä järjestelmään liittyy  
- miten riskejä hallitaan  
- miten järjestelmää valvotaan  
- miten päivitykset dokumentoidaan  

Nämä vaatimukset koskevat provider-roolia.

---

## 2. Copilot Studion avulla rakennettu tekoäly

Copilot Studion avulla rakennettu tekoälyjärjestelmä ei automaattisesti kuulu korkean riskin luokkaan. Riskiluokka määräytyy käyttötarkoituksen perusteella, ei teknisen alustan perusteella.

Esimerkkejä:

- sisäinen chatbot → matalan riskin AI  
- sisäinen automaatio → matalan riskin AI  
- rekrytointipäätöksiä tekevä AI → korkean riskin AI  
- lääketieteellinen AI → korkean riskin AI  

Copilot Studio ei poista provider-roolin velvoitteita, mutta se ei myöskään tee järjestelmästä automaattisesti korkean riskin järjestelmää.

---

## 3. Hyväksyntä ja rekisteröinti

Hyväksyntä vaaditaan vain korkean riskin AI-järjestelmiltä. Tällöin edellytetään:

- vaatimustenmukaisuuden arviointi  
- CE-merkintä  
- rekisteröinti EU:n AI-järjestelmätietokantaan  

Matalan riskin AI-järjestelmät eivät edellytä hyväksyntää tai rekisteröintiä.

---

## 4. Hyväksyntäprosessin kesto

Hyväksyntäprosessin kesto riippuu järjestelmän laajuudesta ja arviointimenetelmästä.

Tyypillisiä aikavälejä:

- sisäinen arviointi: viikoista muutamaan kuukauteen  
- ulkoinen arviointilaitos: 3–12 kuukautta  

Nämä aikavälit koskevat vain korkean riskin AI-järjestelmiä.

---

## 5. Dokumentointivaatimukset

Provider-roolissa on dokumentoitava:

- tekninen arkkitehtuuri  
- datalähteet  
- riskienhallinta  
- testaus  
- valvonta  
- päivitykset  
- käyttäjäohjeet  

Tämä dokumentaatio muodostaa EU AI Actin edellyttämän teknisen dokumentaation.

---

## 6. Valvontavelvoitteet

### Korkean riskin AI-järjestelmät
- jatkuva monitorointi on pakollinen  
- merkittävät päivitykset edellyttävät uutta arviointia  
- pienet päivitykset dokumentoidaan ja lokitetaan  

### Matalan riskin AI-järjestelmät
- ei määrättyä valvontavelvoitetta  
- käyttöohjeet kannattaa tarkistaa vuosittain  
- ohjeita päivitetään, kun:
  - AI-työkalu muuttuu  
  - organisaation prosessit muuttuvat  
  - data- tai tietoturvapolitiikka muuttuu  

---

## 7. Yhteenveto

| Tilanne | Hyväksyntä | Dokumentaatio | Valvonta |
|--------|------------|---------------|----------|
| Sisäinen chatbot Copilot Studiolla | Ei | Kevyt | Ei |
| Sisäinen automaatio | Ei | Kevyt | Ei |
| Rekrytointipäätöksiä tekevä AI | Kyllä | Laaja | Kyllä |
| Lääketieteellinen AI | Kyllä | Laaja | Kyllä |
| AI-järjestelmä, jota myydään muille | Riippuu riskistä | Aina | Riippuu riskistä |

---


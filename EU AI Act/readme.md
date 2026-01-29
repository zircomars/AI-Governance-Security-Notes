# EU AI act

# EU AI Act – yhteenveto ja soveltaminen

EU AI Act on Euroopan unionin yhteinen tekoälyasetus, joka säätelee sekä tekoälyn kehittämistä että käyttöönottoa. Asetus ei koske vain mallien rakentajia, vaan myös organisaatioita, jotka ottavat tekoälyä käyttöön omissa prosesseissaan.

Asetuksen velvoitteet pätevät kaikkiin tekoälyjärjestelmiin, joita käytetään EU:n alueella tai joita tarjotaan EU:n käyttäjille. Sääntely koskee myös EU:n ulkopuolella kehitettyjä tekoälypalveluita, kuten Yhdysvalloissa, Kiinassa, Aasiassa, Afrikassa tai muissa maissa tuotettuja ratkaisuja, jos niitä käytetään Euroopassa tai jos niitä myydään EU:n markkinoille.

Sääntely perustuu samaan periaatteeseen kuin GDPR: käyttöä ja kohdeyleisöä valvotaan, ei teknologian alkuperämaata. Tämän vuoksi EU AI Actin vaatimukset koskevat kaikkia tekoälypalveluita, jotka toimivat EU:n markkinoilla tai käsittelevät EU:n käyttäjiä koskevaa dataa.

> 📅 Päivitetty tammikuussa 2026. Sisältö perustuu EU AI Actin tilanteeseen kyseisenä ajankohtana. Vaatimukset voivat tarkentua myöhemmin.

> Huomiona: virallinen EU AI Act ‑asetus (tekoälylaki) tuli voimaan 1.8.2024, ja ensimmäiset velvoitteet astuvat voimaan helmikuussa 2025.  

## EU ai act aikajana

EU AI Act hyväksyttiin ja tuli virallisesti voimaan syksyllä 2024. Ensimmäiset velvoitteet astuivat voimaan helmikuussa 2025, ja loput vaatimuksista otetaan käyttöön vaiheittain vuosien 2025–2027 aikana. Tämä tarkoittaa, että sääntely täydentyy ja tarkentuu vielä usean vuoden ajan.

Alla oleva aikajana kuvaa keskeiset päivämäärät:
```EU AI Act – aikajana (täsmällinen ja lyhyt)

1.8.2024  
EU AI Act tuli virallisesti voimaan koko EU:ssa.  
(Tämä on juridinen “laki on nyt olemassa” -päivä.)

EU AI Actin rakenteessa on kolme suurta aaltoa:

1) 2025 – Perusvelvoitteet
- AI-rekisteröinti
- Dokumentointi
- Riskiluokitus
- Läpinäkyvyysvaatimukset
- Tietoturvavelvoitteet
- Kiellettyjen käytäntöjen täyskielto (esim. sosiaalinen pisteytys)

2) 2026 – Valvonta, auditointi ja korkean riskin järjestelmät
Vuoden 2026 aikana voimaan tulevat mm.:
- Korkean riskin AI-järjestelmien tekniset vaatimukset
- Pakolliset riskienhallintaprosessit
- Pakollinen data governance ‑kehikko
- Pakolliset auditointimekanismit
- Velvoitteet AI-järjestelmien jatkuvaan seurantaan
- Velvoitteet käyttäjien informoinnista päätöksenteossa
- Viranomaisten valvontavaltuuksien laajeneminen

3) 2027 – Suurten mallien (GPT-tyyppiset) lisävelvoitteet
Vuonna 2027 odotetaan:
- General-purpose AI (GPAI) ‑mallien erityisvaatimuksia
- Mallien turvallisuustestauksen standardointia
- Mallien läpinäkyvyys- ja dokumentointivaatimusten laajentamista
- Mahdollisia lisävaatimuksia mallien koulutusdatasta
- Velvoitteita mallien riskienhallinnan automatisointiin

```

> 2026 tuo mukanaan korkean riskin järjestelmien tekniset ja hallinnolliset velvoitteet.
> 2027 tuo mukanaan suurten mallien (GPT, Claude, Llama) erityisvaatimukset.

Lisätietoa 
- https://artificialintelligenceact.eu/
- https://valtioneuvosto.fi/-/1410877/eu-n-tekoalyasetus-tekoalykaytantojen-kiellot-astuvat-voimaan-2.2.2025
- https://www.lexfutura.fi/ai-act-kaytannossa-vuonna-2026-mita-organisaation-on-oikeasti-tehtava-nyt
- https://tietosuoja.fi/-/uudet-saannot-vahvistavat-luottamusta-tekoalyyn-tekoalyasetusta-valvovien-viranomaisten-toimivaltuudet-tulivat-voimaan-1.1

---

## Riskiperusteinen luokittelu

EU AI Act jakaa tekoälyjärjestelmät neljään riskiluokkaan:

| Riskitaso       | Esimerkki                                      | Velvoitteet                                           |
|-----------------|------------------------------------------------|--------------------------------------------------------|
| Kielletty       | Sosiaalinen pisteytys, manipuloiva AI          | Täysin kielletty                                       |
| Korkea riski    | Rekrytointi, luottopäätökset, terveydenhuolto  | Tiukat vaatimukset: dokumentointi, riskienhallinta, data governance |
| Rajoitettu riski| Chatbotit, generatiivinen AI                   | Läpinäkyvyysvaatimukset                                |
| Vähäinen riski  | Pelit, suodattimet                             | Ei erityisiä velvoitteita                              |

---

## Roolit organisaatiossa

Organisaatio voi olla kahdessa roolissa:

### 1. AI Provider (kehittäjä)
Jos oma malli tai järjestelmä rakennetaan alusta asti, toimitaan kehittäjänä. Velvoitteet määräytyvät riskiluokan mukaan.

- Rekrytointiautomaatiot → korkea riski → laajat velvoitteet  
- Sisäinen generatiivinen assistentti → rajoitettu riski → läpinäkyvyysvaatimukset  

### 2. AI Deployer (käyttäjä)
Jos käyttö perustuu valmiiseen malliin (esim. GPT-4, Claude, Llama), toimitaan käyttäjänä. Velvoitteet ovat kevyemmät, mutta silti:

- käyttö on arvioitava  
- riskit on tunnistettava  
- käyttäjiä on informoitava, jos AI tuottaa sisältöä tai vaikuttaa päätöksiin  

---

## Soveltaminen käytännössä

| Käyttötapa | Rooli | Soveltaminen |
|------------|-------|--------------|
| Oman mallin kehitys | Provider | EU AI Act koskee vahvasti |
| Työkalun rakentaminen GPT:n päälle | Deployer | EU AI Act koskee kevyemmin |
| Valmiin AI-palvelun käyttö | Käyttäjä | Läpinäkyvyys ja riskienhallinta |

---

## Yhteenveto

EU AI Act ei koske vain mallien kehittäjiä. Asetus koskee kaikkia, jotka:

- kehittävät AI-järjestelmiä  
- rakentavat AI-työkaluja  
- tuovat niitä markkinoille  
- integroivat niitä omiin palveluihinsa  

Velvoitteet vaihtelevat roolin ja riskitason mukaan. Shadow AI rikkoo asetusta, jos käyttö ei ole rekisteröityä, dokumentoitua, valvottua tai riskiluokiteltua.



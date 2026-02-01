# 🔷 Agentin ja assistentin peruslogiikka – tekninen ja sääntelyllinen tausta

Tässä osiossa kuvataan, mitä agentti ja assistentti tarkoittavat, miten ne eroavat toisistaan teknisesti ja toiminnallisesti, miten ne käyttäytyvät arkkitehtuurissa, ja miten ne liittyvät päätöksentekoon, valvontaan ja käyttöoikeuksiin. Lisäksi kuvataan, miten ne näkyvät EU AI Actin riskiluokituksessa ja miksi niiden logiikka on dokumentoitava ennen käyttöönottoa.

---

## 🧠 Mitä agentti ja assistentti tarkoittavat?

- **Assistentti** on tekoälyjärjestelmä, joka toimii vuorovaikutteisesti ja reagoi käyttäjän pyyntöihin.  
  → Esimerkkejä: Copilot, ChatGPT, työpöytäavustaja, mobiiliavustaja

- **Agentti** on tekoälyjärjestelmä, joka toimii autonomisesti, tekee päätöksiä, käyttää työkaluja ja suorittaa tehtäviä ilman suoraa käyttäjän pyyntöä.  
  → Esimerkkejä: prosessiautomaation agentti, API-agentti, mobiiliagentti

---

## 🔧 Miten ne eroavat teknisesti ja toiminnallisesti?

| Ominaisuus                  | Assistentti            | Agentti                  |
|-----------------------------|------------------------|--------------------------|
| Vastaa kysymyksiin          | ✔️                     | ✔️                       |
| Ymmärtää kontekstia         | ✔️                     | ✔️                       |
| Käyttää työkaluja           | ❌                     | ✔️                       |
| Tekee itsenäisiä päätöksiä  | ❌                     | ✔️                       |
| Suunnittelee toimintaketjuja| rajoitetusti           | ✔️                       |
| Toimii ilman pyyntöä        | ❌                     | ✔️                       |
| Soveltuu automaatioon       | osittain               | ✔️                       |

---

## 🏗️ Miten ne käyttäytyvät arkkitehtuurissa?

- **Assistentti** toimii käyttöliittymän kautta, reagoi käyttäjän pyyntöihin, ei tee päätöksiä itsenäisesti.  
  → Valvonta on sisäänrakennettu, koska toiminta edellyttää käyttäjän käskyä.

- **Agentti** toimii järjestelmän tai API:n kautta, voi käyttää useita työkaluja ja tehdä päätöksiä ilman käyttäjän pyyntöä.  
  → Valvonta, rajaukset ja hyväksyntä on suunniteltava erikseen.

---

## 🔐 Miten ne liittyvät päätöksentekoon, valvontaan ja käyttöoikeuksiin?

- **Assistentti** ei tee päätöksiä ilman käyttäjän pyyntöä → hyväksyntä on sisäänrakennettu  
- **Agentti** voi tehdä päätöksiä → eksplisiittinen hyväksyntä on suunniteltava

Agentin kohdalla on määriteltävä:

- mitä agentti saa tehdä  
- mitä se ei saa tehdä  
- kuka hyväksyy toimet  
- miten lokitus ja audit trail toteutetaan  
- miten fallback toimii epäonnistumistilanteessa

---

## ⚖️ Miten ne näkyvät EU AI Actin riskiluokituksessa?

- **Assistentti** kuuluu yleensä **limited risk** -luokkaan  
  → velvoitteet: läpinäkyvyys, ilmoitus AI:n käytöstä, deepfake-merkinnät

- **Agentti** voi kuulua **high-risk** -luokkaan  
  → velvoitteet: riskienhallinta, dokumentaatio, ihmisen valvonta, datan laatu, auditointi

Agentin riskiluokka riippuu käyttötarkoituksesta, autonomian tasosta ja vaikutuksista käyttäjiin, järjestelmiin tai päätöksentekoon.

---

## 📄 Miksi logiikka on dokumentoitava ennen käyttöönottoa?

EU AI Act edellyttää, että ennen agentin käyttöönottoa:

- käyttötarkoitus määritellään  
- riskiluokka arvioidaan  
- rajat ja oikeudet suunnitellaan  
- valvonta ja hyväksyntä toteutetaan  
- fallback-mekanismit suunnitellaan  
- kaikki dokumentoidaan ja jäljitettävyys varmistetaan

Ilman dokumentoitua logiikkaa agentin käyttö ei täytä EU AI Actin vaatimuksia.

---

## 🌐 Ympäristöt, joissa agentit ja assistentit toimivat

| Ympäristö         | Nykyiset työkalut                        | Tulevaisuuden ominaisuudet             |
|-------------------|------------------------------------------|----------------------------------------|
| Teollisuus        | Robotiikka, RPA                          | Agentit, autonomiset järjestelmät      |
| Toimistotyö       | Copilot, dokumentointi, RPA              | Agentit, henkilökohtaiset avustajat    |
| Mobiili           | Puheentunnistus, generatiivinen AI       | Puheagentit, kontekstuaalinen toiminta |
| Kuluttajalaitteet | Älykaiutin, älykello, älypuhelin         | Agentit, päätöksenteko, jatkuva käyttö |
| Ajoneuvot         | Navigointi, sensorit, autonominen ajo    | Agentit, tekoäly, päätöksenteko        |
| Turvajärjestelmät | Kamerat, tunnistus, hälytys              | Agentit, tekoäly, päätöksenteko        |
| Organisaatiot     | HR-, talous-, asiakaspalvelujärjestelmät | Agentit, tekoäly, päätöksenteko        |
| Päivittäiset työkalut | Kalenteri, muistutukset, tiedonhaku   | Agentit, tekoäly, jatkuva käyttö       |
| Maatalous         | Sensorit, automaattiset koneet           | Agentit, tekoäly, päätöksenteko        |

---

## 🧠 Yhteenveto

- Assistentti toimii käyttäjän pyynnöstä, ei tee päätöksiä itsenäisesti  
- Agentti toimii autonomisesti, tekee päätöksiä ja käyttää työkaluja  
- Agentti vaatii selkeän käyttötarkoituksen, rajauksen ja valvonnan  
- EU AI Act edellyttää dokumentaatiota, riskienhallintaa ja ihmisen mukanaoloa  
- Agentin logiikka on dokumentoitava ennen käyttöönottoa  
- Erottelu agentin ja assistentin välillä on kriittinen arkkitehtuurin, valvonnan ja sääntelyn kannalta

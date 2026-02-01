# 🔷 Agentin rakentaminen – ajattelumalli, virheet ja vaatimukset

Agentin rakentaminen ei ole enää “iso talo, iso tiimi” -projekti. Pienet tiimit pystyvät nykyään rakentamaan kokonaisia agentti-ekosysteemejä, mutta samalla syntyy uusi ilmiö: agentin rakentaminen muistuttaa toisen ihmisen ajattelutavan mallintamista.

> ⚠️ **Varoitus: agentin ja assistentin rakentaminen vaatii selkeän rakenteen ja valvotun prosessin**  
> Agentin rakentaminen muistuttaa ihmisen ajattelutavan mallintamista. Ilman selkeää rakennetta syntyy väistämättä virheitä. Assistentti ei tee päätöksiä itse, vaan kysyy agentilta vahvistuksen. Jos agentti antaa vihreän valon, assistentti toistaa sen eteenpäin. Vastaavasti agentti tarvitsee ihmisen läsnäolon, kun kohtaa epäselvän tai prosessisen tilanteen. Vihreä valo annetaan vasta, kun ihminen on vahvistanut päätöksen. Tämä prosessi on välttämätön, jotta järjestelmä toimii luotettavasti ja turvallisesti. <br>
> - ℹ️ **Huomautus: sisältö on kirjoitettu tammikuussa 2026**  
> Tässä dokumentissa kuvattu rakenne, päätösmallit ja agenttien toimintalogiikka perustuvat tilanteeseen tammikuussa 2026. Teknologiat, sääntely, käytännöt ja riskienhallintamallit voivat muuttua ajan myötä. Siksi sisältöä tulee päivittää ja tarkentaa myöhemmin, erityisesti jos agenttien ja assistenttien käyttö laajenee tai sääntelyympäristö muuttuu.



---

## 1. Miksi agentin rakentaminen muistuttaa ajattelun mallintamista?

Agentilla on rooli ja tehtävä, joka pitää pystyä selittämään ja perustelemaan. Agentti ei ole pelkkä tekninen järjestelmä, vaan se velvoittaa. Toiminta muistuttaa ihmisen toimintaa:

- Päätöksenteko  
- Tilanteiden tulkinta  
- Ongelmanratkaisu  
- Vuorovaikutus  
- Oppiminen  
- Selittäminen  
- Toiminta eri ympäristöissä ja sidosryhmissä  

Agentti toimii kuin roolihahmo, jolla on kyvyt, rajat ja käyttäytymismalli.

---

## 2. Menetelmät agentin rakentamiseen

### Agent Persona Method
- Rooli  
- Tehtävä  
- Kyvykkyydet  
- Rajaukset  
- Ympäristö  
- Sidosryhmät  
- Tilannekohtainen toiminta  
- Päätöksenteko  
- Selitysmalli  

### Goal–Constraint–Action -malli
- Tavoite (goal)  
- Rajoitteet (constraints)  
- Toiminnot (actions)  
- Malli kuvaa agentin roolia ja velvoitteita  

### Cognitive Loop / OODA for Agents
- Observe  
- Orient  
- Decide  
- Act  
- Toimii ajattelusilmukkana agentin päätöksenteossa  

### Sandboxed Behavior Testing
- Agentin toiminta testataan hiekkalaatikossa  
- Reaktiot eri tilanteisiin arvioidaan  
- Ennustamattomuus hallitaan  

### Human-on-the-Loop Governance
- Toiminnan valvonta  
- Päätösten ohjaus  
- Mahdollisuus keskeyttää agentti  
- Erityisen tärkeää merkittävissä toiminnoissa  

---

## 3. Miksi pienet tiimit pärjäävät?

Agentin rakentaminen ei enää vaadi:

- Monimutkaista koodaamista  
- Massiivista datan keruuta  
- DevOps-osaamista  
- Pilvi-infrastruktuuria  
- Globaalia skaalausta  

Sen sijaan korostuvat:

- Prompttien kirjoittaminen  
- Agenttiarkkitehtuurin suunnittelu  
- Roolin ja tehtävän kuvaaminen  
- Testaus ja valvonta  

Studio-ympäristöt (Copilot Studio, Vertex AI, OpenAI Agent Builder, AWS Bedrock) tukevat kehitystä, mutta onnistuminen syntyy suunnittelusta ja konfiguroinnista.

---

## ⚠️ Yleisimmät virheet agentin rakentamisessa

### 1. Liikaa vapautta liian aikaisin
- Tehtävä annetaan ilman rajauksia  
- Agentti toimii odottamattomasti  
- Virheelliset päätökset ja epäselvä toiminta  

### 2. Roolin määrittelyn puute
- Agentti toimii yleiskäyttöisenä  
- Rajaukset ja kuvaus puuttuvat  
- Testaus jää tekemättä  

### 3. Epämääräinen tehtävä
- Agentti ei tiedä mitä tehdä tai mitä ei saa tehdä  
- Toiminta epäselvää ja virhealtista  

### 4. Valvonnan puute
- Ei auditointia tai kill switchiä  
- Virheitä ei havaita tai keskeytetä  

### 5. Liiallinen työkalujen käyttö
- Agentti saa pääsyn API:hin, tietokantoihin ja järjestelmiin  
- Virheratkaisut ja tietoturvariskit mahdollisia  

### 6. Edge case -testauksen puute
- Normaalitilanteet toimivat, mutta poikkeustilanteet eivät  
- Virhetilanteissa agentti ei toimi luotettavasti  

### 7. Governance-mallin puute
- Ei valvontaa, ohjausta tai vastuuta  
- Agentti ei ole osa ekosysteemiä  

### 8. Chatbot-ajattelu
- Agentti rakennetaan kuin kysymys–vastausbotti  
- Roolihahmo, ajattelija ja toimija jäävät puuttumaan  

### 9. Käyttäytymismallin puute
- Ei persona- tai logiikkamallia  
- Toiminta satunnaista ja virheellistä  

### 10. Liian nopea tuotantoon vienti
- Testaus, valvonta ja mallinnus puuttuvat  
- Agentti ei ole valmis tuotantoon  

---

## 4. Mistä agentin rakentaminen oikeasti alkaa?

- Roolin ja tehtävän määrittely  
- Ajattelumallin ja toimintalogiikan mallinnus  
- Rajojen ja valvonnan suunnittelu  
- Testaus ja simulaatio  
- Käyttöönoton hallinta osana ekosysteemiä


---

# 🔷 Agentin ja assistentin yhteistyö – ajattelumalli, prosessi ja virheiden väistämättömyys

Agentin rakentaminen muistuttaa laajaa ajattelumallin ja toimintalogiikan kuvausta, joka toimii kuin tuhatsivuinen käsikirja. Ajattelutapa perustuu siihen, että agentti toimii kuin ihminen: se tulkitsee tilanteita, tekee päätöksiä, kohtaa epäselvyyksiä ja tarvitsee toisinaan vahvistusta.

Agentin ja assistentin toiminnassa syntyy väistämättä virheitä. Virheettömiä agentteja tai assistentteja ei ole mahdollista rakentaa, koska:

- päätöksenteko perustuu epätäydelliseen tietoon  
- konteksti voi olla epäselvä  
- rajaukset eivät kata kaikkia tilanteita  
- järjestelmät ja data muuttuvat  
- agentti toimii autonomisesti ja tekee tulkintoja  

Tästä syystä agentin ja assistentin väliin tarvitaan prosessi, joka varmistaa toiminnan luotettavuuden.

---

## 🔷 Assistentin ja agentin välinen prosessi

Assistentti toimii käyttöliittymänä ja viestinviejänä. Agentti toimii päätöksentekijänä. Prosessi etenee seuraavasti:

1. **Assistentti vastaanottaa käyttäjän pyynnön.**  
2. **Assistentti arvioi**, pystyykö se vastaamaan itse vai tarvitaanko agentin päätöstä.  
3. **Jos assistentti ei pysty vahvistamaan toimintaa**, pyyntö siirretään agentille.  
4. **Agentti analysoi tilanteen**, tekee päätöksen ja antaa vihreän tai punaisen valon.  
5. **Assistentti toistaa agentin päätöksen** ja välittää sen käyttäjälle.  
6. **Jos agentti ei pysty tekemään päätöstä**, agentti pyytää vahvistusta ihmiseltä.  
7. **Ihminen antaa lopullisen hyväksynnän**, jonka jälkeen agentti jatkaa toimintaansa.

Tämä muodostaa kolmikerroksisen päätösmallin:

**Assistentti → Agentti → Ihminen**

---

## 🔷 Miksi ihminen tarvitaan mukaan?

Agentti toimii autonomisesti, mutta ei voi ratkaista kaikkia tilanteita. Ihminen tarvitaan erityisesti silloin, kun:

- konteksti on epäselvä  
- päätös vaikuttaa turvallisuuteen  
- data on ristiriitaista  
- agentti ei pysty varmistamaan toiminnan oikeellisuutta  
- agentti kohtaa tilanteen, jota ei ole mallinnettu  

Ihmisen rooli on antaa:

- vihreä valo  
- punainen valo  
- lisätietoa  
- uusi rajaus  
- uusi sääntö  

Tämä varmistaa, että agentti toimii hallitusti ja ennakoitavasti.

---

## 🔷 Miksi tämä rakenne on välttämätön?

- Agentti tekee tulkintoja → tulkinnat voivat olla virheellisiä  
- Assistentti toimii käyttöliittymänä → se ei tee päätöksiä  
- Ihminen toimii ylimpänä valvojana → varmistaa turvallisuuden  

Tämä kolmitasoinen malli estää:

- virheelliset automaatiot  
- väärät päätökset  
- hallitsemattomat toimintaketjut  
- agentin liiallisen autonomian  
- riskit, jotka syntyvät ilman valvontaa  

---

## 🔷 Yhteenveto

Agentin ja assistentin rakentaminen ei ole pelkkää teknistä toteutusta, vaan ajattelumallin, roolin, rajojen ja valvonnan mallintamista. Virheet ovat väistämättömiä, ja siksi prosessi perustuu:

- assistentin varmistukseen  
- agentin päätöksentekoon  
- ihmisen lopulliseen hyväksyntään  

Tämä muodostaa turvallisen ja hallitun agentti–assistentti–ihminen -ekosysteemin.


---

# 🔷 Päätösmallit agentti–assistentti–ihminen -ekosysteemissä

Tässä dokumentissa kuvataan keskeiset päätösmallit, joita käytetään agenttien ja assistenttien toiminnassa. Päätösmallit muodostavat rakenteen, jonka avulla varmistetaan turvallinen, valvottu ja ennakoitava toiminta. Mallit perustuvat siihen, että assistentti toimii käyttöliittymänä, agentti toimii päätöksentekijänä ja ihminen toimii ylimpänä valvojana.

Päätösmallit ovat välttämättömiä, koska agentit ja assistentit tekevät väistämättä virheitä. Virheet syntyvät tulkinnasta, kontekstista, rajauksista ja datasta. Siksi päätöksenteko ja valvonta jaetaan usealle tasolle.

---

## 🔷 Päätösmallien yleinen rakenne (tekstikuvaus)

```
Käyttäjä
↓
Assistentti (käyttöliittymä)
↓
Agentti (päätöksenteko)
↓
Ihminen (lopullinen hyväksyntä)
```


Tämä perusrakenne laajenee eri malleiksi riippuen siitä, missä vaiheessa päätöksiä tehdään, missä kohtaa tarvitaan vahvistusta ja miten virhetilanteet käsitellään.

---

## 🔷 Päätösmallit

### 1. Assistentti → Agentti → Ihminen  
Perusmalli, jossa assistentti pyytää agentilta päätöksen ja ihminen toimii lopullisena hyväksyjänä.

### 2. Agentti → Assistentti → Käyttäjä  
Malli, jossa agentti tekee päätöksen ja assistentti selittää sen käyttäjälle.

### 3. Agentti ↔ Agentti → Ihminen  
Käytetään monimutkaisissa prosesseissa, joissa useampi agentti validoi toistensa päätöksiä ennen ihmisen hyväksyntää.

### 4. Assistentti → Ihminen → Agentti  
Riskialttiissa ympäristöissä ihminen hyväksyy pyynnön ennen kuin agentti toimii.

### 5. Agentti → Ihminen → Agentti  
Agentti pyytää vahvistusta kesken prosessin ja jatkaa vasta hyväksynnän jälkeen.

### 6. Agentti → Fallback → Ihminen  
Virhetilanteissa agentti siirtyy fallback-tilaan ja ihminen ratkaisee tilanteen.

### 7. Assistentti → Agentti → Agentti → Ihminen  
Ketjutettu malli, jossa useampi agentti suorittaa eri vaiheita ennen ihmisen hyväksyntää.

---

## 🔷 Päätösmallien taulukko

| Malli | Kuvaus | Käyttötarkoitus |
|-------|--------|------------------|
| Assistentti → Agentti → Ihminen | Perusmalli | Turvallinen yleismalli |
| Agentti → Assistentti → Käyttäjä | Agentti selittää, assistentti välittää | Raportointi, asiakaspalvelu |
| Agentti ↔ Agentti → Ihminen | Agentit validoivat toisiaan | Monivaiheiset prosessit |
| Assistentti → Ihminen → Agentti | Ihminen hyväksyy ennen toimintaa | Riskialttiit ympäristöt |
| Agentti → Ihminen → Agentti | Ihminen vahvistaa kesken prosessin | Epäselvät tilanteet |
| Agentti → Fallback → Ihminen | Virhetilanteiden hallinta | Poikkeustilanteet |
| Assistentti → Agentti → Agentti → Ihminen | Ketjutettu päätösmalli | Laajat automaatiot |

---

## 🔷 Yhteenveto

Päätösmallit muodostavat rakenteen, jonka avulla agenttien ja assistenttien toiminta pysyy hallittuna. Mallit varmistavat, että:

- assistentti ei tee päätöksiä itse  
- agentti tekee päätöksiä rajojen sisällä  
- ihminen toimii ylimpänä valvojana  
- virhetilanteet käsitellään turvallisesti  
- monimutkaiset prosessit voidaan ketjuttaa  

Päätösmallit ovat keskeinen osa agentti–assistentti‑ekosysteemin suunnittelua, dokumentointia ja governance‑mallia.

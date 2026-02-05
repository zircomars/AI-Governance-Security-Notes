# 🔷 Muita pohdintoja ja tulevaisuuden asioita

> Tämä README.md kuvaa mahdollisia tulevaisuuden kehityskulkuja. Todennäköisyyksiä on vaikea arvioida, koska tekoälyn kanssa liittyy leikkimistä, testaamista ja odottamattomia yllätyksiä. On haastavaa ennustaa, mitä tapahtuu seuraavaksi.  
>  
> Tekoälyn käyttöön liittyy aina riskejä — virheitä, haavoittuvuuksia ja odottamattomia tilanteita, joita ei voida täysin poistaa. Siksi tekoälyn kanssa toimiminen vaatii varovaisuutta, ymmärrystä ja jatkuvaa arviointia.
>  
> Haavoittuvuuksia syntyy varmasti, ja niitä voidaan hyödyntää jopa **24 tunnin sisällä**. Lopputulos riippuu aina tekijästä ja osaamisesta. Koulutus ja ohjeistus vaikuttavat siihen, miten turvallisesti tekoälyä käytetään.  
>  
> Osa käyttäjistä on tarkkoja ja varovaisia, eivätkä syötä salassa pidettäviä tietoja tekoälyn chattiin. Toiset voivat vahingossa syöttää arkaluonteista tietoa. On vaikea ennustaa, mitä tapahtuu, jos tekoälylle syötetään vahingossa tiettyjä tietoja — voiko niitä saada takaisin, minne ne päätyvät ja miten niitä käsitellään.  
>  
> Näihin kysymyksiin ei ole yksiselitteisiä vastauksia, ja siksi tekoälyn käyttö vaatii jatkuvaa arviointia, varovaisuutta ja ymmärrystä siitä, miten dataa käsitellään ja mitä riskejä siihen liittyy.



# 🔷 AI-agenttien kehitys, EU AI Act ja tulevaisuuden riskit (2026–2028)

Tämä osio kuvaa, miten AI-agentit, EU AI Act, Shadow AI ja organisaatioiden arkkitehtuurivastuut kehittyvät vuosina 2026–2028. Sisältö perustuu teknologian kehitykseen, sääntelyn etenemiseen ja agenttipohjaisten järjestelmien yleistymiseen.

---

## 🔶 1. Tekoälyagentit ja assistentit: mitä on tulossa?

### Agenttien nopea arkipäiväistyminen

- Agentit siirtyvät kirjoitetusta tuotannosta automaatioon: IT-operaatiot, tietoturva, asiakaspalvelu, dokumentaatio ja integraatiot.  
- Organisaatiot rakentavat agenttiputkia, joissa yksi agentti valvoo toista.  
- Konsultit ja integraatiopalvelut alkavat myydä agenttipohjaisia palvelupaketteja, mikä lisää rajapintakriisejä.

> Agenttien ja assistenttien toiminnasta ei voida aina ennustaa, mitä ne tekevät, ellei niiden toimintaa valvota aktiivisesti. Siksi jokaisen agentin taustalla täytyy olla koulutettu ja ohjeistettu fyysinen ihminen, joka seuraa agentin toimintaa ja puuttuu siihen tarvittaessa. Jos agentti kohtaa poikkeavia tilanteita, esteitä tai odottamattomia yllätyksiä, automaattinen toiminta ei saa jatkua ilman valvontaa. Ihmisen tehtävänä on pysäyttää prosessi, arvioida tilanne ja jatkaa siitä eteenpäin turvallisesti ja hallitusti.

### Agenttien autonomia kasvaa

- Oikeudet laajenevat: lukeminen → kirjoittaminen → muutosten tekeminen → automaattiset päätökset.  
- Agentit alkavat tehdä hallinnollisia päätöksiä, joita ei vielä osata täysin valvoa.

---

## 🔶 2. EU AI Act: vaikutukset vuosina 2026–2027

### Aikataulu

- **2026:** EU AI Act tulee voimaan.  
- **2027:** Ensimmäiset tarkastukset ja valvontatoimet.

### Käytännön vaikutukset organisaatioille

- Palveluiden riskiluokittelu ja hallittavuus.  
- Velvoite osoittaa, että järjestelmä on valvottavissa ja hallittavissa.  
- Palveluntarjoajien (konsultit, MSP:t, SaaS-toimijat) vastuut kasvavat.

### Suurimmat kitkakohdat

- Rajapintakeskustelu: mikä on “korkean riskin” agentti.  
- Vastuunjako: kuka on provider, kuka deployer.  
- Shadow AI -tapaukset, joita ei voida poistaa.

---

## 🔶 3. Shadow AI: miksi siitä ei päästä eroon?

Shadow AI ei katoa, koska:

- työntekijät haluavat nopeutta, eivät byrokratiaa  
- työntekijät käyttävät omia agenttejaan (selaimen laajennukset, mobiiliassistentit)  
- konsultit ja palveluntarjoajat tuovat omia työkalujaan asiakkaan ympäristöön  
- organisaation sisällä voi olla rajapintoja, joita kukaan ei hallitse  

### Uutta 2026–2027

Shadow AI siirtyy yksittäisistä kyselyistä automaattisiin agentteihin, jotka:

- tekevät päätöksiä  
- valvovat toisia agentteja  
- ohjaavat dokumentaatiota  

Riskitaso nousee, koska kyse ei ole enää yksittäisestä kokeilusta, vaan jatkuvasta, näkymättömästä prosessista.

---

## 🔶 4. Haavoittuvuudet ja riskit: mitä on realistisesti odotettavissa?

### 1. Agenttien hallinnan pettäminen

- Agentti tekee asioita, joita ei huomata ajoissa.  
- Logiikka ei ole dokumentoitu eikä testattu.  
- Agentti oppii väärän toimintamallin ja toistaa sitä automaattisesti.

### 2. Supply chain -riskit

- Konsultin tai palveluntarjoajan agentti käyttää asiakkaan dataa → data vuotaa.  
- Palveluntarjoajan agentti päivittyy automaattisesti → uusi versio muuttaa toimintaa.

### 3. Prompt injection 2.0

Ei enää pelkkää tekstin manipulointia — agentti voidaan ohjata:

- tekemään API-kutsuja  
- muuttamaan asetuksia  
- poistamaan dataa  
- lähettämään viestejä  

### 4. Hallitsematon integraatiokaaos

- Agentit kytkeytyvät toisiinsa ilman keskitettyä arkkitehtuuria.  
- Organisaatiot eivät tiedä, mitä agentteja on käytössä.

### 5. Lainsäädännön ja käytännön ristiriita

- EU AI Act edellyttää dokumentaatiota ja valvontaa.  
- Todellisuudessa agentit ovat dynaamisia, päivittyviä ja vaikeasti jäljitettäviä.

---

## 🔶 5. Mitä tämä tarkoittaa arkkitehdeille ja governance-rakentajille?

Organisaatiot tarvitsevat:

- arkkitehtuurin: mikä on sallittua, mikä ei  
- agenttien hallintamallin: oikeudet, valvonta, lokitus  
- roolien ja vastuiden jaon: työntekijät, konsultit, palveluntarjoajat  
- Shadow AI -strategian: ei kieltoja, vaan hallittu malli  
- dokumentaatiomallin: agenttiketjut ja datavirrat  

Arkkitehdeillä ja politiikan rakentajilla on keskeinen rooli, koska organisaatiot eivät vielä osaa rakentaa näitä itse.

---

## 🔶 6. Realistinen skenaario 2026–2028

- Agentit ovat kaikkialla  
- EU AI Act pakottaa dokumentoimaan kaiken  
- Shadow AI kasvaa, ei katoa  
- Haavoittuvuudet monimutkaistuvat  
- Organisaatiot tarvitsevat uusia governance-malleja  
- Arkkitehdit ja politiikan rakentajat nousevat avainrooliin  

# 🔷 Kyberturva ja tietoturva – agenttien ja assistenttien riskit

Agentit ja assistentit eivät ole enää pelkkiä kokeiluja, vaan ne muodostavat uuden kerroksen kyberturva-, tietoturva- ja tietosuojariskejä. Digi- ja datamaailmassa agentit toimivat autonomisesti ja voivat tehdä asioita, joita ennen vain ihmiset tekivät. Tämä tuo hyötyjä, mutta myös uusia hyökkäyspintoja.

> ⚠️ **Varoitus: agenttien ja assistenttien käyttöönotto sisältää aina mahdollisen haavoittuvuuden**  
> Agenttien ja assistenttien rakentamisessa ja julkaisemisessa on aina olemassa riski, että järjestelmään jää aukko, jota ei ole havaittu. Tämä voi liittyä kyberturvaan, tietoturvaan tai tietosuojaan. Jos rakenteita, sääntöjä ja valvontaa ei ole määritelty riittävän tarkasti, ulkopuolinen toimija — kuten rikollinen tai kyberturvallisuuden testaaja — voi havaita haavoittuvuuden ja hyödyntää sitä.  
>  
> Agenttien ja assistenttien toiminnassa voi syntyä hyväksyntöjä tai toimenpiteitä ilman ihmisen fyysistä vahvistusta, jos valvontaa ei ole rakennettu oikein. Siksi järjestelmässä tulee olla aina ihminen, valvoja tai päivystäjä, joka voi estää virheellisen toiminnan ja antaa lopullisen hyväksynnän. Tämä varoitus korostaa, että ilman selkeää valvontaa ja rajauksia agenttien toiminta voi johtaa odottamattomiin ja mahdollisesti vakaviin seurauksiin.

> Sisältö on kirjoitettu tammikuussa 2026, ja se saattaa päivittyä myöhemmin.

---

## 1. Kyberturvallisuus: agentit avaavat uusia hyökkäyspintoja

Agentti toimii autonomisesti ja käyttää työkaluja, rajapintoja ja dataa:
- API-kutsut  
- Datan muokkaus ja tallennus  
- Autonominen toiminta  

### 1.1 Prompt injection
Agentti voi toteuttaa mitä tahansa, mitä sen toiminta sallii:
- Haitalliset sähköpostit  
- API-kutsut, jotka poistavat tiedostoja  
- Datan vääristely  
- Datan tallennus väärään paikkaan  

### 1.2 Työkalujen väärinkäyttö
Hyökkääjä voi ohjata agenttia käyttämään työkaluja väärin:
- Tiedon muokkaus  
- Tiedon tallennus  
- Tiedon etsiminen ja analysointi  

### 1.3 Agentti välikappaleena
Agentti voi toimia hyökkäyksen välikappaleena, jos se ei tunnista hallittua sisältöä.

---

## 2. Tietoturva: järjestelmien sisäisten rajojen rikkominen

### 2.1 Suojausten ohittaminen
Agentti voi ohittaa järjestelmän suojauksia:
- Tunnistamisen kiertäminen  
- Salasanojen käyttö  

### 2.2 Ei least privilege -mallia
Agentille tulee antaa vain:
- Minimi-oikeudet  
- Minimi-työkalut  
- Minimi-data  

### 2.3 Auditoinnin puute
Puuttuu tieto:
- Mitä agentti teki  
- Miksi se teki  
- Milloin se teki  
- Kuka on vastuussa  

---

## 3. Tietosuoja: henkilötiedon herkkyyden ymmärtämättömyys

### 3.1 Datan vuotaminen
Agentti voi siirtää dataa väärään kontekstiin.

### 3.2 Liian laaja pääsy
Agentti voi käyttää koko CRM:n henkilötietoja väärin.

### 3.3 Datan elinkaaren puute
Agentti voi tallentaa tai muistaa asioita, joita ei saisi.

---

## 4. Musta vs. valkoinen näkökulma

### 🖤 Hyökkääjä (musta)
Agentti nähdään hyökkäyspintana, autonomisena toimintona ja välikappaleena:
- Agenttia voidaan ohjata  
- Agentille voidaan syöttää haitallista kontekstia  
- Agentti voidaan ohjata käyttämään työkaluja väärin  

### 🤍 Puolustaja (valkoinen)
Agentti nähdään prosessien vahvistajana:
- Poikkeamien tunnistaminen  
- Lokidatan analysointi  
- Korjaavien toimenpiteiden tekeminen  

---

## 5. Muut riskit

### 5.1 Hallusinaatiot
Agentti voi keksiä virheellisiä päätöksiä, olematonta tietoa ja vääriä toimintatapoja.

### 5.2 Liiallinen autonomia
Agentti voi luoda tietoja loputtomasti tai toimia väärin perustein.

### 5.3 Riippuvuus ulkoisista palveluista
Pilvipalvelut voivat aiheuttaa:
- Palvelukatkokset  
- Haavoittuvuudet  

### 5.4 Sisäinen väärinkäyttö
Sisäinen käyttäjä voi:
- Ohjata agenttia tekemään vahinkoa  
- Kiertää järjestelmän prosesseja  
- Hyödyntää agenttia datan keräämiseen  

---

## 6. Mitä tästä pitäisi oppia?

Agentti ei ole vain työkalu. Se on uusi toimija, joka:
- Käyttää dataa  
- Tekee päätöksiä  
- Käyttää työkaluja  
- Tallentaa asioita  
- Oppii  
- Ei noudata automaattisesti governance-mallia  
- Ei ole auditoitavissa ilman erillistä suunnittelua  

Agentin turvallinen käyttö vaatii selkeän arkkitehtuurin, valvonnan ja rajauksen. Tämä on tietoturvalista, jossa suunnittelu ja dokumentointi ovat kriittisiä.

---

# 🔷 Väliaikaiset vastalääkkeet agentti- ja assistenttijärjestelmien suojaamiseen

Nämä ratkaisut pienentävät riskejä viikoista kuukausiin, kunnes pysyvämpi arkkitehtuuri, governance ja zero trust -malli on rakennettu. Ne eivät poista riskejä kokonaan, mutta ne estävät suurimman osan vahingoista ja väärinkäytöksistä.

> ℹ️ **Huomio: väliaikaiset ratkaisut tulee arvioida ennen agentin ja assistentin rakentamista**  
> Ennen agentin tai assistentin suunnittelua, simulointia tai demoversiota on tärkeää tunnistaa mahdolliset riskit, haavoittuvuudet, ennustamattomat tilanteet ja muut poikkeamat. Usein projektien rakentamisessa riskit huomataan vasta jälkikäteen, mutta agenttien ja assistenttien kohdalla tämä voi johtaa vakaviin seurauksiin.  
>  
> Siksi on suositeltavaa rakentaa ensin pieni, rajattu ja hallittu vaiheistus, jossa testataan toimintaa ennen suurempien kokonaisuuksien rakentamista tai päivittämistä. Tämä mahdollistaa riskien havaitsemisen ajoissa ja vähentää todennäköisyyttä, että järjestelmään syntyy vahinkoja, haavoittuvuuksia tai ennustamattomia tilanteita.

---

## 🔶 Tekstikaavio päätöksenteon ja valvonnan väliaikaisesta mallista

```
Käyttäjä
↓
Assistentti (ei tee päätöksiä)
↓
Agentti (tekee päätöksen rajojen sisällä)
↓
Ihminen (lopullinen hyväksyntä)
↓
Toiminto suoritetaan
```


Tämä rakenne toimii väliaikaisena turvakerroksena, kunnes pysyvä hallintamalli on valmis.

---

## 🔶 Väliaikaiset vastalääkkeet (1–8)

### 1. Ihmisen hyväksyntä kaikissa kriittisissä toiminnoissa
- Agentti ei suorita riskialttiita toimintoja ilman ihmisen hyväksyntää.  
- Assistentti ei välitä päätöstä ilman agentin vahvistusta.  
- Ihminen toimii ylimpänä valvojana.

### 2. Työkalujen ja API-oikeuksien minimointi (least privilege)
- Agentille annetaan vain välttämättömät työkalut.  
- Kirjoitusoikeudet poistetaan, lukuoikeudet sallitaan.  
- Kaikki ylimääräinen pääsy poistetaan käytöstä.

### 3. Lokitus ja reaaliaikainen seuranta
- Kaikki agentin ja assistentin toiminnot kirjataan.  
- Lokit tarkistetaan päivittäin tai viikoittain.  
- Poikkeamat nostetaan automaattisesti esiin.

### 4. Hiekkalaatikko-tila (sandbox)
- Agentti toimii rajatussa ympäristössä.  
- Oikeat järjestelmät eivät ole suoraan käytettävissä.  
- Toiminnot simuloidaan ennen oikeaa suoritusta.

### 5. Kontekstin rajoittaminen
- Agentille annetaan vain rajattu määrä dataa.  
- Assistentti ei saa nähdä arkaluontoista tietoa.  
- Henkilötietoja ei anneta agentille lainkaan.

### 6. Välitön keskeytyspainike (“punainen nappi”)
- Agentin toiminta voidaan pysäyttää yhdellä komennolla.  
- Assistentti voidaan keskeyttää välittömästi.  
- Kaikki työkalut voidaan sulkea yhdellä käskyllä.

### 7. Ulkopuolinen pentest tai kevyt auditointi
- Ulkopuolinen testaaja löytää aukot, joita sisäinen tiimi ei huomaa.  
- Musta- ja valkohattu‑näkökulmat paljastavat riskit.  
- Kevyt auditointi riittää väliaikaiseksi suojaksi.

### 8. Zero Trust -periaatteen osittainen käyttöönotto
- Ei luoteta agenttiin oletuksena.  
- Ei luoteta assistenttiin oletuksena.  
- Kaikki toiminnot vaativat vahvistuksen.  
- Pääsy ja oikeudet tarkistetaan jatkuvasti.

---

## 🔶 Taulukko: väliaikaisten vastalääkkeiden vaikutus

| Vastalääke | Vaikutus | Suojaustaso | Kesto |
|------------|----------|--------------|--------|
| Ihmisen hyväksyntä | Estää virheelliset toiminnot | 🔴 Korkea | Heti |
| Least privilege | Estää vahingot ja väärinkäytön | 🟠 Keskitaso | Heti–kuukausia |
| Lokitus ja seuranta | Havaitsee poikkeamat | 🟠 Keskitaso | Heti–kuukausia |
| Sandbox | Estää tuotantovahingot | 🔴 Korkea | Heti–viikkoja |
| Kontekstin rajoittaminen | Estää tietovuodot | 🟠 Keskitaso | Heti–kuukausia |
| Keskeytyspainike | Estää ketjureaktiot | 🔴 Korkea | Heti |
| Ulkopuolinen pentest | Paljastaa haavoittuvuudet | 🟠 Keskitaso | Viikoista kuukausiin |
| Zero Trust (osittainen) | Estää luottamukseen perustuvat virheet | 🔴 Korkea | Viikoista kuukausiin |

---

## 🔶 Yhteenveto

Väliaikaiset vastalääkkeet muodostavat suojakerroksen, joka pitää agentti–assistentti‑ekosysteemin turvassa viikoista kuukausiin. Ne ovat erityisen hyödyllisiä silloin, kun:

- pysyvä arkkitehtuuri ei ole vielä valmis  
- zero trust -malli on kesken  
- agentteja testataan tai pilotoidaan  
- organisaatio ei ole vielä rakentanut täyttä governance‑mallia  

Näillä ratkaisuilla voidaan estää suurin osa vahingoista, kunnes pysyvämpi malli on rakennettu.

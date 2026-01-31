# EU AI Act – Tekoälyagentit ja assistentit 

EU AI Act ei käytä termejä *agentti*, *assistentti* tai *autonominen agentti*, mutta laki kattaa ne täysin, koska ne ovat tekoälyjärjestelmiä, jotka suorittavat tehtäviä, mahdollisesti itsenäisesti, ja voivat vaikuttaa ihmisiin, prosesseihin tai päätöksiin.  
Agentit ja assistentit luokitellaan samalla tavalla kuin muutkin AI-järjestelmät: **käyttötarkoituksen ja riskin perusteella**.

## ⚠️ Tärkeä huomio tekoälyagenteista ja assistenteista  
> **Ajankohtainen tieto: tammikuu 2026**  
> Tämä tieto voi muuttua ja päivittyä myöhemmin EU AI Actin täsmentyessä ja teknologian kehittyessä.
>
> Tekoälyagentit ja assistentit voivat toimia osittain autonomisesti, minkä vuoksi niiden käyttö edellyttää aina **ihmisen valvontaa**. Vähintään yhden tai useamman fyysisen henkilön on seurattava agentin toimintaa, jotta voidaan estää tilanteet, joissa agentti tekee odottamattomia tai ei-toivottuja toimia ilman ihmisen hyväksyntää.
>
> Autonomisten agenttien toimintaan liittyy aina epävarmuustekijöitä:  
> - agentti voi tehdä päätöksiä, joita ei ole ennakoitu  
> - agentti voi tulkita ohjeita väärin  
> - agentti voi toimia ympäristössä, jossa kaikki muuttujat eivät ole tiedossa  
> - agentti voi oppia tai mukautua tavoilla, joita ei ole täysin dokumentoitu  
>
> Tämän vuoksi agenttien käyttöönotto edellyttää:  
> - **selkeitä pelisääntöjä ja rajoituksia**  
> - **valvontamekanismeja** (human-in-the-loop / human-on-the-loop)  
> - **simuloituja testejä ennen tuotantokäyttöä**  
> - **riskiskenaarioiden läpikäyntiä**  
> - **fallback- ja hätätilaprotokollia**  
>
> Agentin toimintaa ei voida täysin ennustaa kaikissa tilanteissa, ja siksi riskienhallinta perustuu ennakointiin, testaukseen ja jatkuvaan valvontaan. Tämä on erityisen tärkeää korkean riskin ympäristöissä, kuten terveydenhuollossa, teollisuudessa, robotiikassa ja kriittisessä infrastruktuurissa.


---

## 1. Agenttien ja assistenttien riskiluokittelu

| Riskitaso | Esimerkkejä agenteista | Velvoitteet |
|-----------|------------------------|-------------|
| **Vähäinen riski** | koodigenerointiagentit, dokumentaatioagentit, sisäiset workflow-agentit | Ei erityisiä velvoitteita |
| **Rajoitettu riski** | asiakaspalveluagentit, markkinointiautomaatioagentit, HR-assistentit (ei päätöksentekoa) | Läpinäkyvyysvaatimukset |
| **Korkea riski** | rekrytointiautomaatiot, luottopäätösagentit, terveydenhuollon agentit, kriittisen infrastruktuurin agentit, autonomiset robottiagentit | Dokumentointi, riskienhallinta, data governance, CE-merkintä |
| **Kielletty** | manipuloivat agentit, poliittinen vaikuttaminen, biometrinen profilointi | Täysin kielletty |

---

## 2. Milloin agentti muuttuu korkean riskin AI:ksi?

Agentti on korkean riskin AI, jos se:

- tekee päätöksiä ihmisten puolesta  
- vaikuttaa oikeuksiin, terveyteen tai turvallisuuteen  
- toimii kriittisessä prosessissa  
- ohjaa fyysistä robottia tai laitetta  
- arvioi ihmisiä (HR, pankki, terveys)  
- toimii valtion päätöksenteossa  

---

## 3. Provider-, deployer- ja admin-vastuut agenttien kohdalla

### Provider (rakentaa agentin)
- vastaa dokumentaatiosta  
- vastaa riskiluokittelusta  
- vastaa datan laadusta  
- vastaa mallin toiminnasta  
- vastaa CE-merkinnästä (korkean riskin AI)  

### Deployer (käyttää agenttia)
- vastaa käyttöohjeiden noudattamisesta  
- vastaa riskien arvioinnista  
- vastaa valvonnasta  
- vastaa käyttäjien ohjeistamisesta  

### Admin (tukirooli)
- varmistaa teknisen toimivuuden  
- valvoo käyttöoikeuksia  
- ylläpitää lokitusta  
- tukee riskienhallintaa  
- tukee dokumentaatiota  
- toimii jatkuvuuden varmistajana  

---

## 4. Raportointi ja hallinnollinen vastuu

Agentit ja assistentit edellyttävät riskiraportointia, koska ne:

- oppivat  
- muuttuvat  
- saavat uusia kykyjä  
- voivat vaikuttaa prosesseihin  

### Suositeltu raportointitiheys:
- **ennen kehityksen aloittamista**  
- **kehityksen aikana**  
- **julkaisun yhteydessä**  
- **kvartaalittain (3–4 kk välein)**  
- **aina merkittävän muutoksen yhteydessä**  

### Raportointi sisältää:
- riskiluokan perustelut  
- riskienhallintatoimet  
- datalähteet  
- päivitysten vaikutukset  
- vastuut ja roolit  
- mahdolliset väärinkäyttötapaukset  

### Raportointi hallitukselle / johtoryhmälle
Suositeltavaa ISO 27001 -hallintamallin mukaisesti.

---

## 5. Päätöspuu: Mihin riskiluokkaan agentti kuuluu?

```
┌────────────────────────────────────┐
│ 1. Vaikuttaako agentti             │
│    ihmisten oikeuksiin,            │
│    terveyteen tai turvallisuuteen? │
└────────────────────────────────────┘
             │
┌────────────┴────────────┐
│                         │
Kyllä                      Ei
│                         │
┌──────────────────────────┐     ┌──────────────────────────┐
│ 2. Tekee agentti         │     │ 3. Keskusteleeko agentti │
│    päätöksiä itsenäisesti│     │    käyttäjän kanssa?     │
└──────────────────────────┘     └──────────────────────────┘
           │                           │
┌──────────┴──────────┐     ┌──────────┴──────────┐
│                     │     │                     │
Kyllä                  Ei    Kyllä                  Ei
│                     │     │                     │
┌──────────────────┐   ┌──────────────────┐   ┌──────────────────┐
│ Korkea riski     │   │ Rajoitettu riski │   │ Vähäinen riski   │
└──────────────────┘   └──────────────────┘   └──────────────────┘
```


---

## 6. Yhteenveto

- Agentit ja assistentit kuuluvat EU AI Actin piiriin.  
- Ne luokitellaan käyttötarkoituksen mukaan.  
- Suurin osa agenteista on vähäisen tai rajoitetun riskin AI:ta.  
- Osa voi olla korkean riskin AI:ta, jos ne tekevät päätöksiä ihmisten puolesta.  
- Provider ja deployer kantavat vastuun.  
- Admin tukee teknisesti ja varmistaa jatkuvuuden.  
- Riskiraportointi ja dokumentointi ovat välttämättömiä.  
- Tieto on ajankohtainen **tammikuussa 2026**, ja se voi päivittyä myöhemmin.  


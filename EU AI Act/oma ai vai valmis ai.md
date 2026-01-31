# Rakentaako yritys oman tekoälyn vai käyttääkö valmiita palveluja?  

> **Ajankohtainen tieto: tammikuu 2026**  
> Tämä tieto voi muuttua ja päivittyä myöhemmin teknologian ja EU AI Actin kehittyessä.

Yrityksen on päätettävä, rakentaako se oman tekoälymallin vai hyödyntääkö se valmiita palveluja (kuten Copilot, GPT, Claude, Gemini). Päätös vaikuttaa kustannuksiin, riskeihin, aikatauluihin ja EU AI Act -velvoitteisiin.

---

## 1. Vaihtoehto A: Oman tekoälyn rakentaminen

Oman mallin rakentaminen on teknisesti raskas ja kallis prosessi. Se sopii vain yrityksille, joilla on:

- suuri määrä laadukasta dataa  
- merkittävä budjetti  
- vahva tekninen osaaminen  
- tarve, jota valmiit mallit eivät ratkaise  

### Edut
- täysi kontrolli malliin ja dataan  
- räätälöinti omiin tarpeisiin  
- mahdollisuus rakentaa kilpailuetua  

### Haitat
- erittäin korkeat kustannukset  
- pitkä kehitysaika  
- suuret muistivaatimukset (GB → TB → jopa 100+ TB)  
- GPU-klustereiden tarve  
- EU AI Act -dokumentaatiota paljon enemmän  
- riskit kasvavat, jos malli epäonnistuu  

## Todennäköisyysarvio: Rakentaako yritys oman AI:n vai käyttääkö valmista?

Tämä ei ole tieteellinen mittari, mutta se kuvaa hyvin todellisuutta eri käyttäjä- ja yritysryhmissä.

| Käyttäjä / yritys                     | Todennäköisyys rakentaa oma AI | Todennäköisyys käyttää valmista AI:ta |
|--------------------------------------|--------------------------------|----------------------------------------|
| Tavallinen käyttäjä                  | 0–1 %                          | 99–100 %                               |
| Harrastelija                         | 1–5 %                          | 95–99 %                                |
| Pieni yritys (1–20 hlö)              | 1–10 %                         | 90–99 %                                |
| Keskisuuri yritys (50–100 hlö)       | 5–20 %                         | 80–95 %                                |
| Suurehko yritys (100–200 hlö)        | 10–30 %                        | 70–90 %                                |
| Suuri yritys (200+ hlö)              | 20–50 %                        | 50–80 %                                |
| Teknologiajätti (Google, Microsoft, Meta) | 90–100 %                    | 0–10 %                               |

**Yhteenveto:**  
Valtaosa yrityksistä — jopa keskisuuret — käyttävät valmiita AI-palveluja ja rakentavat vain pieniä agentteja, integraatioita tai automaatioita valmiiden mallien päälle.

---

## 2. Vaihtoehto B: Valmiiden tekoälypalvelujen käyttäminen

Tämä on realistinen ja kustannustehokas ratkaisu lähes kaikille yrityksille.

### Edut
- nopea käyttöönotto  
- alhaiset kustannukset  
- ei tarvetta GPU-klustereille  
- ei tarvetta valtaville datamassoille  
- EU AI Act -velvoitteet kevyemmät  
- helppo rakentaa agentteja ja automaatioita päälle  

### Haitat
- ei täyttä kontrollia malliin  
- riippuvuus palveluntarjoajasta  
- osa datasta kulkee pilvipalvelun kautta  

---

## 3. Muistivaatimukset ja tekninen kuorma

### Pienet mallit (agentit, assistentit)
- Muisti: gigatavuluokka  
- Tallennus: gigatavuista kymmeniin gigatavuihin  
- Laskenta: normaali pilvi-infra  

### Keskikokoiset mallit
- Muisti: kymmeniä–satoja gigatavuja  
- Tallennus: satoja gigatavuja – muutama teratavu  
- Laskenta: GPU-palvelimet  

### Suuret kielimallit
- Muisti: kymmenistä teratavuista satoihin teratavuihin  
- Tallennus: 100 TB – petatavuluokka  
- Laskenta: GPU-klusterit  
- Kustannus: miljoonaluokka  

Tämä on yksi tärkeimmistä syistä, miksi yritykset **keskeyttävät AI-projekteja**.

---

## 4. EU AI Act -näkökulma

### Oman mallin rakentaminen
- korkeat dokumentointivaatimukset  
- riskienhallinta pakollinen  
- datan laatuvaatimukset  
- CE-merkintä, jos korkean riskin AI  
- audit trail ja valvonta  

### Valmiin mallin käyttäminen
- kevyemmät velvoitteet  
- provider kantaa suurimman vastuun  
- deployer vastaa käytöstä ja valvonnasta  
- admin tukee teknisesti  

---

## 5. Päätöspuu: Kannattaako yrityksen rakentaa oma AI?

```
┌───────────────────────────────┐
│ Onko yrityksellä paljon dataa?│
└───────────────────────────────┘
             │
┌────────────┴────────────┐
│                         │
Ei                        Kyllä
│                         │
┌──────────────────┐      ┌──────────────────────────┐
│ Käytä valmista   │      │ Onko budjetti > 500k €?  │
└──────────────────┘      └──────────────────────────┘
            │
┌───────────┴───────────┐
│                       │
Ei                      Kyllä
│                       │
┌────────────────────────┐   ┌──────────────────────────┐
│ Käytä valmista AI:ta   │   │ Voidaan harkita oman AI:n│
│ + rakenna agentteja    │   │ rakentamista             │
└────────────────────────┘   └──────────────────────────┘
```


---

## 6. Yhteenveto

- Oman AI:n rakentaminen on raskasta ja kallista.  
- Valmiin AI:n käyttäminen on realistista ja tehokasta.  
- Pienet ja keskisuuret yritykset hyötyvät valmiista AI:sta 10× enemmän.  
- EU AI Act ei pakota rakentamaan omaa AI:ta.  
- Agentit ja automaatiot ovat järkevin polku.  
- Todennäköisyys, että pieni firma rakentaa oman mallin: **1–10 %**.  
- Todennäköisyys, että se käyttää valmista AI:ta: **90–99 %**.  


# 🔷 Agentin rakentaminen – EU AI Actin vaatimukset ja käytännön tarkistuslista

EU AI Act on jo voimassa. Yrityksen oman agentin rakentaminen ei ole enää pelkkä tekninen päätös, vaan strateginen, juridinen ja riskienhallinnallinen kokonaisuus.

---

## 1. Ennen agentin rakentamista on kysyttävä “miksi?” ja “mihin tarkoitukseen?”

Tämä ei ole vain hyvä käytäntö — vaan EU AI Actin vaatimus.

EU AI Act edellyttää, että:

- käyttötarkoitus määritellään  
- riskit arvioidaan  
- varmistetaan, ettei järjestelmä aiheuta haittaa terveydelle, turvallisuudelle tai perusoikeuksille  
- toteutetaan soveltuva valvonta riskiluokan mukaan  
- ihmisen mukanaolo varmistetaan, koska agentti voi toimia autonomisesti ja vaikuttaa todelliseen ympäristöön  

Agenttia ei voida rakentaa ilman perustelua. On osoitettava, miksi agentti on tarpeen ja mitä hyötyä siitä on.

---

## 2. Tämä pätee suoraan EU AI Actin sääntelyyn

Agentit luokitellaan AI-järjestelmiksi, joilla on autonomia toimintoihin.  
Ne voivat kuulua korkean riskin luokkaan, jos ne vaikuttavat:

- turvallisuuteen  
- infrastruktuuriin  
- työntekijöihin  
- päätöksentekoon  

EU AI Act edellyttää:

- dokumentaatiota  
- riskienhallintaa  
- ihmisen valvontaa  
- läpinäkyvyyttä  

Yrityksen on selvitettävä, kuuluuko agentti lain piiriin ja mitä velvoitteita syntyy.

---

## 3. Agentti per käyttäjä vai yhteinen agentti?

Valinta riippuu arkkitehtuurista ja riskitasosta. Molemmat mallit ovat mahdollisia, mutta niillä on eri vaikutukset.

### Vaihtoehto A: Agentti per käyttäjä (henkilökohtainen agentti)

Sopii tilanteisiin, joissa:

- agentti toimii käyttäjän puolesta  
- agentti tarvitsee henkilökohtaisia asetuksia  
- agentti ei saa sekoittaa käyttäjien dataa  
- agentti toimii rajatulla oikeustasolla  

**Hyödyt:**

- selkeä omistajuus  
- pienempi riski  
- helpompi valvonta  

**Haitat:**

- enemmän agentteja ylläpidettävänä  
- korkeampi kustannus  

### Vaihtoehto B: Yhteinen agentti (organisaation agentti)

Sopii tilanteisiin, joissa:

- agentti hoitaa prosesseja, ei henkilökohtaisia tehtäviä  
- agentti toimii osana automaatiota  
- agentti tarvitsee laajempia oikeuksia  

**Hyödyt:**

- tehokas  
- keskitetty valvonta  
- vähemmän ylläpidettävää  

**Haitat:**

- suurempi riski, jos agentti tekee virheen  
- monimutkaisemmat rajaukset ja governance-mallit  

---

## 4. EU AI Act suosii mallia, jossa:

- agentilla on selkeä käyttötarkoitus  
- agentin autonomia on rajattu  
- ihminen valvoo agenttia  
- agentti ei tee päätöksiä ilman hyväksyntää  
- agentti toimii vain niissä rajoissa, jotka yritys on määritellyt  

Tämä on linjassa AI Actin riskiperusteisen lähestymistavan kanssa.

---

## 5. Käytännön tarkistuslista ennen agentin rakentamista

1. **Määrittele käyttötarkoitus**  
   Mihin agenttia tarvitaan?

2. **Arvioi riskiluokka (AI Act)**  
   Onko agentti:  
   - vähäriskinen  
   - korkean riskin  
   - erittäin korkean riskin (GPAI)

3. **Määrittele rajat ja oikeudet**  
   Mitä agentti saa tehdä?  
   Mitä se ei saa tehdä?

4. **Suunnittele valvonta**  
   Kuka hyväksyy agentin toimet?  
   Miten lokitus toimii?

5. **Suunnittele fallback**  
   Mitä tapahtuu, jos agentti epäonnistuu?

6. **Dokumentoi kaikki**  
   AI Act edellyttää dokumentaatiota ja jäljitettävyyttä.

---

## 🔷 Yhteenveto

- Kyllä, yrityksen on ensin kysyttävä miksi ja mihin tarkoitukseen agentti rakennetaan  
- Kyllä, tämä on EU AI Actin vaatimus  
- Kyllä, agentin käyttömalli on valittava — mutta valvottavasti  
- Kyllä, malli voi olla henkilökohtainen tai yhteinen, riippuen käyttötarkoituksesta ja riskitasosta  
- EU AI Act ohjaa vahvasti siihen, että agentit ovat rajattuja, valvottuja ja dokumentoituja

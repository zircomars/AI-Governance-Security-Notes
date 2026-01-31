# EU AI Act – Riskiluokittelu, raportointi ja toimialakohtaiset esimerkit

EU AI Act perustuu riskiperusteiseen malliin, jossa tekoälyjärjestelmät luokitellaan neljään riskitasoon. Riskiluokka määräytyy **käyttötarkoituksen**, ei teknologian, ohjelmointikielen tai tuotemuodon perusteella. Riskiluokittelu ei ole kertaluonteinen tehtävä, vaan jatkuva prosessi, joka edellyttää dokumentointia ja säännöllistä raportointia organisaation sisällä.

---

## 1. Riskiperusteinen luokittelu

| Riskitaso | Esimerkkejä | Velvoitteet |
|-----------|-------------|-------------|
| **Kielletty** | Sosiaalinen pisteytys, manipuloiva AI, biometrinen profilointi | Täysin kielletty |
| **Korkea riski** | Rekrytointi, luottopäätökset, terveydenhuolto, kriittinen infrastruktuuri, robotiikka tietyissä käyttötarkoituksissa | Tiukat vaatimukset: dokumentointi, riskienhallinta, data governance, CE-merkintä |
| **Rajoitettu riski** | Chatbotit, generatiivinen AI, asiakaspalvelubotit, markkinointiautomaatio | Läpinäkyvyysvaatimukset |
| **Vähäinen riski** | Pelit, suodattimet, sisäiset työkalut, koodigenerointi | Ei erityisiä velvoitteita |

---

## 2. Kielletty AI – lisäesimerkkejä

Kiellettyjä ovat järjestelmät, jotka aiheuttavat merkittävää haittaa perusoikeuksille.

- tunteiden tunnistus työpaikalla tai koulussa  
- reaaliaikainen kasvojentunnistus julkisissa tiloissa (poikkeuksin)  
- poliittinen manipulointi AI:n avulla  
- haavoittuvien ryhmien manipulointi  

---

## 3. Korkean riskin AI – laajennettu lista

Korkean riskin AI edellyttää:

- teknistä dokumentaatiota  
- riskienhallintaa  
- datan laadun varmistamista  
- valvontaa ja audit trail -tietoja  
- CE-merkintää ennen markkinoille pääsyä  

### A) Työelämä ja HR
- rekrytointipäätökset  
- työntekijöiden arviointi  
- automatisoidut soveltuvuustestit  

### B) Rahoitus
- luottokelpoisuusarviointi  
- lainapäätökset  
- petosten tunnistus, jos se vaikuttaa oikeuksiin  

### C) Terveydenhuolto
- diagnostiikka  
- hoitosuositukset  
- lääkinnälliset laitteet, joissa on AI-komponentti  

### D) Kriittinen infrastruktuuri
- energia  
- liikenne  
- vesihuolto  
- teollisuusautomaatio  

### E) Robotiikka
Robotiikka on korkean riskin AI, jos se:

- tekee itsenäisiä päätöksiä  
- voi aiheuttaa fyysistä vahinkoa  
- toimii sairaaloissa, tehtaissa tai logistiikassa  

---

## 4. Rajoitetun riskin AI – lisäesimerkkejä

- asiakaspalveluchatit  
- generatiivinen AI (teksti, kuva, ääni)  
- markkinointiautomaatio  
- sisällönsuodatus  
- analytiikka, joka ei tee päätöksiä ihmisten puolesta  

Velvoitteet:  
- käyttäjälle kerrottava, että AI on käytössä  
- sisällön alkuperä ilmoitettava (esim. “tämä teksti on tuotettu AI:n avulla”)  

---

## 5. Vähäisen riskin AI – lisäesimerkkejä

- pelien tekoäly  
- kameran suodattimet  
- koodigenerointi (Python, C#, JavaScript jne.)  
- sisäiset automaatiot  
- API-pohjaiset työkalut, jotka eivät tee päätöksiä ihmisten puolesta  
- exe-ohjelmat, jotka eivät vaikuta oikeuksiin  

---

## 6. Riskiluokittelu eri toimialoilla

Riskiluokka riippuu **vain käyttötarkoituksesta**, ei teknologiasta.

| Toimiala | Esimerkki | Riskiluokka |
|----------|-----------|-------------|
| Teollisuus | autonominen robotti | Korkea |
| Teollisuus | tuotannon optimointialgoritmi | Rajoitettu / vähäinen |
| Sairaalat | diagnostiikka | Korkea |
| Sairaalat | ajanvaraus-chatbot | Rajoitettu |
| Fitness | treeniohjelman suositus | Rajoitettu |
| Fitness | terveydentilan arviointi | Korkea |
| Konsultointi | sisäinen analytiikkatyökalu | Vähäinen |
| Ohjelmistokehitys | koodigenerointi | Vähäinen |
| Markkinointi | generatiivinen sisällöntuotanto | Rajoitettu |
| Pankki | luottopäätökset | Korkea |
| Valtio | sosiaalietuuksien päätöksenteko | Korkea |
| Valtio | asiakaspalvelubotti | Rajoitettu |

---

## 7. Riskiluokittelun raportointi ja hallinnollinen vastuu

Riskiluokittelu ei ole tekninen yksityiskohta, vaan osa organisaation hallintamallia.

### Raportointi suositellaan tehtäväksi:

- **ennen kehityksen aloittamista**  
- **kehityksen aikana**  
- **julkaisun yhteydessä**  
- **kvartaalittain (3–4 kk välein)**  
- **aina merkittävän muutoksen yhteydessä**  

### Raportointi sisältää:

- riskiluokan perustelut  
- riskienhallintatoimet  
- datalähteet ja datan laatu  
- päivitysten vaikutukset  
- vastuut ja roolit  
- mahdolliset väärinkäyttötapaukset (misuse cases)  

### Raportointi hallitukselle / johtoryhmälle

Vaikka EU AI Act ei määrää tätä suoraan, ISO 27001 ja riskienhallinnan parhaat käytännöt edellyttävät:

- riskien raportointia ylimmälle johdolle  
- päätösten dokumentointia  
- riskien hyväksyntää tai hylkäämistä  
- jatkuvaa seurantaa  

---

## 8. Yhteenveto

- Riskiluokka määräytyy käyttötarkoituksen, ei teknologian perusteella.  
- Riskiluokittelu on jatkuva prosessi, ei kertaluonteinen tehtävä.  
- Raportointi hallitukselle tai johtoryhmälle on suositeltavaa.  
- Toimialat kuten terveydenhuolto, pankit, teollisuus ja julkinen sektori ovat lähes aina korkean riskin alueita.  
- Robotiikka voi olla korkean riskin AI, jos se voi aiheuttaa fyysistä vahinkoa.  
- Dokumentointi, riskienhallinta ja läpinäkyvyys ovat keskeisiä kaikissa riskitasoissa.  

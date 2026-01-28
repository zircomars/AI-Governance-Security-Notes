# API-avaimen validointi, lokitus ja järjestelmän reagointi – tekninen rakenne

Tässä kuvataan, mitä tapahtuu, kun API-avain syötetään järjestelmään, miten backend arvioi sen, mitä lokiin tallentuu ja miksi tekoäly ei tee päätöksiä tässä vaiheessa. Rakenne on kirjoitettu siten, että se on ymmärrettävissä DevOps‑, backend‑ ja network‑asiantuntijoille, mutta myös muille lukijoille, joilla ei ole syvää teknistä taustaa.

Tämä osio toimii samalla pohjana sille, miten Shadow AI ‑tilanne voi syntyä, jos API‑avain päätyy vahingossa tekoälyn chattiin. Kuvauksessa avataan yksityiskohtaisemmin, miten järjestelmä käsittelee avaimen, miten lokitus muodostuu ja miten tapahtumaketju etenee teknisestä näkökulmasta.

Tässä kappaleessa on kaksi esimerkkiä, joista toinen sisältää yksityiskohtaisempaa tietoa. Molemmissa kuvataan samaa tapahtumaketjua, mutta eri tarkkuustasoilla. Toistoa esiintyy tarkoituksella, jotta Shadow AI ‑tilanne voidaan hahmottaa sekä yleisellä tasolla että teknisesti syvennettynä. Näiden esimerkkien avulla avataan, miten API‑koodi tai token voi päätyä tekoälyn chattiin ja mitä järjestelmässä tapahtuu vaiheittain.


> 📅 Kirjoitettu tammikuussa 2026. Sisältö voi päivittyä tai tarkentua myöhemmin.

---

## 🔹 1. API-avain voi olla mikä tahansa merkkijono

- Esimerkiksi `API_KEY = "1234"` voi olla täysin validi ja tuotantokäytössä.
- Merkitys ei ole avaimen muodossa, vaan siinä, mitä backend tietää siitä.
- Avaimen arvo syntyy vasta tarkistuspisteessä.

---

## 🔹 2. Tarkistuspiste (auth / validation) määrittää hyväksynnän

Kun pyyntö saapuu, järjestelmä ei kysy “onko tämä hyvä koodi”, vaan arvioi kokonaisuuden:

1. Onko pyyntö suunnattu endpointiin?
2. Onko mukana API-avain?
3. Onko avain aktiivinen?
4. Onko IP sallittu tälle avaimelle?
5. Mitä avain saa tehdä?
6. Onko pyyntö teknisesti oikein?

✅ Vasta jos kaikki täsmää, pyyntö menee eteenpäin.

---

## 🔹 3. Jokaisesta pyynnöstä syntyy loki

Lokitiedot muodostuvat IP-osoitteesta, käyttötarkoituksesta ja lopputuloksesta.

**Esimerkki epäonnistuneesta:**
```
TIMESTAMP: 2026-01-20 14:03:11
API_KEY_ID: 1234
SOURCE_IP: 185.xxx.xxx.xxx
ENDPOINT: /v1/automation/run
RESULT: DENIED (IP not allowed)
```


**Esimerkki onnistuneesta:**
```
RESULT: OK
ACTION: EXECUTE_WORKFLOW
```


🔸 Tämä tapahtuu riippumatta siitä, onko avain “oikea” vai ei.

---

## 🔹 4. Järjestelmä ei luota API-avaimeen yksin

API-avain toimii vain yhtenä signaalina. Todellinen päätös tehdään:

- IP-osoitteen perusteella  
- roolien perusteella  
- aikarajojen perusteella  
- käyttötavan perusteella  

Sama avain voi toimia yhdestä paikasta mutta epäonnistua toisesta.

---

## 🔹 5. Onnistuminen ja epäonnistuminen – molemmat lokitetaan

| Tapahtuma | Jääkö jälki? |
|-----------|--------------|
| Väärä avain | ✅ Kyllä |
| Oikea avain, väärä IP | ✅ Kyllä |
| Oikea avain, oikea IP | ✅ Kyllä |
| Virheellinen payload | ✅ Kyllä |

🔸 Ero näkyy vain siinä, mitä lokiin kirjoitetaan.

---

## 🔹 6. Tekoäly ei tee päätöksiä tässä vaiheessa

Jos kyseessä on AI-API:

- Tekoäly ei tarkista avainta  
- Tekoäly ei näe IP-osoitetta  
- Tekoäly ei lokita kutsua  

Kaikki tapahtuu ennen tekoälyä:
```
API Gateway → Auth → Rate limit → AI model
```

---
---

# API-avaimen käyttö, näkyvyys ja Shadow AI -riskit – tekninen purku - (START HERE);

Tässä kuvataan, mitä tapahtuu, kun API-avain syötetään järjestelmään tai tekoälyn chattiin. Kuvauksessa hahmotetaan, miten avain tallentuu, mihin se voi päätyä ja miksi tekoäly ei ole vastuussa. Rakenne toimii sekä teknisenä purkuna että puolustuksen roadmapina.

---

## 1. Konkreettinen esimerkki – mitä todella tapahtuu

**Tilanne:**

- API-avain syötetään (esim. "1234")
- Käyttö tapahtuu chatissa (esim. "Hei, käytä avainta '1234'")
- Tai avain syötetään Authorization-headeriin (esim. `Authorization: Bearer 1234`)

**Mihin se oikeasti menee:**

- logit  
- analytiikka  
- AI-mallit  
- Shadow AI  
  - ei tiedetä mihin menee  
  - ei tiedetä mitä tapahtuu  
  - ei tiedetä mitä malliin menee  

---

## 2. Syvempi tekninen purku

### 2.1 API-avaimen tekninen luonne

- API-avain = tunniste  
- ei ole identiteetti  
- ei ole varmistettu  
- ei ole turvallinen  

**Todellinen välimuisti:**

- logit  
- analytiikka  
- AI-mallit  

### 2.2 Mistä hyökkääjä voi päätellä mihin avain liittyy?

- palvelun nimi  
- endpoint  
- Authorization-header  
- käyttöympäristö  
- käyttötilanne  
- AI-malli  

---

## 3. Roadmap – mistä → mihin (puolustuksen näkökulma)

**VAIHE 1: Tunnistus**  
- mistä tiedetään  
- mistä tunnistetaan  

**VAIHE 2: Kartoitus**  
**VAIHE 3: Riskien arviointi**  
**VAIHE 4: Shadow AI -havainto**  
- mihin menee  
- mitä tapahtuu  
- mitä malliin menee  

**VAIHE 5: Hallinta**

---

## 4. Code / TXT -esimerkkejä

### 4.1 Yksinkertainen API-kutsu

Käyttäjä syöttää API-avaimen:
```
"Hei, käytä avainta '1234'"
Authorization: Bearer 1234
```

Palvelin saa:
```
"1234", "1234"
Authorization: Bearer 1234
```


### 4.2 Mitä palvelin näkee

- endpoint  
- Authorization-header  
- käyttöympäristö  
- käyttötilanne  

### 4.3 Lokimerkintä (tärkeä)

```
API-avain: 1234
endpoint: /chat
Authorization: Bearer 1234
käyttöympäristö: chat
käyttötilanne: käyttäjä syöttää avaimen ja pyytää
```


---

## 5. Shodan & julkinen näkyvyys

- Shodan = julkinen internet event  
- API-avain = tunniste  
- ei ole identiteetti  
- ei ole turvallinen  

---

## 6. Lyhyt teoria (muistiin)

- API-avain = tunniste  
- API-avain ≠ identiteetti  
- turvallisuus ei ole avaimessa  

---

## 7. Muistiinpanot – tiivis yhteenveto

**Mitä tapahtuu, jos API-koodi "1234" syötetään tekstinä (esim. chattiin):**

- menee palvelimelle  
- menee analytiikkaan  
- menee AI-malliin  
- menee logiin  
- menee välimuistiin  
- menee Shadow AI:hin  

**Jos avain syötetään oikeaan API-kutsuun:**
```
Authorization: Bearer 1234
```

Palvelin saa:

- endpoint: /chat  
- Authorization: Bearer 1234  
- käyttöympäristö: chat  
- käyttötilanne: käyttäjä syöttää avaimen  

---

## 8. Tekoälyn rooli ja näkyvyys

**Jääkö tekoälylle "oma lokitus" API-avaimesta?**

✅ AI-malli saa avaimen  
✅ AI-malli voi käyttää avainta  
✅ AI-malli voi muistaa avaimen  
✅ AI-malli voi oppia avaimesta  
✅ AI-malli voi jakaa avaimen  

**Näkeekö joku, että avainta kokeiltiin?**

✅ palvelin  
✅ analytiikka  
✅ AI-malli  
✅ Shadow AI  
✅ logit  

---

## 9. Entä jos avain on väärä tai merkityksetön?

**Ytimekäs vastaus:**

- API-avain = tunniste  
- ei ole identiteetti  
- ei ole turvallinen  
- menee palvelimelle, analytiikkaan, AI-malliin  
- menee logiin, välimuistiin, Shadow AI:hin  
- ei tiedetä mihin menee  
- ei tiedetä mitä tapahtuu  
- ei tiedetä mitä malliin menee  
- ei varmuutta siitä  

📅 Kirjoitettu tammikuussa 2026. Sisältö voi päivittyä tai tarkentua myöhemmin.


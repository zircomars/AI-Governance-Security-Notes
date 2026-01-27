# Shadow AI – yhteydet, tietoliikenne ja mobiilivalvonta

Tässä osiossa käsitellään, miten VPN, RDP, hotspotit, Wi-Fi ja MDM liittyvät shadow AI ‑riskien hallintaan järjestelmänvalvojan ja IT-tuen näkökulmasta.

Yhteyksien kautta sovellukset, verkkosivustot ja palvelut saavat yhteyden internetiin, jolloin data pääsee liikkumaan — esimerkiksi viestien lähettämisessä, päivityksissä tai tiedonsiirrossa. Suurin haaste liittyy siihen, miten yhteys suojataan ja valvotaan: tapahtuuko datan siirto hallitusti vai syntyykö shadow AI ‑tilanne huomaamatta.

→ Shadow AI voi syntyä missä tahansa yhteydessä, jos tekninen valvonta puuttuu tai ohitetaan. Siksi yhteyksien hallinta on olennainen osa tietoturvaa ja AI-politiikkaa.

### 1) VPN (Virtual Private Network)

✅ VPN suojaa liikennettä, mutta ei estä shadow AI:ta.

- VPN salaa yhteyden, mikä on hyvä asia  
- Käyttäjä voi silti ohjata dataa AI-palveluun  
- VPN ei estä ChatGPT:n, Gemini:n tai Copilotin käyttöä  
- VPN ei estä, mitä käyttäjä kirjoittaa tai lähettää  

🔒 VPN = liikenteen suoja, ei sisällön valvonta  
→ Shadow AI voi tapahtua VPN:n kautta, jos muita valvontakeinoja ei ole käytössä.

---

### 2) RDP (Remote Desktop Protocol)

✅ RDP ei estä shadow AI:ta, mutta voi paljastaa sen.

- RDP-yhteys voi näyttää, mitä sovelluksia käytetään  
- RDP voi paljastaa, jos AI-chat avataan  
- RDP antaa näkyvyyttä käyttäjän toimintaan  

🔍 RDP = näkyvyys, ei estoa  
→ Shadow AI voidaan havaita, mutta ei estää pelkällä RDP:llä.

---

### 3) Hotspotit ja mobiiliverkot

❌ Suurin yksittäinen riskikohta.

Jos käyttäjä:

- käyttää puhelimen hotspotia  
- ohittaa yrityksen verkon  
- käyttää henkilökohtaista mobiilidataa  

→ Kaikki valvonta (proxy, DNS, DLP, CASB) ohitetaan.

⚠️ Hotspot = valvonnan ulkopuolinen reitti  
→ Shadow AI voi tapahtua täysin näkymättömästi.

🛡️ Estämiseksi tarvitaan:

- MDM (Mobile Device Management)  
- VPN-pakotus  
- DNS-tunnistus  
- käyttöpolitiikat  
- mobiililaitteiden hallinta  

---

### 4) Wi-Fi-verkot (yrityksen vs. julkinen)

❌ Julkinen Wi-Fi = sama riski kuin hotspot

- ei valvontaa  
- ei estoa  
- ei DLP:tä  
- ei CASB:tä  
- ei auditointia  

✅ Yrityksen Wi-Fi = valvottavissa

- proxy  
- DNS  
- palomuuri  
- segmentointi  
- tunnistus  

🔒 Wi-Fi = turvallinen vain, jos hallittu

---

### 5) MDM (Mobile Device Management)

✅ MDM = paras tapa hallita mobiililaitteita ja shadow AI ‑riskiä

MDM voi:

- estää AI-sovellusten asennuksen  
- estää henkilökohtaisten tietojen hallinnan  
- pakottaa VPN:n käyttöön  
- valvoa sovelluksia ja liikennettä  
- erottaa työ- ja henkilöprofiilit  
- estää datan kopioinnin AI-palveluihin  

✅ MDM = tekninen kontrolli, joka estää shadow AI:n mobiilissa

---

### 6) Yhteenveto selkeästi

| Yhteystyyppi        | Estää shadow AI:n? |
|---------------------|--------------------|
| VPN                 | ❌ Ei – suojaa liikennettä, ei sisältöä |
| RDP                 | ⚠️ Osittain – näkyvyys, ei estoa |
| Hotspot             | ❌ Ei – ohittaa kaiken valvonnan |
| Julkinen Wi-Fi      | ❌ Ei – sama riski kuin hotspot |
| Yrityksen Wi-Fi     | ✅ Kyllä – jos proxy/DNS/DLP käytössä |
| MDM                 | ✅ Kyllä – paras tapa hallita mobiilivarusteita |

🟦 Yksi lause, joka kiteyttää kaiken  
VPN, RDP ja Wi-Fi suojaavat yhteyttä, mutta vain MDM ja verkon valvonta voivat estää shadow AI:n syntymisen — erityisesti mobiililaitteissa ja hotspot-yhteyksissä.

# Shadow AI ja virtualisointi

## 1) Virtualisointi ei aiheuta shadow AI:ta

Virtuaalikoneet (VMware, VirtualBox, Hyper‑V, Proxmox, QEMU) eivät aiheuta shadow AI:ta, jos niitä käytetään offline‑tilassa tai vain paikallisesti.  
Shadow AI syntyy vain, jos:

- data lähtee internetiin  
- data lähetetään ulkopuoliseen AI‑palveluun  
- data päätyy palveluntarjoajan palvelimille  

Virtuaalikone toimii eristettynä ympäristönä eikä tee mitään automaattisesti.

---

## 2) Milloin shadow AI voi tapahtua virtuaalikoneessa?

Shadow AI voi syntyä vain, jos käyttäjä itse kopioi virtuaalikoneen dataa AI‑palveluun.  
Esimerkiksi:

- komentojen output (dmesg, journalctl, ps aux)  
- konfiguraatiot  
- lokitiedot  

→ Jos nämä liitetään ChatGPT Free / Gemini Free / Copilot Free ‑palveluun, syntyy shadow AI.

Virtuaalikone ei tee tätä itse eikä lähetä dataa AI:lle ilman käyttäjän toimintaa.

---

## 3) Onko Linux‑outputin syöttäminen AI:lle vaarallista?

Turvallista:

- geneerinen komentojen output  
- pakettilistat  
- testidata  
- esimerkkikonfiguraatiot  
- omat harjoitusprojektit  

Vaarallista:

- tuotantopalvelimen lokit  
- asiakkaan tiedot  
- sisäiset IP‑osoitteet  
- salaisuuksia sisältävät konfiguraatiot  
- API‑avaimet  
- käyttäjätunnukset  
- tietokantayhteydet  

→ Virtuaalikone ei ole riski — data voi olla riski.

---

## 4) Voiko shadow AI tapahtua ilman internetiä?

Ei voi.  
Shadow AI syntyy vain, jos data lähetetään ulkopuoliseen AI‑palveluun.

---

## 5) Miten tämä kannattaa hahmottaa?

- Virtuaalikone = hiekkalaatikko  
- Shadow AI = data, joka viedään ulos hiekkalaatikosta  

---

## 6) Yhteenveto

Virtuaalikone ei aiheuta shadow AI:ta.  
Shadow AI syntyy vain, jos käyttäjä itse kopioi dataa ja syöttää sen ulkopuoliseen AI‑palveluun.  
Offline‑labra on täysin turvallinen, kunhan oikeaa dataa ei syötetä AI:lle.

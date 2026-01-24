# AI-Governance-Security-Notes

A repository focused on AI safety, general AI usage practices, and security considerations for both personal and enterprise accounts. Includes notes related to cybersecurity, penetration testing, and an overview of the EU AI Act.

- Tähän repo tulee koskien **Shadow AI** – eli tekoälyn haavoittuvuutta, joka leviää verkkoonsa, ja mitä se oikein tarkoittaa.  
- **AI Pentest** eli penetraatiotesti tarkoittaa eettistä hakkerointia, jossa sekä hyökkäävä että suojeleva tiimi testaa, miten suojata yrityksen palveluita, kuten verkkosivustoja, palvelimia ja muita sovelluksia.  
- **EU AI Act** tarkoittaa Euroopan tekoälylain säädöstä/asetusta, joka tuli voimaan vuonna keväällä 2025. Tämä asetus kertoo, mitä se tarkoittaa ja ketä se koskee.


![alt text](/images/AI-law-concept-img.jpg) 

---

# Tekoälyn chättin käyttö 

Tekoläyn avulla voi rakentaa monipuolisia asioita mm.
- Koodeja (hyökkääviä koodeja/haittaohjelmia tai muuta virusta tai auttaa rakentaa normaalisen koodinsa esim. Skriptejä tai muuta koodi projekteja kuten HTML5 tai syvempiä ohjelmointia C#, Python  ja jne).
	- haavoittuvuutta hyödyntävä menetelmä (Exploit - Hyödyntäminen on menetelmä tai koodinpätkä, joka hyödyntää ohjelmistojen, sovellusten, verkkojen, käyttöjärjestelmien tai laitteiston haavoittuvuuksia tyypillisesti haitallisiin tarkoituksiin. 
- Deepfake (syväväärennös - esim. Henkilö ei ole sanonut tällaista lauseta tai säkeistöä, mutta tekoäly teki sen mm. käyti ihmisten kieltä, sitä huulen liikuvuutta ja jne).
- Viestintä korjauksia - kirjoitusvirheitä ja normaali viestintää varten.

**Syksy 2025**:
- Chat-pohjainen tekoäly voi antaa ohjeita käyttäjälle eri sovellusten tai järjestelmien käyttöön. Esimerkiksi se voi neuvoa, mistä löytää tietyn lomakkeen tai painikkeen, tai miten tehdä muutoksia pilvipalvelussa. Tekoäly ei kuitenkaan tee muutoksia automaattisesti ilman asianmukaista integraatiota.
- Tekoälyn käytön rajoitukset: Tekoäly ei välttämättä pysty seuraamaan sovelluksen tilannetta reaaliajassa. Esimerkiksi, jos kysytään subscription-tyypistä (ilmainen, premium, prioriteetti), tekoäly voi antaa ohjeita vain sen tiedon perusteella, joka on sille saatavilla. Ohjeet voivat olla vanhentuneita, ja tekoäly joutuu itse analysoimaan, mikä ohje pätee ajankohtaisesti.
  - Esimerkkejä:  
  - Microsoft Azure -pilvipalvelu: tekoäly voi kertoa, että lisenssi on ilmainen, P1 tai P2, mutta se ei näe suoraan käyttäjän tilannetta.  
  - Microsoft Office -työkalut: Tekoäly ei tiedä aluksi, onko käyttäjällä selainpohjainen versio vai työasemaohjelma (desktop). Esimerkiksi, jos käyttäjä haluaa tehdä Excelissä pylväskaavion, tekoäly saattaa aluksi antaa ohjeet desktop-version mukaan. Kun käyttäjä kertoo käyttävänsä selainta, tekoäly ymmärtää tilanteen ja antaa ohjeet selainversion mukaisesti.

## Hyviä ja huonoja puolia

### Tässä hyvänä puolena:
- Perus tasolla tekoäly auttaa käyttäjää kirjoittamaan nopeammin ja antaa jatkoehdotuksia, jos käyttäjä haluaa.
- Tekoäly voi tallentaa keskusteluja, jos käyttäjä on kirjautunut sisään, esimerkiksi Google-, Apple- tai Outlook (Microsoft) -tunnuksilla.
  - Usein jokainen uusi keskustelu aloitetaan uutena aiheena, eli aikaisemmat keskustelut eivät automaattisesti jatku.
  - Tästä hyvänä puolena on se, että tekoäly voi joissain tapauksissa hakea rajoitetusti aiempia keskusteluita (esim. päivien, viikkojen tai kuukausien takaa).
  - Tämä ominaisuus näkyy erityisesti **Microsoft Copilot** -tekoälyssä (Viimeisin tieto syksy 2025).
  - Copilot pystyy hyödyntämään aikaisempia keskusteluita, mutta se ei välttämättä pysty tuomaan vanhoja keskusteluita (esim. yli viikon tai kuukauden takaa) suoraan takaisin näkyviin. Sen sijaan se voi muistuttaa käyttäjää ja antaa ohjeita aiempien keskusteluiden perusteella.

### Huono puolet:
- Monille huono puoli on se, että keskustelut joudutaan usein aloittamaan alusta, ja aikaisemmissa versioissa tai palveluissa on ollut rajoituksia keskusteluiden määrään (esim. rajoitettu määrä viestejä yhdessä keskustelussa).
- Joissakin tekoälypalveluissa istunto voi olla rajoitettu. Tämän jälkeen istunto sulkeutuu ja käyttäjä joutuu aloittamaan uuden keskustelun. Tämä koskee erityisesti **ChatGPT:tä**, jos käyttäjä ei ole kirjautunut sisään (Viimeisin tieto syksy 2025).
- Yksi huono puoli on se, että käyttäjän täytyy antaa selkeitä ohjeita ja promptata tekoälyä oikein, jotta se ymmärtää, mitä siltä halutaan.
- Jos käyttäjä pyytää tekoälyä kirjoittamaan tai korjaamaan tekstiä hänen puolestaan, tekoäly ei välttämättä aina osaa tuottaa juuri käyttäjän haluamaa sävyä (esim. kirjallinen vs. suullinen tyyli) ilman tarkempia ohjeita.


**Huomio (syksy 2025):**  
- Hyvinä ja huono puolena, tästä riippuu käyttäjästä miten käyttää tekoälynsä. Osat saattaa huomata sen käytönsä, että pitääkö paikkaansa, ja se ei välttämättä pysty lukemaan käyttäjän sielua ja ajatusta, mitä käyttäjä haluaa seuraavaksi. Useimmin tekoälyn kanssa joutuu kuin opettaa pienen palan, jotta se ymmärtää, ja tästä pätee myös muita tekoälyn sovelluksia ja työkaluja, kuten VSCode:n oma tekoäly, nettisivustojen oma tekoälychätti jne. Tästä riippuu tekoälyn kehityksestä, miten käyttäjä syöttää sen kenttään.

---

## Tekoälyn tulevaisuus

Usein IT/ICT maailmassa tekoälyssä usein käytetään näitä asioita mm:
- Säästä aikaa automatisoimalla toistuvia tehtäviä.
- Sellaisten oivallusten luominen, joiden paljastaminen vei kerran aikaa.
- Päätöksenteon parantaminen ennakoivilla malleilla ja data-analyysillä.
- Sisällön luominen tekoälytyökalujen avulla markkinointiin ja asiakaspalveluun.

Ehkä saatetaan jopa rakentaa erillisenä elektroniina omana laiteena, joka tekee jotakin liikuvuutta/fyysistä:
- Logistiikka esim. Automatisoitu ohjelma joka liikuttaa jotakin painavaa laatikkoa ja seuraamalla tiettyä reittiä - samalla edessä/takana on videokamera, josta reagoi ja skannaa mitä niissä voi tapahtua ja mitä pitäisi tehdä.


## Promptausta

Promptaamalla kerrotaan tekoälylle, mitä sen halutaan tekevän – se on siis kehotteiden kirjoittamista. Yksinkertaisimmillaan prompti voi olla vain esimerkiksi kehote ”kirjoita somepostaus joulunvietosta”, mutta ensimmäisiä kertoja tekoälytyökaluja käyttävälle voi tulla pettymyksenä, että upeat tulokset eivät sittenkään synny vain kertomalla muutamalla sanalla, mitä haluaa. 
- Tästä usein vaattii paljon toistoa, että jota se alkaa ymmärtämään.

# Generatiivinen tekoäly (GenAI)
Generatiivinen tekoäly (GenAI) on tekoälyn osa-alue, joka luo uutta, alkuperäistä sisältöä, kuten tekstiä, kuvia, musiikkia, koodia tai videoita, oppimalla valtavista datamääristä. Se eroaa perinteisestä tekoälystä, joka toimii ennalta määriteltyjen sääntöjen mukaan, sillä generatiivinen tekoäly tunnistaa malleja ja tuottaa sen perusteella uutta, ihmisen luomaa muistuttavaa sisältöä, usein käyttäjän antaman kehotteen (promptin) pohjalta, esimerkiksi ChatGPT, Gemini, DALL-E ja Midjourney ovat tunnettuja esimerkkejä. 





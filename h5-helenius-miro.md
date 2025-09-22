# Haaga-Helia Ammatikorkeakoulu Linux Palvelimet 2025 - Tero Karvinen 

## Tehtävä h5 nimekäs 

Tässä raportissa vuokrasin domainin ja laitoin sen osoittamaan aikaisemmin vuokraamani virtuaalipalvelimeen. 

## Host-operating system spesifikaatiot
  - Operating system: Windows 11 Home
  - Version	10.0.26100 Build 26100
  - Device name	BOOK-QUCSCTFCNT
  - Processor	13th Gen Intel(R) Core(TM) i7-1360P (2.20 GHz)
  - Installed RAM	16,0 GB (15,6 GB usable)
  - System type	64-bit operating system, x64-based processor
  - Pen and touch	Pen and touch support with 10 touch points

# a) Julkisen nimen osoittaminen omaan palvelimeen

Valitsin domain nimen vuokraamiseen "NameCheap", koska olin kuullut siitä suosituksia. Tukeuduin domain nimen vuokraamisessa seuraavaan blogiin: https://susannalehto.fi/2022/teoriasta-kaytantoon-pilvipalvelimen-avulla-h4

Aloitin nimen vuokraamisen menemällä NameCheap kotisivuille: https://www.namecheap.com. Tarkistin onko domain "mirohelenius.com" saatavilla. Domain oli saatavilla, joten lisäsin sen ostoskoriin ja loin tunnuksen palveluun. Siirryin ostoskoriin ja tarkastin, että oikea domain on valittuna. Valitsin vuokrauksen ajaksi vuoden ja jatkoin tietojen täyttämistä. Valitsin myös "Domain Privacy" -vaihtoehdon, koska se estää henkilökohtaisten tietojen näkymisen "whois" -komentoja käyttäessä. Nimipalvelimen asetukset jätin vakioksi, eli käytön NameCheap:in omaa perus nimipalvelua. Lisäsin maksutiedot ja maksoin tilaukseni. Lopputuloksena minulla on nyt omalla nimelläni vuokrattu domaini. 

NameCheap kotisivu

<img width="2734" height="1524" alt="image" src="https://github.com/user-attachments/assets/69671fc1-6d74-4bed-b178-ef6a6781d062" />

Domain nimen hakutulos

<img width="2742" height="1536" alt="image" src="https://github.com/user-attachments/assets/f7155d5b-8b89-47ff-bc05-1bf7c1aba1fd" />

Dashboard kirjautumisen jälkeen

<img width="2738" height="1468" alt="image" src="https://github.com/user-attachments/assets/c099114f-8ecb-4459-9d0a-8b5fe775ed46" />

Ostoskori

<img width="1998" height="502" alt="image" src="https://github.com/user-attachments/assets/2a3e7317-138f-4e4d-bb71-ae1b5ee19177" />

<img width="2018" height="750" alt="image" src="https://github.com/user-attachments/assets/902d4227-d0d8-444d-871c-1d7d82732952" />

Domain Dashboardissa

<img width="2372" height="1286" alt="image" src="https://github.com/user-attachments/assets/b46c11ac-b278-494c-895e-be2fdd7553d4" />

# Domain nimen ohjaaminen omalle palvelimelle 

Seuraavaksi laitoin domainnimen osoittamaan vuokraamani palvelimeen UpCloudin verkkosivuilta. Dashboard näkymästä valitsin valikon "Advanced DNS". Host Records valikon alta valitsin "CNAME Record" ja "URL Redirection Record", poistin ne ja klikkasin punaista "Add New Record" -nappia. Loin uuden A -tietueen, miksi? A-tietue ohjaa/kääntää domainien nimet IPv4 osoitteiksi. Laitoin host nimeksi "upcloud", IP-osoitteeseen palvelimen osoitteen ja TTL ajaksi "5Min". Lopuksi tallensin muutokseni rivin oikeasta reunasta vihreää kuittaus merkkiä painamalla. 

Advanced DNS -valikko 

<img width="2728" height="1510" alt="image" src="https://github.com/user-attachments/assets/504d2534-8628-4623-b23e-20739d59270d" />


<img width="2350" height="1180" alt="image" src="https://github.com/user-attachments/assets/f84a6a0e-cac8-4ca4-82df-4c6038ef172c" />

Seuraavaksi testasin toimiiko mirohelenius.com. Ei näyttänyt vielä toimivan, kävin aktivoimasta kontaktitietoni NameCheapille ja kokeilen uudestaan myöhemmin. 

<img width="2732" height="1502" alt="image" src="https://github.com/user-attachments/assets/7c8a9341-57d1-41bb-8e70-c83741469e5b" />


# b) Alidomaininen luominen palvelimelle

Tässä raportin vaiheessa loin kaksi uutta alidomainia mirohelenius.com:ille. Käytin apuna NameCheapin omaa ohjetta heidän verkkosivuilta: https://www.namecheap.com/support/knowledgebase/article.aspx/9776/2237/how-to-create-a-subdomain-for-my-domain

Käytin myös seuraavia ohjeita apuna: 
https://www.namecheap.com/support/knowledgebase/article.aspx/579/2237/which-record-type-option-should-i-choose-for-the-information-im-about-to-enter
https://www.namecheap.com/support/knowledgebase/article.aspx/319/2237/how-can-i-set-up-an-a-address-record-for-my-domain

Avasin Dashboardin ja menin "Domain List" -alivalikkoon. Valitsin oikealta "Verify Contants" -pudotusvalikosta "Manage". Tämän jälkeen pääsin domain -ikkunaan ja valitsin "Advanced DNS". Valitsin Host Records kohdasta, johon loin aikaisemmin jo A -tietueen "Add New Record". Tämän jälkeen loin vielä CNAME -tietueen. Vaihdoin samalla ensimmäisen A -tietueen isännän "@", koska tajusin, että se osoittaa juureen. Lopuksi tallensin molemmat. 

Loin uuden A -tietueen seuraavilla tiedoilla: 
- host about
- target palvelimen osoite
- TTL 5 Min
  
Loin CNAME -tietueen seuraavilla tiedoilla:
- host wwww
- target mirohelenius.com
- TTL 5 Min

<img width="2728" height="1290" alt="image" src="https://github.com/user-attachments/assets/9d43802e-b34c-4b70-a242-6ea6bb1078ac" />

<img width="2356" height="1514" alt="image" src="https://github.com/user-attachments/assets/343b0753-bb2f-4bde-a7c3-384af13afbf7" />

<img width="2737" height="1533" alt="image" src="https://github.com/user-attachments/assets/686551d3-04c2-48b0-9d04-cb862dd5ea1f" />

<img width="2256" height="676" alt="image" src="https://github.com/user-attachments/assets/f41a1a4d-4553-4e81-ac7a-df2d8c1933c6" />

<img width="2182" height="648" alt="image" src="https://github.com/user-attachments/assets/e7e1740a-4103-4948-b74c-0331e08b0f47" />

## Alidomainien testaaminen

Seuraavaksi testasin alidomainien toimimisen. Molemmat alidomainit toimivat siis halutusti.

about.mirohelenius.com

<img width="2878" height="896" alt="image" src="https://github.com/user-attachments/assets/ea7c063b-45d7-4fb0-9d68-611ad3a78fee" />


www.mirohelenius.com

<img width="2864" height="982" alt="image" src="https://github.com/user-attachments/assets/74f5d190-3617-4216-810a-fdc3e0ed5620" />




# c) nimen dns tietojen tukiminen komennoilla "host" ja "dig"

Tässä raportin vaiheessa testasin komentoja "host" ja "dig" palvelimeeni. Seuraavat artikkelit selittivät hyvin komentojen käyttötarkoitukset: 
https://phoenixnap.com/kb/linux-host ja https://phoenixnap.com/kb/linux-dig-command-examples 

Hyödynsin myös näitä artikkeleita komentojen toimintoja tutkiessa ja käyttäessä: https://www.geeksforgeeks.org/linux-unix/dig-command-in-linux-with-examples/ ja https://www.geeksforgeeks.org/linux-unix/host-command-in-linux-with-examples/

Jouduin asentamaan työasemalleni "DNS Utilities" -paketin, jotta sain kyseiset työkalut käyttööni. Käytin seuraavaa artikkelia apuna: https://webhostinggeeks.com/howto/how-to-fix-nslookup-host-dig-bash-command-not-found-in-linux 

Syötin virtuaalikoneeni terminaaliin seuraavat komennot:
<pre> 
  - sudo apt-get update
  - sudo apt-get install dnsutils
    

</pre>

<img width="2664" height="1016" alt="image" src="https://github.com/user-attachments/assets/7ffbfb56-dcb1-43a8-b0de-3e24c8eb0ded" />

<img width="2658" height="912" alt="image" src="https://github.com/user-attachments/assets/5d33c17b-1865-48d4-a3a8-41adfa95ef2f" />

Asentamisen jälkeen avasin molempien työkalujen Manual -page:sit ja selvitin kunkin työkalun tarkoituksen niiden ja akaisemmin mainitsemieni artikkeleiden avulla. 



## mirohelenius.com host ja dig -komentojen tulokset 


### Dig -komento 
Avasin terminaalin virtuaalikoneellani ja käytin komentoa "dig mirohelenius.com ANY". Kyseinen komento hakee kaikki DNS tietueet. https://www.geeksforgeeks.org/linux-unix/dig-command-in-linux-with-examples

<img width="2776" height="1474" alt="image" src="https://github.com/user-attachments/assets/9e7240c9-9f8b-4aac-91e8-21e4213efce5" />

### Host -komento 

Seuraavaksi syötin terminaaliin komennon "host mirohelenius.com". Host -komennolla lähtökohtaisesti haetaan domainin nimeä vastaava IP-osoite tai päinvastoin. 

<img width="2416" height="402" alt="image" src="https://github.com/user-attachments/assets/8b0ca8ab-6047-4473-93d9-390c90e84db1" />

<img width="2672" height="972" alt="image" src="https://github.com/user-attachments/assets/6ea6c6e1-6fc5-47d5-996b-8413a281fa06" />

### Tuloksien vertailu NameCheap käyttöliittymään

Kuten "dig"-komennon tuloksista näkyy niin luomani A-tietue NameCheapissa näkyy ja mihin IP-osoitteiseen sen viittaa. Vastaus sektion merkitykset olivat selitetty tässä artikkelissa kätevästi: https://www.uptimia.com/questions/what-do-the-five-fields-in-a-dig-querys-answer-section-mean

Vastauskohdan kentät vielä purettuna: 
- Domain Name Field - domainin nimi eli tässä tapauksessa mirohelenius.com.
- TTL - (Time To Live), kertoo miten pitkään DNS resolveri ja client säilöö tietuetta. 
- Class - eli luokka, tässä tapauksessa IN = Internet.
- Record Type Field - eli tietuetyyppi, luomani A -tietue näkyy ja muitakin. NS (Name Server) eli nimipalvelin ja SOA (Start Of Authority), määrittää DNS -alueen auktoritäärisen lähteen.
- IP Address Field, IP-osoitekenttä. Minun tapauksessani UpCloudissa luodun palvelimen osoite.

Kysyin ylläoleviin kenttiin tarkentavia kysymyksiä Microsoft CoPilotilta, koska DNS-teoria on vähän ruosteessa ja tämän tehtävän tarkoituksena ei ole sen läpikäyminen.


## Pienyrityksen tulokset host ja dig -komennolla

Valitsin pienyritykseen Varusteleka.com, ei välttämättä kovin pieni yritys nykyään, mutta menkööt tässä esimerkissä. Syötin terminaalin komennon "dig www.varusteleka.com ANY" ja sain seuraavat tulokset:

<img width="2422" height="1398" alt="varusteleka" src="https://github.com/user-attachments/assets/bef11a80-0153-4da9-b44c-025868375f31" />

Seuraavaksi syötin host komennon ja sain seuraavat tulokset: 

<img width="2446" height="216" alt="varusteleka host" src="https://github.com/user-attachments/assets/64593a12-34fe-43d0-aeda-a5dcc561750e" />



## Suuryrityksen tulokset host ja dig -komennolla

Tässä vaiheessa tarkastin suuryrityksen DNS -tietoja. Valitsin testiä varten NVIDIA:n. Syötin terminaliin komennon "dig www.nvidia.com ANY" ja sain seuraavan tuloksen:


<img width="2400" height="980" alt="nvidia" src="https://github.com/user-attachments/assets/4d7138da-8044-4ed5-b852-590e19240af8" />

Seuraavaksi ajoin komennon "host wwww.nvidia.com" ja sain seuraavan tulokset: 

<img width="2426" height="268" alt="nvidia host" src="https://github.com/user-attachments/assets/2d535445-3fa2-46a7-a0d7-c6bb8ed8058e" />





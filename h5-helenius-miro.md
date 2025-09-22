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

Jouduin asentamaan työasemalleni "DNS Utilities" -paketin, jotta sain kyseiset työkalut käyttööni. Käytin seuraavaa artikkelia apuna: https://webhostinggeeks.com/howto/how-to-fix-nslookup-host-dig-bash-command-not-found-in-linux 

Syötin virtuaalikoneeni terminaaliin seuraavat komennot:
<pre> 
  - sudo apt-get update
  - sudo apt-get install dnsutils
    

</pre>

<img width="2664" height="1016" alt="image" src="https://github.com/user-attachments/assets/7ffbfb56-dcb1-43a8-b0de-3e24c8eb0ded" />

<img width="2658" height="912" alt="image" src="https://github.com/user-attachments/assets/5d33c17b-1865-48d4-a3a8-41adfa95ef2f" />

Asentamisen jälkeen avasin molempien työkalujen Manual -pages ja selvitin kunkin työkalun tarkoituksen, vaikka hyödynsin jo artikkeleita, jotka mainitsin kappaleen alussa. 



## mirohelenius.com host ja dig -komentojen tulokset 


### Dig -komento 
Avasin terminaalin virtuaalikoneellani ja käytin komentoa "dig mirohelenius.com ANY". Kyseinen komento hakee kaikki DNS tietueet. https://www.geeksforgeeks.org/linux-unix/dig-command-in-linux-with-examples

<img width="2776" height="1474" alt="image" src="https://github.com/user-attachments/assets/9e7240c9-9f8b-4aac-91e8-21e4213efce5" />

### Host -komento 

Seuraavaksi syötin terminaaliin komennon "host mirohelenius.com". 

<img width="2416" height="402" alt="image" src="https://github.com/user-attachments/assets/8b0ca8ab-6047-4473-93d9-390c90e84db1" />


## about.mirohelenius.com host ja dig -komentojen tulokset


## www.mirohelenius.com host ja dig -komentojen tulokset


## Pienyrityksen tulokset host ja dig -komennolla

## Suuryrityksen tulokset host ja dig -komennolla



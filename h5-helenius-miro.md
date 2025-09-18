# Haaga-Helia Ammatikorkeakoulu Linux Palvelimet 2025 - Tero Karvinen 

## Tehtävä h5 nimekäs 

Tässä raportissa vuokrasin domainin ja laitoin sen osoittamaan aikaisemmin vuokraamani virtuaalipalvelimeen. 


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

Seuraavaksi laitoin domainnimen osoittamaan vuokraamani palvelimeen UpCloudin verkkosivuilta. Dashboard näkymästä valitsin valikon "Advanced DNS". Host Records valikon alta valitsin "CNAME Record" ja "URL Redirection Record", poistin ne ja klikkasin punaista "Add New Record" -nappia. Loin kaksi uutta A -tietuetta, miksi? A-tietue ohjaa/kääntää domainien nimet IPv4 osoitteiksi. Lopuksi tallensin muutokseni rivien oikeasta reunasta vihreää kuittaus merkkiä painamalla. 

Advanced DNS -valikko 

<img width="2728" height="1510" alt="image" src="https://github.com/user-attachments/assets/504d2534-8628-4623-b23e-20739d59270d" />

<img width="2202" height="620" alt="image" src="https://github.com/user-attachments/assets/5668ff92-f99b-40dc-9ff8-8d8a904ed4e5" />



# b) Alidomaininen luominen palvelimelle


# c) nimen dns tietojen tukiminen komennoilla "host" ja "dig"

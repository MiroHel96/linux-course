# Raportin kirjoittaminen 

## Raportin toistettavuus
-Raportin on oltava toistettavissa, jos toinen henkilö tekee vastaavat toimenpiteet.
-Raportissa on huomioitava spesifit tekniset tiedot ja muuttuja, koska eri verkot/laitteet toimivat eri tavalla.

## Raportin täsmällisyys
-Mitä teit, missä teit, milloin teit. Dokumentoi, vaiheittan onnistumiset ja epäonnistumiste.
-Täsmällisyys, esim kellonaikojen suhteen helpottaa vian täsmentämistä jälkikäteen.

## Raportin Helppolukuisuus
-Jäsentele raportti selkeästi väliotsikoilla, tarkasta kielioppi ennen julkaisua. Hyvä kielioppi antaa ammattimaisen kuvan.
-Raportin alkuun voi luoda raportin kattavan tiivistelmän. 

## Lähteisiin viittaaminen
-Laadukkaassa raportissa on viitatu oikeaoppisesti lähteeseen, kuuluu hyviin tapohin ja osoittaa perehtymisen aiheeseen.

## Raportin Vakiotekstejä
- Esimerkiksi, rarortin pohja, lisenssit, liitteet/lähteet. Tekevät raportista johdonmukaisen ja asiakohtaisen.

## Raportin pahoja mokia 
-Ympäripyöreät selittelyt ja valheellinen tieto yms. 

-Plagiointi kaikissa muodoissa kuvat 

## Lähteenä:
https://terokarvinen.com/2006/raportin-kirjoittaminen-4 - luettu 25.8.2025
 
# Linux asentaminen VirtualBox

Tässä raportissa asensin työasemalleni VirtualBoxin ja Virtuaalikäyttöjärjestelmäksi Linuxin. 

# VirtualBox Asennus


# Virtuaalityöaseman luominen VirtualBoxissa ja alkumäärityksien tekeminen

Aloitin käyttöjärjestelmän asentamisen hakemalla käyttöjärjestelmän ISO-tiedoston verkkosivulta "https://cdimage.debian.org/debian-cd/13.0.0-live/amd64/iso-hybrid". Jakelupaketiksi (Distro) valitsin "debian-live-13.0.0-amd64-standard.iso". 
<img width="1262" height="76" alt="image" src="https://github.com/user-attachments/assets/11d37e95-51bb-46fe-819b-4e4c136622a4" />

Tiedoston lataamisen jälkeen avasin VirtualBoxin. Valitsin vasemmasta yläkulmasta "new" ja tämän jälkeen aloin määrittämään perusasetukset virtuaalikoneelle.

<img width="1436" height="1292" alt="image" src="https://github.com/user-attachments/assets/5ad3a5bd-4feb-4752-92c5-f6738e070e0e" />

Määritin virtuaalikoneelle seuraavat perusasetukset:
VM Name: linux_palvelin
ISO Image: debian-live-13.0.0-amd64-standard.iso
OS: Linux
OS Distribution: Debian
OS Debian (64-bit) 

Proceed with Unattended Installation kohdasta jätin täpän pois, koska määritin asetukset myöhemmin manuaaliseti. 

<img width="1612" height="796" alt="image" src="https://github.com/user-attachments/assets/60dfdad0-3eee-431b-9e63-5a9e2329c841" />

Seuraavaksi määritin virtuaalikoneen käyttämät resurssit. RAM-muistia virtuaalikoneelle asetin 4GB (4096MB). Prosessoreiden määräksi asetin 2 ja levy kooksi asetin 40GB. 

<img width="1628" height="800" alt="image" src="https://github.com/user-attachments/assets/2692b544-2385-49ed-9cbc-4817db7a1f5a" />

Lopuksi yhteenveto asetetuista asetuksista. 
<img width="1614" height="794" alt="image" src="https://github.com/user-attachments/assets/48d85ae3-5402-4ec4-8ea4-43f5b88d3a99" />


# Linux -käyttöjärjestelmän asentaminen Virtuaalikoneeseen

TÄssä vaiheessa asensin Virtuaalikoneelleni Debian käyttöjärjestelmän. Valitsin virtuaalikoneeni ja klikkasin oikealla hiiten painikkeella virtuaalikoneella ja valitsin käynnistä.  

<img width="1442" height="1694" alt="image" src="https://github.com/user-attachments/assets/f3753003-26d8-4e2b-91bd-33824206897a" />

Käynnistämisen jälkeen virtuaalikoneen bootloader -valikosta valitsin "Live system (amd64). Tämä mahdollisti käyttöjärjestelmän tarkastelun ja kokeilun ennen asentamista. Tässä kohtaa tajusin teheeni virheen käyttöjärjestelmän ISO-tiedoston valinnassa. Kyseessä oli "Standard -versio, joka ei tuo graafista näkymää ollenkaan". 
<img width="1270" height="1010" alt="image" src="https://github.com/user-attachments/assets/8e91d77f-df71-4644-92b4-cbcf522cbd43" />

# Linux Asennus virtuaalikoneelle Yritys II 

Uudelle virtuaalikoneelle tein vastaavasti samat alkumääritykset ja asetukset kuin ensimmäisen koneen kohdalla. Poistin edellisen virtuaalikoneen ja vaihdoin uuden koneen käyttöjärjestelmän distron versioon "debian-live-13.0.0-amd64-xfce.iso". 

<img width="1268" height="74" alt="image" src="https://github.com/user-attachments/assets/72fcda89-1816-44d1-a516-e5b93f093b90" />

<img width="1586" height="1082" alt="image" src="https://github.com/user-attachments/assets/b0235b94-a39c-4c31-a304-b81c894f68ac" />


Alkumäärityksen ja virtuaalikoneen luomisen jälkeen testasin GUI:n toimivuuden Live systemin avulla. Tällä kertaa käyttöjärjestelmän image oli valittu oikein ja lähti toimivaan halutusti. 
<img width="1530" height="1160" alt="image" src="https://github.com/user-attachments/assets/c821bd00-d481-4891-8a0a-08382ccc911f" />

Live testin jälkeen sammutin virtuaalikoneen ja käynnistin sen uudestaan. Aloitin käyttöjärjestelmän asentamisen virtuaalikoneelleni ja määritin seuraavat asetukset: 

Kieli English
Sijainti Finland
Locales en-US.UTF-8
Näppäimistön kieli finnish


<img width="1526" height="1164" alt="image" src="https://github.com/user-attachments/assets/4bbbed83-970f-467c-a066-34caa2bf1d02" />

<img width="1526" height="1162" alt="image" src="https://github.com/user-attachments/assets/2eceaa24-4825-4704-b76e-1f7cadea1091" />

<img width="1530" height="1160" alt="image" src="https://github.com/user-attachments/assets/ab88941a-31aa-4afc-8c6e-4bb7b0e98d5d" />

<img width="1536" height="1166" alt="image" src="https://github.com/user-attachments/assets/60a60584-1644-48f7-be72-73c5794501a4" />

Sijainti- ja kieliasetuksien jälkeen jatkoin määrittämään virtuaalikoneen verkkoasetuksia. 

Määritin seuraavat asetukset verkolle:

Hostname linux-palvelimet-test
Domain miroServer.com


<img width="1526" height="1178" alt="image" src="https://github.com/user-attachments/assets/6d8b2420-43fd-42f3-aa6f-92ec3b186803" />

<img width="1538" height="1154" alt="image" src="https://github.com/user-attachments/assets/42d8a15b-3ad4-4022-adf8-d8ba86785816" />

Seuraavaksi määritin käyttäjätunnukset virtuaalikoneeleni. Root -käyttäjälle jätin salasanakentän tyhjäksi ja jatkoin määrittämään peruskäyttäjän nimen ja salasanan. 

<img width="1530" height="1172" alt="image" src="https://github.com/user-attachments/assets/03657462-b4bf-480c-9271-2b27ddfda7df" />








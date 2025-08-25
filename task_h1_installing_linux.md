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


# Linux asentaminen VirtualBoxiin

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









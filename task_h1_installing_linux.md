# Raportin kirjoittaminen 

Tämä raportti on kirjoitettu "https://terokarvinen.com/linux-palvelimet/#h0-hei-weppi", h1 Oma Linux tehtävän pohjalle. 

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
- Esimerkiksi, raportin pohja, lisenssit, liitteet/lähteet. Tekevät raportista johdonmukaisen ja asiakohtaisen.

## Raportin pahoja mokia 
-Ympäripyöreät selittelyt ja valheellinen tieto yms. 
-Plagiointi kaikissa muodoissa kuvat 
 
# Linux käyttöjärjestelmän asentaminen VirtualBox

Tässä raportissa käyn vaihettain läpi virtuaalikoneen luomisen Linux-käyttöjärjestelmällä VirtualBoxiin. 

# VirtualBox Asennus

VirtualBox oli jo asennettu työasemalla aikaisemmin ja se ei ollut vaatimuksena tehtävänannossa "h1 Oma Linux". Tästä syystä VirtualBox asennusta ei käydä tässä raportissa läpi.

# Virtuaalityöaseman luominen VirtualBoxissa ja alkumäärityksien tekeminen

Virtuaalityöasema on asennettu lähtökohtaisesti seuraavaa ohjetta noudattaen, muutamia asetuksia lukuunottamatta. 
"https://github.com/johannaheinonen/johanna-test-repo/blob/main/linux-20082025.md"

Esitietona raporttia lukevalle, tein virheen versiovalinnassa ja huomasin tämän vasta virtuaalikoneen luomisen yhteydessä. Käyn kuitekin läpi asennuksen vaihettain, koska asennusprosessi on muuten sama.

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

"Proceed with Unattended Installation" kohdasta jätin täpän pois.

<img width="1612" height="796" alt="image" src="https://github.com/user-attachments/assets/60dfdad0-3eee-431b-9e63-5a9e2329c841" />

Seuraavaksi määritin virtuaalikoneen käyttämät resurssit. RAM-muistia virtuaalikoneelle asetin 4GB (4096MB). Prosessoreiden määräksi asetin 2 ja levy kooksi asetin 40GB. 

<img width="1628" height="800" alt="image" src="https://github.com/user-attachments/assets/2692b544-2385-49ed-9cbc-4817db7a1f5a" />

Lopuksi yhteenveto asetetuista asetuksista. 
<img width="1614" height="794" alt="image" src="https://github.com/user-attachments/assets/48d85ae3-5402-4ec4-8ea4-43f5b88d3a99" />


# Linux -käyttöjärjestelmän asentaminen Virtuaalikoneeseen

TÄssä vaiheessa asensin Virtuaalikoneelleni Debian käyttöjärjestelmän. Valitsin virtuaalikoneeni ja klikkasin oikealla hiiten painikkeella virtuaalikoneella ja valitsin käynnistä.  

<img width="1442" height="1694" alt="image" src="https://github.com/user-attachments/assets/f3753003-26d8-4e2b-91bd-33824206897a" />

Käynnistämisen jälkeen virtuaalikoneen bootloader -valikosta valitsin "Live system (amd64). Tämä mahdollisti käyttöjärjestelmän tarkastelun ja kokeilun ennen asentamista. Tässä kohtaa tajusin teheeni virheen käyttöjärjestelmän ISO-tiedoston valinnassa. Kyseessä oli "Standard -versio, joka ei tue graafista näkymää ollenkaan". StackExchange Uniz & Linux "https://unix.stackexchange.com/questions/87182/whats-the-difference-between-debian-standard-and-gnome".

<img width="1270" height="1010" alt="image" src="https://github.com/user-attachments/assets/8e91d77f-df71-4644-92b4-cbcf522cbd43" />

# Linux Asennus virtuaalikoneelle osa 2

Tein toisen virheen virtuaalikoneen uudelleenasennuksen yhteydessä ja unohdin määritellä, RAM-muistin, suorittimet ja virtuaalilevyn koon. Tein kyseiset määritykset raportin lopussa omana kappaleena.

Aloitin virtuaalikoneen uudelleenasentamisen poistamalla edellisen virtuaalikoneen ja vaihdoin uuden koneen käyttöjärjestelmän distron versioon "debian-live-13.0.0-amd64-xfce.iso". 

<img width="1268" height="74" alt="image" src="https://github.com/user-attachments/assets/72fcda89-1816-44d1-a516-e5b93f093b90" />

<img width="1586" height="1082" alt="image" src="https://github.com/user-attachments/assets/b0235b94-a39c-4c31-a304-b81c894f68ac" />

Alkumäärityksien (tässä kohtaa väärät) ja virtuaalikoneen luomisen jälkeen testasin GUI:n toimivuuden Live systemin avulla. Tällä kertaa käyttöjärjestelmän image oli valittu oikein ja ruudulle ilmestyi graafinen näkymä.

<img width="1530" height="1160" alt="image" src="https://github.com/user-attachments/assets/c821bd00-d481-4891-8a0a-08382ccc911f" />

Live testin jälkeen sammutin virtuaalikoneen ja käynnistin sen uudestaan. Aloitin käyttöjärjestelmän asentamisen virtuaalikoneelleni ja määritin seuraavat lokaatio-, kieli- ja näppäimistön asetukset:

-Kieli English.
-Sijainti Finland.
-Locales en-US.UTF-8.
-Näppäimistön kieli finnish.

<img width="1526" height="1164" alt="image" src="https://github.com/user-attachments/assets/4bbbed83-970f-467c-a066-34caa2bf1d02" />

<img width="1526" height="1162" alt="image" src="https://github.com/user-attachments/assets/2eceaa24-4825-4704-b76e-1f7cadea1091" />

<img width="1530" height="1160" alt="image" src="https://github.com/user-attachments/assets/ab88941a-31aa-4afc-8c6e-4bb7b0e98d5d" />

<img width="1536" height="1166" alt="image" src="https://github.com/user-attachments/assets/60a60584-1644-48f7-be72-73c5794501a4" />

Sijainti- ja kieliasetuksien jälkeen jatkoin määrittämään virtuaalikoneen verkkoasetuksia. 

## Verkkoasetukset 

Määritin seuraavat asetukset verkolle:

-Hostname linux-palvelimet-test.
-Domain miroServer.com.

<img width="1526" height="1178" alt="image" src="https://github.com/user-attachments/assets/6d8b2420-43fd-42f3-aa6f-92ec3b186803" />

<img width="1538" height="1154" alt="image" src="https://github.com/user-attachments/assets/42d8a15b-3ad4-4022-adf8-d8ba86785816" />

## Käyttäjätunnukset

Seuraavaksi määritin käyttäjätunnukset virtuaalikoneeleni. Root -käyttäjälle jätin salasanakentän tyhjäksi ja jatkoin määrittämään peruskäyttäjän nimen ja salasanan. 

<img width="1530" height="1172" alt="image" src="https://github.com/user-attachments/assets/03657462-b4bf-480c-9271-2b27ddfda7df" />

Peruskäyttäjän etunimeksi ja sukunimeksi asetin oman nimeni eli "miro helenius". Jatkoin salasanan määritykseen, määritin salasanan ja painoin "continue". 

<img width="1516" height="1174" alt="image" src="https://github.com/user-attachments/assets/8f8c7c60-dd1e-41e8-9f6c-32cec0adee28" />

<img width="1524" height="1166" alt="image" src="https://github.com/user-attachments/assets/ef43896b-6193-467b-abe6-965c8ffccd64" />

<img width="1524" height="1156" alt="image" src="https://github.com/user-attachments/assets/0224c148-5ff1-49dc-8189-fbfb5f5ddd0a" />

Käyttäjtunnuksien ja salasanojen määrityksen jälkeen siirryin asennuksessa seuraavaan vaiheeseen.

## Levyosioiden määritykset

Määritin levyosoille seuraavat asetukset: 

Partition disks Guided - use entire disk ! väärän kokoinen levy.
Partition disks virtual disk which I created.
Partitioning scheme - All files in one partition.
Partition disks - Finish partiotining and write changes to diks.

Lopuksi täppä valintaan "Yes" kohdassa "Write changes to the disk".

<img width="1530" height="1164" alt="image" src="https://github.com/user-attachments/assets/e170978a-9841-4353-af7d-42f570ac11f4" />

<img width="1528" height="1158" alt="image" src="https://github.com/user-attachments/assets/64d7caad-a469-4eb8-82df-802be5b5056a" />

<img width="1534" height="1174" alt="image" src="https://github.com/user-attachments/assets/74fe7c79-4579-46f6-bf1d-206cecc21426" />

<img width="1528" height="1160" alt="image" src="https://github.com/user-attachments/assets/1c3dad23-2fb3-4d0f-b150-2c91478ba9d5" />

<img width="1528" height="1168" alt="image" src="https://github.com/user-attachments/assets/f68158df-fb96-41ab-bae4-16beb6955cb1" />

## GRUB boot loader asennus

Ennen asennuksen valmistumista piti vielä valita asennetaanko GRUB boot loader, valitsin "Yes" ja asennuskohteeksi valitsin luomani virtuaalilevyn. Jatkoin tämän jälkeen asennuksen loppuun.

<img width="1518" height="1166" alt="image" src="https://github.com/user-attachments/assets/320b7726-ce31-4685-8908-b627e4dbc557" />

<img width="1534" height="1168" alt="image" src="https://github.com/user-attachments/assets/8a355536-7e7f-4196-9d0b-4d05ee22f709" />


<img width="1530" height="1168" alt="image" src="https://github.com/user-attachments/assets/91afa251-ed68-4006-9462-6d41a57c1d71" />

Lopuksi odotin, että virtuaalikone asenti Linuxin valmiiksi ja painoin "Continue" Finish the installation -valikossa. 

Asennuksen lopputuloksena käytössä on toimiva virtuaalinen Debian Linux alla olevan kuvan mukaisesti.

<img width="1532" height="1162" alt="image" src="https://github.com/user-attachments/assets/1b0c591f-aa1d-42fe-b239-3215cc39d3ac" />

## Virtuaalikoneen asetuksien muuttaminen jälkikäteen

Tein virtuaalityöaseman alustamisvaiheessa toisen virheen ja unohdin määrittää asetukset oikein. Sammutin juuri asentamani virtuaalikoneen ja avasin VirtualBoxin. Hetken tutkimisen jälkeen löysin VirtualBoksista oikeat asetukset muutoksien tekemiseen. Valitsin virtuaalikoneen "Details" ja valitsin hiiren oikealla painikkeela "System". System valikosta asetin muistin määräksi 4096MB. Seuraavaksi valitsin "Processor" -välilehden ja asetin suoritinytimien määräksi 2.

<img width="1542" height="936" alt="image" src="https://github.com/user-attachments/assets/b44ecc8c-c5e1-40a1-9353-1984af20676f" />

<img width="1548" height="944" alt="image" src="https://github.com/user-attachments/assets/1f96d21e-e1de-4465-a231-c284ec738246" />

## Virtuaalikoneen kovalevyn kapasiteetin kasvattaminen jälikäteen 

Ohjeistus tähän ongelaan löytyi pienen Googletuksen jälkeen "https://www.reddit.com/r/virtualbox/comments/nxonby/virtual_disk_expandadd_space". 

Kuten raportin aikaisemmassa vaiheessa huomasin, virtuaalikoneeni kovalevy oli jäänyt liian pieneksi 20GB. Kasvatin sen kokoa jälkikäteen VirtualBoxissa seuraavalla tavalla. 

Valitsin File --> Tools --> Media. Seuraavaksi valitsin luomani virtuaalilevyn "Linux_palvelin.vdi" hiiren oikealla painikkeella ja klikkasin "Properties" ikkunan yläkulamasta. Tämän jälkeen pääsin määrittämään virtuaalikovalevyn kokoa vapaasti ikkunan alareunassa. Valitsin levyn kooksi 40,00GB ja painoin "Apply". 

<img width="1489" height="1529" alt="image" src="https://github.com/user-attachments/assets/87646b2d-3c49-41f4-9083-5479a8ede74f" />

<img width="1488" height="1694" alt="image" src="https://github.com/user-attachments/assets/d31f983e-ab5f-4d9f-b395-3ed09498a5be" />

# Yhteenveto

Nyt käytössäni on valmis virtuaalikone Linux -käyttöjärjestelelmällä. Asennus ei sujunut aivan suoraviivaisesti, mutta ainakin opin VirtualBoxsista uusia ominaisuuksia. Ensi kerralla enemmän tarkkuutta, kun määritellään asetuksia. 

# Lähteet

https://www.reddit.com/r/virtualbox/comments/nxonby/virtual_disk_expandadd_space - Levyosion kasvattaminen jäkikäteen VirtualBox

https://github.com/johannaheinonen/johanna-test-repo/blob/main/linux-20082025.md - Virtuaalikone asennettu seuraavaa ohjetta seuraten. 

https://cdimage.debian.org/debian-cd/13.0.0-live/amd64/iso-hybrid - Linux Distrojen ISO -tiedostot

https://terokarvinen.com/linux-palvelimet/#h0-hei-weppi - Liux palvelimet kurssin materiaali

https://unix.stackexchange.com/questions/87182/whats-the-difference-between-debian-standard-and-gnome 


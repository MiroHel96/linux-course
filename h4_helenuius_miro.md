# Tero Karvinen Haaga-Helia ammatikorkeakoulu syksy 2025 - Linux Palvelimet

Tehtävänanto: h4 Maailma kuulee 


## Tiivistelmä 


## a) Palvelimen Vuokraaminen DigitalOcean

Käytin seuraavaa opasta tukemaan palvelimen vuokrausta: https://www.tutkit.com/fi/tekstioppaat/17058-vuokraa-linux-palvelimesi-digitaloceanilta-yksinkertainen-opas

Tässä raportin vaiheessa vuokrasin verkosta palvelimen, jonka alkukonfiguraatiot toteutin aikaisemmin luomallani virtuaali Linuxilla. Harjoituksen tarkoitus on luoda verkkosivu, joka näkyy verkossa ulkopuolisille. 
Valitsin palvelimen vuokraamiseen DigitalOcean, joten tämä ohjeistus koskettaa vain kyseistä palveluntarjoajaa palvelimen vuokraukseen.

Hain verkkoselaimesta "DigitalOcean", avasin palveluntarjoajan kotisivun ja rullasin sivua alaspäin kohtaan "See our products in action". Napeista oli valittuna valmiiksi "Virutal Machines", joten valitisin alhaalta "Get Started" ja kirjauduin sisään GitHub tunnuksillani.

<img width="1709" height="1387" alt="image" src="https://github.com/user-attachments/assets/c745cfa6-b470-41af-abde-126e79b6f8f2" />

<img width="1708" height="1389" alt="image" src="https://github.com/user-attachments/assets/3ee3f2c2-fabf-489d-bf0e-844959df1530" />

<img width="1718" height="1390" alt="image" src="https://github.com/user-attachments/assets/85d4ac94-778c-4eaf-a34a-5440f0dd25bf" />

## Palvelimen asetuksien valitseminen 

Sisäänkirjautumisen jälkeen pääsin "Create DropletS" -sivulle, pisara viittaa ilmeisesti palvelimeen palvelimien meressä. 

Valitsin palvelimelle alueeksi "Frankfurt", koska se oli lähin vaihtoehto. Datakeskusta en voinut muuttaa, joten jätin sen vakioksi. Seuraavaksi valitsin käyttöjärjestelmän versioksi "Debian, 12 x64". Versio 13 olisi ollut parempi vaihtoehto, mutta jatkoin saatavailla olevalla versiolla. Valitsin palvelimelle peruspaketin eli jaetun prosessorin, koska en tarvitse paljon tehoa palvelimelle. CPU -asetuksista valitsin seuraavan kuukausisuunitelman:
- 1GB / 1CPU
- 25 GN SSD Disk
- 1000 GB transfer

Kyseiset resurssit ovat tämän kurssin demostraation riittävät. En valinnut ylimääräistä tallenustilaa, enkä varmuuskopiointia. Autentikointi keinoksi valitsin salasanan, koska luon SSH -avaimen virtuaalikoneella myöhemmässä vaiheessa tätä raporttia. Tarkastin vielä asettamani asetukset ja viimeistelin palvelimen nimellä "miro-school-test-linux

<img width="1701" height="1356" alt="image" src="https://github.com/user-attachments/assets/eccdec1d-026e-4c29-a63a-b9fb21858842" />

## Käyttöjärjestelmän valitseminen

<img width="1490" height="764" alt="image" src="https://github.com/user-attachments/assets/f1459856-000f-4b7c-b217-2ce713cbe38b" />

## Palvelimen koon ja "raudan" valitseminen

<img width="1485" height="1003" alt="image" src="https://github.com/user-attachments/assets/37ec2367-fc8f-4f0f-92a1-88e7201cc842" />

## Salasanan asettaminen

<img width="1485" height="845" alt="image" src="https://github.com/user-attachments/assets/758e7cc4-74a2-4144-8569-caa6f85641b4" />

## Viimeistely 

<img width="1342" height="443" alt="image" src="https://github.com/user-attachments/assets/310fff2b-49f1-4b96-af86-f0074de72e07" />

Digital Ocean ei jostain syystä suostunyt hyväksymään korttitietojani ja tästä syystä en saanut palvelinta vuokrattua. Päätin vaihtaa UpCloudiin ja kyseisen palvelinvuokraajan kautta sain aktivoitua tunnukseni. Jätin kuitekin tähän raporttiin kyseiset vaihee, jos tulevaisuudessa tarvitsen ohjeita. 

## Palvelimen Vuokraaminen UpCloud

Aloitin palvelimen vuokraamisen menemällä UpCloudin kotisivuille: https://upcloud.com. Valitsin "Sing Up", loin käyttäjätunnuksen, vahvistin sen maksukortillani ja tämän jälkeen pääsin valitsemaan halutun palvelun. Tukeuduin tässä raportissa palvelimen luomiseen UpCloudin oman dokumentaation avulla: https://upcloud.com/docs/guides/quick-start-guide

<img width="2754" height="1604" alt="image" src="https://github.com/user-attachments/assets/a14d4a07-ac5e-4a63-8b20-347134558a63" />

<img width="2768" height="1628" alt="image" src="https://github.com/user-attachments/assets/60c21077-3617-4b5c-bc70-f9e7b8215d9b" />

## Dashboard näkymä, josta voidaan valita eri palveluita. 

<img width="2742" height="1534" alt="image" src="https://github.com/user-attachments/assets/a521f183-b893-4611-9772-8b259d10fa2d" />

Seuraavaksi aloitin luomaan virtuaalikonetta valitsemalla Deploy your trial services -ikkunasta "Deploy now". Valitsin palvelimen ja seuraavaksi määritin palvelimen sijainnin. Valitsin sijainniksi "FI-HEL1".

<img width="1408" height="456" alt="image" src="https://github.com/user-attachments/assets/e379a2d3-d03a-4e44-a97c-8d2db684d9dd" />

<img width="1394" height="1198" alt="image" src="https://github.com/user-attachments/assets/ccb66956-53c4-48a8-a834-d12889165e64" />

<img width="2210" height="1448" alt="image" src="https://github.com/user-attachments/assets/8815c1de-703f-491a-8350-4d8a8d57c0c3" />

## Komponenttien valitseminen 

Valitsin palvelimen suunnitelmaksi "Developer", valitsin RAM-muistin määräksi "1GB", yhden ytimen prosessoriin ja tallenustilaa "20GB". Jätin varmuuskopion ja tallenuksen asetukset vakioksi. 
Tämän jälkeen jatkoin käyttöjärjestelmän valintaan. Valitsin käyttöjärjestelmäksi "Debian GNU/Linux 13(Trixie). 

<img width="2212" height="1416" alt="image" src="https://github.com/user-attachments/assets/e6b5e335-114e-4f42-886c-5bb0235768b9" />

<img width="1574" height="654" alt="image" src="https://github.com/user-attachments/assets/79b25ad0-534c-43ce-b25b-0e92dd0c1623" />

<img width="1588" height="1288" alt="image" src="https://github.com/user-attachments/assets/9fd96f42-955d-4124-bc92-7a9fc300ed0d" />

<img width="1618" height="1334" alt="image" src="https://github.com/user-attachments/assets/eb89db59-ca99-4f98-a4ae-231e0192c056" />

Jätin verkon asetukset ja vaihtoehtoiset asetukset vakioiksi. Seuraavaksi siirryin SSH avaimen luomiseen. Olisin tässä kohtaa halunnut luoda kertakäyttöisen salasana, mutta kyseinen käyttöjärjestelmäversio ei mahdollistanut "one time password" käyttämistä. Jos olisin halunnut käyttää salasanaa, niin Linuxin versio olisi pitänyt olla "Debian GNU/Linux 11 (Bullseye)".

<img width="1518" height="1534" alt="image" src="https://github.com/user-attachments/assets/f5a2ef8b-f1f1-4ad0-ac51-3e787c688a74" />

## SSH avaimen luominen 

Käytin SSH -avaimen luomiseen seuraavia ohjeita: https://upcloud.com/docs/guides/use-ssh-keys-authentication, https://terokarvinen.com/linux-palvelimet/#h4-maailma-kuulee, https://terokarvinen.com/2017/first-steps-on-a-new-virtual-private-server-an-example-on-digitalocean/ ja tarkensin vielä kysymyksiä ongelma tilanteissa Microsoft Copilot avulla.

Kuvassa Tero Karvisen ohjeistus SSH avaimen tekemiseen Linuxilla.

<img width="1550" height="430" alt="image" src="https://github.com/user-attachments/assets/34c4e7d7-4ac3-492c-92ea-7895b01d9d8c" />

Aloitin SSH-avaimen luomisen avaamalla VirtualBoxin työasemallani ja käynnistämällä aikaisemmissa ohjeissa luodun Linux Virtuaalikoneen.

Ensiksi ajoin komennon "**sudo apt-get update**", seuraavaksi tarkastin onko SSH asennettu Linuxille komennolla "**ssh -V**". Tarkastamisen jälkeen aloitin luomaan SSH avainta, käytin komentoa "**ssh-keygen #**" ja painoin "enter" kolme kertaa. SSH avaimen generoimisen kopoin sen käyttämällä Micro -editoria virtuaalikoneella avaamalla polun "~/.ssh/..". 

<img width="1660" height="308" alt="image" src="https://github.com/user-attachments/assets/6b7c48ba-611f-4226-96ef-170e4bbef1bc" />

SSH avaimen kopiointi quest -koneelta host -koneelle ei onnistunut. Jouduin asentamaan "VirtualBox Guest Additions" -ajurit virtuaalikoneelleni, jotta sain kopioinnin toimimaan. Olin asettanut tiedostojen siirtämisen/kopioimisen asetukset aikaisemmin VirtualBoxista "bidirectional" -muotoon, joka tarkoittaa, että voin siirtää tiedsotja edestakaisin koneiden välillä. Selvästi asetukset eivät toimineet oikein, joten jouduin tekemään lisäselvitystä. En avaa asiaa tässä raportissa sen tarkemmin, mutta jos sama ongelma toistuu tätä raporttia seuratessa niin seuraavalla ohjeella ongelman saa ratkaistua: https://linuxconfig.org/install-virtualbox-guest-additions-on-linux-guest

Lopulta sain kopioitua SSH-avaimen UpCloudiin ja jatkoin palvelimen viimeistelyyn. Jätin Hostnamen vakioksi ja Server Nameksi asetin "LinuxPalvelinTestMiro". Huomasin, että näitä voi jälkikäteen muokata palvelimen käynnistämisen jälkeen, joten muutan niitä todennäköisesti myöhemmin.

<img width="990" height="850" alt="image" src="https://github.com/user-attachments/assets/0050370f-749e-4fe1-9233-3b46801a87fb" />

<img width="1608" height="612" alt="image" src="https://github.com/user-attachments/assets/e8766acc-1d17-4d23-855a-8527c1204c89" />


# Toimiva palvelin

<img width="2310" height="958" alt="image" src="https://github.com/user-attachments/assets/340ab372-3ceb-4208-a203-2b1c91e9d240" />

En saanut yhteyttä palvelimeen, koska palvelin ei tunnista virtuaalikonettani. Muokkasin käyttöoikeuksia ja loin virtuaalikoneelleni "known_hosts" -kansion. Lisäsim palvelimen julkiseavaimen tänne ja pääsin yhdistämään palvelimelle.

<img width="1830" height="104" alt="image" src="https://github.com/user-attachments/assets/26d0cc7b-220d-43cd-a1d4-4fe618dfb703" />

<img width="2652" height="748" alt="image" src="https://github.com/user-attachments/assets/2f27999f-2714-4593-94a3-7e997a6171ac" />

# Käyttäjien luominen palvelimelle 

<img width="2568" height="872" alt="image" src="https://github.com/user-attachments/assets/53477e3b-15db-47b2-8a78-b5fd2d1ae33d" />

<img width="2448" height="718" alt="image" src="https://github.com/user-attachments/assets/4766d687-63ba-4eb7-8675-72e60b53ac14" />

<img width="2600" height="616" alt="image" src="https://github.com/user-attachments/assets/88c4672a-3f95-4e21-9935-09736c1352f9" />

Kirjauduin ulos ja kokeilen peruskäyttäjällä kirjautumista 

<img width="2598" height="214" alt="image" src="https://github.com/user-attachments/assets/036602c3-e24b-4fef-b297-0cf761ce49db" />

Seuraavaksi lukitsin ROOT -käyttäjän 

<img width="2598" height="836" alt="image" src="https://github.com/user-attachments/assets/392f31b5-7490-4b2b-857c-41e872aa4f83" />

## b) Tee alkutoimet omalla virtuaalipalvelimella

# Palomuurin ja muiden palveluiden asenttamienn

Aloitin asentamalla palomuurin ufw

<img width="2576" height="926" alt="image" src="https://github.com/user-attachments/assets/ab8493b7-7364-4e29-b751-37f319879153" />

Seuraavaksi asetin säännöt palomuurille

<img width="2594" height="568" alt="image" src="https://github.com/user-attachments/assets/325dfa54-27d7-48ab-991e-47f8daddea70" />

Sallin vielä erikseen SSH, mutta sillä ei ole väliä, koska avasin jo portin 22/TCP. Tarkastin vielä asetukset ja käynnistin tämän jälkeen virtuaalikoneen uudestaan. 

<img width="2578" height="934" alt="image" src="https://github.com/user-attachments/assets/fa499727-545b-4cbb-86a6-86a7be22ab8a" />

Nyt olet luonut palvelimen ja kiteytettynä tein seuraavat asiat:
- Loin tunnukset UpCloudiin
- Loin SSH-avaimen virtuaalikoneellani ja jaoin sen UpCLoudin virtuaalikonelle luomisen yhteydessä
- Yhdistin virtuaalikoneeseen SSH -sessiolla (Jouduin tekemään tässä omia muokkauksia)
- Asensin palomuurin ja sallin portit 22/TPC (SSH) ja 80/TCP (HTTP)
- Loin uuden käyttäjän ja sudo oikeudet sille
- lukitin root -käyttäjän.

# c) Apache2 asentaminen palvelimelle

Palvelin luomisen ja esiastuksien jälkeen aloitin web-palvelimen asentamisen. 

Avasin yhteyden palvelimeen ja terminaali-ikkunaan syötin komennon "sudo apt-get install apache".

<img width="1702" height="388" alt="image" src="https://github.com/user-attachments/assets/d1ba449d-bfcc-4836-a719-67857c6a7a89" />

Apachen statuksen tarkastamienn komennola "sudo systemctl status apache2"

<img width="2658" height="1324" alt="image" src="https://github.com/user-attachments/assets/3191e0cf-0816-469f-b2da-feaa91237c70" />

Indeksitiedoston muokkaaminen 

Seuraavaksi siirryin hakemistoon /var/www/html. Kopioin index.html tiedoston nimellä index.html.orig ja poistin alkuperäisin. Tämän jälkeen lisälin Micro-editorilla tekstiä tiedostoon ja tallensin sen index.html nimellä samaan polkuun.

<img width="2528" height="176" alt="image" src="https://github.com/user-attachments/assets/a10ade26-9a0d-45c6-ae65-36f298651c65" />

<img width="2598" height="258" alt="image" src="https://github.com/user-attachments/assets/7db04d78-3b32-46d2-865e-18d53a4c631c" />

<img width="2600" height="72" alt="image" src="https://github.com/user-attachments/assets/ad04f07d-b283-48cd-81c2-fdb6c790a462" />

<img width="2674" height="1328" alt="image" src="https://github.com/user-attachments/assets/d996f2f0-cc77-4e5a-a511-e1ae37333abb" />

Seuraavaksi avasin verkkoselaimen omalta tietokoneeltani ja testasin sivun toimivuutta. 

<img width="2572" height="272" alt="image" src="https://github.com/user-attachments/assets/84f55a8f-8860-4a39-b514-1787c60e1223" />

<img width="2770" height="412" alt="image" src="https://github.com/user-attachments/assets/c06eba86-9b44-45df-bb15-e6d550fe8da4" />


# d) Vapaaehtoinen, luo namebased virtualhost palvelimelle




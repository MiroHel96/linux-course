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

Käyttöjärjestelmän valitseminen

<img width="1490" height="764" alt="image" src="https://github.com/user-attachments/assets/f1459856-000f-4b7c-b217-2ce713cbe38b" />

Palvelimen koon ja "raudan" valitseminen

<img width="1485" height="1003" alt="image" src="https://github.com/user-attachments/assets/37ec2367-fc8f-4f0f-92a1-88e7201cc842" />

Salasanan asettaminen

<img width="1485" height="845" alt="image" src="https://github.com/user-attachments/assets/758e7cc4-74a2-4144-8569-caa6f85641b4" />

Viimeistely 

<img width="1342" height="443" alt="image" src="https://github.com/user-attachments/assets/310fff2b-49f1-4b96-af86-f0074de72e07" />

Digital Ocean ei jostain syystä suostunyt hyväksymään korttitietojani ja tästä syystä en saanut palvelinta vuokrattua. Päätin vaihtaa UpCloudiin ja kyseisen palvelinvuokraajan kautta sain aktivoitua tunnukseni. Jätin kuitekin tähän raporttiin kyseiset vaihee, jos tulevaisuudessa tarvitsen ohjeita. 

# Palvelimen Vuokraaminen UpCloud

Aloitin palvelimen vuokraamisen menemällä UpCloudin kotisivuille: https://upcloud.com
Valitsin "Sing Up", loin käyttäjätunnuksen, vahvistin sen maksukortillani ja tämän jälkeen aloitin palvelimen vuokraamisen. Tukeuduin palvelimen luomisessa UpCloudin omaan dokumentaatioon: https://upcloud.com/docs/guides/quick-start-guide

<img width="2754" height="1604" alt="image" src="https://github.com/user-attachments/assets/a14d4a07-ac5e-4a63-8b20-347134558a63" />

<img width="2768" height="1628" alt="image" src="https://github.com/user-attachments/assets/60c21077-3617-4b5c-bc70-f9e7b8215d9b" />

Dashboard näkymä rekisteröitymisen jälkeen

<img width="2742" height="1534" alt="image" src="https://github.com/user-attachments/assets/a521f183-b893-4611-9772-8b259d10fa2d" />

Seuraavaksi aloitin luomaan uutta virtuaalikonetta, valitsemalla "Deploy" -ikkunasta. Valitsin palvelimen ja seuraavaksi määritin palvelimen sijainnin. Valitsin sijainniksi "FI-HEL1".

<img width="1408" height="456" alt="image" src="https://github.com/user-attachments/assets/e379a2d3-d03a-4e44-a97c-8d2db684d9dd" />

<img width="1394" height="1198" alt="image" src="https://github.com/user-attachments/assets/ccb66956-53c4-48a8-a834-d12889165e64" />

<img width="2210" height="1448" alt="image" src="https://github.com/user-attachments/assets/8815c1de-703f-491a-8350-4d8a8d57c0c3" />

# Komponenttien valitseminen 

Valitsin palvelimen suunnitelmaksi "Developer", koska palvelimen ei tässä vaiheessa tarvitse olla kovin tehokas, joten valitsin RAM-muistin määräksi "1GB", yhden ytimen prosessoriin ja tallenustilaa "25GB". Jätin varmuuskopion ja tallenuksen asetukset vakioksi. Tämän jälkeen jatkoin käyttöjärjestelmän valintaan. Valitsin käyttöjärjestelmäksi "Debian GNU/Linux 13(Trixie). 

<img width="2212" height="1416" alt="image" src="https://github.com/user-attachments/assets/e6b5e335-114e-4f42-886c-5bb0235768b9" />

<img width="1574" height="654" alt="image" src="https://github.com/user-attachments/assets/79b25ad0-534c-43ce-b25b-0e92dd0c1623" />

<img width="1588" height="1288" alt="image" src="https://github.com/user-attachments/assets/9fd96f42-955d-4124-bc92-7a9fc300ed0d" />

<img width="1618" height="1334" alt="image" src="https://github.com/user-attachments/assets/eb89db59-ca99-4f98-a4ae-231e0192c056" />

Jätin verkon asetukset ja lisäasetukset vakioksi. Seuraavaksi siirryin SSH-avaimen luomiseen. Kyseinen käyttöjärjestelmäversio ei mahdollisanut "one time password" käyttämistä. Kyseinen tapa ei ole ohjeistuksen mukainen, mutta kokelin sen tekemistä silti. Jos olisin halunnut käyttää salasanaa, niin Linuxin versio olisi pitänyt olla "Debian GNU/Linux 11 (Bullseye)".

<img width="1518" height="1534" alt="image" src="https://github.com/user-attachments/assets/f5a2ef8b-f1f1-4ad0-ac51-3e787c688a74" />

# SSH avaimen luominen 

Käytin SSH -avaimen luomiseen seuraavia ohjeita: https://upcloud.com/docs/guides/use-ssh-keys-authentication ja https://terokarvinen.com/linux-palvelimet/#h4-maailma-kuulee. 

Kuvassa Tero Karvisen ohjeistus SSH-avaimen tekemiseen Linuxilla

<img width="1550" height="430" alt="image" src="https://github.com/user-attachments/assets/34c4e7d7-4ac3-492c-92ea-7895b01d9d8c" />

Aloitin SSH-avaimen luomisen avaamalla VirtualBoxin työasemallani ja käynnistämällä aikaisemmissa ohjeissa luodon Linux Virtuaalikoneen. Avasin terminaali-ikkunan ja tarkastin oliko SSH-client asennettu Linuxille. 

Ensiksi ajoin komennon "sudo apt-get update", seuraavaksi tarkastin onko SSH asennettu Linuxille komennolla "ssh -V".  Tarkastamisen jälkeen aloitin luomaan SSH -avainta. Käytin komentoa "ssh-keygen #" ja painoin enter kolme kertaa. (Jätin kuvan laittamatta ssh-avaimen generoinnista, tietoturva syistä). Nyt SSH-avain on generoitu ja voin syöttää sen virtuaalikoneelta UpCloudiin. Kopion SSH-avaimen käyttmällä Micro -editoria virtuaalikoneella avaamalla polun, johon SSH-avain luotiin.

<img width="1660" height="308" alt="image" src="https://github.com/user-attachments/assets/6b7c48ba-611f-4226-96ef-170e4bbef1bc" />


Minulla tuli ongelma avaiken kopioimisessa virtuaalikoneelta host -koneelle. Jouduin asentamaan "VirtualBox Guest Additions" virtuaalikoneelleni, jotta sain kopioitua SSH-avaimen. En avaa asiaa tässä vaiheessa sen tarkemmin, mutta jos sama ongelma toistuu niin seuraamalla seuraavaa ohjetta, ongelman saa varmasti ratkaistua: https://linuxconfig.org/install-virtualbox-guest-additions-on-linux-guest


Syötin SSH-avaimen UpCloudiin ja jatkoin nimen viimeistelyyn. Jätin Hostnamen vakioksi ja Server Nameksi asetin "LinuxPalvelinTestMiro".

<img width="990" height="850" alt="image" src="https://github.com/user-attachments/assets/0050370f-749e-4fe1-9233-3b46801a87fb" />

<img width="1608" height="612" alt="image" src="https://github.com/user-attachments/assets/e8766acc-1d17-4d23-855a-8527c1204c89" />


Valmis palvelin 

<img width="2310" height="958" alt="image" src="https://github.com/user-attachments/assets/340ab372-3ceb-4208-a203-2b1c91e9d240" />

En saanut yhteyttä palvelimeen, koska palvelin ei tunnista virtuaalikonettani. Muokkasin käyttöoikeuksia ja loin virtuaalikoneelleni "known_hosts" -kansion. Lisäsim palvelimen julkiseavaimen tänne ja pääsin yhdistämään palvelimelle.

<img width="1830" height="104" alt="image" src="https://github.com/user-attachments/assets/26d0cc7b-220d-43cd-a1d4-4fe618dfb703" />

<img width="2652" height="748" alt="image" src="https://github.com/user-attachments/assets/2f27999f-2714-4593-94a3-7e997a6171ac" />




## b) Tee alkutoimet omalla virtuaalipalvelimella

## c) Vapaaehtoinen, luo namebased virtualhost palvelimelle




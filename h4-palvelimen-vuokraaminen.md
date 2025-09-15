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



## b) Tee alkutoimet omalla virtuaalipalvelimella

## c) Vapaaehtoinen, luo namebased virtualhost palvelimelle




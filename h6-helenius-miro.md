# Haaga-Helia Ammatikorkeakoulu Linux Palvelimet 2025 - Tero Karvinen 

## Tehtävä h6 salataampa

Tässä raportissa hankin ilmaisen TLS-sertifikaatin luomalleni palvelimelle Let's Encryptilta. 

## Tiivistelmä 

Tiivistelmä seuraavista artikkeleista https://letsencrypt.org/how-it-works/ ja https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample



## Host-operating system spesifikaatiot
  - Operating system: Windows 11 Home
  - Version	10.0.26100 Build 26100
  - Device name	BOOK-QUCSCTFCNT
  - Processor	13th Gen Intel(R) Core(TM) i7-1360P (2.20 GHz)
  - Installed RAM	16,0 GB (15,6 GB usable)
  - System type	64-bit operating system, x64-based processor
  - Pen and touch	Pen and touch support with 10 touch points


# a) TLS-sertifikaatin hankinta Let's Encrypt

Tässä raportin vaiheessa loin ilmaisen TLS-Sertifikaatin palvelimelleni. Hyödynsin seuraavia verkkosivuja sen tekemisessä: https://terokarvinen.com/linux-palvelimet/#h6-salataampa, https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample ja https://certbot.eff.org/instructions?ws=apache&os=snap

Aloitin avaamalla virtuaalikoneeni ja kirjauduin sisään. Tämän jälkeen otin SSH -yhteyden luomaani palvelimeen. 

<img width="1660" height="570" alt="image" src="https://github.com/user-attachments/assets/780dec72-50d1-4a4c-be72-af006f3d4df5" />

Käynnistin ensiksi apache palvelun uudestaan, ennekuin aloitin tekemään TLS-sertifikaattia. 

`sudo systemcelt restart apache2`

Tämän jälken testastin, että verkkosivu toimii eri päätelaitteilla. 

<img width="2552" height="524" alt="image" src="https://github.com/user-attachments/assets/dfe08231-fc0b-47c7-b5eb-fe9158fe801d" />

### Palomuurin asetukset 

Ennen aloitusta minun piti vielä avata palomuurista seuraavat portit http eli 80/tcp; ja https eli 443/tcp.

Tarkastin palomuurin tilanteen komennolla `sudo ufw status verbose`

<img width="1642" height="560" alt="image" src="https://github.com/user-attachments/assets/9c3b1241-c35a-444f-882b-6d4c70211faf" />

Portti 80 oli jo avattu, joten minun piti vielä sallia portti 443. Käytin komentoa `sudo ufw allow 443/tcp`

<img width="1252" height="248" alt="image" src="https://github.com/user-attachments/assets/b7069624-90f4-4af2-97c3-ffaa95752e7d" />

<img width="1588" height="578" alt="image" src="https://github.com/user-attachments/assets/900431a4-61d9-4a95-afb2-6ddb1735f6d2" />

Kuten kuvissa näkyy portit 80 ja 443 ovat sallittu tcp yhtetydelle. Palvelua ei tarvitse päivitää, koska en muokannut palomuurin konfiguraatiota käsin. 
Nyt palvelin on valmis. Lopuksi ajoin vielä varmuudenvuoksi komennot: `sudo apt upgrade` ja `sudo apt update`.

Tarkastin vielä oliko automaattiset tietoturvapäivitykset käytössä palvelimella ja en ollut jostain syystä niitä asentanut, joten asensin ne vielä lopuksi seuraavilla komennoilla ja tarkastin palvelun tilanteen.

`sudo apt install unattended-upgrades apt-listchanges bsd-mailx`

`sudo dpkg-reconfigure unattended-upgrades`

`sudo systemctl status unattended-upgrades`

## Certbot asennus ja TLS-sertifikaatin luominen

Seurasin seuraavaa ohjetta Certbotin asennuksessa: https://certbot.eff.org/instructions?ws=apache&os=snap, https://medium.com/@pi_45757/generate-lets-encrypt-certificate-using-certbot-on-linux-414d8adf2ff3, https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample ja https://terokarvinen.com/linux-palvelimet/#h6-salataampa

Vertasin MicrosoftCopilotilla komentojen `tero karvinen certbot ja certbotin ommia versioita`

Syötin terminaaliin komennon `sudo apt-get install certbot python3-certbot-apache`

<img width="1652" height="916" alt="pythoncertbot" src="https://github.com/user-attachments/assets/7a5d6006-71f0-47a1-b249-fe24fa29169a" />

Asentamisen jälkeen syötin seuraavan kommennon terminaaliin, ohjeistuksessa oli kaksi vaihtoehtoa, joko omalla Linuxilla komennon suorittaminen tai vaihtoehtoisesti pavelimella, jos portti 80 on avattu. Minulla on, joten ajoin komennon vuokraamallani palvelimella. 

`sudo certbot certonly --webroot -w /tmp/webroot -d neural1.dns-dynamic.net \
--staple-ocsp -m test@neural1.dns-dynamic.net --agree-tos`

Sain seuraavan virheilmoituksen, koska ajoin komennon ennen ohjeistuksen loppuun lukemista. Minun pitää vaihtaa `neurall.dns-dynamic.net` omaan domainiini eli `mirohelenius.com`. Sama prosessi piti tehdä sähköpostiosoitteen suhteen, koska SSL sertifikaatin vanhemistiedot lähetetään sinne. Tarkastin vielä `/tpm/webroot/` polun palvelimelta ja loin sen, koska sitä ei ollut olemassa. 

<img width="1598" height="282" alt="tmp kansio ei ole olemassa " src="https://github.com/user-attachments/assets/ca9282f9-558f-42cc-8465-434b1547e75a" />

Käytin komentoa `sudo mkdir -p webroot`

<img width="1630" height="424" alt="webroot 1" src="https://github.com/user-attachments/assets/40fa09fb-b097-421a-8a13-34a0b020206f" />


Tämän jälkeen kokeilin ajaa komennon uudestaan ja se onnistui, mutta en päässyt alkua pidemmälle. Sain uuden virheilmoituksen `Some challenges have failed`, ilmeisesti tilapäisiä haastetiedostoja ei pystytty lataamaan palvelimelta. En osaa sanoa ongelman syytä, mutta ongelma mahdollisesti voisi johtua kansion oikeuksista. 

<img width="1634" height="148" alt="certbot komento 1" src="https://github.com/user-attachments/assets/10269d59-a0e2-4b6c-9493-a41aedf0237f" />


<img width="1666" height="460" alt="certifikaatti onnistui" src="https://github.com/user-attachments/assets/d547aef6-960b-4b49-982f-b76289611995" />


<img width="1634" height="788" alt="certifikaatti ei onnistunut 1" src="https://github.com/user-attachments/assets/fc3f2f70-7b94-4562-99e5-54f2a29ad7d8" />

Tässä vaiheessa kokeilin Tero Karvisen h6 tehtävänannossa olevaa komentoa `Sudo certbot --apache --mirohelenius.com, wwwmirohelenius.com`. Sain vastauksen sertifikaattien hakemisen onnistumisesta. Certbot kuitekin ilmoitti, että www.mirohelenius.com ei löytynyt virtualhostia. Valitsin promtista virtuaalihostiksi `mirohelenius.com`.

<img width="712" height="258" alt="image" src="https://github.com/user-attachments/assets/cced8e49-aec2-43cf-8bee-3afa5a0ab235" />

Certbot sertifikaatin hakeminen

<img width="1850" height="924" alt="certifikaatit toimivat 1 tero" src="https://github.com/user-attachments/assets/81d026c1-9133-49d3-a5fe-fa2e7a6bc492" />


<img width="1814" height="692" alt="certifikaatit toimivat 2 tero" src="https://github.com/user-attachments/assets/0352ebce-87ea-41c7-aa95-f8f8cb0282eb" />

Lopuksi sain promtin `You have successfully enabled HTTPS..` Seuraavaksi avasin domainit `mirohelenius.com` ja `www.mirohelenius.com`. Molemmat sivut olivat nyt salattuja, sertitikaatin saaminen olikin helmpompaa, mitä odotin muiden sivujen ohjeiden mukaan. 

Palaan mahdollisesti myöhemmin ohjeen: https://medium.com/@pi_45757/generate-lets-encrypt-certificate-using-certbot-on-linux-414d8adf2ff3 pariin ja selvitän, miten kyseisen ohjeen sertifikaattien haku eroaa edelliseen tapaan. 

### Verkkosivut ja salaus 

<img width="2126" height="618" alt="Salasutoimii mirohelenius" src="https://github.com/user-attachments/assets/c40ce373-fba2-46a8-942f-882ca635f545" />

<img width="2120" height="602" alt="Salasutoimii wwwmirohelenius" src="https://github.com/user-attachments/assets/f9dd7358-fdc8-40f4-bdca-fdbbbfe64999" />

# b) TLS-testaus 

Tässä raportin vaiheessa testasin TSL -salaukseni seuraavalla verkkosivulla: https://www.ssllabs.com/ssltest
Syötin hakukenttään domainin `mirohelenius.com.

## mirohelenius.com

<img width="1098" height="638" alt="image" src="https://github.com/user-attachments/assets/502906ef-5d8e-424c-bc75-d14ad4ee5e13" />

<img width="1014" height="732" alt="image" src="https://github.com/user-attachments/assets/7e44896e-9b14-4300-8c8b-92a0fc5d5497" />

Kuten tuloksista näkyy domainini sai A -luokan arvion, joka on virallisen SSL Labs dokumentaation mukaan korkein taso: https://github.com/ssllabs/research/wiki/SSL-Server-Rating-Guide


# c) Vapaaehtoinen 



# Lähdeluettelo 

https://letsencrypt.org/how-it-works/
https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample

# Haaga-Helia Ammatikorkeakoulu Linux Palvelimet 2025 H7 - Maalisuora
Tässä raportissa hankin ilmaisen TLS-sertifikaatin luomalleni palvelimelle Let's Encryptilta sekä testaan sen luokituksen.

Tämä tehtävä pohjautuu Tero Karvisen Linux Palvelimet kurssiin: https://terokarvinen.com/linux-palvelimet/#h7-maalisuora


## a) Hello World kolmella eri kielllä

Tässä raportin vaiheessa loin Linux palvelimellani scriptin kolmella eri ohjelmointikielellä ja suoritin ne terminaalissa. Aloitin tehtävän tekemisen avaamalla VirtualBoxista Linux työasemani ja otin SSH -yhteyden palvelimeeni. 

<img width="1640" height="846" alt="image" src="https://github.com/user-attachments/assets/78ed1434-068c-44e1-b9ce-34ef42f684f0" />

Hyödynsin tehtävässä seuraavia artikkeleita: [Hello World Python3, Bash, C, C++, Go, Lua, Ruby, Java – Programming Languages on Ubuntu 18.04](https://terokarvinen.com/2018/hello-python3-bash-c-c-go-lua-ruby-java-programming-languages-on-ubuntu-18-04) ja [Tero Karvinen - Shell Scripting](https://terokarvinen.com/2007/12/04/shell-scripting-4)


### Python 3 

Aloitin avaamalla terminaalin ja tarkastamalla, mikä versio pythonista on asennettu komennolla `python3 --version`. Linux palvelimellani oli asennettuna version `Python 3.13.5`.


<img width="1630" height="118" alt="image" src="https://github.com/user-attachments/assets/dce14327-8368-4c8f-93a8-bc7ca8127d73" />

Seuraavaksi loin tekstitiedoston kotihakemistoon. Käytin komentoa `touch micro hellomiro.py`. Tein komennosa virheen ja syötin seuraavaksi `micro touch hellomiro.py`. Seuraavaksi ongelmaksi koittui kansion oikeudet. Siirryin kotihakemistoon `/home/miro` ja kokelin ajaa komennon uudestaan. Tallensin tekstitiedostoon "Hello World" ja tallensin. Tällä kertaa se onnistui. 

<img width="1644" height="558" alt="image" src="https://github.com/user-attachments/assets/a61d614d-5e2d-45ec-b7d7-004c943a065a" />

<img width="1662" height="386" alt="image" src="https://github.com/user-attachments/assets/11ad0914-6c32-4169-9bd8-74488bc26df1" />


<img width="1622" height="224" alt="image" src="https://github.com/user-attachments/assets/dc119744-7989-4c99-87bb-3d4267873d4b" />

Seuraavaksi tarkastin tekstitiedoston sisällön komennolla `cat hellomiro.py`

<img width="1634" height="224" alt="image" src="https://github.com/user-attachments/assets/a5890bdf-0675-4a2d-b169-d91bfdfbddb3" />

Lopuksi ajoin ohjelman komennolla `python3 hellomiro.py`.

<img width="1652" height="152" alt="image" src="https://github.com/user-attachments/assets/871408ec-401f-4c1a-aa05-84457d79932d" />



### Bash (Bourne-Again SHell)

Seuraavaksi toteutuin vastaaman "Hello World" tekstin Bash komentosarjakielellä. Bash on debianissa valmiiksi asennettuna, joten tarkastin sen version käyttämällä komentoa `bash --version`.
Käytössäni on versio 5.2.37.

<img width="1636" height="890" alt="image" src="https://github.com/user-attachments/assets/3d76a67a-371f-45dd-8383-5fe56ef4c38e" />

Loin jälleen teksitiedoston kotihakemistooni käyttämällä komentoa `micro hellomiro.sh`. Kirjoitin Bash -scriptiä tekstitiedostoon ja tallensin sen kotihakemistoon.

<img width="1636" height="186" alt="image" src="https://github.com/user-attachments/assets/8d1c6cf0-4880-4da5-82d9-d176b22c0c70" />


<img width="1660" height="990" alt="image" src="https://github.com/user-attachments/assets/626a6956-945d-4781-8042-c834de83670c" />

Lopuksi käytin komentoa `cat hellomiro.sh` ja `bash hellomiro.sh`. 

<img width="1632" height="230" alt="image" src="https://github.com/user-attachments/assets/6c65f408-eece-4b20-88fd-ff286af70afa" />


### C 

Tässä vaiheessa loin C -ohjelmointikielellä vastaavasti "Hello World" -tekstin. Käytin seuraavaa ohjeistusta apuna C:n asentamisessa ja käytössä Linuxilla: [How To Compile And Run a C/C++ Code In Linux](https://www.cyberciti.biz/faq/howto-compile-and-run-c-cplusplus-code-in-linux)

Avasin komentokehotteeen ja asensin C:n palvelimelle käyttämällä seuraavia komentoja: 
- `sudo apt-get update`
- `sudo apt-get install  build-essential manpages-dev`

Hyväksyin asennuksen promptin syöttämällä "y" komentokehotteesseen.

<img width="1632" height="396" alt="image" src="https://github.com/user-attachments/assets/5ab6498b-85c2-4b55-ac1c-adbefc65bc1d" />

<img width="1774" height="592" alt="image" src="https://github.com/user-attachments/assets/7240065e-6486-4a83-8b33-5586042e6a2d" />

Seuraavaksi varmistin, että C oli asentunut syöttämällä seuraavat komennot: 
- `whereis gcc`
- `which gcc`
- `gcc --version`

  <img width="1790" height="442" alt="image" src="https://github.com/user-attachments/assets/b253dfe8-b65d-432e-adcd-0231754f7dff" />

Asennuksen jälkeen loin kotihakemistoon uuden teksitiedoston `micro hellomiro.c`. Syötin tekstitiedostoon C -ohjelmointikieltä ja tallensin sen. 

<img width="1628" height="146" alt="image" src="https://github.com/user-attachments/assets/727cbeeb-ed12-4347-9c72-f73c64248227" />

Sain seuraavan virhilmoituksen, kun ajoin komennon `g++ hellomiro.c -o hellomiroc`. Huomasin, että itse käskyssä ja koodissa oli virhe, joten korjasin ne ja ajoin komennon uudestaan. Tämän jälkeen ei tullut virheilmoitusta. Kyseinen käsky ajaa ja muuntaa luomani tekstitiedoston suoritettavaksi tiedostoksi nimellä `hellomiroc`. 

<img width="1656" height="270" alt="image" src="https://github.com/user-attachments/assets/ca719424-dfc2-4e59-8932-3c428c7b1eb8" />

<img width="1660" height="442" alt="image" src="https://github.com/user-attachments/assets/91d786d9-8e3e-4baa-a2cd-272fba747826" />

Ajoin seuraavaksi komennon `./hellomiroc`, kuten terminaalissa näkyy tekstitiedosto on muuttunut suoritettavaksi tiedostoksi. 

<img width="1632" height="292" alt="image" src="https://github.com/user-attachments/assets/00529acf-4570-4f34-b7f5-a95ad380666e" />

## c) Shellscript oman komennon luominen 

Tässä raportissa loin shellscriptin avulla oman komennon Linuxpalvelimelleni, jota kuka tahansa muu voi tarvittaessa käyttää. Hyödynsin tehtävässä seuraavaa artikkelia: [Tero Karvinen - Shell Scripting](https://terokarvinen.com/2007/12/04/shell-scripting-4), [How to update Debian Linux](https://linuxhandbook.com/update-debian) ja [Bash Scripting Tutorial for Beginners](https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners)

Päätin luoda komennon joka automaattisesti ajaa komennot `sudo apt list --upgradable`, `sudo apt update` ja `sudo apt upgrade`. Seuraavaksi muokkasin tiedoston oikeuksia. Muokkasin tiedoston kaikkien suoritettavaksi komennolla `chmod a+x autoupdate.sh`. Tarkemmat tiedot käyttöoikeuksista löysin täältä: [Linuxize - Chmod Command in Linux (File Permissions)](https://linuxize.com/post/chmod-command-in-linux)



<img width="1656" height="1004" alt="image" src="https://github.com/user-attachments/assets/d1fcb63b-f8f7-45e0-bffb-b4d5a69ff4d4" />


<img width="1624" height="468" alt="image" src="https://github.com/user-attachments/assets/01c1db9c-df3a-4c4d-ad7d-56647b12c434" />

Seuraavaksi suoritin oman komentoni komennolla `./autoupdate.sh` ja huomasin, että siinä oli kirjoitusvirhe, joten korjasin sen. 

<img width="1626" height="592" alt="image" src="https://github.com/user-attachments/assets/5401da7d-f9dc-4790-8df8-28143ebe3fe4" />


<img width="1654" height="992" alt="image" src="https://github.com/user-attachments/assets/204c7242-05a0-494d-a001-964c16267d90" />

Lopputuloksena on toimiva oma komento.

<img width="1934" height="482" alt="image" src="https://github.com/user-attachments/assets/9c6b0ba3-6e9f-41d9-b4af-db1de9f6adf7" />

### Kaikkien käytössä oleva komento 

Seuraavaksi tein komennostani suoritettavan kaikille käytäjille. Käytin seuraavaa komentoa`sudo cp autoupdate.sh /usr/local/bin/`. Tämän jälkeen testasin komennon suorittamista. 

<img width="1540" height="112" alt="image" src="https://github.com/user-attachments/assets/0b0ae078-3057-4320-8a9d-dc0c7483c8c1" />

Siirryin juurihakemistoon komennolla `cd ..`. Tämän jälkeen käytin komentoa `autoupdate.sh` ja lopputuloksena on toimiva komento eri hakemistoissa. 

<img width="1948" height="636" alt="image" src="https://github.com/user-attachments/assets/aae246f0-8357-4b08-89c0-f18843e7c9b3" />

## d) Arvioitavan laboratorioharjoituksen ratkaiseminen 

Tässä raportin vaiheessa tein aikasempien laboratoritöiden ratkaistavia tehtäviä osaamiseni perusteella: 

[Tero Karvinen - Arvioitava laboratorioharjoitus 2024](https://terokarvinen.com/2024/arvioitava-laboratorioharjoitus-2024-linux-palvelimet)

Jouduin soveltamaan osassa tehtävistä, koska oma aikani loppui kesken tehtävän tekemiselle ja uuden virtuaalikoneen asentamiseen ja määrityksiin ei ollut enää aikaa.

### c) Ei kolmea sekoseiskaa 

Aloitin tehtävän tekemisen luomalla testiraportin libreoffice ohjlemalla `Documents` -kansioon. Seuraavaksi muutin käyttöoikeuksia `chmod 700`, kyseinen oikeus luo käyttöoikeudet vain tiedoston luojalle. Hyödynsin seuraavaa laskutyökalua oikeuksien muokkaamiseen: [Chmod calculator](https://chmod-calculator.com) En tässä tapauksessa olisi varmaan tarvinnut suorittamista varten oikeuksia, mutta laitoin kuitekin kaikki oikeudet tiedostoon. 

<img width="1660" height="1004" alt="image" src="https://github.com/user-attachments/assets/2cb25da9-77b5-4632-bab2-88a18c34ce74" />

<img width="1630" height="752" alt="image" src="https://github.com/user-attachments/assets/8daf55a8-1ac0-45e1-a0eb-6f7d46b3519c" />

Loin vielä testikäyttäjän, jolla kokeilen tiedoston oikeuksien tomivuutta. Virkistin muistia käyttäjien luomisessa seuraavalla ohjeella: [Adding users in linux](https://linuxhandbook.com/useradd-command) Loin uuden käyttäjäm komennolla `sudo useradd labrauser`.

Kokelin kirjautua sisään uudella käyttäjällä `su labrauser`, kyseinen komento tarkoittaa "substitute user" tai "switch user". En päässyt sisään kirjatumaan, joka johtuu siitä, että salasanaa ei ole asetettu. Loin käyttäjälle salasanan ja kokeilin uudestaan. 

<img width="1624" height="306" alt="image" src="https://github.com/user-attachments/assets/0f512270-71f9-4d3e-bc74-0dfdbc1c8f26" />


Tarkastin komennolla `cat /etc/passwd` oliko labrauser luotu ja se oli.

<img width="1628" height="78" alt="image" src="https://github.com/user-attachments/assets/4db0e0ad-f2e2-4b92-bdb6-c30f86762e54" />

Pääsin kirjatumaan sisään luomalleni käyttäjälle, mutta kuten kuvassa näkyy niin `miro` -kotihakemiston oikeudet ovat vain sallittu itse käyttäjälle, joten en pääse sieltä testaamaan tiedostoa. Siirsin sen testiksi `/home` -hakemistoon. 

<img width="1624" height="430" alt="image" src="https://github.com/user-attachments/assets/3274e180-7a79-4161-aa9e-a17c1198fe8a" />

Tässä vaiheessa olisi pitänyt arvata, että "/home" -hakemisto on suojattu ja sinne ei voi tiedostoja siirtää tai kopioida tavallisilla oikeuksia. Sudottamalla oikeudet muuttuvat rootille, joka toki ajaa saman asian, mutta näiden testien perusteella uskon, että tiedosto on suojattu, koska oikeudet ovat muutettu vain tiedoston omistajalle. 

<img width="1630" height="890" alt="image" src="https://github.com/user-attachments/assets/a4014ab6-0bd3-421e-b7c6-acd96c1754d4" />

### d) Howdy 

Tässä vaiheessa loin kaikille käyttäjille komennon "howdy", joka tulostaa erinäisiä järjtestelmän tietoja. Käytin seuraavan artikkelin komentoja: [14 Commands to Display System Information in Linux.](https://andreybyhalenko.medium.com/14-commands-to-display-system-information-in-linux-135a1d57c26e)

Aloitin howdy -komennon tekemisen siirtymällä terminaalissa työpöydälle ja loin sinne tiedoston käyttämällä komentoa `micro howdy.sh`. Loin Bash -tiedoston sisään Bash-skriptiä ja tallensin sen. 

<img width="1610" height="900" alt="image" src="https://github.com/user-attachments/assets/c86ec0f8-e2f2-4e26-a5c3-390932b34747" />


<img width="1656" height="996" alt="image" src="https://github.com/user-attachments/assets/23670271-88e5-45b8-bbd4-013dfab15bee" />

Lopuksi muokkasin tiedoston kaikkien käyttäjien suoritettavaksi, jotta voin ajaa Bash-skriptin. Käytin komentoa `chmod a+x howdy.sh`. Lopuksi testasin sen toimivuutta komennolla `./howdy.sh`. 

<img width="1632" height="300" alt="image" src="https://github.com/user-attachments/assets/c968b33c-b26c-4865-a2dc-0bf2a78aaac7" />


Jouduin asentamaan paketit `sudo apt-get install coreutils` ja `install sysvinit-utils`, jotta komentoni tulostaisi luomani komennot. En saanut `last reoot` - komentoa toimimaan, joten pitää palata asiaan myöhemmin, jos mahdollista. 


<img width="1622" height="912" alt="image" src="https://github.com/user-attachments/assets/4d8005b1-c843-468d-90c3-d6b106f8881d" />



### e) etusivu uusiksi 

Tässä vaiheessa loin Apache 2 webbipalvelimelle uuden kotisivun, Apache2 oli jo asennettu ja ajanpuutteesta johtuen loin tässä harjoituksessa vain uuden indeksitiedoston ja laitoin sen kotisivuksi. Hyödynsin seuraavia ohjetta: [Install and Configure Apache](https://ubuntu.com/tutorials/install-and-configure-apache#1-overview). 


Tarkastin ensiksi apache palvelimeni tilanteen komennolla `sudo systemctl status apache2`. Kuten kuvasta näkyy palvelu on aktiivinen ja käynnissä. 


<img width="1630" height="820" alt="apachectl" src="https://github.com/user-attachments/assets/f6540227-4fae-4225-a148-a61ca8bee836" />

Seuraavaksi avasin verkkosivun selaimesta ja käytin myös komentoa `curl localhost`, tarkastakseeni sivun sisällön. 

<img width="1620" height="898" alt="curllocalhost" src="https://github.com/user-attachments/assets/0a8c26e3-2281-4ab5-b9bb-6450e9b7fb66" />

<img width="2108" height="1344" alt="localhostwebsite" src="https://github.com/user-attachments/assets/89d554ca-6a85-46c1-a670-6827e814c95f" />

Seuraavaksi loin uuden kansion `public-sites-new`, käytin komentoa `mkdir public-sites-new` omassa kotihakemistossani. Seuravaksi loin uuden tekstitiedoston micro -editorilla `ai.kakonen.com` ja lisäsin sen sisälle esimerkkiä varten tekstiä.

<img width="1650" height="996" alt="public sites new" src="https://github.com/user-attachments/assets/f35192cb-08c8-4958-aed4-6ff45fce7600" />


<img width="1664" height="996" alt="aikakonentiedosto" src="https://github.com/user-attachments/assets/12313d81-d376-436d-ad70-c284d77a9228" />

## Name Based Virtual Host Luominen 

Siirruin kansioon `/etc/apache2/sites-available` ja copion kansiossa olevan konfiguraatiotiedoston `hattu.example.com.conf`, käytin komentoa `sudo cp hattu.example.com.conf ai.kakonen.com.conf`.

<img width="1630" height="630" alt="Namebasedvirtualhost2" src="https://github.com/user-attachments/assets/5312823e-de48-49bc-9320-6d0fda447279" />




### g) salattua hallintaa 


## Lähdeluettelo 


https://docs.python-guide.org/starting/install3/linux

https://ioflood.com/blog/install-bash-shell-linux/#:~:text=The%20Bash%20shell%20is%20typically,command%20sudo%20yum%20install%20bash%20.

https://wiki.debian.org/Java 




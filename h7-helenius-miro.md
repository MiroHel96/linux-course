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




## Lähdeluettelo 


https://docs.python-guide.org/starting/install3/linux

https://ioflood.com/blog/install-bash-shell-linux/#:~:text=The%20Bash%20shell%20is%20typically,command%20sudo%20yum%20install%20bash%20.

https://wiki.debian.org/Java 




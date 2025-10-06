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



### Bash 


### Java 



## Lähdeluettelo 


https://docs.python-guide.org/starting/install3/linux

https://ioflood.com/blog/install-bash-shell-linux/#:~:text=The%20Bash%20shell%20is%20typically,command%20sudo%20yum%20install%20bash%20.

https://wiki.debian.org/Java 




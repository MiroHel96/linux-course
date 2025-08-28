# Tiivistelmä 


## Host-operating system spesifikaatiot
  - Operating system: Windows 11 Home
  - Version	10.0.26100 Build 26100
  - Device name	BOOK-QUCSCTFCNT
  - Processor	13th Gen Intel(R) Core(TM) i7-1360P (2.20 GHz)
  - Installed RAM	16,0 GB (15,6 GB usable)
  - System type	64-bit operating system, x64-based processor
  - Pen and touch	Pen and touch support with 10 touch points

## Micro-editorin asentaminen Linuxiin

Tässä raportin osioissa asennan Micro-editorin Linux -työasemalle- Asentaminen tapahtuu virtuaalikoneella ja fyysisellä työasemalla samalla tavalla, joten tämä ohjeistus on toisettavissa. 

Aloitin asentamisen Avaamalla VirtualBoxin ja käynnistämällä virtuaalikoneeni. Kirjauduin työasemaan sisälle ja avasin terminaalin. Micro-editorin dokumentaation mukaan sovellus on asennattavissa eri paketinhallintajärjestelmillä. Tässä tapauksessa käytetään APT, koska asennettu käyttöjärjestelmä on Debian. Syötin terminaaliin komennon "sudo snap install micro --classic". 

<img width="1390" height="1054" alt="image" src="https://github.com/user-attachments/assets/777e7d4a-ab3c-4f95-bc3d-1c931b4e3d5a" />

Hyväksyin asennuksen syöttämällä "Y", asennus onnistui ja tarkastin vielä sovelluksen olemassa olon Application finderin avulla työpöydältä. 


## Kolmen komentoriviohjelman asentaminen samanaikaisesti

Seuraavaksi asensin kolme erilaista komentoriviohjelmaa työasemalle samanaikaisesti. 
Asensin seuraavat ohjelmat:
 - Cool-Retro-Term, kyseinen sovellus tekee terminaalista retron näköisen. Asensin kyseisen ohjelman, koska olen nuorempana pelannut paljon Fallout sarjan pelejä ja halusin jotain personaalista työasemalle, vaikka se ei olisi kovin käytännölinen pitkällä aikavälillä.
 - Terminator Terminal Emulator, mahdollistaa terminaali-ikkunan jakamisen ja säätämisen omien preferenssien mukaan.
 - Quake 3, Dropdown terminaali, joka mahdollistaa komentorivin nopean käytön.

Asensin kaikki sovellukset syöttämällä terminaaliin seuraavan komennon "sudo apt install cool-retro-term terminator guake". Painoin jatka eli "Y" prompttiin ja odotin sovelluksien asentumisen loppuun. Tämän jälkeen tarkistin asennuksen onnistumisen 

<img width="1866" height="196" alt="image" src="https://github.com/user-attachments/assets/96e6fd05-2a63-46dd-aeed-1424bad99d0a" />


<img width="1856" height="1082" alt="image" src="https://github.com/user-attachments/assets/7acef721-8b3e-40ab-af4e-7f1eb3139ad8" />



<img width="1939" height="1072" alt="image" src="https://github.com/user-attachments/assets/149de2ea-b4a5-4d76-980f-35187c72ddb0" />


# Terminator 

<img width="2248" height="1260" alt="image" src="https://github.com/user-attachments/assets/abb71bd0-7996-495a-872e-075016af11ce" />

# Cool-Retro-Term

<img width="1542" height="1236" alt="image" src="https://github.com/user-attachments/assets/a7b4dc1e-b544-4f7f-85f7-3813c431ede7" />


# Guake 


<img width="2874" height="856" alt="image" src="https://github.com/user-attachments/assets/b66636a7-a296-4abf-ba01-aa6f679a8008" />

# FIlesystemissä liikkuminen

Tässä vaiheessa liikuin tärkeiden kansioden sisällä ja näytän kuvien avulla. 

Root -hakemisto
<img width="1672" height="532" alt="image" src="https://github.com/user-attachments/assets/55fd8ecf-432a-4dec-9085-4ccd30240d12" />

Home -hakemisto

<img width="1670" height="176" alt="image" src="https://github.com/user-attachments/assets/aaecb3d5-7356-46a2-8273-fb4cfdbf5794" />

Tässä näkyy kuinka luomani testitiedosto löytyy kotihakemiston työpöytä kansiosta


<img width="1672" height="304" alt="image" src="https://github.com/user-attachments/assets/429d0bb2-6c46-4867-84e8-f14728d529e4" />

/Etc 


<img width="1676" height="700" alt="image" src="https://github.com/user-attachments/assets/49ad7fd4-e8b2-4c11-9889-cf99998ddc49" />

Syöttämällä komennon "ls -l" hakemiston sisältö saadaan tulostettua laajempana. Kuvassa vasemmassa reunassa näkyvä merkintä "drwxr.." merkintä kertoo tiedoston tyypin ja millaiset oikeudet sen muokkaamiseen/käyttöön on. En käy niitä läpi tässä, koska aihealue on suht laaja. Ensimmäinen kirjain kuitekin kertoo mikä tiedostotyyppi on kyseessä. "d" tarkoittaa että kyseessä hakemisto/kansio sen sijaan pelkkä "-" tarkoittaa, että kyseessä on perustiedosto. Esim tekstitiedosto. 

<img width="1678" height="558" alt="image" src="https://github.com/user-attachments/assets/84f5f07e-a50d-4767-affc-72eed24a9d35" />

Käytin komentoa "cat networks", tämän avulla luin mitä "networks" tiedosto sisälti.


<img width="1670" height="244" alt="image" src="https://github.com/user-attachments/assets/e550f359-30d8-4c74-931a-27755ae85f21" />


<img width="1392" height="1056" alt="image" src="https://github.com/user-attachments/assets/31bc9fd6-045f-4521-95a1-8e60edfe3efe" />

<img width="1028" height="958" alt="image" src="https://github.com/user-attachments/assets/01c99e7f-bf19-4742-9956-4e50ba2b906b" />

Seuraavaksi palasin takaisin juurihakemistoon syöttämällä komennon "cd ..". 


<img width="1678" height="236" alt="image" src="https://github.com/user-attachments/assets/6fd45c6d-0c57-4aca-879a-bf1248fbfd25" />

Seuraavaksi siirryin hakemistoon "Media" syöttämällä komennon "cd /media". Kyseisestä hakemistosta löytyi cdrom ja cdrom0. Jälkimmäinen on linkki ensimmäiseen kansioon. 


<img width="1684" height="506" alt="image" src="https://github.com/user-attachments/assets/81907043-f902-4018-8ca1-29c30b41f061" />

Seuraavaksi siirryin lokihakemistoon syöttämällä komennot "cd.." ja "cd /var/log/". 


<img width="1676" height="434" alt="image" src="https://github.com/user-attachments/assets/e4723dce-7e59-4f13-9952-56ec772c5755" />

Siirryin "Journal" -hakemistoon ja syötin cat -komennon ja putkitin samalla "less" perään. Tein kuitekin virheen koska yritin lukea hakemistoa. Terminaali meni tästä looppiin ja minun piti pystäyttää toiminto painamalla ctrl + z yhdistelmällä. Tämän jälkeen siiryin hakemistoon ja cat- komennolla tarkistin lokeja.

<img width="2002" height="1194" alt="image" src="https://github.com/user-attachments/assets/6f15fd77-b11d-4105-85ff-ae531f563a8d" />



<img width="1980" height="1182" alt="image" src="https://github.com/user-attachments/assets/b969f9e4-32ac-4175-a359-919f7c10a34e" />


## Lähdeluettelo 

https://micro-editor.github.io - Mircro-editori Linuxille. 

https://github.com/zyedidia/micro#installation - Micro-editorin asentaminen.

https://itsfoss.com/cool-retro-term - Retro terminaali Linux

https://gnome-terminator.org 

https://github.com/Guake/guake - Guake 3 





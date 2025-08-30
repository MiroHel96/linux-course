# Tiivistelmä 
 - Linuxissa ja Unixsissa käytettävä komentokehote on kestänyt läpi aejan. Se on ollut käytössä ennen käyttöjärjestelmiä ja internettiä. Sen etuja on nopeus ja helppo automatisointi.
-Komentokehotteessa ollaan aina hakemistossa, hyviä peruskomentoja ovat:
  - pwd, tulosta nykyinen hakemisto
  - ls, listaa hakemiston sisältö
  - cd (tiedostopolku) ja cd .. (liiku taaksepäin hakemistossa)

## Tiedoston manipulointi: 
- nano, editoi tekstitiedosta
- mkdir, luo kansio
- mv, liikuta tiedostoa
- cp, kopio tiedosto
- rm ja rmdir - tiedoston- ja kansion poistaminen.

## Etäyhteyden ottaminen SSH:
- ssh domain.com
- exit, poistu etäyhteydestä
- scp -r Folder domain.com: public_html/, kopio tiedosto turvallisesti etäyhteyden päässä olevasta koneesta.

## Help:
- man, komennolla saa esiin halutun komennon manuaalin.
- ls --help
- wget -h

## History and Guessing:
- Tabulaattorilla voi täydentää komentoja
- Nuoli ylöspäin näyttää edellisen komennon
- Komentoa voi muokata liikkumalla nuolella oikealle tai vasemmalle
- histoy, näyttää komentojen historian

## Tärkeitä hakemistoja:
- / , juuri hakemisto
- /home/ , kotihakemisto. /home/miro/ , kyseiseen hakemistoon käyttäjä voi tallentaa pysyvästi omia tiedostoja ilman sudo -oikeuksia.
- /etc/ , järjestelmän asetukset
- /media/, irroitetava media löytyy tästä hakemistosta
- /var/log , järjestelmän lokit löytyvät täältä

## Järjestelmänvalvojan oikeudet 
- sudo (super user), tällä komennolla voidaan ajaa toimintoja root - käyttäjän oikeuksilla.
- Sudon avulla voidaan tehdä erilaisia toimenpiteitä järjestelmässä, jotka       vaativat korotettuja oikeuksia. Näitä ovat esimerkiksi sovelluksien            asentaminen sekä poistaminen, käyttäjien luominen, hallinta ja                 muokkaaminen.
    
## Host-operating system spesifikaatiot
  - Operating system: Windows 11 Home
  - Version	10.0.26100 Build 26100
  - Device name	BOOK-QUCSCTFCNT
  - Processor	13th Gen Intel(R) Core(TM) i7-1360P (2.20 GHz)
  - Installed RAM	16,0 GB (15,6 GB usable)
  - System type	64-bit operating system, x64-based processor
  - Pen and touch	Pen and touch support with 10 touch points

## Micro-editorin asentaminen Linuxiin

Tässä raportin osioissa asennan Micro-editorin virtuaalityöasemalle, jossa on Linux -käyttöjärjestemlmä. Micro-editori on terminaalipohjainen tekstieditori Linuxille. Asentaminen tapahtuu virtuaalikoneella ja fyysisellä työasemalla samalla tavalla, joten tämän raportin kaikki osiot on toisettavissa. 

Aloitin asentamisen avaamalla VirtualBoxin ja käynnistämällä virtuaalikoneeni. Kirjauduin työasemaan sisälle ja avasin terminaalin. Micro-editorin dokumentaation mukaan sovellus on asennattavissa eri paketinhallintajärjestelmillä. Tässä tapauksessa käytetään APT, koska asennettu käyttöjärjestelmä on Debian. Syötin terminaaliin komennon "sudo snap install micro --classic". 

<img width="1390" height="1054" alt="image" src="https://github.com/user-attachments/assets/777e7d4a-ab3c-4f95-bc3d-1c931b4e3d5a" />


Jatkoin asennusta syöttämällä "Continue" -kehotteeseen "Y". Asennus suoriutui onnistuneesti ja tarkastin vielä sovelluksen olemassa olon Application finderin avulla työpöydältä. 


<img width="1392" height="1056" alt="image" src="https://github.com/user-attachments/assets/31bc9fd6-045f-4521-95a1-8e60edfe3efe" />

<img width="1028" height="958" alt="image" src="https://github.com/user-attachments/assets/01c99e7f-bf19-4742-9956-4e50ba2b906b" />


## Kolmen komentoriviohjelman asentaminen samanaikaisesti

Seuraavaksi asensin kolme erilaista komentoriviohjelmaa työasemalle samanaikaisesti. 

Asensin seuraavat ohjelmat:
 - Cool-Retro-Term, kyseinen sovellus tekee terminaalista retron näköisen. Asensin kyseisen ohjelman, koska olen nuorempana pelannut paljon Fallout sarjan -pelejä ja halusin jotain personaalista työasemalle, vaikka se ei olisi kovin käytännölinen pitkällä aikavälillä.
 - Terminator Terminal Emulator mahdollistaa terminaali-ikkunan jakamisen ja säätämisen omien preferenssien mukaan.
 - Quake 3 on dropdown terminaali, joka mahdollistaa komentorivin nopean käytön. Terminaali-ikkuna on avattivissa F12 painikkeella ja se pysyy piilossa taustalla työkalupalkissa.

Asensin kaikki sovellukset syöttämällä terminaaliin seuraavan komennon "sudo apt install cool-retro-term terminator guake". Painoin jatka eli "Y" prompttiin ja odotin sovelluksien asentumisen loppuun. Tämän jälkeen tarkistin asennuksen onnistumisen jälleenkerran application finderistä. 


<img width="1866" height="196" alt="image" src="https://github.com/user-attachments/assets/96e6fd05-2a63-46dd-aeed-1424bad99d0a" />


<img width="1856" height="1082" alt="image" src="https://github.com/user-attachments/assets/7acef721-8b3e-40ab-af4e-7f1eb3139ad8" />


<img width="1939" height="1072" alt="image" src="https://github.com/user-attachments/assets/149de2ea-b4a5-4d76-980f-35187c72ddb0" />


# Terminator 


<img width="2248" height="1260" alt="image" src="https://github.com/user-attachments/assets/abb71bd0-7996-495a-872e-075016af11ce" />

# Cool-Retro-Term

<img width="1542" height="1236" alt="image" src="https://github.com/user-attachments/assets/a7b4dc1e-b544-4f7f-85f7-3813c431ede7" />


# Guake 


<img width="2874" height="856" alt="image" src="https://github.com/user-attachments/assets/b66636a7-a296-4abf-ba01-aa6f679a8008" />


# Filesystemissä liikkuminen

Tässä raportin vaiheessa liikuin käyttöjärjestelmän tiedostojärjestelmässä terminaalin avulla käyttämällä eri komentoja.  

Juuri -hakemisto 

Kuten juurihakemiston (/) kuvassa näkyy, hakemisto sisältää käyttöjärjestelmän kaikki näkyvät kansiot. Komnenolla "ls -a" saa näkyviin hakemiston piilotetut kansiot/tiedostot.

<img width="1672" height="532" alt="image" src="https://github.com/user-attachments/assets/55fd8ecf-432a-4dec-9085-4ccd30240d12" />

Home -hakemisto

Kotihakemistossa näkyy käyttöjäjestelmän eri käyttäjät, tässä tapauksessa virtuaalikoneellani on vain yksi käyttäjä "miro". 

<img width="1670" height="176" alt="image" src="https://github.com/user-attachments/assets/aaecb3d5-7356-46a2-8273-fb4cfdbf5794" />


Tässä näkyy kuinka luomani testitiedosto "TestFile" löytyy kotihakemiston työpöytä -kansiosta.


<img width="1672" height="304" alt="image" src="https://github.com/user-attachments/assets/429d0bb2-6c46-4867-84e8-f14728d529e4" />


Etc -hakemisto

Etc -hakemisto sisältää käyttöjärjestelmän kaikki konfiguraatio tiedostot. "The Linux Foundation"

<img width="1676" height="700" alt="image" src="https://github.com/user-attachments/assets/49ad7fd4-e8b2-4c11-9889-cf99998ddc49" />

Syötin komennon "ls -l", jolla hakemiston sisältö saadaan tulostettua laajempana. Kuvassa vasemmassa reunassa näkyvä merkintä "drwxr.." merkintä kertoo tiedoston tyypin ja millaiset oikeudet sen muokkaamiseen/käyttöön on. 

En käy tiedostojärjestelmää läpi tässä raportissa sen tarkemmin. Ensimmäinen kirjain kuitekin kertoo mikä tiedostotyyppi on kyseessä. "d" tarkoittaa että kyseessä hakemisto/kansio sen sijaan pelkkä "-" tarkoittaa, että kyseessä on perustiedosto. Esim tekstitiedosto. Medium - Understanding Linux File Permission. 


<img width="1678" height="558" alt="image" src="https://github.com/user-attachments/assets/84f5f07e-a50d-4767-affc-72eed24a9d35" />

Tulostin /etc -kansiossa "networks" tiedoston sisällön käyttämällä komentoa "cat networks".

<img width="1670" height="244" alt="image" src="https://github.com/user-attachments/assets/e550f359-30d8-4c74-931a-27755ae85f21" />


Seuraavaksi palasin takaisin juurihakemistoon syöttämällä komennon "cd ..". 


<img width="1678" height="236" alt="image" src="https://github.com/user-attachments/assets/6fd45c6d-0c57-4aca-879a-bf1248fbfd25" />

Media -hakemisto

Seuraavaksi siirryin hakemistoon "Media" syöttämällä komennon "cd /media". Kyseisestä hakemistosta löytyi cdrom ja cdrom0. Jälkimmäinen on linkki ensimmäiseen kansioon. Kansio sisältää irroitettavat media-laitteet kuten muistitikut ja kovalevyt - terokarvinen.com


<img width="1684" height="506" alt="image" src="https://github.com/user-attachments/assets/81907043-f902-4018-8ca1-29c30b41f061" />

/var/log -hakemisto

Seuraavaksi siirryin lokihakemistoon syöttämällä komennot "cd.." ja "cd /var/log/". Kyseisestä tiedostopolusta löytyy työaseman tuottamia lokeja. MM hyödyllinen vika- ja virhetilanteita selvittäessä.


<img width="1676" height="434" alt="image" src="https://github.com/user-attachments/assets/e4723dce-7e59-4f13-9952-56ec772c5755" />

Siirryin "Journal" -hakemistoon ja syötin cat -komennon ja putkitin samalla "less" perään. Tein kuitekin virheen koska yritin lukea hakemistoa. Terminaali meni tästä looppiin ja minun piti pystäyttää toiminto painamalla "ctrl + z". Tämän jälkeen siiryin hakemistoon ja "cat" -komennolla tulostin lokien tekstiä. 

Esimerkkikuvassa avasin "user-1000.journal". 


<img width="2002" height="1194" alt="image" src="https://github.com/user-attachments/assets/6f15fd77-b11d-4105-85ff-ae531f563a8d" />



<img width="1980" height="1182" alt="image" src="https://github.com/user-attachments/assets/b969f9e4-32ac-4175-a359-919f7c10a34e" />


## Grep -kommennon käyttäminen 

Tässä vaiheessa demostroin grep-komennon eri käyttötarkoituksia. Grep on tarkoitettu tiedostojen etsimiseen tiedostojärjestelmästä. GeekForgeeks - grep command in Unix/Linux, 

Loin työpöydälle "TestFile" -nimisen tekstitiedoston ja lisäsin sinne satunnaisesti eri autojen merkkejä. Seuraavaksi avasin terminaalin ja syötin komennon "grep -e "Audi" -e "BMW" -e "Toyota" TestFile". Kyseinen komento etsii vastinetta antamilleni automerkeille testitiedoston sisältä ja tulostaa tulokset. Server Academy - Grep Multiple String in Linux


<img width="750" height="240" alt="image" src="https://github.com/user-attachments/assets/a3fc44ab-7b12-4d50-841f-f28bdf5f6d1e" />


Seuraavassa esimerkissä syötin komennon "grep -w "DHCP" dhcp.conf".  kyseinen komento hakee vastineita hakusanalle tekstiriveiltä. Esimerkissä etsin tiedoston esimerkiksi "/etc" -kansiosta.


<img width="808" height="158" alt="image" src="https://github.com/user-attachments/assets/93975cde-601f-44d3-819a-f7cdfa417b61" />


"Grep" -komennolle löytyy paljon hyödyllisiä yhdistelmiä, mutta en käy niitä läpi tässä sen tarkemmin. Tämän esimerkin tarkoitus oli demostroida komennon perusideaa.

## Piping eli putkittaminen

Putkittaminen on useiden komentojen yhdistämistä yhteen komentoon. Tämän avulla nopeutetaan työskentelyä ja kokeneet käyttäjät pystyvätkin tämän avulla ajamaan hyvin monimutkaisia toimintoja. GeekForGeeks - Piping in Unix or Linux

Lisäsin esimerkkitekstiä työpöydällä olevaan "TestFile.txt" -tiedostoon ja avasin tämän jälkeen terminaalin. Syötin terminaaliin seuraavan komennon "cat TestFile.txt | grep -Ei "Car|Ferrari|Toyota". Vastauksena sain kokonaiset tekstirivit, jotka sisältivät haluamani hakusanat. 

<img width="806" height="270" alt="image" src="https://github.com/user-attachments/assets/98f7268e-073e-415d-9796-2c80a389230d" />


## Testityöaseman rauta 

Tässä vaiheessa listasin virtuaalikoneeni raudan käyttämällä komentoa "sudo lshw -short -sanitize". 

Kuten kuvassa näkyy, komento listasi järjestelmän laitetiedot seuraavasti:
 - H/W path on laitteen fyysinen polku/kytkennän järjestys. 
 - Device on kuvaus, missä laite sijaitsee tiedostojärjestelmässä. Tämä koskee oheislaitteita ja komponentteja kuten hiiret, näppäimisöt ja kovalevyt. 
 - Class eli luokka kuvastaa minkä tyypin laite on kyseessä esim. prosessori, muistit, verkkoadapteri, käyttöjärjestelmä yms.
 - Description kuvaa tarkemmin laitteen tietoja, esim muistin määrä, prosessorin malli tai mikä hiiri on koneessa kiinni.

<img width="1000" height="662" alt="image" src="https://github.com/user-attachments/assets/865756bb-e570-4647-87bc-a0f3d0987307" />


## Lähdeluettelo 

https://micro-editor.github.io

https://micro-editor.github.io - Mircro-editori Linuxille. 

https://github.com/zyedidia/micro#installation - Micro-editorin asentaminen.

https://itsfoss.com/cool-retro-term - Retro terminaali Linux

https://gnome-terminator.org 

https://github.com/Guake/guake - Guake 3 

https://www.geeksforgeeks.org/linux-unix/grep-command-in-unixlinux 

https://serveracademy.com/blog/grep-multiple-strings-in-linux/#:~:text=The%20simplest%20way%20to%20search,for%20in%20a%20single%20command.

https://www.geeksforgeeks.org/linux-unix/piping-in-unix-or-linux

https://linuxhandbook.com/lshw-command

https://www.linuxfoundation.org/blog/blog/classic-sysadmin-the-linux-filesystem-explained



# Tiivistelmä 

## H3 Demonit 

# (a Apache 2 asentaminen Linux

Tässä raportiss asensin virtuaalikoneelleni Apache 2 web -palvelimen. Aloitin asennuksen avaamalla virtuaalikoneeni, avasin terminaali-ikkunna ja syötin seuraavan komennon "sudo apt update" ja tämän jälkeen komennon "sudo apt install apache2". 

<img width="696" height="162" alt="image" src="https://github.com/user-attachments/assets/be5811a3-90c8-47aa-85fa-47de253cdc60" />

Sain seuraavan virheen "sudo apt update" -komennon jälkeen en tiedä mistä se johtuu, mutta selvityksen jälkeen sain selville, että...

<img width="1080" height="416" alt="image" src="https://github.com/user-attachments/assets/49b79686-87c4-4866-b81b-4cbd7ab94c0d" />

Seuraavaksi syötin komennon "sudo apt install -y apache2". Asennus onnistui ja tämän jälkeen testasin palvelimen toimivuutta.

<img width="882" height="160" alt="image" src="https://github.com/user-attachments/assets/0eb81c0e-9680-4175-92d1-bf4a60314fa2" />

Selvitin, miten palvelimen toimivuuden pysti testaamaan ja komennolla "sudo systemctl status apache2" -komennolla pääsin testaamaan palvelinta. Palvelimen status oli "active (running), joten se oli käynnistynyt onnistuneesti. Kokeilin vielä verkkoselaimesta "localhost" -osoitetta onnistuneesti. 

Terminaali-ikkunan kautta pystyi myös testaamaan sivun toimivuutta ja kokeilinkin seuraavan ohjeen mukaisesti https://curl.se/docs/tutorial.html. Pystyin siis "curl" -komennon avulla tulostamaan sivun html sisällön suoraan terminaali-ikkunaan. 

<img width="878" height="402" alt="image" src="https://github.com/user-attachments/assets/d9cd06d5-6966-4ab4-9d79-15cfb588f310" />

<img width="1018" height="852" alt="image" src="https://github.com/user-attachments/assets/45d927f9-fdcb-47f3-b8c6-8296f6a20df1" />

<img width="958" height="252" alt="image" src="https://github.com/user-attachments/assets/b745fa5a-14a8-4834-bb0c-5599dd81e59e" />

# (b lokit

Tässä raportin vaiheessa tarkastelin apache2 palvelimeni luomia lokeja. En ollut varma tai muista mihin polkuun lokitiedostot tallentui, joten nopean Googlettamisen jälkeen löysin artikkelin, jossa oli hyvin ohjeistettu lokien polut ja tarkasteluun käytettävät komennot: https://phoenixnap.com/kb/apache-access-log

Apache2 lokit sijaitsevat tiedostojärjestelmässä polussa /var/log/apache2, siirryin kyseiseen tiedostopolkuun terminaali-ikkunassa. Seuraavaksi avasin verkkoselaimen työpäydällä ja kirjoitin selaimen hakuun "localhost". 

<img width="936" height="594" alt="image" src="https://github.com/user-attachments/assets/9cd30598-8937-4b1c-9849-f2e8f19a5475" />

Kuten, kuvassa näkyy lokeihin ilmestyy HTTP GET -kättely pyyntö aina, kun verkkosivun lataa uudelleen. Lokien tarkempaa analyysia varten löysin hyvän artikkelin verkosta: https://www.sumologic.com/blog/apache-access-log


<img width="954" height="1028" alt="image" src="https://github.com/user-attachments/assets/c41fdf26-1578-4456-866c-46a5161df0b5" />

Lokit analysoituna vasemmalta oikealle kohta kohdalta:
 - 127.0.0.1 on yhteyspyynnön tekijän IP-osoite.
 - - - Tässä kohtaa pitäisi näky käyttäjän identiteetti, ensimmäinen viiva RFC1413 indentiteetti ja toinen viima ei autentikoitua käyttäjänimeä - Copilot
  - [04/Sep/2025:16:56:27 +0300], tämä on pyynnön päivämäärä ja kellonaika.
  - "GET / HTTP/1.1", pyynnön tyyppi ja tässätapauksessa kyseessä on perus HTTP pyyntö.
  - 200 HTTP statuksen koodi
  - 481 objektin koko joka palautettiin clientille, eli pyynnön tehneelle. 

<img width="924" height="44" alt="image" src="https://github.com/user-attachments/assets/ca46e3d3-92e6-4ca3-98bf-186b522108ca" />



# Oman verkkosivun luominen

Tässä vaiheessa loin uuden index.html tiedoston (sijainti) ja testasin sen toimivuuden apache -palvelimellani. Poistin ja loin uuden index.html tiedoston /var/www/html -polkuun. Tiedostot olivat suojattu, joten kirjauduin sisälle root -käyttäjäksi ja siirryin tidostopolkuun apache2/. Kansiosta löytyi seuraavat tiedostot, access.log, error.log ja other_vhost_access.log.

Avasin tiedoston "tail -f" -komennolla. Kyseinen komento näyttää tiedoston viimeiset rivit, -f valinta tulostaa lokin tiedot reaaliajassa terminaali-ikkunaan, jos muutoksia tapahtuu. 




<img width="632" height="502" alt="image" src="https://github.com/user-attachments/assets/dde0195b-fd1d-4dd0-b514-8992e849fae0" />

<img width="618" height="74" alt="image" src="https://github.com/user-attachments/assets/d46fd77f-c045-4185-b8ae-43d5b6ac1df6" />

Tiedoston luomisen jälkeen testasin sivun toimivuutta verkkoselaimessa osoitteessa "localhost". 

<img width="838" height="434" alt="image" src="https://github.com/user-attachments/assets/4c65c02e-e4e7-47e6-a833-10203b8f2a29" />

#Palomuurin salliminen 

Asensin komentohekotteela ufw

<img width="556" height="602" alt="image" src="https://github.com/user-attachments/assets/00c71a85-0cb7-42bf-b955-c7877d68cdda" />



# C Etusivu uusiksi 

Tässä vaiheessa raporttia tehtäväni oli luoda uusi name based virtual host eli uusi verkkosivu nimellä hattu.example.com. Käytin sivun tekemiseen seuraavaa sivua, josta sain ohjeistuksen avulla toteutettua uuden sivun: https://terokarvinen.com/2018/04/10/name-based-virtual-hosts-on-apache-multiple-websites-to-single-ip-address

ALoitin avaamlla terminaalin ja syötin siihen seuraavan komennon "sudoedit /etc/apache2/sites-available/hattu.example.com.conf". Tämän jälkeen lisäsin teksieditorissa alla olevan kuvan mukaisesti verkkosivun määritykset alla olevan kuvan mukaisesti.

<img width="556" height="606" alt="image" src="https://github.com/user-attachments/assets/08eda54e-2688-4ee0-8c4d-1c126dcfd89b" />

Seuraavaksi aktivoin uuden configuraation palvelimelle käyttämällä seuraavia komentoja "sudo a2ensite hattu.example.com" ja "sudo systemctl restart apache2". 

<img width="539" height="130" alt="image" src="https://github.com/user-attachments/assets/d8e8cc99-6c4d-4067-8fe1-c7044a7c4c76" />

Seuraavaksi loin uuden kasion ja index.html tiedoston peruskäyttäjän kotihakemistoon "public-sites". Loin kansion nimellä "hattu.example.com" ja tiedoston, kuten mainitsin index.html. Käytin seuraavia komentoja toimenpiteen suorittamiseen: 
 - sudo mkdir -p /home/miro/public-sites/hattu.example.com/
 - sudo echo hattu > /home/miro/public-sites/hattu.example.com/index.html

Jouduin käyttämään sudo -oikeuksia näiden tekemiseen ja en ole varma, miksi näin on. Käyttöoikeudet eivät selvästi ole oikein, joten päätin selvittää asiaa hieman.

<img width="545" height="181" alt="image" src="https://github.com/user-attachments/assets/89c8c4dc-bee0-44cd-80ea-5dd111dff8fb" />

En pystynyt luomaan index.html tiedostoa ollenkaan.
<img width="543" height="90" alt="image" src="https://github.com/user-attachments/assets/408a9566-4f24-427e-94c5-c8512b451613" />

Loin tiedoston root -käyttäjällä, mutta tämä ei ole optimaalista. Katsoin vielä käyttöoikeudet ja kaikilla käyttäjillä on tiedostoon luku -oikeus. Tällä tosin ei pitäisi olla väliä? 
<img width="543" height="208" alt="image" src="https://github.com/user-attachments/assets/51fcddc6-4257-44f3-9636-fdbfad971b4c" />


 ## Curl testi

 Ensimmäinen testi tuotti puutteeliset käyttöoikeudet:
 <img width="543" height="249" alt="image" src="https://github.com/user-attachments/assets/9cb1cdd2-d582-42c9-923e-d43a6a3548ae" />

Toinen testi latasi eri tiedoston sisällöin, jonka olin tehnyt aikaisemmin. Ongelmaksi epäilin, että hosts -tiedoston sisältö ei ollut muokattu uuden sivun mukaisesti. Tein tarvittavat muutokset.

<img width="544" height="180" alt="image" src="https://github.com/user-attachments/assets/af9296ff-de9b-480d-8ffa-cc266777b811" />

<img width="557" height="603" alt="image" src="https://github.com/user-attachments/assets/5919f85d-0f4e-46c4-8255-e71c60207a8b" />

Host tiedostoon lisäsin seuraavat osoitetiedot:
hattu.example.com
www.hattu.example.com

<img width="395" height="364" alt="image" src="https://github.com/user-attachments/assets/787acba6-48a5-48c2-965a-d8b13fac5e4d" />


Tämän jälkeen testasin avata verkkosivun selaimesta, mutta lopputulos ei siltikään ollut oikein. Aloitin tekemään lisäselvitystä juurisyylle. 

<img width="661" height="637" alt="image" src="https://github.com/user-attachments/assets/54c92ed5-d129-47b1-9b40-38798ed9049c" />

Ongelma ilmeisesti oli tiedostojen oikeuksissa, tarkasin kyseisestä ohjeesta kohdan 5. name based virtual hosts ja siellä mainitaan, että apachen pitää pystyä lukemaan tiedostot, jotta verkkosivu toimii. https://github.com/johannaheinonen/johanna-test-repo/blob/main/linux-03092025.md 

Seuraavaksi tarkastin tiedostojen ja kansioiden oikeudet. Ne näyttivät oikelta. Poistin ylimääräiset esimerkkitiedostot työasemalta ja tarkasin polusta "sudoedit /etc/apache2/sites-available/hattu.example.conf" konffitiedostos. Huomasin, että dokumentin polku ja juurisijainnissa "publicsites" oli kirjoitettu yhteen väliviivan sijaan. Korjasin sen muotoon "public-sites" ja testasin uudestaan verkkosivun toimivuutta. 

<img width="904" height="733" alt="image" src="https://github.com/user-attachments/assets/e0f0499f-1710-44b2-81ca-82c9c846727e" />

Ongelma ei vieläkään korjaantunut, joten jatkoin asian selvittämistä. Väärä tiedosto aukeaa vieläkin.

<img width="483" height="511" alt="image" src="https://github.com/user-attachments/assets/671bfee4-5d9b-4c9a-81db-2bdc760ba384" />


# (e Validi HTML5 sivu

# (f curl -l ja curl esimerkit

# (m Vapaaehtoinen 1

# (0 vapaaehtoinen 2

# Lähdeluettelo 

https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-debian-11

https://www.linux.fi/wiki/CURL

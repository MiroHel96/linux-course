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

# Oman verkkosivun luominen

Tässä vaiheessa loin uuden index.html tiedoston (sijainti) ja testasin sen toimivuuden apache -palvelimellani. Poistin ja loin uuden index.html tiedoston /var/www/html -polkuun. 


<img width="632" height="502" alt="image" src="https://github.com/user-attachments/assets/dde0195b-fd1d-4dd0-b514-8992e849fae0" />

<img width="618" height="74" alt="image" src="https://github.com/user-attachments/assets/d46fd77f-c045-4185-b8ae-43d5b6ac1df6" />

Tiedoston luomisen jälkeen testasin sivun toimivuutta verkkoselaimessa osoitteessa "localhost". 

<img width="838" height="434" alt="image" src="https://github.com/user-attachments/assets/4c65c02e-e4e7-47e6-a833-10203b8f2a29" />


# C Etusivu uusiksi 

# (e Validi HTML5 sivu

# (f curl -l ja curl esimerkit

# (m Vapaaehtoinen 1

# (0 vapaaehtoinen 2

# Lähdeluettelo 

https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-debian-11

https://www.linux.fi/wiki/CURL

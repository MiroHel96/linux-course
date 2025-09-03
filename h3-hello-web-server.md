# Tiivistelmä 

## H3 Demonit 

# Apache 2 asentaminen Linux

Tässä raportiss asensin virtuaalikoneelleni Apache 2 web -palvelimen. Aloitin asennuksen avaamalla virtuaalikoneeni, avasin terminaali-ikkunna ja syötin seuraavan komennon "sudo apt update" ja tämän jälkeen komennon "sudo apt install apache2". 

<img width="696" height="162" alt="image" src="https://github.com/user-attachments/assets/be5811a3-90c8-47aa-85fa-47de253cdc60" />

Sain seuraavan virheen "sudo apt update" -komennon jälkeen en tiedä mistä se johtuu, mutta selvityksen jälkeen sain selville, että...

<img width="1080" height="416" alt="image" src="https://github.com/user-attachments/assets/49b79686-87c4-4866-b81b-4cbd7ab94c0d" />

Seuraavaksi syötin komennon "sudo apt install -y apache2". Asennus onnistui ja tämän jälkeen testasin palvelimen toimivuutta.

<img width="882" height="160" alt="image" src="https://github.com/user-attachments/assets/0eb81c0e-9680-4175-92d1-bf4a60314fa2" />

#


# Lähdeluettelo 

https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-debian-11

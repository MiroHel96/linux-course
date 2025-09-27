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

Tässä raportin vaiheessa loin ilmaisen TLS-Sertifikaatin palvelimelleni. Hyödynsin seuraavia verkkosivuja sen tekemisessä: https://terokarvinen.com/linux-palvelimet/#h6-salataampa, https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample ja ....

Aloitin avaamalla virtuaalikoneeni ja kirjauduin sisään. Tämän jälkeen otin SSH -yhteyden luomaani palvelimeen. 

<img width="1660" height="570" alt="image" src="https://github.com/user-attachments/assets/780dec72-50d1-4a4c-be72-af006f3d4df5" />

Käynnistin ensiksi apache palvelun uudestaan, ennekuin aloitin tekemään TLS-sertifikaattia. 

'sudo systemcelt restart apache2' 

Tämän jälken testastin, että verkkosivu toimii eri päätelaitteilla. 

<img width="2552" height="524" alt="image" src="https://github.com/user-attachments/assets/dfe08231-fc0b-47c7-b5eb-fe9158fe801d" />


# b) TLS-testaus 


# c) Vapaaehtoinen 



# Lähdeluettelo 

https://letsencrypt.org/how-it-works/
https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample

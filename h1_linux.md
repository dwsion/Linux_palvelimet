# h1 - Linuxin asennus ja raportin kirjoittaminen

 


## Hyvä raportti 

- Täsmällinen ja sisältää tarkat tiedot tehdyistä asioista 

- Lopputulos ja vaiheet toistettavissa kenen tahansa raportin lukijan toimesta 

- Helppolukuinen ja ymmärrettävä 

- Viittaa lähteisiin ja ei ole plagioitu 

- On totuudenmukainen 

## FSF 

- Vapaa ohjelmisto kunnioittaa käyttäjien vapauksia ja yhteisöä. Käyttäjillä on vapaus kopioida, levittää, tutkia, muuttaa ja parantaa ohjelmistoa. 

- Vapaa ohjelmisto voi olla myös kaupallista 

  ## Neljä keskeistä vapautta: 

- Vapaus käyttää ohjelmaa haluamallaan tavalla mihin tahansa tarkoitukseen  

- Vapaus tutkia, miten ohjelma toimii, ja muokata sitä tarpeen mukaan. Vapaa lähdekoodi on edellytys tälle 

- Vapaus levittää ohjelman kopioita muille 

- Vapaus jakaa muokattuja versioita ohjelmasta, jotta yhteisö voi hyötyä muutoksista 

 

# Linuxin asennus 

### Laitteisto 

Tehtävän suorittamiseen käytin seuraavanlaista tietokonetta: 

Lenovo X1 /Intel Core Ultra 7 155U/14WUXGA/32GB/512SSD/5G/W11P

 

### Tehtävän anto  

Kotitehtävänä oli asentaa Linux virtuaalikoneeseen ja raportoida siihen liittyvät vaiheet. 

 

### Valmistelu 

Aloitin tehtävän suorittamisen lukemalla ensin tehtävänannon ja siihen liittyvät vinkit, sekä lataamalla 21.08.2024 n. klo 20.30 Debian live 12.6.0 amd64 Xfce-latauspaketin. Seuraavaksi latasin ja asensin myös Oraclen Virtual Box 6.1.50:n ja olin valmis aloittamaan varsinaisen tehtävän suorittamisen, joka oli asentaa Linux virtuaalikoneeseen. 

### Virtuaalikoneen luominen 

Asentamisen jälkeen avasin Virtual boxin ja valitsin ylälaidasta kohdan New. 

![image](https://github.com/user-attachments/assets/ba70cb94-1265-4205-a04c-80d6626a479c)

 

Näytölle ilmestyi ponnahdusikkuna, jossa täytettiin seuraavaksi koneen nimi, tallennuspolku sekä valittiin asennettava ohjelmisto. Valitsin koneen nimeksi Asentaja ja Debian Linuxin ohjelmistoksi. Seuraavaksi valittiin virtuaalikoneelle annettava RAM-muistin määrä, jota annoin 4096Mb, sekä luotiin virtuaalinen kovalevy. Kovalevyn tyypiksi valittiin VDI ( VirtualBox Disk Image). Seuraavassa kohdassa valittiin dynaamisesti allakoitu kovalevytila isäntäkoneelta. Levytilan määräksi asetettiin 60Gb. 

 ![image](https://github.com/user-attachments/assets/04fb6f73-a7e1-4d62-bc0a-34b721368ce9)


Nyt virtuaalikone on luotu ja valmiina käyttöjärjestelmän asentamista varten. 

![image](https://github.com/user-attachments/assets/0fd1fb9d-fdb6-4d6f-8b42-bd474ab9a9b1)

### Käyttöjärjestelmän asentaminen virtuaalikoneeseen

Virtual Boxin vasemmasta laidasta valittiin aktiiviseksi äsken luto kone, jonka jälkeen ylhäältä valittiin settings. Seuraavassa kuvassa näkyy, kohta jossa ollaan settings-välilehdellä avaamassa virtual optical disk fileä. 

 ![image](https://github.com/user-attachments/assets/30ae0430-5051-42aa-a6c7-dc026d4fdff5)

Valinnan jälkeen levykuva näkyy nyt Storagen alla, joka vielä äsken oli tyhjänä. 

 ![image](https://github.com/user-attachments/assets/adb7eed8-44a3-4113-9272-72ec31f21a8f)


Tämän jälkeen buuttasin virtuaalikoneen tuplaklikkaamalla sitä vasemmasta valikosta. 

Näin saimme koneen käyntiin ja pääsin valitsemaan, että testaanko suoraan debianin toimivuutta koneella avaamalla sen livetilassa vai käynnistänkö suoraan asennuksen. Tein samalla tavalla kuin luennolla tehtiin ja testasin sitä ensin livenä valitsemalla ylimpänä olevan vaihtoehdon. 

  ![image](https://github.com/user-attachments/assets/8c5ca3c8-9efe-4f14-ae51-5ac11013ef5e)


 

Kone asentui ennen avautumista työpöydälle noin kaksi minuuttia. Seuraavaksi testasin koneen eri osien toimivuutta, ennen kuin siirryin varsinaiseen asentamiseen. 

Kokeilin internettiä, avasin applikaation ja file systemsin. Kaikki näytti toimivan hyvin, joten aloitin debianin asentaminen klikkaamalla työpöydältä löytyvää Install Debian-kuvaketta. 

 ![image](https://github.com/user-attachments/assets/7fd1b2a8-64c5-44d8-b618-65024e9f21e7)


 

Asennusohjelmiston avauduttua määritin ensin kielen amerikan englanniksi, alueeksi valitsin euroopasta Suomen, näppäimistönä ajattelin kokeilla ihan vaan suomenkielistä asettelua sekä valitsin tyhjentää koko levyn ja tehdä täysin uudenasennuksen virtuaalikoneelle.
Sitten vielä piti nimetä kone ja luoda pääkäyttäjän tunnus, sekä salasana. 

 ![image](https://github.com/user-attachments/assets/b52bce39-cd83-4bbc-96c0-18683695c2d4)


 

Seuraavaksi painoin Install, jolloin asennus käynnistyi. Lopuksi vielä avasin  terminal emulaattorin, josta hain päivitykset komennolla:

![image](https://github.com/user-attachments/assets/eca835c6-f573-4e6a-a1e4-f0d3b23bf254)


    $ sudo apt-get update 

asensin kaikki päivitykset  

![image](https://github.com/user-attachments/assets/cb715bff-fd8d-4ff1-a1f3-2a1ac073d991)


    $ sudo-apr-get –y dist-upgrade  

ja asensin palomuurin ja laitoin sen päälle:  

![image](https://github.com/user-attachments/assets/6d37b0ca-6323-427a-b484-6b1c6f4f5eb7)

![image](https://github.com/user-attachments/assets/b265a45e-cbc7-4123-8fff-e1acf918dfd9)


    $ sudo apt-get -y install ufw
    $ sudo ufw enable 

 

Loppuun vielä buuttaus ja sisäänkirjautumisen testaaminen. 

 

	 

 

## Lähteet 

### - Karvinen, Tero 2024: Oma Linux, harjoitus 2. Luettavissa:  https://terokarvinen.com/linux-palvelimet/#h1-oma-linux 

Luettu: 27.08.2024 

 

### - Karvinen, Tero, Raportin kirjoittaminen, 2024. Luettavissa:  https://terokarvinen.com/2006/raportin-kirjoittaminen-4/  

Luettu:27.08.2024 

 

### - Karvinen, Tero, Install Debian on Virtualbox, 2023. Luettavissa: https://terokarvinen.com/2021/install-debian-on-virtualbox/  

Luettu: 27.08.2024 

 

### - Gnu, What is free software,2024. Luettavissa:  https://www.gnu.org/philosophy/free-sw.html  

Luettu 27.08.2024 

 

### - Debian Live 12.6.0 amd64 Xfce, Debian LIve Xfce asennuspaketin lataus. Ladattavissa: https://www.debian.org/distrib/ 

Ladattu 21.08.2024 

 

### - Oracle, Virtual box download. Ladattavissa: https://download.virtualbox.org/virtualbox/6.1.50/VirtualBox-6.1.50-161033-Win.exe 

Ladattu: 21.08.2024 

 

	 

 

 

 

 

 

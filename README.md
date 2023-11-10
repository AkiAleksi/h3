# h3
Tehtävien teko alkaa 8.11.2023 klo 9:48

# x

Velu 2022: Mastering Kali Linux for Advanced Penetration Testing 4ed: Chapter 10 - Exploitation: kappaleet "The Metasploit Framework", "The exploitation of targets using Metasploit" ja "Using public exploits". Eli ei enää kappaletta "Developing a Windows exploit" ja siitä eteenpäin.

Tiivistelmä:

 -Metasploit Framework (MSF) on avoimen lähdekoodin työkalu. Se on
 suunniteltu helpottamaan tunkeutumistestauksen suorittamista.

 -MSF on kirjoitettu Ruby-ohjelmointikielellä. 

 -Käyttää modulaarista lähestymistapaa helpottamaan 
 hyökkäyksiä hyödyntämisvaiheessa kyberhyökkäysten ketjumenetelmässä.
 
 -Frameworkki voidaan jakaa kolmeen pääosaan: Libraries, Interfaces ja Modules.

 -MSF (Metasploit Framework) on yhtä tehokas sekä käyttöjärjestelmän haavoittuvuuksia että kolmannen osapuolen sovelluksia vastaan. 

 -jokaisella hyökkääjällä on aina silmänsä auki etsiessään julkisia hyödyntämismenetelmiä 
  ja muokkaamassa niitä tarpeidensa mukaisesti. 

  
  
# a.)

Minulla oli jo valmiiksi Kali Linux asennettuna virtuaalikoneeseen.

<img width="831" alt="Screenshot 2023-11-07 at 12 35 24" src="https://github.com/AkiAleksi/h3/assets/112399816/750a597a-cc04-405c-bd5a-98f2924e00b8">

# b.)

Asensin metasploitable 2 virtuaalikoneeseen.
Seurasin näitä ohjeita: https://www.geeksforgeeks.org/how-to-install-metasploitable-2-in-virtualbox/

<img width="785" alt="Screenshot 2023-11-07 at 12 57 11" src="https://github.com/AkiAleksi/h3/assets/112399816/bbd7ab80-b2d8-494b-b052-0d9b4bb34ae6">

Tehtävien teko sessio päättyi 8.11.2023 klo 10:30. Tehtävien teko jatkuu 9.11.2023 klo 9:30.

# c.)

Laitoin kalin asetuksista network adapterit sopiviksi.
Adapter 1 NAT ja adapter 2 host only network.

<img width="604" alt="adapter1" src="https://github.com/AkiAleksi/h3/assets/112399816/042d59c0-2250-4684-8e36-256e81f22942">

<img width="576" alt="adapter2" src="https://github.com/AkiAleksi/h3/assets/112399816/21b1ac4b-7ebf-4c98-82c5-b3e1c8dc8c10">

Laitoin metaportable 2 asetukset myös.
Tässä vain only host network adapter 1.

<img width="703" alt="Screenshot 2023-11-08 at 14 30 45" src="https://github.com/AkiAleksi/h3/assets/112399816/2b266ce7-ff3c-49dd-a8d8-7be5e42fdc55">

Ajoin ifconfig metaportable 2. inet addr: 192.168.56.3


<img width="357" alt="ip" src="https://github.com/AkiAleksi/h3/assets/112399816/ec302910-4e3a-4b1e-a7a1-829bc36d69f4">

Ajoin ping 192.168.56.3. Ping vastaa!

<img width="208" alt="Screenshot 2023-11-08 at 14 11 47" src="https://github.com/AkiAleksi/h3/assets/112399816/ee1d3a91-6a17-424b-ae5f-846f867d2142">


Ajoin komennon curl www.google.com. Internet yhteys katkeaa


<img width="254" alt="komento" src="https://github.com/AkiAleksi/h3/assets/112399816/d99bf245-f63f-4929-ae91-442c4020625b">

Ajoin komennon ping www.google.com. Internet yhteys katkeaa

<img width="226" alt="komento 2" src="https://github.com/AkiAleksi/h3/assets/112399816/8a6a7283-3cc8-45c8-922e-e5e167822d87">

Tehtävien teko sessio päättyi 9.11.2023 klo 10:15. 
Tehtävien teko jatkuu 10.11.2023 klo 11:00.

# d.)

Ensin ajoin msfbd init komennon, jotta tulee database.
Sen jälkeen ajoin komennon msfconsole.
Sitten ajoin db_nmap -sn <kohde>
Näkyy, että metasploitable on päällä.

<img width="491" alt="-sn" src="https://github.com/AkiAleksi/h3/assets/112399816/5a942437-e64f-464e-b9bb-65c8f597abce">


Katsoin selaimesta.

<img width="906" alt="metasploitable" src="https://github.com/AkiAleksi/h3/assets/112399816/b9171664-6c98-4e9a-8d49-61d5b96b0fa7">





# e.)

ajoin komennon db_nmap -A -p0- <kohde>.


<img width="680" alt="1" src="https://github.com/AkiAleksi/h3/assets/112399816/67fc95ec-fafb-427c-9389-c4712921652f">



<img width="655" alt="2" src="https://github.com/AkiAleksi/h3/assets/112399816/fd40d87f-350e-40c7-882b-2c1e3ad567d1">



<img width="663" alt="3" src="https://github.com/AkiAleksi/h3/assets/112399816/564427b6-213e-4e13-9893-aadb5f7fbadd">

Skannauksessa näkyy kaikki mahdolliset portit. Siinä näkyy myös palvelutiedot, käyttöjärjestelmätiedot ja versiotiedot.

# f.)

Avasin msfconsolin. Syötin search vsftpd. use 1, set RHOSTS <kohde>, exploit.

Toisen tietokoneen shell auki.



<img width="658" alt="Screenshot 2023-11-10 at 14 57 07" src="https://github.com/AkiAleksi/h3/assets/112399816/368d5e17-8411-4765-813d-77f1788dfad7">











Lopuksi ajoin id. Näkyy root.

<img width="281" alt="Screenshot 2023-11-10 at 15 03 15" src="https://github.com/AkiAleksi/h3/assets/112399816/a380efcc-d88d-402a-8592-a23e48a34701">


# g.)

Ohjeet: https://infosecwriteups.com/metasploit-upgrade-normal-shell-to-meterpreter-shell-2f09be895646

Päivitin session meterpreter sessioksi.



<img width="545" alt="Screenshot 2023-11-10 at 15 33 54" src="https://github.com/AkiAleksi/h3/assets/112399816/77604fb8-75c3-480f-b6b5-c59abf0faf9a">






<img width="665" alt="meterpreter" src="https://github.com/AkiAleksi/h3/assets/112399816/e63ec3a1-885a-4611-b7dd-16a8e35fa4dd">

# h.)

ExploitDB on tietokanta, joka sisältää tietoja tietoturva-aukoista, haavoittuvuuksista
ja niiden hyödyntämiskeinoista.
Löysin tämän hyökkäyksen sieltä.
https://www.exploit-db.com/exploits/51746

Python skripti, joka pyrkii aiheuttamaan palvelunestohyökkäyksen OpenPLC WebServerin kolmanteen versioon. Kyseessä on siis Denial of Service (DoS) hyökkäys.

<img width="969" alt="Screenshot 2023-11-10 at 15 59 41" src="https://github.com/AkiAleksi/h3/assets/112399816/21b4e8ad-8135-4484-b956-e60505d8b2b8">

<img width="1007" alt="Screenshot 2023-11-10 at 16 01 49" src="https://github.com/AkiAleksi/h3/assets/112399816/2efabbf4-c107-4050-8e38-be461c81dfae">

# i.)

Ensin ajoin komennon searchsploit -u. Päivitin siis.

Sen jälkeen nmappasin ip-osoitteen.

<img width="454" alt="xddd" src="https://github.com/AkiAleksi/h3/assets/112399816/cf7b0dbb-5d51-4498-b083-cacccdc5fecb">

searchsploit vsftpd 2.3.4

<img width="372" alt="exploit" src="https://github.com/AkiAleksi/h3/assets/112399816/f3cb23dc-4328-4b7a-aca7-64501601740d">

Tämä viittaa siihen, että vsftpd-version 2.3.4:ssä voi olla tietoturva-aukko, ja Python-skriptiä tunnuksella 49757.py voi käyttää hyväksi etäältä Unix-pohjaisessa järjestelmässä.

# j.)

Nikto on tietoturvatrakastusohjelma. Se on suunniteltu palvelinten ja verkkosivustojen
haavoittuvuuksien havaitsemiseen.

Aja komento nikto -h <kohde>

<img width="497" alt="Screenshot 2023-11-10 at 17 07 51" src="https://github.com/AkiAleksi/h3/assets/112399816/2460b499-6dd0-4434-8023-7cae45d76fd9">

Skannauksessa näkyy, että Apache mod_negotiation on käytössä MultiViews:lla, mikä mahdollistaa tiedostonimien helpon bruteforcen.
Bruteforce tarkoittaa menetelmää, jossa kokeillaan systemaattisesti ja peräkkäin kaikkia vaihtoehtoja kunnes oikea vastaus löytyy.

# k.)

Tehtävän anto oli hieman epäselvä. Päätin perehtyä tarkemmin meterpreteriin.
Käytin sitä aikaisemmassa tehtävässä, mutta en tarkemmin pohtinut mikä se on.

Meterpreter on Metasploit Frameworkin osa. Se tarjoaa tehokkaan, joustavan sekä modulaarisen tietokonehyökkäyksen työkalun.
Metasploit Framework on avoimen lähdekoodin työkalupaketti.
Se tarjoaa tietoturva-ammattilaisille ja tutkijoille keinoja testata tietokonejärjestelmien haavoittuvuuksia ja suorittaa erilaisia hyökkäyksiä.

Meterpreter on suunniteltu olemaan huomaamaton ja jättämään mahdollisimman vähän jälkiä järjestelmään.
Se tukee myös kryptattua liikennettä, mikä tekee sen vaikeaksi havaita perinteisillä verkon valvontatyökaluilla.

Meterpreter-sessio eroaa tavallisesta tietokoneen istunnosta monin tavoin. Meterpreter on Metasploit Frameworkin erityinen payload, joka tarjoaa kehittyneempiä työkaluja ja ominaisuuksia hyökkääjälle, kun hän on saanut pääsyn uhrin järjestelmään. 
Esimerkiksi perinteiset istunnot saattavat olla helposti havaittavissa ja seurattavissa. Meterpreter on taas suunniteltu olemaan huomaamaton.

<img width="665" alt="meterpreter" src="https://github.com/AkiAleksi/h3/assets/112399816/e63ec3a1-885a-4611-b7dd-16a8e35fa4dd">


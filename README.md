# h3
8.11.2023 klo 9:48
# a.)

Minulla oli jo valmiiksi Kali Linux asennettuna virtuaalikoneeseen.

<img width="831" alt="Screenshot 2023-11-07 at 12 35 24" src="https://github.com/AkiAleksi/h3/assets/112399816/750a597a-cc04-405c-bd5a-98f2924e00b8">

# b.)

Asensin metasploitable 2 virtuaalikoneeseen.
Ohjeet: https://www.geeksforgeeks.org/how-to-install-metasploitable-2-in-virtualbox/

<img width="785" alt="Screenshot 2023-11-07 at 12 57 11" src="https://github.com/AkiAleksi/h3/assets/112399816/bbd7ab80-b2d8-494b-b052-0d9b4bb34ae6">

8.11.2023 klo 10:30

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

d.)

Ensin ajoin msfbd init komennon, jotta tulee database.
Sen jälkeen ajoin komennon msfconsole.
Sitten ajoin db_nmap -sn <kohde>

<img width="491" alt="-sn" src="https://github.com/AkiAleksi/h3/assets/112399816/5a942437-e64f-464e-b9bb-65c8f597abce">

Näkyy, että metasploitable on päällä.


<img width="906" alt="metasploitable" src="https://github.com/AkiAleksi/h3/assets/112399816/b9171664-6c98-4e9a-8d49-61d5b96b0fa7">



Katsoin selaimesta.

e.)

ajoin komennon db_nmap -A -p0- <kohde>.


<img width="680" alt="1" src="https://github.com/AkiAleksi/h3/assets/112399816/67fc95ec-fafb-427c-9389-c4712921652f">



<img width="655" alt="2" src="https://github.com/AkiAleksi/h3/assets/112399816/fd40d87f-350e-40c7-882b-2c1e3ad567d1">



<img width="663" alt="3" src="https://github.com/AkiAleksi/h3/assets/112399816/564427b6-213e-4e13-9893-aadb5f7fbadd">

Skannauksessa näkyy kaikki mahdolliset portit. Siinä näkyy palvelutiedot, käyttöjärjestelmätiedot ja versiotiedot.

f.)

Avasin msfconsolin. Syötin search vsftpd. use 1, set RHOSTS <kohde>, exploit.
Lopuksi ajoin id.

<img width="658" alt="Screenshot 2023-11-10 at 14 57 07" src="https://github.com/AkiAleksi/h3/assets/112399816/368d5e17-8411-4765-813d-77f1788dfad7">



<img width="281" alt="Screenshot 2023-11-10 at 15 03 15" src="https://github.com/AkiAleksi/h3/assets/112399816/a380efcc-d88d-402a-8592-a23e48a34701">


g.)
Ohjeet: https://infosecwriteups.com/metasploit-upgrade-normal-shell-to-meterpreter-shell-2f09be895646

Päivitin session meterpreter sessioksi.



<img width="545" alt="Screenshot 2023-11-10 at 15 33 54" src="https://github.com/AkiAleksi/h3/assets/112399816/77604fb8-75c3-480f-b6b5-c59abf0faf9a">






<img width="665" alt="meterpreter" src="https://github.com/AkiAleksi/h3/assets/112399816/e63ec3a1-885a-4611-b7dd-16a8e35fa4dd">

h.)

ExploitDB on tietokanta, joka sisältää tietoja tietoturva-aukoista, haavoittuvuuksista
ja niiden hyödyntämiskeinoista.
Löysin tämän hyökkäyksen sieltä.
https://www.exploit-db.com/exploits/51746

Python skripti, joka pyrkii aiheuttamaan palvelunestohyökkäyksen OpenPLC WebServerin kolmanteen versioon. Kyseessä on siis Denial of Service (DoS) hyökkäys.

<img width="969" alt="Screenshot 2023-11-10 at 15 59 41" src="https://github.com/AkiAleksi/h3/assets/112399816/21b4e8ad-8135-4484-b956-e60505d8b2b8">

<img width="1007" alt="Screenshot 2023-11-10 at 16 01 49" src="https://github.com/AkiAleksi/h3/assets/112399816/2efabbf4-c107-4050-8e38-be461c81dfae">

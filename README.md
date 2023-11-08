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





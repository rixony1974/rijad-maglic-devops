## Računarske mreže

Računarske mreže su skup povezanih računara koji omogućavaju razmenu podataka i resursa. Postoje različiti tipovi mreža,
uključujući:

- **Lokalne mreže (LAN)**: Male mreže koje povezuju uređaje unutar iste geografske lokacije, poput kuće, kancelarije ili
škole.

- **Bežične mreže (Wi-Fi)**: Mreže koje koriste bežičnu komunikaciju za povezivanje uređaja na Internet.

- **Širokopojasne mreže (WAN)**: Mreže koje povezuju LAN-ove na većim geografskim udaljenostima, često preko javne
infrastrukture kao što je Internet.

- **Internet**: Globalna mreža koja povezuje mreže širom sveta i omogućava pristup različitim servisima i resursima.

## OSI Model

OSI (Open Systems Interconnection) model je referentni model koji opisuje kako računari komuniciraju putem mreže.
Sastoji se od sedam slojeva, svaki odgovoran za određene funkcije komunikacije.

1. **Fizički sloj (Physical Layer)**: Ovaj sloj definiše fizičku vezu između uređaja. Uključuje karakteristike poput
električnih i optičkih specifikacija za prenos podataka.

2. **Sloj veze (Data Link Layer)**: Ovaj sloj omogućava pouzdan prenos podataka između susednih uređaja. Deli se na dva
podnivoa - LLC (Logical Link Control) koji upravlja tokom podataka i MAC (Media Access Control) koji omogućava
identifikaciju uređaja u mreži putem MAC adresa.

3. **Mrežni sloj (Network Layer)**: Mrežni sloj upravlja rutiranjem podataka između različitih mreža. IP (Internet
Protocol) protokol je ključan na ovom sloju. IP adrese se koriste za identifikaciju uređaja i omogućavaju im da
komuniciraju preko internetske mreže.

4. **Transportni sloj (Transport Layer)**: Ovaj sloj obezbeđuje pouzdan prenos podataka između krajnjih tačaka.
Najpoznatiji protokoli na ovom sloju su TCP (Transmission Control Protocol) i UDP (User Datagram Protocol).

5. **Sloj sesije (Session Layer)**: Ovaj sloj omogućava uspostavljanje, održavanje i prekid veze između aplikacija na
različitim uređajima. Pomaže u sinhronizaciji komunikacije između aplikacija.

6. **Prezentacioni sloj (Presentation Layer)**: Prezentacioni sloj obrađuje kodiranje i dekodiranje podataka, obezbeđuje
kompresiju, enkripciju i dekripciju. Takođe, prevodi različite formate podataka kako bi bili kompatibilni između
različitih uređaja.

7. **Aplikativni sloj (Application Layer)**: Ovaj sloj je najbliži korisniku i omogućava pristup mrežnim uslugama kao
što su e-pošta, pretraživači, FTP (File Transfer Protocol), HTTP (Hypertext Transfer Protocol), itd.

## Protokoli

Protokoli su skup pravila koja omogućavaju komunikaciju između uređaja u mreži. Neki od važnih protokola uključuju:

- **IPv4 Adresiranje**: IPv4 (Internet Protocol version 4) je najrašireniji protokol za adresiranje i rutiranje paketa u
Internet mreži. Koristi 32-bitne adrese, što pruža oko 4,3 milijarde adresa.

- **Subnet Mask - Maska podmreže**: Maska podmreže se koristi zajedno s IP adresom kako bi se odredila mrežna adresa i
adresa hosta unutar mreže.

- **IPv6**: IPv6 (Internet Protocol version 6) je novija verzija IP protokola koja koristi 128-bitne adrese i omogućava
značajno veći broj adresa u poređenju s IPv4.

- **TCP (Transmission Control Protocol)**: TCP je pouzdan protokol na transportnom sloju koji obezbeđuje pouzdan prenos
podataka putem uspostavljanja veze, potvrde primitka (ACK) i ponovnog slanja u slučaju gubitka podataka.

- **UDP (User Datagram Protocol)**: UDP je protokol na transportnom sloju koji omogućava brži, ali manje pouzdan prenos
podataka u odnosu na TCP.

- **HTTP (Hypertext Transfer Protocol)**: HTTP je protokol aplikativnog sloja koji omogućava komunikaciju između
klijenata i web servera.

- **Cookies**: Cookies su male tekstualne datoteke koje se koriste za praćenje informacija o korisniku na web
stranicama.

- **HTTPS (Hypertext Transfer Protocol Secure)**: HTTPS je sigurna verzija HTTP protokola koja koristi SSL/TLS za
zaštitu privatnosti i integriteta podataka.

- **DNS (Domain Name System)**: DNS se koristi za prevod domenskih imena u IP adrese.

- **VPN (Virtual Private Network)**: VPN je sigurna veza koja omogućava korisnicima da pristupaju mreži preko javnog
Interneta kao da su povezani iznutra, obezbeđujući privatnost i sigurnost.
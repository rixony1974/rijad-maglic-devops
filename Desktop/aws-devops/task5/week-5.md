## Server

Server je računarski sistem ili softver koji pruža usluge drugim računarima, poznatim kao klijenti, u okviru računarske mreže. Serveri mogu obavljati različite funkcije, uključujući čuvanje i upravljanje podacima, obradu zahteva klijenata, deljenje resursa i omogućavanje komunikacije između klijenata. Postoje različiti tipovi servera, a najčešći su:

### Tipovi servera

- **Web server**: Web serveri pružaju web stranice i sadržaj putem HTTP protokola klijentima, najčešće pretraživačima. Oni obrađuju zahteve klijenata i isporučuju odgovarajuće HTML, CSS, JavaScript i druge resurse.

- **Aplikacijski server**: Aplikacijski serveri pružaju različite usluge i funkcionalnosti za obradu poslovnih logika i transakcija aplikacija. Oni često komuniciraju s bazom podataka i integriraju se s web serverima kako bi pružili dinamički sadržaj.

- **Data centar**: Data centar je fizički objekat ili prostorija gde se smeštaju serveri i povezana oprema kako bi se čuvali, upravljali i obezbedili podaci i aplikacije organizacije.

### Server Operativni Sistem

Server operativni sistem je specijalizovani operativni sistem koji se koristi za upravljanje serverima. Neke od popularnih server OS su Windows Server, Linux (npr. CentOS, Ubuntu Server) i macOS Server.

### Web Serveri

Web serveri su softverski programi dizajnirani da obrađuju i odgovaraju na HTTP zahteve. Oni omogućavaju pregledavanje web stranica putem pretraživača. Dva od popularnih web servera su:

1. **NGINX**: NGINX je visoko performantan i skalabilan web server koji se često koristi kao reverse proxy i load balancer. Može služiti statički sadržaj brzo i efikasno, a takođe je sposoban da preusmerava zahteve ka drugim serverima, što ga čini idealnim za poboljšanje performansi web aplikacija.

#### Instalacija NGINX-a na CentOS 7

Da biste instalirali NGINX na CentOS 7, pratite ove korake:
- Otvorite terminal i izvršite sledeću komandu da biste ažurirali pakete sistema :sudo yum update

- Zatim instalirajte NGINX pomoću sledeće komande: sudo yum install nginx

- Nakon instalacije, pokrenite NGINX i omogućite ga da se pokrene pri svakom podizanju sistema

sudo systemctl start nginx
sudo systemctl enable nginx

- Proverite status NGINX servera da biste potvrdili da je uspešno pokrenut:

sudo systemctl status nginx

## NGINX Konfiguracijski fajlovi

Konfiguracija NGINX-a nalazi se u direktorijumu `/etc/nginx/`. Dva ključna konfiguracijska fajla su:

1. `/etc/nginx/nginx.conf`: Glavni konfiguracijski fajl koji definiše globalne postavke servera.

2. `/etc/nginx/conf.d/`: Direktorijum u kojem se čuvaju konfiguracijski fajlovi za pojedinačne veb lokacije (npr. mywebsite.conf).

## Apache

Apache HTTP Server (ili jednostavno Apache) je još jedan popularan web server koji je poznat po svojoj fleksibilnosti i širokoj podršci. Apache je sposoban da služi statički i dinamički sadržaj, uključujući PHP, i ima bogatu biblioteku modula koji omogućavaju dodatne funkcionalnosti.

## Apache Tomcat

Apache Tomcat je aplikacijski server specijalizovan za izvršavanje Java Servleta i JavaServer Pages (JSP) aplikacija. Omogućava Java aplikacijama da se izvršavaju na serveru i pruža okruženje za upravljanje zahtevima i bazama podataka.

## Reverse Proxy

Reverse proxy je posrednik koji prima zahteve klijenata i prosleđuje ih na druge servere. Oni se koriste za poboljšanje performansi, sigurnosti i skalabilnosti veb aplikacija. NGINX se često koristi kao reverse proxy server.

## Forward Proxy

Forward proxy je posrednik koji prima zahteve klijenata i prosleđuje ih na ciljane servere na internetu. On omogućava klijentima da sakriju svoj identitet od ciljanih servera i omogućava kontrolu pristupa internet sadržaju.

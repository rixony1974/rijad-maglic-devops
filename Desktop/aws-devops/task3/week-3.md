## Week-3: Bash / Shell Scripting

Shell je program koji omogućuje korisniku direktnu interakciju sa operativnim sustavom. Na početku je Unix OS koristio shell program pod nazivom Bourne shell. Danas se koristi Bash shell program koji je kompatibilan s Bourne shell-om. Bash shell je standardni shell program na većini Linux distribucija.

Postoje više različitih shell programa koji su razvijani za različite verzije UNIX-a. Ovo su neki od njih:
- `sh` - Bourne shell
- `csh` - C shell
- `ksh` - Korn shell
- `tcsh` - Tenex C shell / poboljšani C shell
- `zsh` - Z shell / ekstenzija za bash, ksh i tcsh
- `bash` - GNU Bourne again shell
- `fish` - Friendly interactive shell

Detaljnije o razlikama između različitih shellova možete pogledati na [ovom linku](link).

Kad god ukucamo neku komandu u Terminal shella, shell (`bin/bash`) je odgovoran da pravilno izvrši komandu. Aktivnosti koje shell izvršava su:
- parsiranje komande
- procjenjivanje meta karaktera kao što su zamjenski znakovi, specijalni znakovi, itd.
- obrada signala
- pokretanje programa za izvršenje komande

Da biste provjerili koji shell koristite, možete ukucati komandu `echo $SHELL`. Ova komanda će vam vratiti putanju do shell programa koji se trenutno koristi.

$ echo $SHELL
/bin/bash


Prethodna komanda nam govori da koristimo `/bin/bash`, odnosno Bash shell. Sljedećom komandom možemo provjeriti verziju Bash shell-a.


### Bash shell konfiguracijski fajlovi

Shell konfiguracijski fajl je tekstualni fajl koji se koristi za konfiguriranje okoline shell-a. Konfiguracijski fajlovi se koriste za postavljanje okoline, definiranje shell varijabli, kreiranje aliasa, postavljanje putanja (`PATH`) i drugih varijabli, kao i za dodavanje funkcionalnosti shell-u koristeći skripte i druge dodatke. Kada se shell pokrene, prvo se čita konfiguracijski fajl kako bi se postavilo okruženje, prije nego što se shell prikaže na ekranu i korisnik može početi unositi komande. Konfiguracijski fajl se izvršava za svaki novi shell koji se pokrene, bilo da se shell pokrene na početku sesije, ili putem skripte ili terminala. Ovi fajlovi se nalaze u korisničkom direktoriju (home folder-u) i mogu biti uređeni koristeći bilo koji tekst editor.

$ pwd
/home/centos

$ ls -la .*

-rw-------. 1 centos centos 6744 Feb 28 22:19 .bash_history
-rw-r--r--. 1 centos centos   18 Nov 24  2021 .bash_logout
-rw-r--r--. 1 centos centos  193 Nov 24  2021 .bash_profile
-rw-r--r--. 1 centos centos  259 Feb 28 19:07 .bashrc

`.bashrc` - Ovaj fajl se izvršava svaki put kada se pokrene Bash shell. Ovaj fajl se nalazi u korisnikovom home direktoriju. Ovaj fajl se koristi za postavljanje promenljivih okruženja, aliasa, funkcija itd.

`.bash_profile` - Ovaj fajl se izvršava samo kada se pokrene Bash shell u interaktivnom modu. Ovaj fajl se nalazi u korisnikovom home direktoriju. Ovaj fajl se koristi za postavljanje promenljivih okruženja, aliasa, funkcija itd.

`.bash_history` - Ovaj fajl se nalazi u korisnikovom home direktoriju. Ovaj fajl sadrzi istoriju komandi koje je korisnik izvršio u Bash shell-u.

`.bash_logout` - Ovaj fajl se izvršava kada se korisnik izloguje iz Bash shell-a. Ovaj fajl se nalazi u korisnikovom home direktoriju.

`.profile` - Ako postoji, ovaj konfiguracijski fajl interno poziva `.bashrc`.

Različiti shellovi imaju različite nazive i putanje do konfiguracijskih fajlova. Ovo su neki od njih:
- `sh` - `.profile`
- `csh` - `.cshrc`
- `ksh` - `.kshrc`
- `tcsh` - `.tcshrc`
- `zsh` - `.zshrc`
- `bash` - `.bashrc`
- `fish` - `.config/fish/config.fish`

## Skriptu možemo izvršiti na nekoliko načina:

1. `$ bash hello.sh`: Na ovaj način izvršavamo skriptu koristeći Bash shell program tako što smo proslijedili naziv skripte kao argument komandi bash.

2. `$ ./hello.sh`: Na ovaj način izvršavamo skriptu koristeći Bash shell program tako što smo proslijedili naziv skripte kao argument komandi `./`. Ova komanda će pokrenuti skriptu ako je fajl izvršiv. Ako fajl nije izvršiv, dobit ćemo grešku "Permission denied". Da bi fajl bio izvršiv, potrebno je da mu dodamo prava za izvršavanje. To možemo uraditi sa komandom `chmod +x hello.sh`. Nakon toga možemo izvršiti skriptu sa komandom `./hello.sh`.

- `./`: U UNIX sistemima, `./` predstavlja relativnu putanju do trenutnog direktorija u kojem se nalazimo u shell-u. `.` predstavlja trenutni direktorij, a `/` predstavlja putanju. Kada se koristi `./` zajedno sa nazivom izvršnog fajla (npr. `./hello.sh`), to znači da se taj fajl pokreće iz trenutnog direktorija. Ovo je korisno kada se nalazimo u direktoriju u kojem se nalazi izvršni fajl, jer nam omogućava da pokrenemo fajl bez potrebe za kucanjem pune putanje do fajla.

## Kompajler vs Interpreter:

- Kompajler: Kompajler je program koji prevodi izvorni kod u izvršni fajl. Programski jezici koji koriste kompajler (C, C++, Java...) za izradu izvršnog fajla.

- Interpreter: Interpreter je program koji u toku izvršavanja prevodi jednu po jednu naredbu. Shell je zasnovan na interpreteru, svaka linija programa odnosno skripte se izvršava jedna po jedna sekvencijalno. Čak i ako druga linija skripte ima grešku, shell interpreter će izvršiti prvu liniju.

## Environment Variables:

Environment variables su varijable (promjenjive vrijednosti) koje su definisane u operativnom sistemu i dostupne su svim procesima koji se pokreću u tom okruženju. One sadrže informacije koje se koriste za postavljanje okruženja za procese koji se pokreću u operativnom sistemu, kao što su putanje do direktorija, sistemski parametri, konfiguracijske postavke i druge informacije koje su potrebne da bi se programi izvršavali ispravno.

Environment variables su u osnovi nazivi koji su povezani sa određenim vrijednostima. Na primjer, `PATH` je environment variable koja sadrži putanje do direktorija u kojima se nalaze izvršni fajlovi, a `HOME` je environment variable koja sadrži putanju do korisničkog direktorija (home folder-a).

Environment variables se mogu definisati i mijenjati na različite načine, ovisno o operativnom sistemu. U Unix sistemima se najčešće koristi `export` komanda kako bi se kreirale ili modificirale environment variables.

Programi koji se izvršavaju u UNIX okruženju mogu koristiti environment variables da bi pristupili informacijama o okruženju u kojem se pokreću. Na primjer, programi koji se koriste u skriptama mogu koristiti environment variables kako bi pristupili informacijama o putanjama do direktorija ili drugim informacijama koje su neophodne da bi se programi izvršili ispravno.

## PATH Environment Variable:

`PATH` je jedna od najvažnijih environment varijabli na UNIX sistemima. Ona definiše putanje direktorija u kojima se operativni sistem traži izvršne (executable) fajlove kad izvršavate komande u shell-u.

Kada korisnik unese neku komandu u shell, operativni sistem traži tu komandu u nizu direktorija definisanim u `PATH` varijabli, počevši od prvog direktorija u nizu, sve dok ne pronađe traženi fajl. Ako se fajl ne pronađe u nijednom direktoriju u PATH-u, operativni sistem će prijaviti grešku i prikazati poruku o grešci.

Standardne putanje koje su definisane unutar `PATH` varijable obično uključuju direktorije poput `/usr/bin`, `/bin` i `/usr/local/bin`. Kada korisnik unese neku komandu, npr. `ls`, OS će pretražiti direktorije navedene u `PATH` putanji unutar kojih će tražiti izvršni (executable) fajl komande `ls`. Ako se izvršni fajl za komandu `ls` nalazi u jednom od tih direktorija, komanda `ls` će biti uspješno izvršena.

## $ which ls
`which` je komanda koja nam pokazuje putanju do izvršnog fajla `ls`.

## Alias za ls

alias ls='ls --color=auto'

/usr/bin/ls - Putanja na kojoj se nalazi ls izvršni fajl.

## Putanje u PATH-u na UNIX sistemima su odvojene dvotačkom `:`.

Korisnici mogu mijenjati `PATH` varijablu kako bi dodali nove direktorije u nju, omogućavajući im da pokrenu programe koji se nalaze u drugim direktorijima osim standardnih direktorija. To se može uraditi dodavanjem novih direktorija u `PATH` putem komandne linije odnosno terminala ili putem konfiguracijskih fajlova za shell, kao što je `.bashrc`.

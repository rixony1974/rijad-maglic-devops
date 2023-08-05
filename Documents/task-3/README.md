# Shell i Bash - Ključne tačke

Shell je program koji omogućuje korisniku direktnu interakciju sa operativnim sistemom. Bash (Bourne Again Shell) je danas najčešće korišteni shell program na Linux distribucijama. Postoje i drugi shell programi, kao što su sh, csh, ksh, tcsh, zsh, fish itd., ali su mnogi od njih kompatibilni sa Bash-om.

## Izvršavanje bash shell skripti
U direktoriju "Week-3" nalazi se skup bash shell skripti koje se mogu izvršiti na nekoliko načina: putem bash naredbe (`$ bash ime_skripte.sh`) ili koristeći relativnu putanju (`$ ./ime_skripte.sh`), ali prije toga potrebno je osigurati da skripta ima dozvolu za izvršavanje (`$ chmod +x ime_skripte.sh`). Skripte se izvršavaju liniju po liniju, a ukoliko dođe do greške u jednoj liniji, preostale linije će i dalje biti izvršene.

## Konfiguracijski fajlovi
U ovom direktoriju se također nalaze i konfiguracijski fajlovi (`.bashrc`, `.bash_profile`, `.bash_logout`, `.profile` itd.) koji pomažu postavljanje okoline shell-a, definisanje promenljivih, kreiranje aliasa, postavljanje putanja i drugih varijabli, kao i dodavanje funkcionalnosti shell-u kroz skripte i dodatke. Shell će prvo čitati konfiguracijski fajl za postavljanje okoline pre nego što prikaže prompt na ekranu, omogućavajući korisniku da unese komande.

## Environment varijabla PATH
Jedna od najvažnijih environment varijabli na UNIX sistemima je PATH. Ona definiše putanje direktorija u kojima operativni sistem traži izvršne fajlove kad se unese komanda u shell. Standardne putanje u PATH varijabli obično uključuju direktorije kao što su /usr/bin, /bin i /usr/local/bin. Korisnici mogu dodavati nove direktorije u PATH kako bi omogućili izvršavanje programa koji se nalaze van standardnih direktorija.

## Bash shell skripte
Skripte u ovom direktoriju demonstriraju različite funkcionalnosti bash shell-a, kao što su rad sa promenljivim varijablama, petljama, uslovima i funkcijama. Kroz razumevanje bash shell-a i konfiguracijskih fajlova, korisnici mogu prilagoditi svoje okruženje i olakšati svoj rad na UNIX sistemima.

## Week-2: Linux / UNIX Operativni sistemi

### UNIX: Stabilan, Moćan i Fleksibilan Operativni Sistem

UNIX je impresivan operativni sistem visokih performansi, poznat po svojoj stabilnosti i fleksibilnosti, što ga čini idealnim za izvršavanje kritičnih aplikacija od iznimne važnosti. Snažno je povezan s mrežnim servisima temeljenim na TCP/IP protokolu, što je dramatično promijenilo percepciju UNIX servera i radnih okruženja u posljednjim godinama.

### Evolucija UNIX Servera:

U prošlosti, UNIX serveri su se često koristili s klasičnim serijskim terminalima. Međutim, danas se UNIX serveri nalaze u mreži, ostvarujući vezu putem LAN/WAN mreže i TCP/IP skupa protokola s radnim stanicama. Ova moderna arhitektura pruža bolju povezanost i skalabilnost, čineći UNIX sustave idealnim za današnje zahtjeve.

### Popularnost i Rasprostranjenost:

UNIX ima širok spektar varijanti razvijenih od strane renomiranih svjetskih proizvođača računara. Ova raznolikost potvrđuje kvalitetu, popularnost i raširenost UNIX-a kao operativnog sustava. Međutim, većina tih varijanti je komercijalna, što znači da korisnik mora platiti licencu za njihovo korištenje, a izvorni kod često nije dostupan.

### Uzlet Linux Sustava:

S obzirom na komercijalne ograničenja UNIX-a i potrebu za slobodnim i otvorenim izvornim kodom, Linux je postao izvanredna alternativa. Linux zadržava većinu odlika UNIX-a, ali uz dodatak otvorenog izvornog koda i gotovo besplatnog korištenja. Ova kombinacija je potakla nagli porast popularnosti Linuxa.

### Linux je Postao Prva Odabir:

Danas većina proizvođača računara, osim sopstvenih komercijalnih UNIX varijanti, također nudi podršku za Linux. Ovaj operativni sustav često se koristi na radnim stanicama i serverima, posebno u manjim i srednje veličinama servera. Jedno od područja u kojem Linux dominira je u Internet servisima, gdje veliki broj korisnika podržava i promovira Linux kao temeljni server.

### Svijet koji podržava Linux:

Otvoreni izvorni kod i besplatno korištenje čine Linux ne samo ekonomičnim izborom već i snažnom zajednicom korisnika i razvojnih programera. Zahvaljujući ovom entuzijazmu i podršci, Linux je postao široko korišten i priznat operativni sistem u raznim industrijama i aplikacijama.
## Osnovne Linux/UNIX komande

- `$ man ssh`: Manual for `ssh` command.
- `$ ssh [ip or hostname]`: Secure shell, an encrypted network protocol allowing for remote login and command execution.
- `$ ssh -vvv`: Verbose for troubleshooting access.

- `$ pwd`: Displays the current directory.
- `$ ls`: List files and directories in the current directory.
- `$ ls -l`: List files and directories in long format (detailed information).
- `$ cd /`: Change directory to the root of the filesystem.
- `$ cd target`: Change directory to the "target" directory.
- `$ cd ~`: Change directory to your user home directory.
- `$ cd ..`: Move up one directory level.
- `$ mkdir directory`: Create a new directory with the specified name.
- `$ rmdir directory`: Remove an empty directory.

- `$ cp file1 file2`: Copy `file1` to `file2`.
- `$ cp -r dir1 dir2`: Copy directory `dir1` to `dir2`.
- `$ mv file1 file2`: Move `file1` to `file2` (file1 is deleted).
- `$ rm file1`: Remove `file1`.
- `$ rm -r dir1`: Remove directory `dir1` and all its contents.

- `$ cat file`: Display the content of `file`.
- `$ less file`: View the content of `file` one page at a time.
- `$ head file`: Display the first few lines of `file`.
- `$ tail file`: Display the last few lines of `file`.
- `$ grep pattern file`: Search for `pattern` in `file`.
- `$ wc file`: Count the number of lines, words, and characters in `file`.
- `$ chmod permissions file`: Change permissions of `file` (e.g., `chmod 755 file`).

- `$ ps`: Display a snapshot of the current processes.
- `$ top`: Display a dynamic view of system processes.
- `$ kill process_id`: Terminate a process with the specified ID.

- `$ history`: Display the command history of the current session.
- `$ clear`: Clear the terminal screen.

- `$ sudo command`: Execute `command` with administrative privileges.

- `$ df`: Display disk space usage of file systems.
- `$ du`: Estimate file space usage.

- `$ date`: Display the current date and time.

- `$ ping host`: Send ICMP echo requests to a `host`.

- `$ ifconfig`: Display network interface configuration.

- `$ uname -a`: Display system information.

- `$ tar options file/directory`: Archive or extract files/directories using tar.

- `$ find directory -name filename`: Search for `filename` in the specified `directory`.

- `$ wget url`: Download files from the internet using URL.

- `$ nano filename`: Open `filename` in the Nano text editor.

- `$ exit`: Exit the current shell session.

## `sudo` (SuperUser Do)

`sudo` je naredba u Linux i UNIX operativnim sistemima koja omogućuje korisnicima da izvrše druge naredbe s privilegijama superkorisnika (root korisnika) ili s privilegijama drugih specifičnih korisnika.

Kada se korisnik prijavi na Linux sistem, obično ima ograničene ovlasti koje su mu dodijeljene. Ova ograničenja sprečavaju korisnika da izvrši potencijalno opasne ili destruktivne operacije koje bi mogle utjecati na cjelokupni sistem. Međutim, postoje situacije u kojima korisnik treba izvršiti naredbu s višim privilegijama, kao što je instaliranje programa, upravljanje servisima ili mijenjanje postavki sistema.

Upravo za to služi `sudo`. Kada korisnik koristi `sudo` prije naredbe, sistem će provjeriti postavke kako bi utvrdio je li taj korisnik ovlašten za izvršavanje te naredbe kao superkorisnik. Ako je korisnik ovlašten, naredba će se izvršiti s višim privilegijama; inače, dobit će se poruka o grešci.

## Simboličke i Tvrde Poveznice (Links) u UNIX Sistemima

U UNIX sistemima, postoje dva tipa poveznica (links) koje se koriste za stvaranje referenci na datoteke i direktorije - simboličke (symbolic links) i tvrde (hard links).

Simbolička poveznica, također poznata i kao soft link, je datoteka koja predstavlja simboličku referencu na neku drugu datoteku ili direktorij. Simbolička poveznica sadrži putanju do izvorne datoteke ili direktorija, a kada se na nju pristupa, sistem će slijediti putanju koju simbolička poveznica pokazuje i doći do izvorne datoteke. Simboličke poveznice se stvaraju uz pomoć naredbe `ln -s`, a brisanje simboličke poveznice neće utjecati na izvornu datoteku ili direktorij.

S druge strane, tvrda poveznica, također poznata i kao hard link, je druga kopija iste datoteke ili direktorija. Tvrde poveznice se stvaraju uz pomoć naredbe `ln`, a nakon stvaranja tvrde poveznice, izvorna datoteka i njena tvrda poveznica se tretiraju kao jedna te ista datoteka. To znači da ako se promijeni sadržaj izvorne datoteke, promjena će se vidjeti i u tvrdoj poveznici, jer su to ista datoteka. Brisanje izvorne datoteke neće utjecati na tvrdu poveznicu, jer tvrda poveznica nije samo referenca na izvornu datoteku, već je to druga kopija te datoteke.

Ključna razlika između simboličkih i tvrdih poveznica u UNIX sistemima je u tome što simboličke poveznice predstavljaju samo referencu na izvornu datoteku ili direktorij, dok su tvrde poveznice kopije izvorne datoteke ili direktorija.

Primjeri kreiranja poveznica:

- `ln -s /putanja/do/datoteke /putanja/do/simbolicke-poveznice`: Kreiranje simboličke poveznice na datoteku.
- `ln /datoteka1 /datoteka2`: Kreiranje tvrde poveznice na datoteku1.



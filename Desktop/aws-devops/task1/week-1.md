## Week 1: Git - Sistem za verzionisanje koda

### Git - Osnovni pojmovi

- **Git**: Git je alat koji je razvio Linus Torvalds kako bi olakšao vođenje jednog velikog i kompleksnog projekta - Linux kernela. Git je de-facto postao standardni alat za verzionisanje koda.

- **Init**: Inicijalizacija Git repozitorijuma. Inicijalizacija se obavlja komandom `git init` u direktorijumu u kojem se nalazi projekat.

- **Repozitorijum**: Git repozitorijum je mesto gde se nalaze sve verzije projekta.

- **Remote**: Remote je udaljeni/remote repozitorijum (npr. onaj koji ste kreirali na git serveru, GitHub-u, itd.).

- **Local**: Local je lokalni repozitorijum (inicijaliziran na vašem lokalnom računaru).

- **Add**: Add je proces dodavanja fajlova u staging area. Fajlovi se dodaju komandom `git add` ili `git add .` (dodaje sve fajlove u trenutnom direktorijumu).

- **Staging Area**: Staging area je mesto gde se nalaze fajlovi koji će biti dodati u commit.

- **Commit**: Commit je verzija projekta. Commit se sastoji od snapshot-a projekta i metapodataka koji opisuju commit.

- **Push**: Push je proces slanja izmjena koda iz lokalnog repozitorijuma na udaljeni/remote repozitorijum (npr. na GitHub).

- **Branch**: Branch je nezavisna linija/grana razvoja projekta. Branch se koristi da bi se razvijale nove funkcionalnosti neovisno od glavne `main` grane. Branch/grana se može spojiti sa drugom granom/branch-om.

- **Pull**: Pull je proces preuzimanja izmjena koda iz udaljenog/remote repozitorijuma na lokalni repozitorijum (onaj na vašem računaru).

- **Merge**: Merge je proces spajanja dvije grane/branch-a u jednu granu/branch.

- **Pull Request**: Pull request je zahtjev za spajanje izmjena iz jedne grane/branch-a u drugu granu/branch.

- **Fork**: Fork je kopija projekta. Fork se koristi da bi se napravila kopija postojećeg projekta i nastavio rad na njemu bez uticaja na originalni projekat. Fork se može spojiti sa originalnim projektom koristeći Pull Request.

### Osnovne Git Naredbe

Ovdje su neke od osnovnih Git naredbi koje su često korištene u toku razvoja softverskih projekata:

- `git init`: Inicijalizacija novog Git repozitorijuma u trenutnom direktorijumu.

- `git add <file>`: Dodavanje određenog fajla u staging area.

- `git add .`: Dodavanje svih fajlova iz trenutnog direktorijuma u staging area.

- `git commit -m "Poruka komitovanja"`: Kreiranje commit-a sa porukom koja opisuje promjene koje su napravljene.

- `git status`: Prikazuje status trenutnih promjena u repozitorijumu.

- `git log`: Prikazuje istoriju commit-ova.

- `git push`: Slanje commit-ova na udaljeni repozitorijum (npr. GitHub).

- `git pull`: Preuzimanje izmjena sa udaljenog/remote repozitorijuma i spajanje sa lokalnim repozitorijumom.

- `git branch`: Prikazuje sve grane u repozitorijumu.

- `git checkout <branch>`: Prebacivanje na određenu granu.

- `git merge <branch>`: Spajanje određene grane sa trenutnom granom.

- `git clone <url>`: Kloniranje postojećeg repozitorijuma na lokalni računar.


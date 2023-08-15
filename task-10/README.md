# Kreiranje infrastrukture na AWS

## Postavljanje Tagova za Resurse:

Prvi korak koji sam preduzeo bio je postavljanje odgovarajućih tagova na sve AWS resurse koje sam kreirao. Ovo je omogućilo bolje praćenje resursa i njihovog vlasnika.

- Tag Ime: Rijad Maglić
- Tag E-mail: rijad.maglic@unvi.edu.ba 

## Kreiranje AMI Image-a:

Da bih kreirao AMI image, koristio sam AWS Management Console. Prvo sam kreirao AMI image od postojeće EC2 instance "ec2-moje-ime-prezime-web-server". Nazvao sam AMI image "ami-moje-ime-prezime-web-server".

## Kreiranje Application Load Balancera (ALB):

Da bih omogućio ravnomjernu raspodjelu opterećenja, kreirao sam Application Load Balancer koji je bio povezan sa Target Group "tg-web-servers". Nazvao sam ALB "alb-web-servers". Prilagodio sam listenere i target grupu prema potrebama naše aplikacije.

## Kreiranje Auto Scaling Grupe (ASG):

Kako bih osigurao automatsku skalabilnost, kreirao sam Auto Scaling grupu s minimalno 2 i maksimalno 4 instance. Kao tip instance, odabrao sam "t3.micro". ASG sam povezao sa ALB-om "alb-web-servers". Postavio sam skaliranje prema gore kada CPU pređe 18%, i skaliranje prema dolje kada CPU padne ispod 18%.

## Konfiguracija Security Grupa:

Nakon postavljanja svih resursa, pažljivo sam konfigurisao security grupe kako bih omogućio otvorene portove potrebne za ispravno funkcioniranje aplikacije.

## Kreiranje Dijagrama Infrastrukture:

Vizualizacija je ključna, pa sam koristio draw.io alat kako bih napravio dijagram infrastrukture. Ovo je pomoglo da jasno vidim kako su svi resursi povezani.

## Simuliranje Visoke Dostupnosti:

Kako bih testirao visoku dostupnost, namjerno sam zaustavljao neke instance unutar Auto Scaling grupe. Zahvaljujući tome, ASG je automatski kreirao nove instance kako bi održao minimalnu količinu instanci.

## Simuliranje CPU Load-a:

Pratio sam online tutorijale kako bih simulirao CPU load na nekoliko instanci. Ovo je bilo korisno za testiranje skalabilnosti ASG-a.

## Priprema Pull Request-a:

Nakon što sam završio sve korake, kreirao sam Pull Request na našem repozitoriju. U komentaru sam priložio link ka dijagramu infrastrukture i detaljan opis svih resursa koje sam kreirao.

## Postavljanje DNS Zapisa:

Dodao sam minimalni DNS zapis za Load Balancer kako bi drugi mogli pristupiti našoj aplikaciji.

## Terminacija Resursa:

Nakon što je Pull Request odobren, bilo je važno terminirati sve AWS resurse kako ne bi trošili nepotrebne resurse i novac.

# Nedelja 7: Uvod u Amazon Web Services (AWS) - Elastic Compute Cloud (EC2) i Identity Access Management (IAM)

U ovoj sedmici, dublje ćemo istražiti dva ključna servisa u okviru Amazon Web Services (AWS) ekosistema: Elastic Compute Cloud (EC2) i Identity Access Management (IAM). Ovi servisi omogućavaju fleksibilno i sigurno upravljanje resursima i pristupom unutar vašeg AWS računa. Upoznajte se sa sveobuhvatnim detaljima i tehničkim aspektima koji definišu ove servise.

## Elastic Compute Cloud (EC2) - Osnove

Elastic Compute Cloud (EC2), čvrsto utemeljen u kategoriji Infrastructure as a Service (IaaS) servisa, predstavlja jedan od najvažnijih stubova AWS oblaka. EC2 pruža revolucionarnu sposobnost stvaranja i upravljanja virtuelnim računarskim resursima, uključujući procesorsku moć, radnu memoriju, grafičke jedinice i mrežnu povezanost. EC2 instance su efikasno virtuelne mašine u oblaku, koje se izdvajaju kao središnji element prilagodljive infrastrukture.

Amazon Machine Image (AMI) predstavlja ključnu komponentu koja omogućava brzo i efikasno kreiranje EC2 instanci. AMI je svojevrsna konfiguracija ili šablon koji sadrži informacije o operativnom sistemu, arhitekturi (32/64-bit), prethodno instaliranim aplikacijama i postavkama. AMI-ji se mogu klasifikovati kao javni, privatni ili deljeni, pružajući raznovrsne opcije za personalizaciju instanci.

Tipovi instanci (Instance Types) predstavljaju različite nivoe resursa koje možete dodeliti EC2 instancama. AWS nudi obilje različitih tipova instanci, svrstanih u porodice i kategorije, sa preciznim oznakama kao što su t2.micro, m5.large i c5.2xlarge. Ovi tipovi omogućavaju fino podešavanje performansi i resursa u skladu sa zahtevima vaših aplikacija.

## Identity Access Management (IAM) - Osnove

Identity Access Management (IAM) predstavlja stub sigurnosti i pristupa unutar AWS okruženja. IAM omogućava autentifikaciju i autorizaciju za sve akcije koje se izvršavaju u okviru vašeg AWS računa. Bez obzira da li koristite AWS konzolu, Software Development Kit (SDK) ili AWS Command Line Interface (CLI), IAM je ključan za verifikaciju identiteta i dozvola za željene operacije.

IAM koristi dvostruki pristup kako bi kontrolisao pristup i ovlašćenja:

- Autentifikacija: Identifikuje ko pristupa računu putem korisničkog imena i lozinke ili pristupnih ključeva.
- Autorizacija: Definiše koje akcije su dozvoljene za svakog korisnika ili entitet kroz korisničke grupe, uloge i politike.

Svaki korisnik ili entitet unutar IAM okruženja ima svoj jedinstveni Amazon Resource Name (ARN), omogućavajući precizno upravljanje pristupom i privilegijama. IAM politike definišu tačno šta korisnici mogu da rade, pružajući granularnu kontrolu nad resursima i servisima.

Uz to, IAM se integriše sa AWS Security Token Service (STS), omogućavajući vanjskim entitetima da sigurno pristupe AWS resursima unutar vašeg računa.

## Zaključak

U ovoj sedmici smo istražili osnove Amazon Elastic Compute Cloud (EC2) i Identity Access Management (IAM) servisa. EC2 nam omogućava stvaranje i upravljanje virtuelnim računarskim resursima sa visokom prilagodljivošću, dok IAM osigurava preciznu kontrolu nad autentifikacijom i autorizacijom za pristup AWS resursima. Razumevanje ovih ključnih servisa je osnovna tačka za gradnju sigurnih, skalabilnih i pouzdanih aplikacija u oblaku.

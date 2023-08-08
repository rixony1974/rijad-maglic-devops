# Korak 1: Kreiranje EC2 instance

Prvo, treba da se prijavite na vaš AWS (Amazon Web Services) nalog i otvorite AWS Management Console.

# Korak 2: Odabir AMI (Amazon Machine Image)

Kliknite na "Services" u gornjem meniju, zatim odaberite "EC2" iz sekcije "Compute". U "EC2 Dashboard", kliknite na "Launch Instances" da biste započeli proces kreiranja nove instanci.

# Korak 3: Konfiguracija instanci

Odaberite "Amazon Linux 2023" kao željeni AMI.
U odjeljku "Instance Type", selektujte "t2.micro" kao tip instance.
U polju "Number of instances", ostavite broj na 1.

# Korak 4: Konfiguracija Instance Details

Prelazite na korak "Configure Instance Details":

- Ostavite "Number of instances" na 1.
- U polju "Network", ostavite "Amazon Virtual Private Cloud (VPC)" na zadanoj vrijednosti.
- U pododjeljku "Subnet", također ostavite zadano.

# Korak 5: Add Storage (Dodavanje skladišta)

Preskočite ovaj korak jer želimo koristiti zadane postavke skladišta.

# Korak 6: Add Tags (Dodavanje oznaka)

Dodajte oznaku (tag) kako biste mogli lakše prepoznati vašu instancu:

- Key: Name
- Value: web-server-01

# Korak 7: Configure Security Group (Konfiguracija sigurnosne grupe)

Kliknite na "Add Rule" kako biste dodali pravilo sigurnosne grupe:

- Type: SSH
- Source: Anywhere (0.0.0.0/0)

Zatim, kliknite na "Review and Launch" da biste pregledali sve vaše postavke.

# Korak 8: Pregled i lansiranje instance

Pregledajte sve postavke i kliknite na "Launch" kako biste pokrenuli instancu.

# Korak 9: Kreiranje Key Paira

Kada odaberete "Launch", pojavit će se prozor koji vam traži da odaberete ili kreirate key pair. Odaberite "Create a new key pair" i unesite naziv "rijad-maglic-devops". Kliknite na "Download Key Pair" kako biste preuzeli key pair (datoteku sa .pem ekstenzijom) na vaš lokalni računar. Bitno je da ovu datoteku sačuvate na sigurnom mjestu jer će vam biti potrebna za SSH pristup instanci.

# Korak 10: Pristupanje instanci putem SSH

Otvorite terminal na vašem lokalnom računaru i premjestite se u direktorij gdje ste sačuvali preuzeti .pem fajl. Koristite komandu `chmod 400 rijad-maglic-devops.pem` da biste promijenili dozvole fajla kako bi bio siguran. Zatim koristite SSH komandu kako biste se povezali sa instancom:


ssh -i "rijad-maglic-devops.pem" ec2-user@<public_ip_instance>
Umjesto <public_ip_instance> unesite javnu IP adresu vaše EC2 instance.

# Korak 11: Provjera SSH veze

Ako ste ispravno slijedili korake, trebali biste biti uspješno povezani na vašu EC2 instancu putem SSH. Možete provjeriti da li ste uspješno povezani tako što ćete vidjeti prompt sa imenom vaše instance.

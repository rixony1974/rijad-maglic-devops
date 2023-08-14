# Sedmica 8: Amazon Elastic Load Balancer, Amazon EC2 Auto Scaling

## Elastic Load Balancer (ELB) i Amazon EC2 Auto Scaling

- ELB preusmjerava saobraćaj ka zdravim EC2 instancama u target grupama po portu i protokolu definisanim pri kreiranju target grupe.
- Health checks provjeravaju status svake instance.
- Ručno registrovanje novih instanci za odgovor na povećan broj zahtjeva.
- ELB preusmjerava saobraćaj na zdrave instance.
- Amazon EC2 Auto Scaling omogućava automatizovano dodavanje i terminiranje instanci.
- Auto Scaling grupa povezana sa Load Balancerom.

## Load Balancer u stvarnom životu

- Analogija Load Balancera sa portirom u banci.
- Portir reguliše saobraćaj klijenata ka različitim salterima.
- Salteri predstavljaju EC2 instance u različitim target grupama.
- Listener rules određuju kako se saobraćaj preusmjerava na target grupe.

## Health Check

- Periodični zahtjevi prema EC2 instancama za provjeru njihovog stanja.
- Neispravne instance označene kao unhealthy.
- Pravila za health check strategije.

## Tipovi Load Balancera

1. **Application Load Balancer (ALB)** za HTTP/HTTPS saobraćaj.
   - Listener komponenta za osluškivanje saobraćaja.
   - Listener Rule set za rutiranje ka target grupama.

2. **Network Load Balancer (NLB)** za TCP/UDP saobraćaj.
   - Transportni nivo OSI modela.
   - Milioni zahtjeva po sekundi, nisko kašnjenje.

3. **Gateway Load Balancer (GWLB)** za 3rd party appliances.
   - Mrežni nivo OSI modela.
   - GWLBE i GWLB endpoints za upravljanje saobraćajem.

## Amazon EC2 Auto Scaling

- Auto Scaling grupa (ASG) je kolekcija EC2 instanci.
- Parametri: minimum, desired, maximum broj instanci.
- Launch Template za kreiranje instanci.

## Auto Scaling Policies

- Target tracking scaling za automatsko skaliranje na osnovu metrika.
- Step scaling sa pragovima za povećanje/terminaciju instanci.
- Simple scaling sa fiksnom kritičnom vrijednošću.

## Load Balancer vs Auto Scaling

- Load Balancer omogućava visoku dostupnost i balansiranje saobraćaja.
- Auto Scaling grupe omogućavaju kreiranje/terminaciju instanci.
- ELB koristi health checks za zamjenu nezdravih instanci.

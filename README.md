# Master-rad

Preduslovi za pokretanje aplikacije jesu da korisnik na lokalnoj mašini ima instaliran:
- python 2.7
- django 1.11.4.

S obzirom da alati koji se koriste u aplikaciji nisu besplatno dostupni neakademskim korisnicima, iz
tog razloga sami alati nisu dostupni zajedno sa kodom aplikacije. Akademski korisnici mogu ove alate besplatno da preuzmu na adresi [http://www.cbs.dtu.dk/][1] i to:
- netMHC-4.0
- netMHCpan-3.0
- netCTLpan-1.1
- pickpocket-1.1
- netMHCcons-1.1

I konačno, neophodno je promeniti deo koda u views.py tako da odgovara fizičkim putanjama direktorijuma u kojima se nalaze pobrojani alati na korisnikovoj mašini. 

```sh
####################PUTANJE DO DIREKTORIJUMA ALATA########################
netmhc_path = '/Users/milicakojicic/Documents/ALATI_ZA_PREDIKCIJU/netMHC-4.0'
netmhcpan_path = '/Users/milicakojicic/Documents/ALATI_ZA_PREDIKCIJU/netMHCpan-3.0'
netctlpan_path = '/Users/milicakojicic/Documents/ALATI_ZA_PREDIKCIJU/netCTLpan-1.1'
pickpocket_path = '/Users/milicakojicic/Documents/ALATI_ZA_PREDIKCIJU/pickpocket-1.1'
netmhccons_path = '/Users/milicakojicic/Documents/ALATI_ZA_PREDIKCIJU/netMHCcons-1.1'
input_files_path = '/Users/milicakojicic/Desktop/master/main/static/main/input_files/'
output_files_path = '/Users/milicakojicic/Desktop/master/main/static/main/output_files/'
```

Aplikacija se pokreće ulaskom u dikrektorijum master u kom se nalazi skripta  **manage.py**  na sledeći način:
**python manage.py runserver**

# Master-rad

Ovaj rad osmišljen je sa namerom da se neki od najpopularnijih alata za predikciju T-ćelijskih epitopa u naučnoj zajednici objedine u jednoj aplikaciji. Omogućeno je njihovo samostalno pokretanje kroz veb interfejs, koje je tako implementirano da korisnicima pruža svu udobnost u radu sa ovim alatima. Korisniku je data sloboda da sam podešava parametre koji odgovaraju njegovom istraživanju i dat mu je detaljan opis za korišćenje i pokretanje alata, kao i objašnjenje izlaznih rezultata. Implementiran je i novi metaprediktor koji koristiti predikcije svih razmatranih alata i donosi konačnu odluku na osnovu različitih glasačkih šema (konsenzusa). Metaprediktor je zapravo pokušaj da se rezultati razmatranih alata integrišu, kao i da se obezbedi sigurnija i pouzdanija predikcija. 

Preduslovi za pokretanje aplikacije jesu da korisnik na lokalnoj mašini ima instaliran:
- python 2.7
- django 1.11.4.

S obzirom da alati koji se koriste u aplikaciji nisu besplatno dostupni neakademskim korisnicima, iz
tog razloga alati nisu dostupni zajedno sa kodom aplikacije. Akademski korisnici mogu ove alate besplatno da preuzmu na adresi [http://www.cbs.dtu.dk/][1] i to:
- netMHC-4.0
- netMHCpan-3.0
- netCTLpan-1.1
- pickpocket-1.1
- netMHCcons-1.1

I konačno, neophodno je promeniti deo koda na početku *views.py* tako da odgovara fizičkim putanjama direktorijuma na korisnikovoj mašini u kojima se nalaze pobrojani alati. 

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

Aplikacija se pokreće ulaskom u dikrektorijum *master* u kom se nalazi skripta  *manage.py*  na sledeći način: <br /> 
**python manage.py runserver**

[1]: http://www.cbs.dtu.dk/services/

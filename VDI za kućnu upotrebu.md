# VDI za kućnu upotrebu

 

VDI (**V**irtual **D**esktop **I**nfrastructure) se u najkraćim crtama definiše kao tip *virtuelizacije desktopa*, mehanizam koji više desktopa izvršava na pojedinačnim virtuelnim mašinama (koje su smeštene na jednom, centralnom serveru) i dostavlja klijentima putem mreže. Lepota ove tehnologije je mogućnost da klijentski uređaj može biti i veoma slab računar, tablet, pametni telefon ili bilo koji tip "tankog" terminala. Međutim, to znači da mašina na kojoj je server mora biti jaka. I to je u redu, jer se VDI uglavnom koristi u korporativnom okruženju, za firme sa više stotina ili hiljada zaposlenih. 

### Zahtevi

---

Moje pitanje je - *da li je moguće iskoristiti VDI tehnologiju za kućnu upotrebu?* Odgovor koji sam dobio istraživajući po Internetu je, u najmanju ruku, kontradiktoran.

Motiv da počnem da čeprkam po dubinama reddit-a, microsoftovih support centara i gomili blogova je jednostavan - moram da kupim novi računar.  Mora i moj otac da kupi sebi nov, kao i braća. Dakle, to su 3 laptop računara prosečnih mogućnosti, svaki od njih po 500 ili 600 evra i dolazimo do cifre koja nije zanemarljiva. Zapitao sam se da li je moguće da kupovinom jednog jakog desktop računara i konfigurisanjem VDI možemo da uštedimo ili makar povećamo radne mogućnosti. U tom slučaju bismo mogli sa svojih trenutnih, skoro pa zastarelih računara da pristupamo ozbiljnoj mašineriji.
Glavni problem je sledeći - svako od nas ima različite zahteve. Oca smo odmah otpisali kao prosečnog korisnika (email, surfovanje netom, društvene mreže, word/excel), te smo ostali braća i ja. Najzahtevnije stvari koje braća koriste su softveri za editovanje videa i muzike, a ja bih koristio za 3D modeling i pokretanje emulatora na npr. Android studiu što traje satima na mom trenutnom laptopu. Naravno, odmah sam znao da korišćenje VDI-a za te programe neće biti moguće, te sam došao do neke vrste kompromisa. Pre toga, odgovor na glavno pitanje.

### Istraživanje

---

**Moguće** je napraviti kućnu varijantu VDI. 

Međutim, to što je moguće, ne znači da je isplativo u vidu vremena, novca i truda. Da krenemo od hardvera: realno je sklopiti regularan PC računar sa veoma jakim performansama i od njega napraviti server za korišćenje VDI tehnologije. Ideja je da se umesto mašine namenjene za server koristi regularan jači računar kako bi bilo moguće i korišćenje Desktopa za zahtevnije programe. To bih verovatno uradio dual boot-om. Dakle, sa te strane je ovo isplativija varijanta, sve komponente za jak računar bi bile 1200-1400$. Već ovakva mašina je sigurno duplo bolja od laptopa od 600$, da ne pominjem ako bi se uložilo još novca.
Što se tiče softvera, to je druga priča. Poprilično je komplikovano uspostaviti VDI server i podesiti ga po želji, iako rad na pojednostavljivanju uveliko napreduje. Svaka od dodatnih stavki za pojedinačne desktope traje po više sati. Međutim, tu nije kraj - činjenica koja je najviše naglašavana na skoro svakom od sajtova jeste da VDI server nije nešto što se *instalira i zaboravi*, već je potrebna **konstantna** briga, ažuriranje i sređivanje problema koji će se neminovno događati. Vreme uloženo u održavanje servera i desktopa, posebno za nekoga ko je tek uplivao u ceo IT svet se graniči sa nemogućim. Razlog tome je što i ozbiljni stručnjaci govore o VDI kao veoma zahtevnoj tehnologiji. Stoga, što se tiče vremena - veliki minus za VDI. 
Kada je u pitanju novac, tu su mišljenja podeljena. Mnogi forsiraju korišćenje Windows Servera sa Hyper-V virtuelizacijom, međutim licenciranje svake od virtuelnih mašina, to jest svake instance desktopa košta 100$ godišnje. Ne baš sjajno. Srećom tu su open-source varujante koje nam nude širok dijapazon opcija, poput Xen servera, FlexVDI i FOSS-Cloud alata. Naravno, većina njih ima unapređenu verziju koja se, gle čuda - plaća. Mora biti rečeno da sve što se plaća nosi sa sobom bezbroj mogućnosti koje su fenomenalne, međutim za kućnu upotrebu nama bi bile dovoljne osnovne verzije.  

## Prednosti i mane

Sama ideja za kućnom varijantom VDI-a je potekla zbog korišćenja više različitih desktopa sa različitim funkcionalnostima na jednoj mašini. Stoga, najbitnija **prednost** VDI tehnologije jeste upravo mogućnost kreiranja velikog broja desktopa i ograničavanja funkcionalnosti svakog od njih. Jedan od mogućih slučaja primene jeste dolazak gostiju, bilo odraslih ili dece. Nije mi najprijatnije da pustim malo dete ili nekoga ko nema puno iskustva sa računarima da nenadgledano čeprka po mom laptopu, ili da "samo pogleda nešto na netu". Dakle, za goste - jedan desktop sa popriličnim ograničenjima. Za majku kojoj je potreban samo Youtube - jedan desktop. Za oca koji je "prosečan korisnik"- poseban desktop. Za strimovanje - jedan poseban desktop. Za šta god mi padne na pamet - jedan desktop. Za braću i mene - tu dolazimo do neizbežnog kompromisa. Kao što sam ranije pomenuo nemoguće je preko virtuelizovanog desktopa pokretati ozbiljnije programe, programe specijalne namene. Stoga, ono što je meni palo na pamet jeste da svakodnevno korišćenje i npr. rad u razvojnom okruženju omogućim virtuelnim desktopom, jednim za sebe, drugim za braću, a da rad za u zahtevnijim programima delimo vreme na samoj mašini. Kao što se može zaključiti, ne baš sjajno rešenje, ali naizgled jedino moguće. Sa strane novca, ova varijanta može biti isplativa u određenim slučajevima, ali je pitanje da li je vredno truda sa aspekta manje-više svega ostalog.

Dolazimo do mana, koje se pojavljuju na svakom koraku. Krenućemo od najvažnije, a to je vreme utrošeno u kreiranje i ažuriranje svakog pojedinačnog desktopa. Ovo **nije** program na koji možete da zaboravite nakon instalacije, već je potrebno ozbiljno održavanje. To nas dovodi do druge mane usko povezane za gorepomenutu, a to je znanje potrebno za odražavanje VDI-a. IT početniku bi bilo veoma, veoma zahtevno da se upusti u ovu priču bez ozbiljnije predznanja, što opet zahteva dosta uloženog vremena. Opet, u slučaju da se izabere VDI varijanta koja se plaća, prednost koju nosi jeftiniji hardver se briše plaćanjem licenci za svaku instancu desktopa. 

## Zaključak

Iako je danas ova tehnologija dovoljno napredovala da se preko nje može raditi maltene sve sem igranja 3D igara, za obične korisnike, pa čak i one naprednije nije isplativo koristiti VDI. Pametni telefoni su preuzeli skoro sve funkcionalnosti računara, te su radnje poput surfovanja internetom, gledanja Youtube-a, pisanja mejlova, pa čak i rada u MS Office paketu potpuno prenete na mobilne telefone. Stoga - prednosti VDI-a gube na vrednosti, osim u nekim specijalnim slučajevima. U mom konkretnom slučaju, ne isplati se pre svega uloženog vremena, što u učenje tehnologije, što u samo održavanje. Za sada ostajem običan korisnik računara. Međutim, ako se desi prilika u kojoj bih imao novca i vremena da uložim u ovi veoma zanimljivu tehnologiju, zašto da ne. Postoje čak i skoro "plug and play" varijante VDI-a. Kažem skoro jer je i tu potrebno dosta tweak-ovanja, što opet konzumira određeno vreme, ali ako bude novca - ko zna...

Zaključak - treba vam veoma snažan povod za korišćenje VDI-a u svom domu. 



Spisak sajtova sa kojih su izvučene najbitnije informacije:

* [Dokaz](https://www.jasonsamuel.com/the-how-to-build-a-windows-virtual-desktop-vdi-experience-properly-cheat-sheet/) koliko je komplikovano podešavanje.
* [Top 5](https://learn.g2.com/free-vdi) (pseudo) besplatnih VDI rešenja.

* [VDI](https://xenproject.org/) koji pruža najviše mogućnosti. 
* [Neformalno mišljenje](https://www.reddit.com/r/sysadmin/) manje ili više stručnih ljudi.
* [Šta kaže Microsoft](https://docs.microsoft.com/en-us/windows-server/remote/remote-desktop-services/rds-vdi-recommendations), i još [ponešto](https://social.technet.microsoft.com/Forums/windowsserver/en-US/3ad37684-4f55-4680-8466-577840807ee0/vdilike-setup-for-household-use?forum=winserverTS).
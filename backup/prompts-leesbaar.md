# PromptFinder – leesbare lijst
Export: 2026-09-24T09:24:36Z · 994 items


## Algemeen (142)

### Bestanden & mappen
- `Bestandssysteem` — **Hoe bestanden georganiseerd zijn**: De manier waarop bestanden en mappen op de schijf bewaard worden. Op Linux is dat één grote boom die start bij de root-map /, zonder stationsletters zoals C: op Windows.
- `Map (directory)` — **Een container voor bestanden**: Wat je op Windows een 'folder' noemt. In de terminal heet het een directory. Mappen kunnen andere mappen bevatten, zo ontstaat een boomstructuur.
- `Root-map ( / )` — **Het begin van het bestandssysteem**: De bovenste map waar alles onder hangt. Belangrijke mappen eronder: /home (thuismappen), /bin en /usr (programma's), /etc (instellingen), /tmp (tijdelijke bestanden).
- `Thuismap ( ~ )` — **Jouw eigen map**: Elke gebruiker heeft een eigen map, bv. /home/guest. Het teken ~ is er een afkorting voor. Met cd zonder argument ga je er altijd naartoe.
- `Pad (absoluut en relatief)` — **Het 'adres' van een bestand**: Een absoluut pad start bij de root: /home/guest/data/seq.fasta. Een relatief pad start vanaf de map waar je nu staat: data/seq.fasta. . betekent 'deze map', .. betekent 'één map hoger'.
- `Verborgen bestand` — **Bestand dat met een punt begint**: Bestanden zoals .bashrc worden niet getoond door een gewone ls. Ze bevatten meestal instellingen. Toon ze met ls -a.
- `Bestandsrechten (rwx)` — **Wie mag wat met een bestand**: Elk bestand heeft rechten voor de eigenaar, de groep en de rest: lezen (r), schrijven (w) en uitvoeren (x). ls -l toont ze, bv. -rwxr-xr--. Je past ze aan met chmod.
- `Bestandsnamen in Linux` — **Regels voor goede bestandsnamen**: In Linux is alles een bestand en zijn extensies (zoals .txt) niet verplicht, maar wel handig. Gebruik geen speciale tekens zoals ( ) [ ] { } / ? * ' " ~ ` & $ ! | in namen; punten en komma's mogen wel. _(bron: Chapter 3 - Organizing files.pptx, dia 4)_
- `Bestandstypes` — **Soorten bestanden in Linux**: Linux kent gewone bestanden (tekst), uitvoerbare bestanden (programma's), mappen, links (verwijzing naar een bestand op een andere plaats), sockets (netwerkcommunicatie tussen processen) en named pipes (communicatie tussen processen zonder netwerk). _(bron: Chapter 3 - Organizing files.pptx, dia 5)_
- `Systeemmappen` — **Vaste mappen van het systeem**: Systeembestanden staan in vaste mappen: bin/sbin/lib voor programma's, etc voor configuratie, dev/media/mnt voor hardware, doc/share voor documentatie. /boot bevat de kernel, /proc en /run lopende processen, /lost+found teruggevonden bestanden. Die mappen bestaan op drie niveaus: /, /usr en /usr/local. _(bron: Chapter 3 - Organizing files.pptx, dia 9)_
- `Inode` — **Verwijzing naar data op schijf**: Een inode is een verwijzing naar de datablokken van een bestand op de harde schijf. Eén of meer bestandsnamen zijn gekoppeld aan een inode; zo kan dezelfde data meerdere namen hebben (links). _(bron: Chapter 3 - Organizing files.pptx, dia 24)_
- `Hardlink en symbolische link` — **Twee soorten links**: Een hardlink is een extra naam voor dezelfde inode (dezelfde data); verwijder je het origineel, dan blijft de data bereikbaar via de hardlink. Een symbolische link (symlink) is een klein apart bestand met een eigen inode dat naar een andere bestandsnaam wijst; verwijder je het origineel, dan werkt de symlink niet meer. _(bron: Chapter 3 - Organizing files.pptx, dia 25)_
- `Archief` — **Veel bestanden in één bestand**: Een archief bundelt veel bestanden en mappen in één bestand (bv. .tar). Zo kan je ze makkelijk als één geheel verplaatsen of een back-up maken. Een archief is niet automatisch gecomprimeerd. _(bron: Chapter 6 - The work environment.pptx, dia 24)_
- `Compressie` — **Bestand kleiner maken**: Compressie maakt een bestand kleiner zodat het minder schijfruimte inneemt, bv. met gzip (.gz) of bzip2 (.bz2). Een .tar.gz is een archief dat daarna gecomprimeerd werd. _(bron: Chapter 6 - The work environment.pptx, dia 27)_
- `Scheidingsteken (delimiter)` — **Teken tussen de kolommen**: Het scheidingsteken is het teken dat de kolommen (velden) van een tabel van elkaar scheidt, meestal een tab, spatie of komma. Bij veel commando's kun je het instellen, bv. cut -d, join -t of de awk-variabele FS. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 9)_
- `Record en veld` — **Regel en kolom van een tabel**: In een tabelbestand is een record één regel (één rij) en een veld één kolom binnen die regel. Commando's zoals cut, sort, join en awk werken met die velden. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 22)_

### Bio-informatica
- `PDB (Protein Data Bank)` — **Databank met 3D-structuren**: Een publieke databank met experimenteel bepaalde 3D-structuren van eiwitten en nucleïnezuren. Elke structuur heeft een code van 4 tekens, bv. 1UBQ. In PyMOL laad je die met fetch 1ubq.
- `FASTA` — **Tekstformaat voor sequenties**: Een eenvoudig formaat voor DNA- of eiwitsequenties: een regel die begint met > bevat de naam, de regels eronder de sequentie. Daarom telt grep -c '>' het aantal sequenties.
- `PyMOL` — **Programma om moleculen in 3D te bekijken**: Toont eiwitstructuren in 3D en laat je ze kleuren, selecteren en meten. Je kan klikken in de menu's of commando's typen achter de PyMOL>-prompt.
- `Eiwitstructuur (primair tot quaternair)` — **De vier niveaus van een eiwit**: Primair: de volgorde van aminozuren. Secundair: lokale vormen zoals α-helices en β-sheets. Tertiair: de volledige 3D-vouwing van één keten. Quaternair: hoe meerdere ketens samen een complex vormen.
- `Reproduceerbaarheid` — **Analyse opnieuw met zelfde resultaat**: Een analyse is reproduceerbaar als iemand anders ze later opnieuw kan uitvoeren en hetzelfde resultaat krijgt. Dat is nodig voor goed databeheer en FAIR-data (Findable, Accessible, Interoperable, Reusable). Hoe meer je isoleert (VENV < container < virtuele machine), hoe reproduceerbaarder. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 4)_
- `Virtuele omgeving (VENV)` — **Afgeschermde set software-versies**: Een virtuele omgeving is een aparte omgeving waarin je analysetools en hun afhankelijkheden in een bepaalde versie installeert, los van de rest van het systeem. Je kunt ze exporteren en elders opnieuw opbouwen, bv. met Conda. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 6)_
- `Conda` — **Pakketbeheerder met virtuele omgevingen**: Conda is een pakketbeheerder die afgeschermde omgevingen beheert, inclusief afhankelijkheden en versies. Je hebt geen administratorrechten nodig. Miniconda is een afgeslankte versie van de volledige Anaconda. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 9)_
- `Kanaal (conda channel)` — **Bron van kant-en-klare pakketten**: Een kanaal is een online verzameling voorgecompileerde conda-pakketten. Voorbeelden: defaults, conda-forge (algemene software en bibliotheken) en bioconda (bio-informaticasoftware). De volgorde van de kanalen staat in ~/.condarc. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 9)_
- `Wet lab en dry lab` — **Experimenteel labo versus computerwerk**: In het wet lab doe je experimenten met echte biologische stalen. In het dry lab werk je op de computer: je ontwikkelt en gebruikt algoritmes en tools om biologische data om te zetten in kennis, die dan weer tot nieuwe experimenten leidt. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 5)_
- `Moleculaire visualisatiesoftware` — **Programma's om moleculen te bekijken**: Programma's die 3D-structuren van moleculen tonen, bv. PyMOL, Cn3D, Jmol, Swiss-PdbViewer, VMD en YASARA. Een lijst vind je op de RCSB-website (rcsb.org/docs/additional-resources/molecular-graphics-software). _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 14)_
- `LiteMol` — **3D-viewer in de webbrowser**: Gratis HTML5-webapplicatie om moleculen in 3D te bekijken in je browser. Ze is ingebouwd in PDBe (Protein Data Bank in Europe) en andere websites zoals UniProt en Ensembl; de broncode staat op GitHub. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 15)_
- `Multiple sequence alignment (MSA)` — **Meerdere sequenties onder elkaar uitlijnen**: Meerdere eiwit- of DNA-sequenties zo onder elkaar zetten dat overeenkomstige posities in dezelfde kolom staan. Zo zie je welke residuen geconserveerd zijn tussen soorten of familieleden. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 10)_
- `RCSB-sequentieweergave` — **Annotaties langs de sequentie**: Op rcsb.org/sequence/<PDB-code> zie je per keten de sequentie met annotaties: secundaire structuur, UniProt-koppeling, bindingsplaatsen, glycosylaties, disulfidebruggen, domeinen (Pfam, CATH) en validatie-outliers. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 11)_
- `PyMOL Script Library` — **Verzameling kant-en-klare PyMOL-scripts**: Op de PyMOL-wiki (pymolwiki.org, Category:Script_Library) staan veel gratis scripts die extra functies toevoegen, bv. findseq of kleuren volgens conservering. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 4)_
- `NCBI Protein` — **Databank met eiwitsequenties**: Databank van het NCBI met eiwitsequenties. Je zoekt er bv. isoformen van een eiwit en bewaart de sequenties in FASTA-formaat, bv. voor een alignment. _(bron: SB-workshop-5-databases-tools.pptx, dia 2)_
- `RefSeq` — **Gecureerde referentiesequenties (NCBI)**: Collectie van het NCBI met één gecontroleerde, niet-redundante referentiesequentie per transcript of eiwit. Handig om te tellen hoeveel echte eiwitvarianten een gen heeft. _(bron: SB-workshop-5-databases-tools.pptx, dia 2)_
- `NCBI Gene` — **Databank met informatie per gen**: Databank van het NCBI met per gen de officiële naam en het symbool, de transcripten en eiwitten, en links naar andere databanken. _(bron: SB-workshop-5-databases-tools.pptx, dia 3)_
- `CD-search` — **Geconserveerde domeinen zoeken**: Tool van het NCBI (Conserved Domain search) die in een eiwitsequentie de gekende domeinen zoekt en hun posities en belangrijke residuen toont. _(bron: SB-workshop-5-databases-tools.pptx, dia 3)_
- `HGNC (genenames.org)` — **Officiële menselijke gennamen**: Het HUGO Gene Nomenclature Committee kent officiële namen en symbolen toe aan menselijke genen en groepeert ze in genfamilies, bv. de cadherines (CDH1, CDH2 ...). _(bron: SB-workshop-5-databases-tools.pptx, dia 7)_
- `PubMed` — **Databank met wetenschappelijke artikels**: Zoekmachine van het NCBI voor biomedische wetenschappelijke publicaties (pubmed.ncbi.nlm.nih.gov). _(bron: SB-workshop-5-databases-tools.pptx, dia 7)_
- `PubMed en MeSH` — **Wetenschappelijke literatuur zoeken**: PubMed (NCBI) doorzoekt miljoenen biomedische publicaties, vooral uit MEDLINE. Automatic Term Mapping koppelt zoektermen aan MeSH-trefwoorden, tijdschriften en auteurs; met een zoektag of een zinsdeel tussen aanhalingstekens ("transcription factor") wordt dat overgeslagen. _(bron: SB-05-data-representation-databases.pptx, dia 46)_
- `salmonella AND (hamburger OR eggs)` — **Zoektermen combineren met operatoren**: Booleaanse operatoren combineren zoektermen in PubMed. Ze worden van links naar rechts verwerkt; haakjes veranderen de volgorde. _(bron: SB-05-data-representation-databases.pptx, dia 50)_
- `transcript* [ti]` — **Zoeken in titel met truncatie**: Zoekveldtags tussen vierkante haken beperken de zoekopdracht tot één veld. Met * zoek je alle woorden die met dat stuk beginnen (transcript, transcription, transcriptase …). _(bron: SB-05-data-representation-databases.pptx, dia 53)_
- `2014:2018 [dp]` — **Zoeken binnen een periode**: Zoekt publicaties binnen een bereik van publicatiedatums. _(bron: SB-05-data-representation-databases.pptx, dia 53)_

### Computer & besturingssysteem
- `Besturingssysteem (OS)` — **Software die je computer beheert**: Het basisprogramma dat de hardware (processor, geheugen, schijf) beheert en andere programma's laat draaien. Voorbeelden: Windows, macOS, Linux, Android.
- `Kernel` — **Het hart van het besturingssysteem**: Het centrale deel van het OS dat rechtstreeks met de hardware praat: het verdeelt processortijd en geheugen over programma's en regelt de toegang tot bestanden en apparaten. Je werkt er nooit rechtstreeks mee; je vraagt dingen via de shell of programma's.
- `Linux` — **Een gratis, open besturingssysteem**: Een besturingssysteem gebouwd rond de Linux-kernel. Het wordt veel gebruikt op servers en in de bio-informatica, omdat veel analyseprogramma's er (enkel) voor gemaakt zijn en alles met commando's te automatiseren is.
- `Distributie (distro)` — **Een 'versie' van Linux**: Een pakket van de Linux-kernel met programma's, een pakketbeheerder en een bureaublad errond. Voorbeelden: Ubuntu, Fedora, Debian. De commando's zijn grotendeels dezelfde; vooral de pakketbeheerder verschilt (apt op Ubuntu, dnf op Fedora).
- `Virtuele machine (VM)` — **Een computer in je computer**: Software die een volledige computer nabootst, zodat je bv. Linux kan draaien binnen Windows. Wat je in de VM doet, raakt je eigen systeem niet. Programma's: VirtualBox, VMware, WSL op Windows.
- `UNIX` — **Voorloper van Linux**: UNIX is een besturingssysteem dat eind jaren '60 bij Bell Labs ontwikkeld werd, eenvoudig en in de taal C geschreven zodat code herbruikbaar was. Het werd veel gebruikt door grote bedrijven, maar was duur. Linux is een gratis kloon van UNIX. _(bron: Chapter 1 - Introduction.pptx, dia 10)_
- `GNU` — **Vrij UNIX-achtig softwareproject**: GNU ('GNU's Not UNIX') is een beweging die gratis, vrije UNIX-software aanbiedt, zoals Bash, GCC en de coreutils. Samen met de Linux-kernel vormt die software een volledig besturingssysteem. _(bron: Chapter 1 - Introduction.pptx, dia 11)_
- `GNOME` — **Grafische desktopomgeving van GNU**: GNOME is de GNU-desktopomgeving: de grafische gebruikersinterface (GUI) met vensters, iconen en menu's. Fedora Workstation gebruikt standaard GNOME. _(bron: Chapter 1 - Introduction.pptx, dia 22)_
- `Fedora Workstation` — **Linux-distributie van deze cursus**: Fedora is een gratis open-sourcedistributie van Linux, ondersteund door Red Hat. In deze cursus installeer je Fedora Workstation in een virtuele machine. _(bron: Chapter 1 - Introduction.pptx, dia 24)_
- `ISO-bestand` — **Installatiebestand van een besturingssysteem**: Een ISO-bestand is een kopie (image) van een installatieschijf in één bestand. Je hebt het ISO-bestand van Fedora Workstation nodig om Linux in een virtuele machine te installeren. _(bron: Chapter 1 - Introduction.pptx, dia 25)_

### Gebruikers
- `Root (superuser)` — **De beheerder van het systeem**: De gebruiker die alles mag, ook systeembestanden aanpassen of verwijderen. Daarom werk je normaal als gewone gebruiker en gebruik je sudo alleen als het echt nodig is.
- `sudo` — **Eén commando als beheerder uitvoeren**: Zet je sudo voor een commando, dan wordt het uitgevoerd met root-rechten (na je wachtwoord). Nodig om bv. software te installeren. Wees voorzichtig: fouten met sudo kunnen het systeem beschadigen.
- `Multi-user omgeving` — **Meerdere gebruikers op één systeem**: Linux laat meerdere gebruikers tegelijk op één systeem werken. Daarom heeft elk bestand een eigenaar, een groep en rechten, voor privacy en veiligheid. _(bron: Chapter 3 - Organizing files.pptx, dia 41)_
- `Octale notatie van rechten` — **Rechten als letters en getallen**: r (lezen) = 4, w (schrijven) = 2, x (uitvoeren; bij een map: binnengaan met cd) = 1. Tel ze op per gebruikersgroep: u (user), g (group), o (others). Zo is rwx = 7, rw- = 6 en r-x = 5; 755 betekent rwxr-xr-x. _(bron: Chapter 3 - Organizing files.pptx, dia 44)_

### In- en uitvoer
- `stdin, stdout, stderr` — **De drie standaardkanalen**: Elk commando heeft standaardinvoer (stdin, meestal het toetsenbord), standaarduitvoer (stdout, gewone uitvoer) en standaardfout (stderr, foutmeldingen). Beide uitvoerkanalen verschijnen in de terminal, maar je kan ze apart doorsturen.
- `Redirect ( > en >> )` — **Uitvoer naar een bestand sturen**: Met > schrijf je de uitvoer van een commando in een bestand (overschrijft), met >> voeg je toe aan het einde. Met 2> stuur je foutmeldingen apart door. Bv. ls -l > lijst.txt.
- `Pipe ( | )` — **Commando's aan elkaar koppelen**: Stuurt de uitvoer van het ene commando als invoer naar het volgende. Bv. grep '>' seq.fasta | wc -l telt het aantal sequenties. Zo bouw je met kleine commando's een grotere analyse.
- `Jokerteken (wildcard)` — **Patroon om meerdere bestanden te kiezen**: De shell vervangt patronen door passende bestandsnamen: * = eender welke tekens, ? = precies één teken, [abc] = één van deze tekens, [!abc] = geen van deze. Bv. ls *.fasta.
- `Reguliere expressie (regex)` — **Zoekpatroon voor tekst**: Een krachtigere zoektaal dan jokertekens, gebruikt door grep, sed en awk. Bv. ^ATG zoekt regels die met ATG beginnen, [0-9]+ zoekt één of meer cijfers. Let op: regex en jokertekens gebruiken * en ? anders.
- `File descriptor (0, 1, 2)` — **Nummer voor invoer- of uitvoerkanaal**: De shell geeft elk in- en uitvoerkanaal een nummer: 0 = standaardinvoer (stdin), 1 = standaarduitvoer (stdout), 2 = standaardfout (stderr). Met die nummers kan je ze apart omleiden, bv. 2> voor foutmeldingen. _(bron: Chapter 5 - Input and output.pptx, dia 13)_
- `Delimiter (scheidingsteken)` — **Teken dat stukken tekst scheidt**: Een delimiter is een teken of reeks tekens die de verschillende stukken in een tekst van elkaar scheidt, zoals een komma, puntkomma, tab of spatie. In PHP gebruik je een delimiter bij explode() en implode(). _(bron: 4. Fundamentals of PHP.pptx, dia 87)_

### Netwerk
- `Server en client` — **Wie aanbiedt en wie vraagt**: Een server is een computer (of programma) die diensten aanbiedt, zoals websites of rekenkracht. Een client vraagt die op, bv. je browser of je terminal via ssh.
- `SSH` — **Veilig inloggen op een andere computer**: Secure Shell: hiermee open je een terminal op een andere computer (bv. een rekenserver van school) via het netwerk, beveiligd met versleuteling. Bv. ssh student@server.be.
- `SFTP` — **Bestanden veilig overzetten**: (S)FTP staat voor (SSH) File Transfer Protocol: een manier om bestanden van en naar een server over te zetten, bv. met het programma FileZilla. _(bron: Chapter 2 - The terminal.pptx, dia 37)_
- `Poort (netwerk)` — **Genummerd toegangspunt voor netwerkverkeer**: Een poort is een nummer waarmee netwerkverkeer bij het juiste programma terechtkomt, bv. poort 80 voor een webserver. Met docker run --publish koppel je een poort van de host aan een poort in de container. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 32)_
- `localhost en poort` — **Je eigen computer als server**: localhost betekent: je eigen computer. Het poortnummer (bv. 8080) kies je als een 'kamer' waarin je website draait; kies een getal tussen 1024 en 65535, meestal 8000 of 8080. Zo kun je je site privé testen in de browser. _(bron: 5. Dynamic Web Pages.pptx, dia 4)_

### Programma's & processen
- `Proces` — **Een programma dat nu draait**: Elke keer dat je een programma start, maakt het besturingssysteem er een proces van met een eigen nummer (PID). Je bekijkt processen met ps of top en stopt ze met kill.
- `Pakketbeheerder` — **Installeert en updatet software**: Een programma dat software downloadt, installeert en up-to-date houdt, zoals een app store in de terminal. Voorbeelden: apt (Ubuntu), dnf (Fedora), conda en pip (Python/bio-informatica).
- `Script` — **Een bestand vol commando's**: Een tekstbestand (bv. analyse.sh) met commando's die na elkaar uitgevoerd worden. Handig om een analyse te herhalen of te automatiseren. Maak het uitvoerbaar met chmod +x en start het met ./analyse.sh.
- `Variabele` — **Een naam die een waarde onthoudt**: In bash maak je een variabele met NAAM=waarde (zonder spaties rond =) en gebruik je ze met $NAAM, bv. echo $NAAM.
- `Omgevingsvariabele` — **Instelling die programma's kunnen lezen**: Een variabele die voor alle programma's in je shell geldt, bv. $HOME (je thuismap) of $USER (je gebruikersnaam). Toon ze allemaal met env.
- `PATH` — **Waar de shell programma's zoekt**: Een omgevingsvariabele met een lijst mappen. Typ je ls, dan zoekt de shell in die mappen naar een programma met die naam. 'command not found' betekent vaak dat het programma niet in je PATH staat of niet geïnstalleerd is.
- `Open source` — **Software met vrij beschikbare broncode**: Open source betekent dat de broncode van software vrij beschikbaar is: iedereen mag ze bekijken, aanpassen en verder verspreiden. Linux en de GNU-tools zijn open source. _(bron: Chapter 1 - Introduction.pptx, dia 11)_
- `GPL (General Public License)` — **Belangrijkste open-sourcelicentie**: De GPL is de licentie die door GNU opgesteld werd. Ze bepaalt dat je software vrij mag gebruiken, aanpassen en delen, op voorwaarde dat aangepaste versies ook onder de GPL vrij blijven. _(bron: Chapter 1 - Introduction.pptx, dia 11)_
- `GCC (GNU C Compiler)` — **Compiler voor broncode**: GCC is de compiler van GNU: hij zet broncode (bv. in C) om naar een programma dat de computer kan uitvoeren. Je gebruikt hem om toepassingen vanuit hun broncode te bouwen. _(bron: Chapter 1 - Introduction.pptx, dia 15)_
- `Coreutils` — **Basisprogramma's van GNU**: De coreutils zijn een set basisopdrachten die op elk Linux-systeem aanwezig zijn, zoals ls (inhoud van mappen tonen), cat (bestanden bekijken) en chmod (bestandsrechten wijzigen). _(bron: Chapter 1 - Introduction.pptx, dia 15)_
- `PID (proces-ID)` — **Uniek nummer van een proces**: Elk programma dat je start krijgt een PID: een uniek getal waarmee Linux het proces herkent. Je gebruikt de PID om een proces op te zoeken (ps) of te stoppen (kill). _(bron: Chapter 4 - Processes.pptx, dia 5)_
- `Job` — **Programma gestart vanuit de shell**: Een job is één of meer programma's die je als één shellcommando uitvoert. In je terminal krijgt elke job een jobnummer (bv. [1]) dat je met jobs, fg, bg en kill %nr gebruikt. _(bron: Chapter 4 - Processes.pptx, dia 5)_
- `Batchproces` — **Automatisch proces in een wachtrij**: Een proces dat niet vanuit een terminal gestart wordt, maar automatisch. Batchprocessen staan in een wachtrij en worden volgens het FIFO-principe (first in, first out) uitgevoerd. _(bron: Chapter 4 - Processes.pptx, dia 6)_
- `Ouder- en kindproces` — **Proces dat een ander proces start**: Een kindproces (child) is een proces dat door een ander proces, de ouder (parent), gestart wordt. Start je een commando in de terminal, dan is de shell de ouder en het commando het kind. Elk proces heeft een ouder, behalve init. _(bron: Chapter 4 - Processes.pptx, dia 6)_
- `init` — **Eerste proces van het systeem**: init is het allereerste proces dat bij het opstarten gestart wordt; het heeft als enige proces geen ouder. Het adopteert ook weesprocessen. Op moderne Fedora heet dit proces systemd (PID 1). _(bron: Chapter 4 - Processes.pptx, dia 6)_
- `Daemon` — **Achtergronddienst zonder terminal**: Een daemon is een serverproces dat continu op de achtergrond draait zonder terminal. Het wacht op werk en levert een dienst, bv. een maildaemon of de cron-daemon. _(bron: Chapter 4 - Processes.pptx, dia 7)_
- `Weesproces (orphan)` — **Proces waarvan de ouder gestopt is**: Een weesproces is een proces waarvan het ouderproces afgesloten (gekild) werd. Het blijft verder draaien en wordt overgenomen door init. _(bron: Chapter 4 - Processes.pptx, dia 7)_
- `Zombieproces` — **Beëindigd proces nog in procestabel**: Normaal leest het ouderproces de exitstatus van een beëindigd kindproces, waarna het uit de procestabel verdwijnt. Een zombie is al gestopt maar staat nog in de procestabel. top toont hoeveel zombies er zijn. _(bron: Chapter 4 - Processes.pptx, dia 8)_
- `Voorgrond en achtergrond` — **Waar een proces draait**: Een voorgrondproces 'bezet' de terminal: je kan pas verder typen als het klaar is. Een achtergrondproces (gestart met &) laat de terminal vrij; handig voor programma's die lang lopen en geen invoer nodig hebben. _(bron: Chapter 4 - Processes.pptx, dia 10)_
- `Signaal (SIGTERM, SIGKILL …)` — **Bericht om proces te sturen**: Met kill stuur je een signaal naar een proces. SIGTERM (15) stopt het proces netjes, SIGINT (2) onderbreekt het (kan genegeerd worden), SIGKILL (9) stopt het altijd, SIGHUP (1) laat een daemon zijn configuratie opnieuw inlezen. _(bron: Chapter 4 - Processes.pptx, dia 22)_
- `Prioriteit (nice-waarde)` — **Hoe voorrang een proces krijgt**: De nice-waarde bepaalt hoeveel processortijd een proces krijgt, van -20 (hoogste prioriteit) tot +19 (laagste). Standaard is ze 0. Hoe 'vriendelijker' (nicer) een proces, hoe minder voorrang het neemt. _(bron: Chapter 4 - Processes.pptx, dia 26)_
- `Cron-daemon` — **Voert geplande taken automatisch uit**: De cron-daemon kijkt elke minuut of er taken uitgevoerd moeten worden. Die taken staan in crontab-bestanden: elke regel is een taak die herhaald wordt, bv. dagelijks de index voor locate bijwerken. _(bron: Chapter 4 - Processes.pptx, dia 33)_
- `RPM- en DEB-pakketten` — **Softwarepakketten per distributie**: Welke pakketten je gebruikt, hangt af van de distributie: RPM (Red Hat Package Manager) bij Red Hat, Fedora, CentOS; DEB bij Debian en Ubuntu. Daarnaast bestaan bronpakketten (.tar.gz met broncode) die je zelf moet compileren. _(bron: Chapter 6 - The work environment.pptx, dia 32)_
- `Container` — **Geïsoleerde omgeving voor een programma**: Een container is een afgeschermde omgeving die binnen het besturingssysteem van de host draait en een tool met al zijn afhankelijkheden bevat. Containers zijn lichter en sneller dan virtuele machines, makkelijk over te zetten naar andere systemen en te automatiseren. Docker is het bekendste systeem, Singularity een ander. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 17)_
- `Image (Docker)` — **Alleen-lezen sjabloon voor containers**: Een image is een alleen-lezen sjabloon met een besturingssysteem en software. Een container is een draaiend exemplaar van een image; van één image kun je veel containers starten. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 19)_
- `Docker registry` — **Online opslagplaats van images**: Een registry is een online plaats waar kant-en-klare images klaarstaan om te downloaden (pull). Docker Hub is het belangrijkste publieke registry; BioContainers verzamelt images van bio-informaticatools. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 24)_
- `Dockerfile` — **Recept om een image te bouwen**: Een Dockerfile is een tekstbestand met instructies om een image te bouwen. Het start meestal van een basis-image (bv. ubuntu of alpine) en elke regel voegt een laag toe. Met docker build maak je er een image van. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 34)_
- `Docker compose` — **Meerdere containers samen beheren**: Docker compose is de volgende stap na Docker: waar Docker één container start, beheert Docker compose meerdere containers samen. De instellingen staan in een yaml-bestand (standaard docker-compose.yml). _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 37)_
- `Podman` — **Veiliger alternatief voor Docker**: Podman is een alternatief voor Docker, gebruikt in omgevingen waar veiligheid belangrijk is. Bijna alle commando's zijn gelijk aan die van Docker, maar Podman gebruikt geen daemon op de achtergrond en vraagt geen lidmaatschap van de docker-groep of sudo. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 41)_
- `Lus (loop)` — **Opdrachten herhalen**: Een lus herhaalt een reeks opdrachten: voor elk element uit een lijst (for) of zolang een voorwaarde waar is (while). Zonder stopvoorwaarde loopt een lus eindeloos door. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 23)_
- `Teksteditor (VS Code)` — **Programma om code te schrijven**: Een teksteditor is een programma waarin je gewone tekst en code schrijft, zoals HTML-, CSS- en PHP-bestanden. In deze les gebruik je Visual Studio Code (VS Code). _(bron: 1. Introduction.pptx, dia 7)_
- `RPM-pakket (.rpm)` — **Installatiebestand voor Fedora**: Een .rpm-bestand is een softwarepakket voor Linux-distributies zoals Fedora. Je installeert het met sudo dnf install gevolgd door de naam van het bestand. _(bron: 1. Introduction.pptx, dia 14)_
- `Scripttaal` — **Taal voor geautomatiseerde instructies**: Een scripttaal is een programmeertaal waarmee je de computer een reeks geschreven instructies automatisch laat uitvoeren, in plaats van het werk met de hand te doen. PHP is zo'n scripttaal: je gebruikt het om data te verwerken of om dynamische webpagina's te maken. _(bron: 4. Fundamentals of PHP.pptx, dia 3)_
- `Voorwaarde (conditional)` — **Beslissing nemen in code**: Met een voorwaarde (conditional) laat je code een beslissing nemen: het programma controleert of iets waar (true) of onwaar (false) is en voert op basis daarvan andere code uit. Bijvoorbeeld: ALS het getal even is, DAN toon "even", ANDERS toon "oneven". _(bron: 4. Fundamentals of PHP.pptx, dia 50)_

### Terminal & shell
- `Terminal` — **Het venster waarin je commando's typt**: Een programma dat een tekstvenster toont waarin je commando's intypt en de uitvoer leest. De terminal zelf voert niets uit: hij geeft wat je typt door aan de shell.
- `Shell` — **Het programma dat je commando's uitvoert**: Leest wat je in de terminal typt, begrijpt het en start de juiste programma's. Het is de 'tolk' tussen jou en het besturingssysteem. Er bestaan verschillende shells: bash, zsh, fish …
- `Bash` — **De meest gebruikte shell op Linux**: Bourne Again SHell: de standaardshell op de meeste Linux-systemen. Naast losse commando's kan je in bash ook scripts schrijven met variabelen, lussen en voorwaarden.
- `Prompt (in de terminal)` — **Het tekstje dat wacht op je commando**: De tekst voor je cursor, bv. guest@fedora:~$. Die toont wie je bent (guest), op welke computer (fedora), in welke map (~ = thuismap) en eindigt op $ (gewone gebruiker) of # (root). Je typt je commando erachter.
- `Prompt (bij AI)` — **Een opdracht of vraag aan een AI**: Bij AI-programma's zoals Claude is een prompt de tekst die je intypt om iets te vragen. Dat is iets anders dan de prompt in de terminal, al lijken beide op 'de plek waar je iets typt'.
- `Commando` — **Een opdracht die je in de shell typt**: Een instructie voor de computer, meestal de naam van een programma gevolgd door opties en argumenten. Bv. in 'ls -l documenten' is ls het commando.
- `Optie (flag)` — **Past aan hoe een commando werkt**: Begint met - of --, bv. -l of --all. Opties veranderen het gedrag: ls toont namen, ls -l toont ook details. Korte opties mag je combineren: -la is hetzelfde als -l -a.
- `Argument` — **Waarop het commando werkt**: De extra informatie na een commando, zoals een bestandsnaam of map. In 'cp a.txt b.txt' zijn a.txt en b.txt de argumenten.
- `Manpage` — **De ingebouwde handleiding**: Elke gebruikelijke Linux-opdracht heeft een handleiding die je opent met man, bv. man ls. Blader met de pijltjes, zoek met /, sluit af met q. Veel commando's tonen ook korte hulp met --help.
- `Tab-aanvulling` — **Laat de terminal namen afmaken**: Druk op Tab terwijl je een commando of bestandsnaam typt: de shell vult de rest aan. Twee keer Tab toont alle mogelijkheden. Scheelt typwerk en typfouten.
- `GUI en CLI` — **Grafische vs. tekstinterface**: Een GUI (graphical user interface, bv. GNOME) bedien je met muis, vensters en iconen: eerst kies je het object, dan de actie. Een CLI (command line interface, de terminal) bedien je met getypte commando's: eerst de actie, dan het object (bv. rm bestand). _(bron: Chapter 2 - The terminal.pptx, dia 4)_
- `Virtuele console` — **Pure terminal zonder grafische omgeving**: Een virtuele console is een volledig scherm met enkel een tekstterminal, zonder GUI. Je opent er een met Ctrl + Alt + F3 tot F6 en keert terug naar de grafische omgeving met Ctrl + Alt + F2. _(bron: Chapter 2 - The terminal.pptx, dia 7)_
- `Ingebouwd commando (shell built-in)` — **Commando dat deel is van Bash**: Sommige commando's, zoals cd, pwd en exit, zijn geen apart programma maar zitten ingebouwd in de shell Bash zelf. Ze werken dus zodra een terminal met Bash opstart. _(bron: Chapter 2 - The terminal.pptx, dia 18)_
- `Exitstatus` — **Getal na afloop van commando**: Als een commando klaar is, geeft het een getal terug aan de shell: de exitstatus. 0 betekent dat alles goed ging; een ander getal (bv. 1 of 2) wijst op een fout. De man page legt de betekenis uit onder EXIT STATUS. _(bron: Chapter 2 - The terminal.pptx, dia 29)_
- `Configuratiebestand` — **Bestand met instellingen**: Een tekstbestand met instellingen die een programma of de shell bij het opstarten inleest. Shellconfiguratiebestanden zijn eigenlijk scripts met shellcommando's, bv. ~/.bashrc (voor jezelf) en /etc/profile (voor het hele systeem). _(bron: Chapter 6 - The work environment.pptx, dia 6)_
- `Soorten shellvariabelen` — **Omgevings-, gewone en systeemvariabelen**: Linux kent 3 soorten: omgevingsvariabelen (beheerd door de shell en doorgegeven aan elke nieuwe shell, bv. $PATH), gewone variabelen (door jezelf gemaakt, enkel in je huidige shell tot je ze exporteert) en systeemvariabelen (van het systeem, bv. $OSTYPE). _(bron: Chapter 6 - The work environment.pptx, dia 10)_
- `Subshell` — **Shell gestart binnen een shell**: Een nieuwe shell die je vanuit je huidige shell start, bv. door bash te typen. Ze erft enkel geëxporteerde variabelen. Met exit keer je terug naar de vorige shell. _(bron: Chapter 6 - The work environment.pptx, dia 13)_
- `Alias` — **Korte bijnaam voor een commando**: Een alias is een korte, eigen naam voor een (lang) commando dat je vaak gebruikt, bv. ll voor ls -l. Zet je hem in ~/.bashrc, dan blijft hij bewaard. _(bron: Chapter 6 - The work environment.pptx, dia 21)_

### Web
- `HTML` — **De structuur van een webpagina**: HyperText Markup Language: beschrijft wat er op een pagina staat (titels, tekst, afbeeldingen, links) met tags zoals <h1> en <p>. HTML is geen programmeertaal: het rekent niets uit.
- `CSS` — **De opmaak van een webpagina**: Cascading Style Sheets: bepaalt hoe HTML eruitziet, zoals kleuren, lettertypes, marges en indeling. Bv. p { color: blue; } maakt alle alinea's blauw.
- `JavaScript` — **Interactie op een webpagina**: Een programmeertaal die in de browser draait en pagina's laat reageren, bv. op een klik. HTML = structuur, CSS = opmaak, JavaScript = gedrag.
- `PHP` — **Code die op de server draait**: Een programmeertaal die op de webserver wordt uitgevoerd en HTML maakt voor die naar de browser gaat, bv. om gegevens uit een databank te tonen. De bezoeker ziet enkel het resultaat, niet de PHP-code.
- `Tag, element en attribuut` — **De bouwstenen van HTML**: Een tag staat tussen < >, bv. <a>. Een element is de openingstag, de inhoud en de sluittag samen: <a>tekst</a>. Een attribuut geeft extra info in de openingstag: <a href="pagina.html">.
- `Browser` — **Programma dat webpagina's toont**: Chrome, Firefox, Edge … lezen HTML, CSS en JavaScript en maken er een zichtbare pagina van. Met F12 open je de ontwikkelaarstools om de code van een pagina te bekijken.
- `Statische en dynamische webpagina` — **Vaste versus veranderende webpagina**: Een statische webpagina toont altijd dezelfde inhoud en is gemaakt met HTML (en CSS voor de opmaak). Een dynamische webpagina kan haar inhoud aanpassen, bv. met PHP op de server. _(bron: 1. Introduction.pptx, dia 4)_
- `Self-closing tag` — **Tag zonder sluitingstag of inhoud**: De meeste tags hebben een openings- en sluitingstag met inhoud ertussen. Self-closing tags zoals <br>, <hr> en <img> bestaan uit één tag en bevatten geen inhoud. _(bron: 2. Introduction to HTML.pptx, dia 7)_
- `Block-level en inline elementen` — **Twee soorten elementen in body**: Een block-level element (bv. <h1>, <p>, <div>) begint op een nieuwe regel en laat niets naast zich op dezelfde regel. Een inline element (bv. <a>, <span>, <code>) laat andere inhoud op dezelfde regel staan. _(bron: 2. Introduction to HTML.pptx, dia 18)_
- `Monospaced lettertype` — **Letters allemaal even breed**: In een monospaced lettertype neemt elk teken evenveel ruimte in, zodat tekst netjes uitlijnt. Ideaal voor DNA- of eiwitsequenties; <pre> en <code> gebruiken zo'n lettertype. _(bron: 2. Introduction to HTML.pptx, dia 23)_
- `Witruimte in HTML` — **Extra spaties worden één spatie**: De browser toont meerdere spaties, tabs en regeleinden in HTML-code als één spatie. Wil je een nieuwe regel, gebruik dan <br>; wil je alle witruimte behouden, gebruik <pre>. _(bron: 2. Introduction to HTML.pptx, dia 24)_
- `Beeldverhouding (aspect ratio)` — **Verhouding breedte en hoogte**: De verhouding tussen de breedte en hoogte van een afbeelding. Pas je beide los van elkaar aan, dan kan de afbeelding vervormen; stel daarom best enkel de breedte of enkel de hoogte in. _(bron: 2. Introduction to HTML.pptx, dia 39)_
- `CSS-regel en declaratie` — **Onderdelen van CSS-code**: Een declaratie is een eigenschap met een waarde (bv. color: red;). De eigenschap zegt wat je verandert, de waarde hoe. Een CSS-regel is een selector plus een declaratieblok { … } met één of meer declaraties. _(bron: 3. Introduction to CSS.pptx, dia 4)_
- `Inline, interne en externe CSS` — **Drie manieren van CSS toepassen**: Inline CSS staat in het style-attribuut van één element. Interne CSS staat in een <style>-tag in de <head> en geldt voor die ene pagina. Externe CSS staat in een apart .css-bestand dat je met <link> aan meerdere pagina's koppelt. _(bron: 3. Introduction to CSS.pptx, dia 5)_
- `Selector (CSS)` — **Patroon dat elementen kiest**: Een selector is het deel van een CSS-regel dat aangeeft op welke HTML-elementen de stijl van toepassing is, bv. op tagnaam (p), id (#naam) of klasse (.naam). _(bron: 3. Introduction to CSS.pptx, dia 13)_
- `Ouder, kind en sibling (elementenboom)` — **Familierelaties tussen HTML-elementen**: HTML-elementen zitten in elkaar zoals een stamboom. Een element binnen een ander is een kind (direct kind als er niets tussen zit); het buitenste is de ouder of voorouder. Elementen met dezelfde ouder zijn siblings (broers/zussen). Combinator-selectors gebruiken deze relaties. _(bron: 3. Introduction to CSS.pptx, dia 25)_
- `Pseudo-klasse` — **Selectie op positie of toestand**: Een pseudo-klasse is een sleutelwoord met een dubbelepunt achter een selector (bv. :hover, :first-child). Zo geef je een stijl op basis van de positie van een element tussen zijn siblings of van zijn toestand, zoals wanneer de muis erover staat. _(bron: 3. Introduction to CSS.pptx, dia 31)_
- `Shorthand-eigenschap` — **Meerdere eigenschappen tegelijk instellen**: Een shorthand-eigenschap stelt in één keer meerdere CSS-eigenschappen in. border zet bijvoorbeeld border-width, border-style en border-color; padding zet padding-top, -right, -bottom en -left. _(bron: 3. Introduction to CSS.pptx, dia 46)_
- `CSS-eenheden (px, %, em, vw, vh)` — **Eenheden voor maten in CSS**: px is een vaste maat in pixels. % is relatief t.o.v. het ouder-element, em t.o.v. de lettergrootte (1em = huidige lettergrootte). vw en vh zijn een percentage van de breedte en hoogte van het browservenster (de viewport). _(bron: 3. Introduction to CSS.pptx, dia 49)_
- `Box model` — **Lagen rond elk element**: Een element bestaat van binnen naar buiten uit inhoud, padding, rand (border) en marge (margin). Standaard geldt width/height alleen voor de inhoud, zodat padding en rand de totale grootte groter maken. Je ziet het box model via rechtsklik > Inspecteren in de browser. _(bron: 3. Introduction to CSS.pptx, dia 54)_
- `Ontwikkelaarstools (Inspecteren)` — **HTML en CSS bekijken in browser**: Via rechtsklik op een element en 'Inspecteren' open je de ontwikkelaarstools van de browser. Daar zie je de HTML, de toegepaste CSS en het box model van het element. _(bron: 3. Introduction to CSS.pptx, dia 54)_
- `Blok- en inline-element` — **Twee soorten HTML-elementen**: Een blokelement (block-level, bv. <div>, <p>) begint op een nieuwe regel, laat niets naast zich toe en kan een breedte en hoogte krijgen. Een inline-element (bv. <span>, <a>) staat op dezelfde regel als andere elementen en negeert width en height (uitzondering: <img>). _(bron: 3. Introduction to CSS.pptx, dia 71)_
- `Dynamische webpagina` — **Pagina die de server aanmaakt**: Een webpagina waarvan de inhoud door code op de server (bv. PHP) wordt gemaakt, bijvoorbeeld op basis van wat de gebruiker invult. De browser kan PHP niet zelf lezen: de PHP-server voert de code uit en stuurt gewone HTML en CSS naar de browser. _(bron: 5. Dynamic Web Pages.pptx, dia 3)_
- `GET en POST` — **Twee manieren om formulierdata te versturen**: Met GET komen de ingevulde gegevens zichtbaar in de URL; alleen geschikt voor niet-gevoelige data. Met POST worden de gegevens in de body van het verzoek meegestuurd: veiliger en geschikt voor grotere hoeveelheden, wachtwoorden en bestanden. _(bron: 5. Dynamic Web Pages.pptx, dia 13)_

## Linux (375)

### Archieven & compressie
- `tar -xvf archief.tar` — **Archief uitpakken**: Haalt alle bestanden uit een tar-archief en zet ze in de huidige map. _(bron: Chapter 6 - The work environment.pptx, dia 24)_
- `tar -cvf archief.tar map` — **Archief maken van een map**: Maakt één archiefbestand met alle bestanden uit de map, bv. tar -cvf /var/tmp/archive.tar /home/guest. tar comprimeert niet: het archief is dus niet kleiner. Het minteken voor de opties mag je vaak weglaten. _(bron: Chapter 6 - The work environment.pptx, dia 25)_
- `tar -tf archief.tar | grep bestand` — **Zoeken in inhoud van archief**: tar -t toont de inhoud van een archief zonder het uit te pakken. Met | grep controleer je of een bepaald bestand erin zit. _(bron: Chapter 6 - The work environment.pptx, dia 26)_
- `gzip bestand` — **Bestand comprimeren met gzip**: Comprimeert een bestand tot bestand.gz zodat het minder ruimte inneemt. Let op: het originele bestand wordt verwijderd. _(bron: Chapter 6 - The work environment.pptx, dia 27)_
- `bzip2 bestand` — **Bestand comprimeren met bzip2**: Alternatieve compressiemethode; maakt bestand.bz2. Ook hier wordt het originele bestand verwijderd. _(bron: Chapter 6 - The work environment.pptx, dia 27)_
- `zcat / zless / zgrep` — **Gzip-bestand lezen zonder uitpakken**: Werken zoals cat, less en grep, maar dan rechtstreeks op .gz-bestanden, zonder ze eerst te decomprimeren. Bv. zgrep Desktop file.gz. _(bron: Chapter 6 - The work environment.pptx, dia 28)_
- `bzcat / bzless / bzgrep` — **Bzip2-bestand lezen zonder uitpakken**: Zoals cat, less en grep, maar voor .bz2-bestanden. _(bron: Chapter 6 - The work environment.pptx, dia 28)_
- `zipgrep patroon bestand.zip` — **Zoeken in zip-bestand**: Zoekt zoals grep in de bestanden binnen een .zip-bestand, zonder het uit te pakken. (De dia noemt ook zipless voor .zip-bestanden.) _(bron: Chapter 6 - The work environment.pptx, dia 28)_
- `gunzip bestand.gz` — **gzip-bestand decomprimeren**: Zet een .gz-bestand terug om naar het originele bestand. Het gecomprimeerde bestand wordt daarbij verwijderd. _(bron: Chapter 6 - The work environment.pptx, dia 29)_
- `bunzip2 bestand.bz2` — **bzip2-bestand decomprimeren**: Zet een .bz2-bestand terug om naar het originele bestand. Het gecomprimeerde bestand wordt verwijderd. _(bron: Chapter 6 - The work environment.pptx, dia 29)_
- `tar -czvf archief.tar.gz map` — **Gecomprimeerd archief maken**: Maakt in één stap een archief én comprimeert het met gzip (optie -z). Zo krijg je een .tar.gz-bestand. _(bron: Chapter 6 - The work environment.pptx, dia 30)_
- `tar -xzvf bestand.tar.gz` — **Gecomprimeerd archief uitpakken**: Pakt een .tar.gz-archief in één stap uit en decomprimeert het. Wordt bv. gebruikt voor broncode van software. _(bron: Chapter 6 - The work environment.pptx, dia 36)_

### Bestanden & mappen
- `mkdir -p data/ruw` — **Maak mappen aan**: Maakt de map 'data' en daarin 'ruw' aan in één keer. Bestaan ze al, dan krijg je geen foutmelding.
- `touch [option(s)] file(s)` — **Leeg bestand aanmaken**: Maakt snel een nieuw, leeg tekstbestand aan (0 kB). Bestaat het bestand al, dan wordt enkel de datum van laatste wijziging aangepast. _(bron: Chapter 3 - Organizing files.pptx, dia 13)_
    - voorbeeld: `touch [option(s)] file(s)`
- `cp ./source file ./destination file` — **Bestand kopiëren**: Maakt een exacte kopie van een bestand. Let op: bestaat het doelbestand al, dan wordt het zonder waarschuwing overschreven! Zonder pad werkt cp in de huidige map. _(bron: Chapter 3 - Organizing files.pptx, dia 14)_
    - voorbeeld: `cp ./source file ./destination file`
- `cp file3 ~/Downloads` — **Kopiëren naar map, zelfde naam**: Geef je als doel enkel een map (zonder bestandsnaam), dan krijgt de kopie dezelfde naam als het origineel. _(bron: Chapter 3 - Organizing files.pptx, dia 15)_
- `cp file{1,2} ~/Downloads` — **Meerdere bestanden tegelijk kopiëren**: Kopieert file1 en file2 samen naar ~/Downloads. Bij meerdere bronbestanden moet het laatste argument een map zijn. De accolades worden uitgebreid tot file1 file2. _(bron: Chapter 3 - Organizing files.pptx, dia 16)_
- `mv file3 P00687.fasta` — **Bestand hernoemen**: mv verplaatst en/of hernoemt bestanden. Blijft het bestand in dezelfde map, dan krijgt het gewoon een nieuwe naam. _(bron: Chapter 3 - Organizing files.pptx, dia 17)_
- `mv ~/Documents/P00687.fasta .` — **Bestand naar huidige map verplaatsen**: Verplaatst het bestand uit ~/Documents naar de map waarin je nu bent (.). _(bron: Chapter 3 - Organizing files.pptx, dia 17)_
- `rm file(s)` — **Bestanden verwijderen**: Verwijdert één of meer bestanden. Let op: er is geen prullenbak, het bestand is echt weg. _(bron: Chapter 3 - Organizing files.pptx, dia 18)_
- `rm ~/Documents/file? ~/Downloads/file?` — **Bestanden met jokerteken verwijderen**: Verwijdert in ~/Documents en ~/Downloads alle bestanden met 'file' + precies één teken, zoals file1, file2 en file3. _(bron: Chapter 3 - Organizing files.pptx, dia 18)_
- `ln target linkname` — **Hardlink maken**: Maakt een hardlink: een tweede naam (linkname) voor dezelfde data als target. _(bron: Chapter 3 - Organizing files.pptx, dia 27)_
- `ln -s file1 link_to_file1` — **Symbolische link maken**: Maakt een symbolische link link_to_file1 die naar file1 wijst. Met ls -l zie je de link als link_to_file1 -> file1. _(bron: Chapter 3 - Organizing files.pptx, dia 27)_
- `basename /home/guest/file.txt` — **Bestandsnaam uit pad halen**: Haalt uit een volledig pad enkel de bestandsnaam. _(bron: Chapter 3 - Organizing files.pptx, dia 29)_
    - voorbeeld: `basename /home/guest/file.txt` → file.txt
- `dirname /home/guest/file.txt` — **Mappad uit pad halen**: Haalt uit een volledig pad enkel de map waarin het bestand staat. _(bron: Chapter 3 - Organizing files.pptx, dia 29)_
    - voorbeeld: `dirname /home/guest/file.txt` → /home/guest
- `mkdir directory(ies)` — **Nieuwe map aanmaken**: Maakt één of meer nieuwe mappen; relatieve en absolute paden kunnen. Bv. mkdir folder1 folder2. _(bron: Chapter 3 - Organizing files.pptx, dia 30)_
- `rmdir directory(ies)` — **Lege map verwijderen**: Verwijdert één of meer mappen, maar enkel als ze leeg zijn. Bv. rmdir folder* verwijdert alle lege mappen die met folder beginnen. _(bron: Chapter 3 - Organizing files.pptx, dia 30)_

### Bestanden bekijken
- `head -n 20 sequentie.fasta` — **Toon de eerste 20 regels**: Toont de eerste 20 regels van een FASTA-bestand, handig om snel te zien hoe het bestand eruitziet zonder alles te openen.
- `echo "thx mate :)"` — **Print tekst op het scherm**: Schrijft de tekst tussen aanhalingstekens gewoon terug naar het scherm. De aanhalingstekens zorgen dat spaties en tekens zoals :) als één stuk tekst gezien worden.
- `ls -a` — **Ook verborgen bestanden tonen**: Toont alle bestanden, ook de verborgen bestanden (namen die met een punt beginnen, zoals .bashrc, en ook . en ..). _(bron: Chapter 2 - The terminal.pptx, dia 9)_
- `ls -al` — **Opties -a en -l combineren**: Toont alle bestanden (ook verborgen) als lange lijst met eigenschappen. Opties met één letter mag je combineren: ls -a -l, ls -al en ls -la doen hetzelfde. _(bron: Chapter 2 - The terminal.pptx, dia 9)_
- `ls /etc` — **Inhoud van een andere map tonen**: Toont de inhoud van de map /etc zonder dat je er naartoe gaat. Het argument /etc is het pad waarop het commando werkt; /etc bevat de configuratiebestanden. _(bron: Chapter 2 - The terminal.pptx, dia 11)_
- `ls -F` — **Bestandstype met teken aanduiden**: Zet achter elke naam een teken dat het bestandstype toont: / map, * uitvoerbaar bestand, @ link, = socket, | named pipe. Gewone bestanden krijgen geen teken. _(bron: Chapter 2 - The terminal.pptx, dia 12)_
- `ls -l` — **Lijst met eigenschappen tonen**: Toont de inhoud als lange lijst met eigenschappen: bestandstype en rechten, aantal hardlinks, eigenaar, groep, grootte, datum en naam. Het eerste teken toont het type: - gewoon bestand, d map, l link, s socket, p named pipe, b block device, c character device. _(bron: Chapter 2 - The terminal.pptx, dia 14)_
- `wc` — **Regels, woorden en tekens tellen**: wc (word count) telt in een bestand het aantal regels, woorden en bytes (tekens), in die volgorde. Algemene vorm: wc [opties] [bestanden]. _(bron: Chapter 2 - The terminal.pptx, dia 16)_
    - voorbeeld: `wc` → 20 166 924 file.txt
- `wc -l` — **Aantal regels tellen**: Toont enkel het aantal regels van een bestand. _(bron: Chapter 2 - The terminal.pptx, dia 16)_
- `wc -w` — **Aantal woorden tellen**: Toont enkel het aantal woorden van een bestand. Combineren kan: wc -lw of wc -wl toont regels en woorden. _(bron: Chapter 2 - The terminal.pptx, dia 16)_
- `tree -FL 1 /` — **Mappenstructuur als boom tonen**: Toont de inhoud van de root / als boomstructuur, hier maar 1 niveau diep, met een teken achter elke naam volgens het type. _(bron: Chapter 3 - Organizing files.pptx, dia 10)_
    - voorbeeld: `tree -FL 1 /` → 20 directories, 0 files
- `ls -alF` — **Alles tonen met details en type**: Combineert drie opties: alle bestanden (ook verborgen), als lange lijst, met een teken achter de naam volgens het type. _(bron: Chapter 3 - Organizing files.pptx, dia 13)_
- `file [file(s)]` — **Bestandstype achterhalen**: Toont wat voor soort bestand iets is (bv. map, tekst, PNG-afbeelding, programma), soms met extra info zoals de grootte. Handig omdat Linux geen extensies nodig heeft. _(bron: Chapter 3 - Organizing files.pptx, dia 19)_
    - voorbeeld: `file [file(s)]`
- `cat file(s)` — **Inhoud van tekstbestand tonen**: Toont de volledige inhoud van één of meer tekstbestanden in de terminal, bv. cat /etc/fedora-release. _(bron: Chapter 3 - Organizing files.pptx, dia 20)_
- `less file(s)` — **Bestand pagina per pagina lezen**: Toont de inhoud van een bestand scherm per scherm, zodat je door lange bestanden kan bladeren. Stop met q. _(bron: Chapter 3 - Organizing files.pptx, dia 20)_
- `nl file(s)` — **Inhoud met regelnummers tonen**: Toont de inhoud van een tekstbestand met een regelnummer vóór elke regel. _(bron: Chapter 3 - Organizing files.pptx, dia 20)_
- `head file` — **Eerste 10 regels tonen**: Toont de eerste 10 regels van een bestand, bv. head /usr/share/doc/zip/WHATSNEW. Meer opties vind je met man head. _(bron: Chapter 3 - Organizing files.pptx, dia 21)_
- `tail file` — **Laatste 10 regels tonen**: Toont de laatste 10 regels van een bestand. Handig voor logbestanden zoals /var/log/boot.log, waar nieuwe info onderaan komt. _(bron: Chapter 3 - Organizing files.pptx, dia 22)_
- `tail -f file` — **Einde van bestand live volgen**: Toont de laatste regels en blijft nieuwe regels tonen zodra ze toegevoegd worden (live). Stop met Ctrl + C. _(bron: Chapter 3 - Organizing files.pptx, dia 22)_
- `strings file` — **Leesbare tekst uit binair bestand**: Toont enkel de leesbare tekens uit een bestand. Nuttig bij binaire bestanden (programma's) zoals /usr/bin/who, waar cat vooral onleesbare tekens toont. _(bron: Chapter 3 - Organizing files.pptx, dia 23)_
- `ls -i` — **Inodenummers tonen**: Toont vóór elke bestandsnaam het inodenummer. Bestanden met hetzelfde inodenummer zijn hardlinks naar dezelfde data. _(bron: Chapter 3 - Organizing files.pptx, dia 26)_
- `stat object` — **Gedetailleerde bestandsinfo tonen**: Toont alle details van een bestand of map: grootte, inodenummer, aantal links, rechten, eigenaar en datums. _(bron: Chapter 3 - Organizing files.pptx, dia 26)_
- `/zoekterm (in man)` — **Zoeken in een manpage**: In een manpage (bv. man man) typ je / gevolgd door een zoekterm en Enter om ernaar te zoeken, bv. /exit status. Met n spring je naar de volgende treffer. _(bron: Chapter 4 - Processes.pptx, dia 20)_
- `wc bestand` — **Regels, woorden en tekens tellen**: Telt het aantal regels, woorden en tekens in een bestand. De les gebruikt het als voorbeeld: de invoer is de tekst in het bestand, de uitvoer zijn de getallen. _(bron: Chapter 5 - Input and output.pptx, dia 4)_
- `v (in less)` — **Bestand openen in editor**: Terwijl je een bestand bekijkt met less, open je het met v in de standaard teksteditor (ingesteld via $VISUAL of $EDITOR). _(bron: Chapter 6 - The work environment.pptx, dia 5)_
- `cat -n /etc/profile` — **Bestand tonen met regelnummers**: Toont de inhoud van /etc/profile met een regelnummer voor elke regel. _(bron: Chapter 6 - The work environment.pptx, dia 8)_
- `head -n 5 snp151*` — **Eerste 5 regels van bestanden**: Toont de eerste 5 regels van elk bestand waarvan de naam met snp151 begint. Bij meerdere bestanden zet head telkens de bestandsnaam erboven. Handig om snel te zien hoe een tabel eruitziet. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 8)_
    - voorbeeld: `head -n 5 snp151*` → ==> snp151annotation.txt <==
name class valid func alleles alleleFreqs
rs745593600 insertion by-cluster,by-frequency,by-1000genomes unknown -,A,AAC, 0.979633,0.001997,0.018371
==> snp151position.txt <
- `head -n 1 snp151annotation.txt > HEADER` — **Kopregel apart bewaren**: Schrijft enkel de eerste regel (de kopregel) naar het bestand HEADER. sort sorteert de kopregel anders gewoon mee; daarom haal je hem eerst apart. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 17)_
- `tail -n +2 snp151annotation.txt > DATA` — **Alles behalve de kopregel**: Toont alle regels vanaf regel 2, dus de tabel zonder kopregel, en bewaart ze in DATA. Na het sorteren zet je kopregel en data terug samen met bv. cat HEADER DATA_gesorteerd > nieuw_bestand. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 17)_
- `ll` — **Inhoud van map uitgebreid tonen**: Toont de inhoud van de huidige map in lange vorm (rechten, eigenaar, grootte, datum). Op Fedora is ll een snelkoppeling (alias) voor ls -l. _(bron: 1. Introduction.pptx, dia 13)_
    - voorbeeld: `ll` → [guest@fedora Downloads]$ ll
total 133388
-rw-r--r--. 1 guest guest 136586090 Aug 30 10:17

### Doorsturen (redirect)
- `ls -l > ile.txt` — **Bewaar maplijst in een bestand**: Maakt een gedetailleerde lijst van de huidige map en schrijft die niet naar het scherm maar in het bestand ile.txt. Bestaat ile.txt al, dan wordt het overschreven.

### Hulp & documentatie
- `ls --version` — **Versie van ls tonen**: Toont welke versie van het programma ls geïnstalleerd is. Opties met twee streepjes zijn voluit geschreven, leesbare opties. _(bron: Chapter 2 - The terminal.pptx, dia 10)_
- `ls --help` — **Korte gebruiksuitleg van commando**: Toont hoe je het commando gebruikt en welke opties er zijn. --help werkt bij bijna elk commando, bv. wc --help. _(bron: Chapter 2 - The terminal.pptx, dia 10)_
- `man commando` — **Handleiding van commando openen**: Opent de man page (handleiding) van een commando met naam, syntax (SYNOPSIS), beschrijving, opties en voorbeelden. Bv. man ls, of man man voor uitleg over man zelf. _(bron: Chapter 2 - The terminal.pptx, dia 25)_
- `h / q / f / b / /woord` — **Navigeren in een man page**: Toetsen binnen een man page: h toont alle navigatietoetsen, q sluit de man page, f gaat één pagina vooruit, b één pagina terug. Met /woord zoek je een woord in de tekst. _(bron: Chapter 2 - The terminal.pptx, dia 26)_
- `info commando` — **Uitgebreide hulpdocumentatie openen**: Opent de info-documentatie van een commando, vaak uitgebreider dan de man page. Bv. info ls of info info. Is info niet beschikbaar, gebruik dan man. _(bron: Chapter 2 - The terminal.pptx, dia 31)_
- `whatis ls` — **Korte omschrijving van commando**: Toont één regel uitleg over een commando, overgenomen uit de man page (met het sectienummer tussen haakjes). _(bron: Chapter 2 - The terminal.pptx, dia 32)_
    - voorbeeld: `whatis ls` → ls (1) - list directory contents
- `apropos browser` — **Commando zoeken op trefwoord**: Zoekt in de korte omschrijvingen van alle man pages naar een woord. Handig als je niet weet welk commando je nodig hebt. _(bron: Chapter 2 - The terminal.pptx, dia 32)_
    - voorbeeld: `apropos browser` → firefox (1) - a Web browser for X11 derived from the Mozilla br...
git-web--browse (1) - Git helper script to launch a web browser
- `ls /usr/share/doc` — **Documentatie van programma's bekijken**: Toont de map /usr/share/doc, waarin geïnstalleerde programma's (bv. gedit) extra documentatie bewaren. _(bron: Chapter 2 - The terminal.pptx, dia 33)_

### In- en uitvoer
- `ls -l > file.txt` — **Uitvoer naar bestand schrijven**: Het teken > stuurt de uitvoer van een commando naar een bestand in plaats van naar het scherm. Bestaat het bestand al, dan wordt de inhoud overschreven. _(bron: Chapter 2 - The terminal.pptx, dia 16)_
- `ls -l >> file.txt` — **Uitvoer aan bestand toevoegen**: Het teken >> voegt de uitvoer van een commando toe aan het einde van een bestand, zonder de bestaande inhoud te wissen. _(bron: Chapter 2 - The terminal.pptx, dia 16)_
- `echo` — **Tekst op het scherm tonen**: Toont (herhaalt) de tekst die je erachter typt. Handig om iets te testen of om de waarde van een variabele te bekijken. _(bron: Chapter 2 - The terminal.pptx, dia 21)_
    - voorbeeld: `echo` → thx mate :)
- `commando > bestand` — **Uitvoer naar bestand schrijven**: Schrijft de uitvoer van een commando naar een bestand in plaats van naar het scherm. Bestaat het bestand niet, dan wordt het gemaakt; bestaat het wel, dan wordt het overschreven. _(bron: Chapter 5 - Input and output.pptx, dia 7)_
    - voorbeeld: `commando > bestand` → [guest@fedora ~]$ date > date.txt
[guest@fedora ~]$ cat date.txt
Thu 30 Sep 14:43:08 CEST 2021
- `cat bestand1 bestand2 > nieuwbestand` — **Bestanden samenvoegen in één bestand**: cat toont de bestanden na elkaar; met > wordt die samengevoegde inhoud in een nieuw bestand bewaard. Voorbeeld: cat date.txt my_home_today.txt > my_home_20210930. _(bron: Chapter 5 - Input and output.pptx, dia 7)_
- `set -o noclobber` — **Overschrijven met > verbieden**: Zet de shelloptie noclobber aan: > geeft dan een foutmelding in plaats van een bestaand bestand te overschrijven. Standaard staat ze uit. Terug uitzetten met set +o noclobber. _(bron: Chapter 5 - Input and output.pptx, dia 8)_
- `> bestand` — **Bestand leegmaken**: Zonder commando ervoor maakt > een bestaand bestand leeg (truncating): de inhoud verdwijnt, het bestand blijft bestaan met grootte 0. _(bron: Chapter 5 - Input and output.pptx, dia 9)_
    - voorbeeld: `> bestand` → -rw-rw-r--. 1 guest guest 1153 Sep 30 14:44 my_home_20210930
[guest@fedora ~]$ > my_home_20210930
-rw-rw-r--. 1 guest guest 0 Sep 30 14:48 my_home_20210930
- `commando >> bestand` — **Uitvoer achteraan bestand toevoegen**: Voegt de uitvoer van een commando toe aan het einde van een bestand, zonder de bestaande inhoud te overschrijven. Bestaat het bestand niet, dan wordt het gemaakt. _(bron: Chapter 5 - Input and output.pptx, dia 10)_
- `date > date_`date +%y%m%d`` — **Bestandsnaam met datum van vandaag**: De backticks voeren eerst date +%y%m%d uit (bv. 210930); die uitvoer wordt in de bestandsnaam geplakt. Zo krijg je een bestand zoals date_210930. Daarna kan je met ls -l >> date_`date +%y%m%d` iets toevoegen. _(bron: Chapter 5 - Input and output.pptx, dia 10)_
- `commando < bestand` — **Bestand als invoer gebruiken**: Gebruikt een bestand als invoer (stdin) voor een commando, in plaats van het toetsenbord. Vaak samen met grep, bv. grep pts/0 < processen.txt om enkel de regels met pts/0 te tonen. _(bron: Chapter 5 - Input and output.pptx, dia 12)_
- `commando 2> bestand` — **Enkel foutmeldingen naar bestand**: Stuurt alleen de foutmeldingen (stderr, nummer 2) naar een bestand; de gewone uitvoer blijft op het scherm. Bv. grep guest /etc/* 2> error. _(bron: Chapter 5 - Input and output.pptx, dia 14)_
- `commando > bestand 2>&1` — **Uitvoer én fouten naar bestand**: Stuurt zowel de gewone uitvoer als de foutmeldingen naar hetzelfde bestand. Zet 2>&1 achteraan. Handig bij geplande taken (cron) om fouten in een logbestand te bewaren, bv. */5 * * * * touch /var/tmp/test > /var/tmp/cron.log 2>&1. _(bron: Chapter 5 - Input and output.pptx, dia 16)_
- `commando1 | commando2` — **Uitvoer doorgeven aan volgend commando**: De pipe | geeft de uitvoer van het eerste commando als invoer aan het tweede. Vaak gebruikt om met grep in de uitvoer van ps of ls te zoeken, bv. ps -ef | grep firefox. _(bron: Chapter 5 - Input and output.pptx, dia 18)_
- `ls -l /etc | grep cron | grep -v crontab` — **Meerdere pipes na elkaar**: Je kan meerdere pipes koppelen. Hier: toon de inhoud van /etc, houd enkel regels met 'cron' en laat daarvan de regels met 'crontab' weg. _(bron: Chapter 5 - Input and output.pptx, dia 19)_
- `who | sort | awk '{print $1}'` — **Gesorteerde lijst van gebruikersnamen**: Toont wie aangemeld is, sorteert die lijst en drukt met awk enkel de eerste kolom (de gebruikersnaam) af. _(bron: Chapter 5 - Input and output.pptx, dia 19)_
- `commando | tee bestand` — **Uitvoer tonen én bewaren**: tee kopieert de uitvoer: je ziet ze in de terminal én ze wordt in een bestand geschreven. Met > of >> kan dat niet, want dan zie je niets op het scherm. Met tee -a voeg je toe in plaats van te overschrijven (zoals >>). _(bron: Chapter 5 - Input and output.pptx, dia 20)_
    - voorbeeld: `commando | tee bestand` → [guest@fedora ~]$ who | tee file
guest tty2 2021-09-30 13:44 (tty2)
root tty3 2021-09-30 16:23
- `cat files_to_remove.txt | xargs rm` — **Regels omzetten tot argumenten**: xargs leest regels tekst van de invoer en geeft ze als argumenten aan een commando. Hier worden alle bestandsnamen uit files_to_remove.txt aan rm gegeven, dus al die bestanden worden verwijderd. _(bron: Chapter 5 - Input and output.pptx, dia 21)_
- `echo wc -l myfile | bash` — **Tekst als commando laten uitvoeren**: echo maakt de tekst 'wc -l myfile'; via de pipe krijgt bash die tekst en voert hem uit als commando. Zo kan je commando's als tekst opbouwen en daarna uitvoeren. _(bron: Chapter 5 - Input and output.pptx, dia 22)_
- `echo [argumenten]` — **Tekst op het scherm tonen**: Drukt de argumenten af op de standaarduitvoer. Handig in scripts om iets te vragen vóór read of om waarden te tonen. Opties: -n (geen nieuwe regel op het einde), -e (escapetekens zoals \n of \a interpreteren). _(bron: Chapter 5 - Input and output.pptx, dia 24)_
    - voorbeeld: `echo [argumenten]` → [guest@fedora ~]$ echo Enter your name
Enter your name
- `printf "FORMAT" [ARGUMENTEN]` — **Opgemaakte tekst afdrukken**: Uitgebreide echo: drukt tekst af volgens een opmaakstring. Plaatshouders zoals %s (tekst) en %d (geheel getal) worden vervangen door de argumenten. \n zet een nieuwe regel. Bv. printf "A %s team counts %d players.\n" soccer 11 geeft: A soccer team counts 11 players. _(bron: Chapter 5 - Input and output.pptx, dia 25)_
- `clear` — **Terminalscherm leegmaken**: Maakt het terminalvenster leeg zodat je met een proper scherm verder werkt. _(bron: Chapter 5 - Input and output.pptx, dia 26)_
- `echo "Hello world!"` — **Tekst op het scherm tonen**: Toont de tekst op het scherm (stdout). In een script gebruik je echo om uitvoer of berichten te geven. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 5)_
    - voorbeeld: `echo "Hello world!"` → Hello world!
- `read TEXT` — **Invoer van gebruiker vragen**: Wacht tot de gebruiker tekst typt en op Enter drukt, en bewaart die tekst in de variabele TEXT. Zo vraag je in een script interactief een waarde op. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 10)_
- `seq 1 100` — **Reeks getallen maken**: Toont de getallen van 1 tot en met 100, elk op een aparte regel. Handig in een for-lus: for i in $(seq 1 100). _(bron: Chapter 9 - Shell scripting - student.pptx, dia 32)_

### Jokertekens (wildcards)
- `ls [!MV]*` — **Toon alles behalve wat met M of V begint**: Toont alle bestanden en mappen waarvan de naam NIET met een hoofdletter M of V begint (dus zonder Music en Videos). Omdat het ook mappen zijn, toont ls van elke map de inhoud eronder.
- `wc ?ile.txt` — **Tel in bestanden die op 'ile.txt' eindigen**: Telt regels, woorden en bytes van elk bestand waarvan de naam bestaat uit precies één willekeurig teken + 'ile.txt'. Bij jou vond het file.txt (20 regels, 166 woorden, 924 bytes). ile.txt zelf valt erbuiten, want ? moet precies één teken zijn.
- `wc *ile.txt` — **Tel in alle bestanden op 'ile.txt'**: Telt regels, woorden en bytes van elk bestand dat eindigt op 'ile.txt', met om het even wat (ook niets) ervoor. Daarom vond het zowel file.txt als ile.txt, plus een totaalregel.
- `*` — **Nul of meer willekeurige tekens**: Het jokerteken * staat voor nul of meer willekeurige tekens. Bash vervangt het eerst door alle passende namen en geeft pas daarna het commando door: ls D* wordt ls Desktop Documents Downloads. _(bron: Chapter 2 - The terminal.pptx, dia 20)_
    - voorbeeld: `*` → 20 166 924 file.txt
11 92 522 ile.txt
31 258 1446 total
- `?` — **Precies één willekeurig teken**: Het jokerteken ? staat voor precies één willekeurig teken. wc ?ile.txt past op file.txt, maar niet op ile.txt (daar staat geen teken voor 'ile'). _(bron: Chapter 2 - The terminal.pptx, dia 21)_
    - voorbeeld: `?` → 20 166 924 file.txt
- `[set]` — **Eén teken uit een reeks**: Staat voor precies één teken dat in de reeks tussen de haakjes staat. ls [VM]* toont alles dat met V of M begint (Videos, Music); ls [A-Z]* alles dat met een hoofdletter begint. _(bron: Chapter 2 - The terminal.pptx, dia 21)_
- `[!set]` — **Eén teken níet uit reeks**: Staat voor precies één teken dat NIET in de reeks staat; [^set] doet hetzelfde. ls [!MV]* toont alles behalve wat met M of V begint. _(bron: Chapter 2 - The terminal.pptx, dia 21)_
- `echo curly bra{cket,ce}s` — **Accolades uitbreiden tot meerdere woorden**: Bash breidt een uitdrukking met accolades uit tot meerdere argumenten: elk stuk tussen { } gescheiden door komma's geeft een apart woord. Zo maak je snel meerdere gelijkaardige namen. _(bron: Chapter 2 - The terminal.pptx, dia 22)_
    - voorbeeld: `echo curly bra{cket,ce}s` → curly brackets braces
- `echo curly bra\*` — **Speciaal teken letterlijk gebruiken**: Een backslash \ vóór een speciaal teken zorgt dat Bash het niet interpreteert (escapen). Zo wordt * niet als jokerteken gebruikt maar gewoon als sterretje getoond. _(bron: Chapter 2 - The terminal.pptx, dia 22)_
    - voorbeeld: `echo curly bra\*` → Desk*

### Navigatie
- `ls -la` — **Toon alle bestanden in detail**: Toont alle bestanden in de huidige map, ook verborgen bestanden, met rechten, eigenaar, grootte en datum.
- `cd ~/projecten` — **Ga naar de map projecten**: Wisselt naar de map 'projecten' in je thuismap. ~ is een afkorting voor je thuismap.
- `ls` — **Toon inhoud van de map**: Toont de bestanden en mappen in de map waarin je nu staat. Mappen verschijnen meestal in het blauw.
- `cd` — **Terug naar je thuismap**: cd zonder map erachter brengt je altijd terug naar je thuismap (~). Je zag de prompt veranderen van ~/Documents naar ~.
- `pwd` — **Huidige map tonen**: Toont het volledige (absolute) pad van de map waarin je nu werkt (present working directory). pwd is ingebouwd in Bash. _(bron: Chapter 2 - The terminal.pptx, dia 15)_
- `.` — **Huidige map**: Een punt staat voor de map waarin je nu bent. Je gebruikt het in relatieve paden, bv. scp ... . om iets naar de huidige map te kopiëren. _(bron: Chapter 2 - The terminal.pptx, dia 15)_
- `..` — **Bovenliggende map**: Twee punten staan voor de map één niveau hoger (parent directory). ../.. is twee niveaus hoger, bv. ls ../.. toont de inhoud van de map twee niveaus hoger. _(bron: Chapter 2 - The terminal.pptx, dia 15)_
- `cd /usr/share/vim` — **Naar map via absoluut pad**: Gaat naar de map /usr/share/vim. Omdat het pad met / begint, is het een absoluut pad: het vertrekt vanaf de root, waar je ook bent. _(bron: Chapter 3 - Organizing files.pptx, dia 7)_
- `cd vim91` — **Naar submap via relatief pad**: Gaat naar de map vim91 die in de huidige map staat. Dit is een relatief pad: het hangt af van waar je nu bent. _(bron: Chapter 3 - Organizing files.pptx, dia 7)_
- `cd ../../systemd` — **Twee niveaus hoger, dan submap**: Gaat twee mappen omhoog (../..) en daar naar de map systemd. Vanuit /usr/share/vim/vim91 kom je zo in /usr/share/systemd. _(bron: Chapter 3 - Organizing files.pptx, dia 7)_
- `cd /` — **Naar de root-map gaan**: Gaat naar de root /, het beginpunt van het hele bestandssysteem. _(bron: Chapter 3 - Organizing files.pptx, dia 7)_
- `cd ~user` — **Naar thuismap van andere gebruiker**: Gaat naar de thuismap van een bepaalde gebruiker; de shell vervangt ~user door bv. /home/user. _(bron: Chapter 3 - Organizing files.pptx, dia 8)_
- `cd Downloads` — **Naar de map Downloads gaan**: Verandert je huidige map naar de map Downloads in je thuismap. Zo kan je daarna met het gedownloade installatiebestand werken. _(bron: 1. Introduction.pptx, dia 12)_

### Netwerk & op afstand
- `ssh [user@]hostname` — **Verbinden met een externe server**: Maakt een beveiligde verbinding (Secure Shell) met een andere Linux-computer, zodat je die via de terminal kan bedienen. Sluit de verbinding met exit of Ctrl + D. _(bron: Chapter 2 - The terminal.pptx, dia 35)_
- `ssh guest@172.19.8.101` — **Inloggen op Howest BIT-server**: Logt in als gebruiker guest op de server met IP-adres 172.19.8.101. Daarna geef je je wachtwoord in. _(bron: Chapter 2 - The terminal.pptx, dia 36)_
- `scp [source] [destination]` — **Bestand kopiëren over SSH**: Kopieert bestanden tussen je eigen computer en een server via SSH (Secure Copy Protocol). Eerst geef je aan welk bestand (bron), dan waar het naartoe moet (doel). _(bron: Chapter 2 - The terminal.pptx, dia 37)_
- `scp /path/to/file username@IP:/path/to/destination` — **Bestand naar server kopiëren**: Kopieert een bestand van je eigen computer naar een map op de server. _(bron: Chapter 2 - The terminal.pptx, dia 38)_
- `scp username@IP:/path/to/file /path/to/destination` — **Bestand van server kopiëren**: Kopieert een bestand van de server naar een map op je eigen computer. Als doel mag je ook . gebruiken (de huidige map). _(bron: Chapter 2 - The terminal.pptx, dia 38)_
- `scp guest@172.19.8.101:/home/guest/welcome.txt .` — **welcome.txt van server ophalen**: Kopieert het bestand welcome.txt van de Howest BIT-server naar de huidige map op je eigen computer. Je moet eerst het wachtwoord ingeven. _(bron: Chapter 2 - The terminal.pptx, dia 39)_
    - voorbeeld: `scp guest@172.19.8.101:/home/guest/welcome.txt .` → guest@172.19.8.101's password:
welcome.txt 100% 75 6.7KB/s 00:00
- `wget www.uniprot.org/uniprot/P00687.fasta` — **Bestand downloaden van internet**: Downloadt een bestand van een webadres naar de huidige map, hier een FASTA-sequentie van UniProt. _(bron: Chapter 3 - Organizing files.pptx, dia 14)_
- `wget URL` — **Bestand downloaden van internet**: Downloadt het bestand op het opgegeven webadres naar de huidige map. In de les gebruik je dit om het Miniconda-installatiescript te downloaden. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 11)_
- `curl localhost:80` — **Webpagina opvragen in terminal**: Vraagt de webpagina op poort 80 van je eigen computer (localhost) op en toont de inhoud in de terminal. Zo test je of een webserver bereikbaar is. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 32)_
- `efetch -db protein -id NP_000509 -format fasta` — **Sequentie ophalen uit NCBI**: Commando uit het conda-pakket entrez-direct (EDirect). Het downloadt de eiwitsequentie met identifier NP_000509 uit de NCBI-databank in FASTA-formaat. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 42)_

### Omgeving & variabelen
- `date` — **Huidige datum en tijd tonen**: Toont de huidige datum en tijd van het systeem. _(bron: Chapter 2 - The terminal.pptx, dia 21)_
- `$HOME` — **Variabele met pad naar thuismap**: De variabele HOME bevat het pad naar je thuismap (bv. /home/guest). Je bekijkt ze met echo $HOME. _(bron: Chapter 3 - Organizing files.pptx, dia 8)_
- `echo $VARIABLE` — **Inhoud van variabele tonen**: Toont de waarde van een variabele. Zet een $ voor de naam. _(bron: Chapter 3 - Organizing files.pptx, dia 38)_
- `echo $PATH` — **Zoekpad voor programma's tonen**: Toont de mappen waarin de shell programma's zoekt, gescheiden door een dubbelpunt ':'. Programma's in die mappen kan je vanuit elke map starten. _(bron: Chapter 3 - Organizing files.pptx, dia 38)_
- `set -o` — **Status van shellopties tonen**: Toont alle shellopties en of ze aan (on) of uit (off) staan, bv. om te controleren of noclobber actief is. _(bron: Chapter 5 - Input and output.pptx, dia 8)_
- `EDITOR=`which gedit`; VISUAL=`which gedit`; export EDITOR VISUAL` — **gedit als standaardeditor instellen**: Stelt gedit in als standaard teksteditor, bv. voor crontab -e of v in less. which gedit geeft het volledige pad van gedit, dat in EDITOR en VISUAL komt; export maakt ze beschikbaar voor andere programma's. Zet dit in ~/.bashrc om het blijvend te maken. _(bron: Chapter 6 - The work environment.pptx, dia 5)_
- `~/.bashrc` — **Persoonlijk configuratiebestand van bash**: Verborgen bestand in je thuismap dat bash inleest bij elke nieuwe shell. Hier zet je je eigen aliassen, functies en export-regels zodat ze blijvend zijn. Ook ~/.bash_profile is zo'n persoonlijk bestand. _(bron: Chapter 6 - The work environment.pptx, dia 7)_
- `source .bashrc` — **Configuratie opnieuw inlezen**: Leest .bashrc opnieuw in in je huidige shell, zodat nieuwe instellingen (bv. een alias) meteen werken zonder een nieuwe shell te openen. _(bron: Chapter 6 - The work environment.pptx, dia 7)_
- `/etc/profile` — **Systeembrede configuratie van de shell**: Het eerste bestand dat de shell bij het aanmelden leest; bevat instellingen en omgevingsvariabelen voor alle gebruikers. Ook de bestanden in /etc/profile.d/ horen daarbij. Bekijken met cat -n /etc/profile. _(bron: Chapter 6 - The work environment.pptx, dia 8)_
- `echo $VARIABELE` — **Inhoud van variabele tonen**: Toont de waarde van een variabele. Bij het opvragen zet je een $ voor de naam, bv. echo $PATH of echo $OSTYPE. _(bron: Chapter 6 - The work environment.pptx, dia 11)_
- `printenv` — **Alle omgevingsvariabelen tonen**: Toont een lijst van alle omgevingsvariabelen met hun waarde, bv. HOME en USERNAME. Een gewone variabele die je niet geëxporteerd hebt, staat er niet bij. _(bron: Chapter 6 - The work environment.pptx, dia 11)_
- `export VARIABELE` — **Variabele doorgeven aan andere programma's**: Maakt van een variabele een omgevingsvariabele, zodat ook subshells en andere programma's ze kennen. Zonder export ben je ze kwijt in een nieuwe shell. Blijvend maken? Zet de export in ~/.bashrc. _(bron: Chapter 6 - The work environment.pptx, dia 12)_
    - voorbeeld: `export VARIABELE` → [guest@fedora ~]$ UNAME=guest
[guest@fedora ~]$ bash
[guest@fedora ~]$ echo $UNAME

[guest@fedora ~]$ exit
[guest@fedora ~]$ export UNAME
- `VARIABELE=waarde` — **Variabele een waarde geven**: Maakt een variabele en geeft ze een waarde. Geen $ en geen spaties rond het =-teken. De naam mag niet met een cijfer beginnen. Zonder export bestaat ze enkel in je huidige shell. _(bron: Chapter 6 - The work environment.pptx, dia 13)_
- `bash` — **Subshell starten**: Start een nieuwe bash-shell binnen je huidige shell (een subshell). Handig om te testen welke variabelen of aliassen doorgegeven worden. Terugkeren doe je met exit. _(bron: Chapter 6 - The work environment.pptx, dia 13)_
- `export PATH=$PATH:/home/guest/Scripts` — **Scriptsmap toevoegen aan PATH**: Voegt de map Scripts achteraan toe aan PATH, zodat je scripts in die map overal kan starten door enkel hun naam te typen. $PATH behoudt de bestaande mappen; : scheidt de mappen. _(bron: Chapter 6 - The work environment.pptx, dia 14)_
- `unset VARIABELE` — **Variabele verwijderen**: Verwijdert een variabele volledig, bv. unset PINGU. Daarna is ze leeg bij echo en verdwijnt ze uit printenv. _(bron: Chapter 6 - The work environment.pptx, dia 15)_
- `set` — **Alle shellvariabelen tonen**: Toont alle variabelen van de shell: omgevingsvariabelen, systeemvariabelen én variabelen die enkel in deze shell bestaan (bv. HISTFILE, OSTYPE). Die laatste zie je niet met printenv. _(bron: Chapter 6 - The work environment.pptx, dia 16)_
- `$HISTFILE` — **Bestand met commandogeschiedenis**: Pad naar het bestand waarin je commandogeschiedenis bewaard wordt (meestal ~/.bash_history). Deze variabele zie je met set, niet met printenv. Bekijken met echo $HISTFILE. _(bron: Chapter 6 - The work environment.pptx, dia 16)_
- `set -o optie / set +o optie` — **Shelloptie aan- of uitzetten**: set -o zet een shelloptie aan, set +o zet ze uit. Bv. set -o noclobber voorkomt dat > bestaande bestanden overschrijft. _(bron: Chapter 6 - The work environment.pptx, dia 17)_
- `$EDITOR / $VISUAL` — **Standaard teksteditor**: Bepalen welke editor programma's openen, bv. bij crontab -e. Bekijken met echo $EDITOR. _(bron: Chapter 6 - The work environment.pptx, dia 19)_
- `$HISTSIZE` — **Aantal bewaarde commando's**: Hoeveel commando's de shell in de geschiedenis (history) bewaart. Bekijken met echo $HISTSIZE. _(bron: Chapter 6 - The work environment.pptx, dia 19)_
- `$HOSTNAME` — **Naam van de computer**: Naam van de machine waarop je werkt. Bekijken met echo $HOSTNAME. _(bron: Chapter 6 - The work environment.pptx, dia 19)_
- `$USERNAME` — **Je gebruikersnaam**: Bevat de naam van de aangemelde gebruiker. Bekijken met echo $USERNAME. _(bron: Chapter 6 - The work environment.pptx, dia 19)_
- `$LANG` — **Voorkeurstaal**: Taal- en landinstelling van het systeem, bv. en_US.UTF-8. Bekijken met echo $LANG. _(bron: Chapter 6 - The work environment.pptx, dia 19)_
- `$DISPLAY` — **Scherm van grafische omgeving**: Wordt door de grafische omgeving gebruikt om te weten op welk scherm vensters getoond worden. Bekijken met echo $DISPLAY. _(bron: Chapter 6 - The work environment.pptx, dia 19)_
- `$MAIL` — **Map met binnenkomende mail**: Locatie waar binnenkomende mail van de gebruiker bewaard wordt. Bekijken met echo $MAIL. _(bron: Chapter 6 - The work environment.pptx, dia 19)_
- `$PATH` — **Mappen waar commando's gezocht worden**: Lijst van mappen, gescheiden door :, waarin de shell zoekt naar het programma dat je typt. Niet zomaar overschrijven; wel iets toevoegen. Bekijken met echo $PATH. _(bron: Chapter 6 - The work environment.pptx, dia 20)_
- `$PS1 / $PS2` — **Opmaak van de prompt**: PS1 is de gewone prompt (bv. [guest@fedora ~]$); PS2 is de tweede prompt die verschijnt als een commando over meerdere regels loopt. Aanpassen geeft een persoonlijke prompt. Bekijken met echo $PS1. _(bron: Chapter 6 - The work environment.pptx, dia 20)_
- `$PWD` — **Naam huidige map**: Bevat het pad van de map waarin je nu werkt. Bekijken met echo $PWD. _(bron: Chapter 6 - The work environment.pptx, dia 20)_
- `$SHELL` — **Pad van de huidige shell**: Bevat naam en pad van je shell, bv. /bin/bash. Bekijken met echo $SHELL. _(bron: Chapter 6 - The work environment.pptx, dia 20)_
- `$OSTYPE` — **Type besturingssysteem**: Systeemvariabele met informatie over het besturingssysteem, bv. linux-gnu. Bekijken met echo $OSTYPE. _(bron: Chapter 6 - The work environment.pptx, dia 20)_
- `$UID` — **Nummer van de gebruiker**: Identificatienummer (user ID) van de gebruiker; root heeft 0. Bekijken met echo $UID. _(bron: Chapter 6 - The work environment.pptx, dia 20)_
- `$TERM` — **Type terminal**: Welk type terminal je gebruikt, bv. xterm-256color. Bekijken met echo $TERM. _(bron: Chapter 6 - The work environment.pptx, dia 20)_
- `alias naam='commando -opties'` — **Korte naam voor commando maken**: Maakt een alias: een korte naam voor een commando dat je vaak gebruikt, bv. alias la='ls -a'. Zonder argumenten toont alias alle aliassen. Een alias in de terminal verdwijnt als je de shell sluit; zet hem in ~/.bashrc om hem te bewaren. _(bron: Chapter 6 - The work environment.pptx, dia 21)_
- `alias nb='nano ~/.bashrc'` — **Alias om .bashrc te bewerken**: Voorbeeld van een handige alias: nb opent je .bashrc in de editor nano. Een tweede alias sb='source ~/.bashrc' leest het bestand daarna opnieuw in. _(bron: Chapter 6 - The work environment.pptx, dia 23)_
- `alias nohead="awk 'NR > 1 && NR <= 11'"` — **Alias: head zonder kopregel**: Maakt een alias nohead die 10 regels van een bestand toont zoals head, maar de eerste regel (kopregel) overslaat. Gebruik: nohead bestand. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 37)_
- `export PATH=$PATH:directory` — **Map toevoegen aan PATH**: Voegt een map toe aan de lijst waarin de shell naar programma's zoekt. Daarna kun je scripts in die map van overal uitvoeren zonder ./. Zet deze regel in ~/.bashrc of ~/.bash_profile om hem blijvend te maken. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 7)_
- `ANSWER=yes` — **Variabele aanmaken**: Maakt de variabele ANSWER met waarde yes in de huidige shell. Er mogen geen spaties rond het = staan. Hoofdletters zijn niet verplicht. In een subshell (bv. na het commando bash) bestaat deze variabele niet. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 8)_
- `echo $ANSWER` — **Waarde van variabele tonen**: Toont de waarde van de variabele ANSWER. Het $-teken vóór de naam haalt de inhoud van de variabele op. Met Tab kun je variabelenamen aanvullen ($ANS + Tab). _(bron: Chapter 9 - Shell scripting - student.pptx, dia 8)_
- `export ANSWER=yes` — **Variabele doorgeven aan subshells**: Maakt de variabele en exporteert ze, zodat ze ook bekend is in subshells en scripts die je vanuit deze shell start. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 9)_
- `date +%A` — **Dag van de week tonen**: Toont de naam van de huidige dag van de week (bv. Monday). Met +% bepaal je hoe date de datum weergeeft. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 14)_

### Pakketten & software
- `sudo dnf install info` — **Programma info installeren**: Installeert het programma info met de pakketbeheerder dnf van Fedora, als het nog niet op je systeem staat. _(bron: Chapter 2 - The terminal.pptx, dia 31)_
- `sudo dnf install xterm` — **Het programma xterm installeren**: Installeert xterm, een eenvoudige terminal die heel weinig geheugen gebruikt (minder dan 1 MB RAM). Je moet je wachtwoord ingeven omdat installeren beheerdersrechten vraagt. _(bron: Chapter 4 - Processes.pptx, dia 11)_
- `sudo dnf install pakket` — **Software installeren met dnf**: Installeert een programma met dnf, de pakketbeheerder voor RPM-pakketten (Fedora). Je kan een pakketnaam geven of een gedownload .rpm-bestand. sudo is nodig omdat je als beheerder installeert. _(bron: Chapter 6 - The work environment.pptx, dia 33)_
- `dnf list` — **Beschikbare pakketten oplijsten**: Toont alle beschikbare (en geïnstalleerde) programma's/pakketten. _(bron: Chapter 6 - The work environment.pptx, dia 33)_
- `dnf search patroon` — **Pakket zoeken**: Zoekt pakketten waarvan naam of beschrijving het patroon bevat, bv. dnf search perl. _(bron: Chapter 6 - The work environment.pptx, dia 33)_
- `sudo dnf upgrade` — **Alle pakketten bijwerken**: Werkt alle geïnstalleerde pakketten bij naar de nieuwste versie. _(bron: Chapter 6 - The work environment.pptx, dia 33)_
- `which programma` — **Controleren of programma geïnstalleerd is**: Toont het volledige pad van een programma (bv. /usr/bin/gedit). Krijg je niets, dan staat het niet in je PATH of is het niet geïnstalleerd. _(bron: Chapter 6 - The work environment.pptx, dia 35)_
- `ln -s programma /usr/bin/programma` — **Programma beschikbaar maken voor iedereen**: Maakt in /usr/bin een symbolische link (snelkoppeling) naar het programma, zodat elke gebruiker het kan starten door de naam te typen. Geef als eerste argument het volledige pad naar het programma; in /usr/bin schrijven vraagt meestal sudo. _(bron: Chapter 6 - The work environment.pptx, dia 35)_
- `./configure` — **Broncode voorbereiden voor compileren**: Eerste stap bij installeren vanaf broncode (na tar -xzvf): het script controleert je systeem en bereidt het compileren voor. Lees eerst het INSTALL- of README-bestand. _(bron: Chapter 6 - The work environment.pptx, dia 36)_
- `make` — **Broncode compileren**: Compileert de broncode tot een uitvoerbaar programma, volgens de instructies in het Makefile. _(bron: Chapter 6 - The work environment.pptx, dia 36)_
- `sudo make install` — **Gecompileerd programma installeren**: Laatste stap: kopieert het gecompileerde programma naar de systeemmappen. Vraagt beheerdersrechten. _(bron: Chapter 6 - The work environment.pptx, dia 36)_
- `git clone URL` — **Broncode van project downloaden**: Downloadt (kloont) de volledige broncode van een project, bv. een bio-informaticatool, naar je computer. Dit is de eerste stap van de klassieke, minst reproduceerbare manier om software te installeren. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 5)_
- `hisat2 --version` — **Versie van een tool tonen**: Toont welke versie van de tool (hier hisat2) geïnstalleerd is. Zo controleer je of de installatie gelukt is en welke versie je gebruikt, belangrijk voor reproduceerbaarheid. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 5)_
- `which seqtk` — **Locatie van een programma zoeken**: Toont in welke map het uitvoerbare bestand seqtk staat. Als je de conda-omgeving deactiveert, vindt which het programma niet meer, omdat het enkel in die omgeving geïnstalleerd is. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 14)_
- `sudo dnf -y install dnf-plugins-core` — **Plugins voor dnf installeren**: Installeert extra plugins voor de pakketbeheerder dnf, waaronder config-manager, nodig om de Docker-repository toe te voegen. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 21)_
- `sudo dnf-3 config-manager --add-repo https://download.docker.com/linux/fedora/docker-ce.repo` — **Docker-repository toevoegen**: Voegt de officiële softwarebron van Docker toe aan dnf, zodat je daarna Docker kunt installeren. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 21)_
- `sudo dnf install docker-ce docker-ce-cli containerd.io` — **Docker Engine installeren**: Installeert de Docker Engine, het docker-commando en containerd. Tijdens de installatie aanvaard je de GPG-sleutel. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 21)_
- `sudo dnf install docker-compose` — **Docker compose installeren**: Installeert Docker compose op Fedora. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 38)_
- `fastqc WT*.fq.gz` — **Kwaliteitscontrole van fastq-bestanden**: Voert een kwaliteitscontrole uit op alle bestanden die met WT beginnen en op .fq.gz eindigen. Per bestand maakt fastqc een html-rapport dat je in je browser opent. Werkt na conda install fastqc of in een container. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 44)_
- `sudo dnf install firefox php` — **Firefox en PHP installeren**: Installeert de webbrowser Firefox en de programmeertaal PHP op Fedora met de pakketbeheerder dnf. Je hebt sudo nodig omdat software installeren beheerdersrechten vraagt. _(bron: 1. Introduction.pptx, dia 8)_
- `sudo dnf install code-1.81.1-1691620770.el7.x86_64.rpm` — **VS Code installeren uit .rpm-bestand**: Installeert Visual Studio Code vanuit een gedownload .rpm-bestand in de huidige map. dnf toont eerst een overzicht en vraagt dan bevestiging: typ y om door te gaan of n om te stoppen. _(bron: 1. Introduction.pptx, dia 14)_
    - voorbeeld: `sudo dnf install code-1.81.1-1691620770.el7.x86_64.rpm` → Install 1 Package
Total size: 130 M
Installed size: 362 M
Is this ok [y/N]:
- `code` — **Visual Studio Code openen**: Start de teksteditor Visual Studio Code vanuit de terminal. Handig om te testen of de installatie gelukt is. _(bron: 1. Introduction.pptx, dia 16)_
- `sudo dnf install pymol` — **Open-source PyMOL installeren (Fedora)**: Installeert de open-source versie van PyMOL op Fedora Linux via de pakketbeheerder dnf. De officiële versie van Schrödinger (pymol.org) vraagt een licentie; studenten kunnen een gratis academische licentie van 1 jaar krijgen. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 16)_
- `pip install --user pyqt5` — **PyQt5 installeren als PyMOL crasht**: Installeert het Python-pakket PyQt5 (grafische bibliotheek) alleen voor jouw gebruiker. Mogelijke oplossing als PyMOL 3.1 op Fedora 42 crasht. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 16)_
- `python -m pip install --upgrade pip` — **pip zelf bijwerken (Windows)**: Werkt pip, de pakketbeheerder van Python, bij naar de nieuwste versie. Eerste stap bij het installeren van PyMOL 3.1 op Windows. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 16)_
- `pip install pmw` — **Pmw installeren voor PyMOL (Windows)**: Installeert het Python-pakket Pmw (Python megawidgets), dat PyMOL nodig heeft voor zijn grafische vensters. Tweede stap bij het installeren van PyMOL 3.1 op Windows. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 16)_

### Processen
- `xterm` — **Lichte terminal openen**: Opent een nieuw, eenvoudig terminalvenster. Zonder & bezet het je huidige terminal tot je het sluit; met xterm & blijft je terminal bruikbaar. _(bron: Chapter 4 - Processes.pptx, dia 11)_
- `commando &` — **Commando op de achtergrond starten**: Met een & achter een commando start je het op de achtergrond, zodat je terminal vrij blijft. De shell toont het jobnummer tussen haakjes en de PID. _(bron: Chapter 4 - Processes.pptx, dia 12)_
    - voorbeeld: `commando &` → [guest@fedora ~]$ xterm &
[1] 9167
- `jobs` — **Jobs in huidige shell tonen**: Toont de jobs die in je huidige shell draaien of gepauzeerd zijn, met hun jobnummer en status. Dat jobnummer gebruik je bij fg, bg en kill. _(bron: Chapter 4 - Processes.pptx, dia 13)_
    - voorbeeld: `jobs` → [1]- Running xterm &
[2]+ Running firefox &
- `bg %nr` — **Gepauzeerde job op achtergrond hervatten**: Laat een job die je met Ctrl + Z gepauzeerd hebt verder lopen op de achtergrond. Het jobnummer vind je met jobs. _(bron: Chapter 4 - Processes.pptx, dia 13)_
- `fg %nr` — **Job naar de voorgrond halen**: Haalt een achtergrondjob (of gepauzeerde job) terug naar de voorgrond, zodat hij de terminal weer gebruikt. _(bron: Chapter 4 - Processes.pptx, dia 13)_
- `kill %nr` — **Achtergrondjob stoppen**: Stopt een job via zijn jobnummer; het is als Ctrl + C, maar dan voor een job op de achtergrond. In plaats van %nr kan je ook de PID gebruiken. _(bron: Chapter 4 - Processes.pptx, dia 13)_
- `ps` — **Je lopende processen tonen**: Toont informatie over de processen die je in je huidige terminal draait. Kolommen: PID (procesnummer), TTY (terminal, pts = pseudo-terminal), TIME (gebruikte processortijd) en CMD (commandonaam). ps heeft meer dan 80 opties. _(bron: Chapter 4 - Processes.pptx, dia 14)_
- `w` — **Aangemelde gebruikers en hun activiteit**: Toont wie aangemeld is en wat ze doen. De eerste lijn is dezelfde als uptime. Kolommen: USER en TTY (wie, waar), LOGIN@ en IDLE (sinds wanneer, hoe lang niets gedaan), JCPU en PCPU (processortijd), WHAT (huidig proces). _(bron: Chapter 4 - Processes.pptx, dia 15)_
    - voorbeeld: `w` → 16:35:20 up 7:10, 2 users, load average: 0.00, 0.02, 0.03
USER TTY LOGIN@ IDLE JCPU PCPU WHAT
guest pts/1 16:29 5:54 0.03s 0.03s bash
- `top` — **Processen live bekijken**: Toont een live overzicht van het systeem, ook batchprocessen. Bovenaan staan de processen die het meeste processortijd gebruiken; het scherm ververst om de paar seconden. Je ziet ook Tasks (aantal processen), Cpu(s) (belasting), Mem (geheugen) en Swap. Stoppen met q. _(bron: Chapter 4 - Processes.pptx, dia 16)_
    - voorbeeld: `top` → top - 16:53:03 up 7:27, 2 users, load average: 0.07, 0.03, 0.00
Tasks: 241 total, 1 running, 240 sleeping, 0 stopped, 0 zombie
- `uptime` — **Hoe lang systeem draait en belasting**: Toont de huidige tijd, hoe lang het systeem al aanstaat, het aantal aangemelde gebruikers en de gemiddelde belasting (load average) van de laatste 1, 5 en 15 minuten. Dit is ook de eerste lijn van w en top. _(bron: Chapter 4 - Processes.pptx, dia 18)_
- `htop` — **Interactieve procesviewer**: Een interactieve, overzichtelijkere variant van top. Bovenaan zie je per processor/kern een balk met de belasting. Bij 1 kern betekent load 1 = 100 %, bij 4 kernen load 4 = 100 %. _(bron: Chapter 4 - Processes.pptx, dia 19)_
- `echo $?` — **Exitstatus van vorig commando tonen**: Toont de exitstatus van het laatst uitgevoerde commando. 0 betekent: normaal beëindigd. Bij grep: 0 = gevonden, 1 = niet gevonden, 2 = fout (bv. bestand bestaat niet of onbekende optie). _(bron: Chapter 4 - Processes.pptx, dia 21)_
    - voorbeeld: `echo $?` → [guest@fedora ~]$ grep jasper /etc/jasper
grep: /etc/jasper: No such file or directory
[guest@fedora ~]$ echo $?
2
- `ps -ef` — **Alle processen met details tonen**: Toont alle processen van het hele systeem in volledige vorm, met o.a. gebruiker, PID en PID van het ouderproces. Handig om de PID van een proces op te zoeken, bv. om het te stoppen. _(bron: Chapter 4 - Processes.pptx, dia 22)_
- `kill [-signaal] PID` — **Proces stoppen via PID**: Stuurt een signaal naar het proces met die PID. Zonder signaal wordt SIGTERM (15) gestuurd: het proces stopt netjes. De PID zoek je op met ps -ef. _(bron: Chapter 4 - Processes.pptx, dia 22)_
- `kill -9 PID` — **Proces geforceerd stoppen**: Stuurt SIGKILL (9): het proces wordt meteen gestopt en kan dit signaal niet negeren. Gebruik dit pas als een gewone kill (SIGTERM) niet werkt. _(bron: Chapter 4 - Processes.pptx, dia 22)_
- `kill -l` — **Alle signalen oplijsten**: Toont de lijst van alle signalen die je met kill kan sturen, met hun nummer. _(bron: Chapter 4 - Processes.pptx, dia 22)_
- `xkill` — **Grafisch programma sluiten**: Na dit commando verandert je muiswijzer; klik op een venster om dat grafische programma te beëindigen. _(bron: Chapter 4 - Processes.pptx, dia 22)_
- `timeout [opties] seconden commando` — **Tijdslimiet instellen voor commando**: Voert een commando uit, maar stopt het automatisch na het opgegeven aantal seconden. Voorbeeld: timeout 5 sleep 60 stopt sleep al na 5 seconden. _(bron: Chapter 4 - Processes.pptx, dia 24)_
- `time commando` — **Uitvoeringstijd van commando meten**: Werkt als een chronometer: voert het commando uit en toont daarna hoe lang het duurde. Handig om lange processen te meten, bv. time find /usr. _(bron: Chapter 4 - Processes.pptx, dia 25)_
- `nice [-n niveau] [commando]` — **Commando starten met andere prioriteit**: Start een commando met een aangepaste prioriteit (nice-waarde) van -20 (hoogste) tot +19 (laagste). Zonder nice is de waarde 0; met nice zonder -n wordt het 10. Een negatieve waarde vraagt rootrechten. _(bron: Chapter 4 - Processes.pptx, dia 26)_
- `renice [-n] prioriteit IDs` — **Prioriteit van lopend proces aanpassen**: Verandert de prioriteit van een proces dat al draait. Je geeft de nieuwe nice-waarde en de PID('s). Met -u gebruiker pas je alle processen van die gebruiker aan, bv. renice +1 987 -u root. _(bron: Chapter 4 - Processes.pptx, dia 26)_
- `r (in top)` — **Prioriteit wijzigen binnen top**: In top druk je r om de prioriteit van een proces te veranderen. Je geeft de PID in + Enter, en daarna de nieuwe nice-waarde (-20 tot 19) + Enter. _(bron: Chapter 4 - Processes.pptx, dia 27)_
- `sleep seconden` — **Een tijd wachten**: sleep doet niets anders dan wachten, standaard in seconden. Handig om een commando later te laten starten. _(bron: Chapter 4 - Processes.pptx, dia 29)_
- `(sleep 10; echo -e "\a Time for a break!") &` — **Herinnering na 10 seconden**: Wacht op de achtergrond 10 seconden en toont dan een bericht met een piepgeluid. De haakjes groeperen de twee commando's zodat ze samen op de achtergrond draaien. _(bron: Chapter 4 - Processes.pptx, dia 29)_
    - voorbeeld: `(sleep 10; echo -e "\a Time for a break!") &` → [1] 41699
[guest@fedora ~]$ Time for a break!
- `watch [opties] commando` — **Commando telkens opnieuw uitvoeren**: Voert een commando steeds opnieuw uit, standaard om de 2 seconden, en toont het resultaat schermvullend. Het blijft lopen tot je Ctrl + C drukt. Voorbeeld: watch date. _(bron: Chapter 4 - Processes.pptx, dia 30)_
- `at tijd` — **Taak eenmalig inplannen**: Opent een at>-prompt waar je commando's typt die één keer op het gekozen tijdstip uitgevoerd worden. Sluit de prompt met Ctrl + D. Tijd bv. 19:30 of now + 2 minutes. (Pakket 'at' nodig.) _(bron: Chapter 4 - Processes.pptx, dia 31)_
    - voorbeeld: `at tijd` → [guest@fedora Documents]$ at now + 2 minutes
at> touch /home/guest/Documents/test.txt
at> <EOT>
job 7 at Mon Sep 27 16:14:00 2021
- `atq` — **Geplande at-taken tonen**: Toont de wachtrij (queue) met alle taken die met at gepland zijn, met hun jobnummer en tijdstip. _(bron: Chapter 4 - Processes.pptx, dia 32)_
    - voorbeeld: `atq` → 6 Tue Sep 26 19:30:00 2023 a guest
- `atrm jobnummer` — **Geplande at-taak verwijderen**: Verwijdert een geplande at-taak uit de wachtrij. Het jobnummer vind je met atq, bv. atrm 6. _(bron: Chapter 4 - Processes.pptx, dia 32)_
- `crontab -e` — **Herhalende taken bewerken**: Opent je crontab (lijst van herhalende taken) in een editor (die in $VISUAL of $EDITOR, vaak nano). Elke regel is één taak. Sluit nano met Ctrl + X, bevestig met Y en Enter. Zet een # vooraan een regel om die taak uit te schakelen. (Pakket 'cronie' nodig.) _(bron: Chapter 4 - Processes.pptx, dia 34)_
    - voorbeeld: `crontab -e` → no crontab for guest - using an empty one
crontab: installing new crontab
- `crontab -l` — **Geplande cron-taken tonen**: Toont (list) alle taken in je crontab. _(bron: Chapter 4 - Processes.pptx, dia 36)_
- `min uur dag maand weekdag commando` — **Opbouw van een crontab-regel**: Elke regel in een crontab begint met vijf tijdvelden, gevolgd door het commando. * betekent 'elke', 1-5 is een reeks, 1,3,5 een opsomming. Bv. */5 * * * * touch /var/tmp/test maakt elke 5 minuten een bestand. _(bron: Chapter 4 - Processes.pptx, dia 36)_
- `sudo systemctl start docker` — **Docker Engine starten**: Start de Docker-service (daemon), zodat je containers kunt gebruiken. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 22)_
- `sudo systemctl enable docker` — **Docker automatisch laten opstarten**: Zorgt dat de Docker Engine bij elke herstart van de computer automatisch start. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 23)_

### Rechten & gebruikers
- `chmod +x script.sh` — **Maak script uitvoerbaar**: Geeft een script uitvoerrechten, zodat je het daarna kan starten met ./script.sh.
- `sudo commando` — **Commando uitvoeren als beheerder**: Zet sudo voor een commando om het uit te voeren met rechten van de superuser (root), bv. om software te installeren. Je moet dan je wachtwoord ingeven. _(bron: Chapter 2 - The terminal.pptx, dia 8)_
- `umask` — **Standaardrechten nieuwe bestanden**: Toont het gebruikersmasker: een waarde die afgetrokken wordt van de standaardrechten van nieuwe bestanden en mappen. Zo zijn nieuwe, zelfgemaakte bestanden standaard niet uitvoerbaar, wat helpt tegen virussen. Met umask gevolgd door een getal wijzig je het masker. _(bron: Chapter 3 - Organizing files.pptx, dia 45)_
- `chmod [ugoa][-+=][rwx...] file` — **Rechten wijzigen met letters**: Wijzigt de toegangsrechten van een bestand of map. Je kiest voor wie (u, g, o, a), wat je doet (- afnemen, + geven, = instellen) en welk recht (r, w, x). _(bron: Chapter 3 - Organizing files.pptx, dia 47)_
- `chmod a-x mydir` — **Uitvoerrecht op map afnemen**: Neemt bij iedereen het x-recht af van de map mydir. Daarna kan niemand nog met cd in die map. _(bron: Chapter 3 - Organizing files.pptx, dia 47)_
- `ls -ld mydir` — **Rechten van map zelf tonen**: Toont de eigenschappen (rechten) van de map zelf in plaats van haar inhoud. _(bron: Chapter 3 - Organizing files.pptx, dia 47)_
- `chmod 400 file` — **Bestand beschermen tegen overschrijven**: Enkel de eigenaar mag lezen (r--------). Beschermt tegen per ongeluk overschrijven. _(bron: Chapter 3 - Organizing files.pptx, dia 48)_
- `chmod 500 directory` — **Map beschermen tegen wijzigingen**: Eigenaar mag lezen en binnengaan (r-x), niet schrijven. Zo verwijder, hernoem of verplaats je niet per ongeluk bestanden in die map. _(bron: Chapter 3 - Organizing files.pptx, dia 48)_
- `chmod 600 file` — **Privébestand voor eigenaar**: Enkel de eigenaar mag lezen en schrijven (rw-------); anderen hebben geen toegang. _(bron: Chapter 3 - Organizing files.pptx, dia 48)_
- `chmod 644 file` — **Openbaar leesbaar bestand**: Iedereen mag lezen, maar enkel de eigenaar mag wijzigen (rw-r--r--). _(bron: Chapter 3 - Organizing files.pptx, dia 48)_
- `chmod 660 file` — **Bestand voor eigen groep**: Eigenaar en groep mogen lezen en wijzigen (rw-rw----); anderen hebben geen toegang. _(bron: Chapter 3 - Organizing files.pptx, dia 48)_
- `chmod 700 file` — **Alle rechten enkel voor eigenaar**: Enkel de eigenaar mag lezen, schrijven en uitvoeren (rwx------). _(bron: Chapter 3 - Organizing files.pptx, dia 48)_
- `chmod 755 file` — **Uitvoerbaar voor iedereen**: Iedereen mag lezen en uitvoeren, enkel de eigenaar mag wijzigen (rwxr-xr-x). Typisch voor programma's en scripts. _(bron: Chapter 3 - Organizing files.pptx, dia 48)_
- `chmod 770 file` — **Alle rechten voor groep**: Eigenaar en groep hebben alle rechten (rwxrwx---); anderen niets. Standaard binnen een groep. _(bron: Chapter 3 - Organizing files.pptx, dia 48)_
- `chmod 777 file` — **Alle rechten voor iedereen**: Iedereen mag lezen, schrijven en uitvoeren (rwxrwxrwx). Onveilig, dus zelden gebruiken. _(bron: Chapter 3 - Organizing files.pptx, dia 48)_
- `chown [options] user_spec files` — **Eigenaar van bestand wijzigen**: Stelt in wie de eigenaar is van bestanden of mappen. Meestal heb je daarvoor sudo nodig. _(bron: Chapter 3 - Organizing files.pptx, dia 49)_
- `chgrp [options] group_spec files` — **Groep van bestand wijzigen**: Stelt in tot welke groep bestanden of mappen behoren. _(bron: Chapter 3 - Organizing files.pptx, dia 49)_
- `sudo usermod -aG docker guest` — **Gebruiker aan groep toevoegen**: Voegt gebruiker guest toe aan de groep docker, zodat die docker kan gebruiken zonder sudo. Dit werkt pas na opnieuw inloggen. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 23)_

### Reproduceerbaar werken
- `VBoxManage startvm "rnaseq" --type headless` — **Virtuele machine zonder venster starten**: Start de VirtualBox virtuele machine met de naam rnaseq op de achtergrond, zonder grafisch venster. Daarna kun je met ssh inloggen en de analyse in de VM uitvoeren. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 8)_
- `conda init` — **Conda in de shell activeren**: Stelt je shell zo in dat conda na het opstarten van een nieuwe terminal beschikbaar is. Dit doe je één keer na het installeren van Miniconda. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 11)_
- `conda config --add channels bioconda` — **Kanaal toevoegen aan conda**: Voegt het kanaal bioconda toe aan de lijst waar conda pakketten zoekt. In de les voeg je na elkaar defaults, bioconda en conda-forge toe; het laatst toegevoegde kanaal krijgt de hoogste prioriteit. De volgorde staat in ~/.condarc. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 12)_
- `conda config --set channel_priority strict` — **Strikte kanaalvolgorde instellen**: Zorgt dat conda de volgorde van de kanalen strikt volgt: een pakket wordt uit het kanaal met de hoogste prioriteit gehaald. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 12)_
- `conda create --yes --name env_name` — **Nieuwe conda-omgeving maken**: Maakt een nieuwe, lege conda-omgeving met de opgegeven naam, bv. my_tool. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 13)_
- `conda activate env_name` — **Conda-omgeving activeren**: Activeert de omgeving: vanaf nu gebruik je de tools die in die omgeving geïnstalleerd zijn. De naam van de omgeving verschijnt in je prompt. Met --stack activeer je een omgeving bovenop een andere. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 13)_
- `conda deactivate` — **Conda-omgeving verlaten**: Schakelt de actieve conda-omgeving uit, zodat je terug in de vorige omgeving zit. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 13)_
- `conda env list` — **Alle conda-omgevingen tonen**: Toont een lijst van alle conda-omgevingen op het systeem; de actieve omgeving is gemarkeerd met een *. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 13)_
- `conda install --yes seqtk=1.3` — **Pakket installeren in omgeving**: Installeert het pakket seqtk (een tool om FASTA- of FASTQ-sequenties te verwerken) in versie 1.3 in de actieve omgeving. Zonder =versie krijg je de nieuwste versie. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 14)_
- `conda list` — **Geïnstalleerde pakketten tonen**: Toont alle pakketten in de actieve omgeving, met hun versie en het kanaal waaruit ze komen. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 14)_
- `conda env export > my_tool.yaml` — **Omgeving exporteren naar bestand**: Schrijft een beschrijving van de actieve omgeving (pakketten en versies) naar een yaml-bestand. Zo kun je je omgeving delen, bv. bij een publicatie. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 15)_
- `conda env create -n <env-name> --file <environment.yaml>` — **Omgeving maken uit yaml-bestand**: Maakt op een ander systeem een nieuwe omgeving met exact de pakketten en versies uit het yaml-bestand. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 15)_
- `conda env update --file <environment.yaml>` — **Bestaande omgeving bijwerken**: Installeert de pakketten uit het yaml-bestand in een bestaande omgeving. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 15)_
- `chroot map` — **Programma opsluiten in een map**: Start een shell (of commando) waarbij de opgegeven map als root-map (/) geldt. Het programma kan niet buiten die map, zoals in een gevangenis (jail). Dit is een eenvoudige voorloper van containers; meestal zijn rootrechten nodig. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 17)_
- `sudo docker run hello-world` — **Docker-installatie testen**: Start een container van het testimage hello-world. Als het image nog niet lokaal staat, wordt het eerst gedownload. De boodschap bevestigt dat Docker werkt. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 22)_
    - voorbeeld: `sudo docker run hello-world` → Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
Status: Downloaded newer image for hello-world:latest
Hello from Docker!
This message shows that your install
- `docker pull ubuntu` — **Image downloaden uit registry**: Downloadt het ubuntu-basisimage van Docker Hub naar je computer. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 24)_
- `docker pull biocontainers/fastqc:v0.11.9_cv8` — **Specifieke imageversie downloaden**: Downloadt het fastqc-image van BioContainers in een vaste versie. Het deel na de dubbele punt is de tag (versie); zo gebruik je altijd exact dezelfde tool. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 24)_
- `docker images` — **Lokale images oplijsten**: Toont alle images die lokaal op je computer staan, met hun naam, tag, IMAGE ID, ouderdom en grootte. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 25)_
    - voorbeeld: `docker images` → REPOSITORY TAG IMAGE ID CREATED SIZE
ubuntu latest 597ce1600cf4 7 days ago 72.8MB
biocontainers/fastqc v0.11.9_cv8 7b8f85bb68da 6 months ago 839MB
- `docker rmi -f IMAGE_ID` — **Image verwijderen**: Verwijdert een image van je computer. Met -f forceer je het verwijderen, ook als er nog een (gestopte) container van dat image bestaat. Het IMAGE_ID vind je met docker images. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 25)_
- `docker run ubuntu /bin/ls` — **Commando in container uitvoeren**: Start een container van het ubuntu-image en voert er ls in uit; je ziet de inhoud van de root-map (/) van de container. De uitvoer gaat naar stdout en daarna stopt de container. Dit is een container op de voorgrond. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 26)_
- `docker run --rm --name` — **Container benoemen en opruimen**: Nuttige opties bij docker run: --name geeft de container een eigen naam, zodat je hem later makkelijk kunt aanspreken. --rm verwijdert de container automatisch zodra hij stopt. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 27)_
- `docker run -v /path/in/host/:/path/in/container/` — **Hostmap in container koppelen**: Koppelt (bind mount) een map van je eigen computer aan een map in de container, bv. -v ~/data/:/data. Zo kan de container, die anders volledig afgeschermd is, je bestanden lezen en resultaten wegschrijven. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 27)_
- `docker run --rm -u="$(id -u):$(id -g)" -v ~/fastq/:/data -w="/data" biocontainers/fastqc:v0.11.9_cv8 /bin/bash -c "fastqc WT*.fq.gz"` — **FastQC draaien in een container**: Voert fastqc uit op de fastq-bestanden in ~/fastq met het fastqc-image. De map wordt gekoppeld aan /data en /data is de werkmap; door je eigen gebruikers- en groeps-ID te gebruiken zijn de resultaatbestanden van jou. De html-resultaten open je daarna in je browser. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 28)_
- `docker run --detach ubuntu sleep 100` — **Container op achtergrond starten**: Start de container losgekoppeld (detached) op de achtergrond, als een daemon. Handig voor lange processen; je terminal blijft vrij. Je krijgt enkel het container-ID te zien. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 29)_
- `docker run -it ubuntu /bin/bash` — **Interactief in container werken**: Start een container en opent er een bash-shell in, zodat je zelf commando's in de container kunt typen. Met exit verlaat je de container. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 29)_
- `docker ps` — **Draaiende containers tonen**: Toont de containers die op dit moment draaien, met onder andere hun CONTAINER ID en naam. Met docker ps -a zie je alle containers, ook de gestopte. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 30)_
- `docker stop CONTAINER_ID` — **Draaiende container stoppen**: Stopt een container die draait. Je kunt het container-ID (via docker ps) of de naam gebruiken, bv. docker stop webserver. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 30)_
- `docker exec CONTAINER_ID command` — **Commando in draaiende container**: Voert een nieuw commando uit in een container die al draait, bv. docker exec webserver curl localhost:80. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 30)_
- `docker rm -f CONTAINER_ID` — **Container verwijderen**: Verwijdert een (gestopte) container. Met -f verwijder je ook een container die nog draait. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 31)_
- `docker system prune` — **Alles van Docker opruimen**: Verwijdert in één keer alle gestopte containers, ongebruikte netwerken en ongebruikte (dangling) images en build-cache. Docker vraagt eerst om bevestiging. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 31)_
    - voorbeeld: `docker system prune` → WARNING! This will remove:
- all stopped containers
- all networks not used by at least one container
- all dangling images
- all dangling build cache
Are you sure you want to continue? [y/N]
- `docker run --rm --detach --name webserver nginx` — **Webserver-container starten**: Start een nginx-webserver in een container op de achtergrond met de naam webserver. Omdat de container afgeschermd is, kun je hem van op je eigen systeem niet bereiken; binnen de container wel (docker exec webserver curl localhost:80). _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 32)_
- `docker run --detach --name webserver --publish 80:80 nginx` — **Containerpoort openzetten naar host**: Start de webserver en koppelt poort 80 van je computer aan poort 80 in de container, zodat curl localhost:80 op je eigen systeem nu wel werkt. Met -p 8080:80 is de server op de host via poort 8080 bereikbaar, terwijl hij in de container op poort 80 blijft. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 33)_
- `FROM ubuntu:18.04` — **Basis-image kiezen in Dockerfile**: Eerste instructie in een Dockerfile: het parent-image waarop je nieuwe image gebouwd wordt (de basislaag). _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 35)_
- `RUN apt install -y wget` — **Commando uitvoeren in Dockerfile**: Instructie in een Dockerfile die tijdens het bouwen een commando uitvoert (als root), hier wget installeren. Elke regel in de Dockerfile vormt een nieuwe laag in het image. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 35)_
- `docker compose up` — **Compose-containers bouwen en starten**: Leest het bestand docker-compose.yml in de huidige map en bouwt en start alle containers die erin beschreven staan. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 38)_
- `docker compose down` — **Compose-containers stoppen en verwijderen**: Stopt de containers van het compose-bestand in de huidige map en verwijdert ze, samen met de bijhorende netwerken (en eventueel images en volumes). _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 39)_
- `docker compose ps` — **Compose-containers oplijsten**: Toont de draaiende containers van Docker compose. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 39)_
- `docker compose exec` — **Commando in compose-container**: Voert een commando uit in een draaiende container van Docker compose, zoals docker exec, bv. docker compose exec dienstnaam bash. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 39)_
- `podman run ubuntu /bin/ls` — **Container draaien met Podman**: Doet hetzelfde als docker run ubuntu /bin/ls, maar met Podman: bijna alle docker-commando's werken door docker te vervangen door podman. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 41)_

### Scripts
- `read VARIABELE` — **Invoer van gebruiker inlezen**: Wacht tot de gebruiker iets typt en Enter drukt, en bewaart dat in een variabele. Met $VARIABELE gebruik je het daarna. _(bron: Chapter 5 - Input and output.pptx, dia 24)_
    - voorbeeld: `read VARIABELE` → [guest@fedora ~]$ read NAME
jasper
[guest@fedora ~]$ echo Welcome $NAME
Welcome jasper
- `bash script_name` — **Script uitvoeren met bash**: Voert een shellscript uit met bash, ook als het nog niet uitvoerbaar gemaakt is. Zo start je bv. het Miniconda-installatiescript. _(bron: Chapter 8 - Reproducible bioinformatics research in Linux_student.pptx, dia 11)_
- `#!/bin/bash` — **Shebang: bash leest het script**: De eerste regel van een script, de shebang (hash bang #!). Erachter staat het pad naar het programma dat het script moet uitvoeren, meestal bash. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 5)_
- `# commentaar` — **Commentaar in een script**: Alles na een # op een regel is commentaar: bash voert het niet uit. Je gebruikt het om uitleg bij je script te schrijven. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 5)_
- `chmod 755 script_name.sh` — **Script uitvoerbaar maken (cijfers)**: Geeft de eigenaar lees-, schrijf- en uitvoerrechten (rwx) en de groep en anderen lees- en uitvoerrechten (r-x). Zo wordt het script uitvoerbaar. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 6)_
- `chmod a+x script_name.sh` — **Uitvoerrecht voor iedereen geven**: Voegt het uitvoerrecht (x) toe voor alle gebruikers: eigenaar, groep en anderen. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 6)_
- `./script_name.sh` — **Script in huidige map uitvoeren**: Voert het script uit dat in de huidige map staat. Met ./ zeg je expliciet dat het script in deze map staat, want de huidige map zit meestal niet in PATH. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 6)_
- `$0` — **Naam van het script**: Binnen een script bevat $0 de naam van het script zelf, zoals je het opgestart hebt. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 11)_
- `$1, $2, …` — **Argumenten van het script**: Positionele parameters: $1 is het eerste argument dat je na de scriptnaam typt, $2 het tweede, enzovoort. Bij ./script_name.sh parameter1 parameter2 is $1 gelijk aan parameter1. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 11)_
- `\$VALUE` — **Backslash: teken niet interpreteren**: Een backslash zorgt dat het volgende teken niet geïnterpreteerd wordt. echo \$VALUE toont dus letterlijk $VALUE in plaats van de waarde van de variabele. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 12)_
- `'$VALUE'` — **Enkele aanhalingstekens: alles letterlijk**: Tussen enkele aanhalingstekens wordt niets geïnterpreteerd. echo '$VALUE' toont letterlijk $VALUE. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 12)_
- `"$VALUE"` — **Dubbele aanhalingstekens rond variabele**: Tussen dubbele aanhalingstekens wordt tekst letterlijk genomen, behalve $, ` en !. Een variabele wordt dus wel vervangen door haar waarde. Zet variabelen tussen dubbele aanhalingstekens als ze spaties kunnen bevatten: dan wordt de waarde als één geheel gezien in plaats van als losse woorden. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 13)_
- `$(commando)` — **Uitvoer van commando gebruiken**: Commandosubstitutie: het commando wordt uitgevoerd en de uitvoer komt op die plaats in de opdracht. Zo geef je een variabele een waarde die een commando berekent, bv. TODAY=$(date +%A). Dit is de aangeraden manier. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 14)_
- ``commando`` — **Oude vorm van commandosubstitutie**: Backticks (`) doen hetzelfde als $(commando): de uitvoer van het commando wordt ingevuld. Verwar ze niet met enkele aanhalingstekens ('), die alles letterlijk laten. $( ) is de voorkeur. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 14)_
- `TODAY=$(date +%A)` — **Uitvoer in variabele bewaren**: Bewaart de dag van de week in de variabele TODAY; echo $TODAY toont bv. Monday. Let op: TODAY='date +%A' (enkele aanhalingstekens) bewaart gewoon de tekst date +%A, terwijl backticks (`date +%A`) wel het commando uitvoeren. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 15)_
- `${VARIABLE:-word}` — **Standaardwaarde als variabele leeg is**: Geeft de waarde van VARIABLE terug; als die niet bestaat (of leeg is), wordt word gebruikt. De variabele zelf verandert niet. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 18)_
- `${VARIABLE:=word}` — **Variabele standaardwaarde toekennen**: Als VARIABLE niet bestaat (of leeg is), krijgt ze de waarde word en wordt die teruggegeven. Daarna heeft de variabele die waarde echt. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 18)_
- `${VARIABLE:?error_message}` — **Stoppen als variabele ontbreekt**: Als VARIABLE niet bestaat (of leeg is), stopt het script en verschijnt de foutmelding. Handig om te controleren of een verplicht argument opgegeven is, bv. ${1:?geef een bestandsnaam}. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 18)_
- `${VAR#/*/}` — **Kortste match links weghalen**: Verwijdert vanaf het begin (links) het kortste stuk tekst dat op het patroon /*/ past. Met VAR=/one/two/three/four/ geeft echo ${VAR#/*/} het resultaat two/three/four/. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 19)_
    - voorbeeld: `${VAR#/*/}` → two/three/four/
- `${VAR##/*/}` — **Langste match links weghalen**: Verwijdert vanaf het begin het langste stuk dat op het patroon past. Met VAR=/one/two/three/four/ past het patroon /*/ op de hele tekst, dus het resultaat is leeg. Bij een pad zonder / op het einde houd je zo enkel de bestandsnaam over. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 19)_
- `${VAR%.*}` — **Kortste match rechts weghalen**: Verwijdert vanaf het einde (rechts) het kortste stuk dat op het patroon .* past. Met VAR=/usr/bin/info.hallo.tk is het resultaat /usr/bin/info.hallo. Handig om een extensie te verwijderen. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 20)_
    - voorbeeld: `${VAR%.*}` → /usr/bin/info.hallo
- `${VAR%%.*}` — **Langste match rechts weghalen**: Verwijdert vanaf het einde het langste stuk dat op .* past, dus alles vanaf de eerste punt. Met VAR=/usr/bin/info.hallo.tk is het resultaat /usr/bin/info. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 20)_
    - voorbeeld: `${VAR%%.*}` → /usr/bin/info
- `${VAR/one/four}` — **Eerste match vervangen**: Vervangt de eerste keer dat one voorkomt door four. Met VAR=/one/two/three/two/one/ is het resultaat /four/two/three/two/one/. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 21)_
    - voorbeeld: `${VAR/one/four}` → /four/two/three/two/one/
- `${VAR//one/four}` — **Alle matches vervangen**: Vervangt elke keer dat one voorkomt door four. Met VAR=/one/two/three/two/one/ is het resultaat /four/two/three/two/four/. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 21)_
    - voorbeeld: `${VAR//one/four}` → /four/two/three/two/four/
- `COUNTER=$((COUNTER+1))` — **Rekenen met variabelen**: Berekent de som tussen $(( )) en bewaart het resultaat: hier wordt COUNTER met 1 verhoogd. Mogelijke bewerkingen: + (optellen), - (aftrekken), * (vermenigvuldigen), / (delen, enkel gehele getallen) en % (modulo = rest na deling). _(bron: Chapter 9 - Shell scripting - student.pptx, dia 24)_
- `test -f /etc/passwd` — **Testen of iets een bestand is**: test controleert een voorwaarde en geeft een exitstatus terug: 0 als het klopt, 1 als het niet klopt. -f test of het pad een gewoon bestand is. Alle mogelijke tests vind je met man test. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 25)_
- `[ string1 = string2 ]` — **Korte schrijfwijze van test**: Doet hetzelfde als test: hier controleren of twee teksten gelijk zijn. Vergeet de spatie na [ en vóór ] niet, anders krijg je een fout. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 25)_
- `if [ ] then … elif [ ] then … else … fi` — **Meerdere voorwaarden na elkaar**: Met elif (else if) test je een tweede voorwaarde als de eerste niet klopte. Je kunt meerdere elif's na elkaar zetten; else vangt alle overige gevallen op. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 27)_
- `[ ] && …` — **Uitvoeren als test lukt**: Het commando na && wordt enkel uitgevoerd als de test ervoor gelukt is (exitstatus 0), bv. [ -f $1 ] && echo bestand. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 27)_
- `[ ] || …` — **Uitvoeren als test mislukt**: Het commando na || wordt enkel uitgevoerd als de test ervoor mislukt is (exitstatus niet 0), bv. [ -e $1 ] || echo bestaat niet. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 27)_
- `for i in … do … done` — **Lus over een lijst**: Voert de opdrachten tussen do en done uit voor elk element uit de lijst; i krijgt telkens de waarde van het volgende element, bv. for i in $(seq 1 100). _(bron: Chapter 9 - Shell scripting - student.pptx, dia 27)_
- `if test -f $1 then … else … fi` — **Keuze maken met if**: Voert de opdrachten na then uit als de test lukt (hier: $1 is een bestand); anders de opdrachten na else. fi sluit het if-blok af. then staat meestal op een nieuwe regel of na een ;. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 28)_
- `$#` — **Aantal argumenten**: Bevat het aantal argumenten dat aan het script meegegeven is. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 29)_
- `"$*"` — **Alle argumenten als één geheel**: Bevat alle argumenten samen als één tekst. In for i in "$*" loopt de lus dus maar één keer, met alle argumenten tegelijk. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 29)_
- `"$@"` — **Alle argumenten apart**: Bevat alle argumenten, maar elk als apart element. In for i in "$@" loopt de lus één keer per argument. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 29)_
- `case $ANS in … esac` — **Meerdere waarden testen met case**: Vergelijkt de waarde van een variabele met verschillende patronen en voert de opdrachten uit bij het eerste patroon dat past. Handiger dan een lange if/elif bij veel waarden. Elk blok eindigt met ;; en esac sluit af. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 30)_
- `while true do … done` — **Lus die blijft herhalen**: Herhaalt de opdrachten tussen do en done zolang de test lukt (exitstatus 0). true lukt altijd, dus deze lus stopt nooit vanzelf (stoppen met Ctrl+C). Gebruik test of [ ] voor een echte voorwaarde. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 31)_
- `while read LINE do … done < file` — **Bestand regel per regel lezen**: Leest een bestand regel per regel: door invoerredirectie (< file) is het bestand de stdin van de lus, en read zet elke regel in de variabele LINE. De lus stopt aan het einde van het bestand. _(bron: Chapter 9 - Shell scripting - student.pptx, dia 33)_

### Tekst bewerken
- `cut -f 1 snp151annotation.txt` — **Eén kolom uit tabel halen**: cut selecteert kolommen uit een tabel; hier kolom 1 (de SNP-namen). Standaard is het scheidingsteken een tab; met -d kies je een ander scheidingsteken (bv. -d ','). _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 9)_
- `cut -f 1-3 snp151position.txt` — **Meerdere kolommen selecteren**: Selecteert kolommen 1 tot en met 3. Met een koppelteken (-) geef je een bereik op, met een komma losse kolommen, bv. -f 1,4. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 9)_
- `paste tmp5 tmp6 tmp1` — **Bestanden naast elkaar plakken**: paste zet de regels van meerdere bestanden naast elkaar als kolommen (gescheiden door een tab). Zo kun je kolommen in een andere volgorde zetten: eerst knippen met cut, dan in de gewenste volgorde plakken. cat zet bestanden net ónder elkaar. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 10)_
- `join FILE1 FILE2` — **Twee tabellen koppelen op sleutel**: join voegt de regels van twee bestanden samen die dezelfde waarde hebben in een gemeenschappelijke kolom (standaard de eerste kolom). Beide bestanden moeten eerst gesorteerd zijn met sort. Standaard is het scheidingsteken een spatie. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 13)_
- `join -t $'\t' FILE1 FILE2` — **Koppelen met tab als scheiding**: Zelfde als join, maar met een tab als scheidingsteken in plaats van een spatie. Gebruik --header als de bestanden een kopregel hebben, zodat die niet mee gesorteerd/gekoppeld wordt. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 13)_
- `join -t $'\t' -o '1.1 1.2 2.2' --header snp151position-sorted.txt snp151annotation-sorted.txt` — **Gekozen kolommen na join**: Koppelt twee gesorteerde tabellen op kolom 1 en houdt enkel de opgegeven kolommen over. Met -o kies je welke velden in de uitvoer komen, in de vorm bestand.kolom. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 15)_
- `sort /etc/passwd` — **Regels alfabetisch sorteren**: Sorteert de regels van een bestand: eerst cijfers (0-9), dan letters (aA-zZ). Het sorteert teken per teken, daarom komt 10 vóór 2. Hetzelfde resultaat krijg je met cat /etc/passwd | sort. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 16)_
    - voorbeeld: `sort /etc/passwd` → abrt:x:173:173::/etc/abrt:/sbin/nologin
adm:x:3:4:adm:/var/adm:/sbin/nologin
apache:x:48:48:Apache:/usr/share/httpd:/sbin/nologin
- `sort -k 2 DATA` — **Sorteren op een kolom**: Sorteert de regels op basis van kolom 2 in plaats van vanaf het begin van de regel. Met -k 2,2 sorteer je strikt op enkel kolom 2. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 16)_
- `sort -k 6 -n -r DATA` — **Numeriek omgekeerd sorteren**: Sorteert op kolom 6 volgens de getalwaarde (-n), van groot naar klein (-r). Zonder -n sorteert sort als tekst, waardoor bv. 10 vóór 2 komt. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 16)_
- `sort -R bestand` — **Regels willekeurig schudden**: Zet de regels in een willekeurige volgorde (random sort). _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 16)_
- `sort -u -k 1,1 DATA` — **Sorteren en dubbels verwijderen**: Sorteert en houdt per waarde in kolom 1 maar één regel over (unique sort). Zonder -k verwijdert sort -u enkel regels die volledig identiek zijn. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 16)_
- `cut -f 2 DATA | sort -u | wc -l` — **Aantal verschillende waarden tellen**: Haalt kolom 2 uit DATA, houdt elke waarde maar één keer over en telt het aantal regels. Zo krijg je het aantal verschillende (distinct) waarden in die kolom. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 18)_
- `sort bestand | uniq` — **Aangrenzende dubbele regels weglaten**: uniq herkent enkel identieke regels die direct na elkaar staan. Daarom sorteer je eerst, en gebruik je daarna uniq. Het resultaat is gelijk aan sort -u. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 19)_
- `uniq -d bestand` — **Alleen herhaalde regels tonen**: Toont enkel regels die meer dan één keer (na elkaar) voorkomen, telkens één keer. Sorteer het bestand eerst. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 19)_
- `uniq -c -f 1 snp151annotation-short.txt` — **Herhaalde regels tellen**: Telt hoe vaak elke (aangrenzende) regel voorkomt, waarbij het eerste veld genegeerd wordt; zo tel je hier de waarden van de class-kolom. Omdat uniq enkel aangrenzende regels vergelijkt, moet je eerst op die kolom sorteren: sort -k 2 snp151annotation-short.txt | uniq -c -f 1. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 20)_
- `sed s/chr/chromosome/g snp151position.txt` — **Tekst vervangen in bestand**: sed is een stream editor die tekst filtert en omzet. Hier wordt overal 'chr' vervangen door 'chromosome'. Het bestand zelf verandert niet; het resultaat verschijnt op het scherm. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 21)_
- `awk 'condition {action}' inputfile` — **Basisvorm van awk**: awk is een kleine programmeertaal voor tabellen. Het leest het bestand regel per regel (record) en voert de actie uit op elke regel die aan de voorwaarde voldoet. Elke regel wordt opgedeeld in velden (kolommen). _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 22)_
- `$0, $1, NR, NF, FS` — **Ingebouwde variabelen van awk**: Deze variabelen gebruik je binnen een awk-opdracht. Ze geven de hele regel, een bepaalde kolom, het regelnummer, het aantal kolommen of het scheidingsteken. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 23)_
- `awk '{print $1}' snp151annotation.txt` — **Eerste kolom afdrukken**: Drukt van elke regel enkel het eerste veld (kolom) af. Er is geen voorwaarde, dus de actie gebeurt op alle regels. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 24)_
- `awk '{print $1, $3, $2}' snp151annotation.txt` — **Kolommen herschikken met awk**: Drukt kolom 1, 3 en 2 af in die volgorde, gescheiden door een spatie. De komma tussen de velden zet er een spatie tussen. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 24)_
- `awk '{print $1, "\t", $3, "\t", $2}' snp151annotation.txt` — **Kolommen herschikken, tab-gescheiden**: Herschikt de kolommen en zet een tab tussen de velden. Door de komma's komt er ook een spatie rond elke tab; schrijf $1 "\t" $3 "\t" $2 (zonder komma's) voor enkel een tab. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 24)_
- `awk '{print NF}' snp151annotation.txt` — **Aantal kolommen per regel**: Drukt voor elke regel het aantal velden (kolommen) af. Met awk '{print NF, $0}' zet je dat aantal als extra eerste kolom vóór de inhoud van de regel. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 25)_
- `awk '{print $NF}' snp151annotation.txt` — **Laatste kolom afdrukken**: Drukt van elke regel het laatste veld af. NF is het aantal kolommen, dus $NF is de inhoud van de laatste kolom (en niet het aantal). _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 25)_
- `awk 'BEGIN {print "some text"}'` — **Actie vóór het lezen**: BEGIN voert de actie uit vóór er regels gelezen worden, hier tekst afdrukken. Er is zelfs geen invoerbestand nodig. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 27)_
- `awk 'BEGIN {print "2+3=" 2+3}'` — **Rekenen met awk**: awk kan rekenen: dit drukt de tekst 2+3= af, gevolgd door het resultaat van de berekening. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 27)_
    - voorbeeld: `awk 'BEGIN {print "2+3=" 2+3}'` → 2+3=5
- `awk 'END {print NR}' snp151annotation.txt` — **Totaal aantal regels tellen**: END voert de actie uit nadat alle regels gelezen zijn; NR is dan het totale aantal regels. awk '{print NR}' (zonder END) drukt daarentegen bij elke regel het regelnummer af. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 28)_
- `awk 'NR > 1 {s=0; for (i=2; i<=NF; i++) s=s+$i; print s}' arrayDat.txt` — **Som per regel berekenen**: Slaat de kopregel over en telt per regel (gen) alle waarden vanaf kolom 2 op, dus de expressiewaarden van alle stalen. Daarna wordt de som afgedrukt. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 36)_
- `awk 'NR > 1 {s=0; n=NF-1; for (i=2; i<=NF; i++) s=s+$i; s=s/n; print s}' arrayDat.txt` — **Gemiddelde per regel berekenen**: Zelfde als de som per regel, maar deelt de som door het aantal stalen (NF-1, want kolom 1 is de ProbeID). Zo krijg je de gemiddelde expressie per gen. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 36)_

### Terminal & sneltoetsen
- `Ctrl + Alt + F3` — **Virtuele console openen**: Opent een virtuele console: een tekstterminal over het hele scherm, zonder grafische omgeving. F3 tot F6 geven elk een andere console. _(bron: Chapter 2 - The terminal.pptx, dia 7)_
- `Ctrl + Alt + F2` — **Terug naar grafische omgeving**: Verlaat de virtuele console en brengt je terug naar de grafische omgeving (GNOME). _(bron: Chapter 2 - The terminal.pptx, dia 7)_
- `exit` — **Terminal of sessie afsluiten**: Sluit de shell af: het terminalvenster sluit, of je logt uit van een virtuele console of een SSH-verbinding. exit is een ingebouwd Bash-commando. _(bron: Chapter 2 - The terminal.pptx, dia 7)_
- `↑ / ↓` — **Vorige commando's herhalen**: Met de pijltjestoetsen omhoog en omlaag blader je door de commando's die je eerder typte, zodat je ze niet opnieuw moet typen. _(bron: Chapter 2 - The terminal.pptx, dia 23)_
- `Tab` — **Commando of naam aanvullen**: Druk op Tab terwijl je typt en Bash vult de naam van het commando, bestand of map automatisch aan. Twee keer Tab toont alle mogelijke aanvullingen als er meerdere zijn. _(bron: Chapter 2 - The terminal.pptx, dia 23)_
- `dubbelklik / 3× klikken / middelste muisknop` — **Kopiëren en plakken met muis**: In de terminal selecteer je met een dubbelklik een heel woord en met drie klikken een hele regel. Plakken doe je met de middelste muisknop (of links en rechts tegelijk). _(bron: Chapter 2 - The terminal.pptx, dia 23)_
- `Ctrl + D` — **Terminal afsluiten**: Sluit de terminal of de shell af, net als exit. Werkt ook om een SSH-verbinding te sluiten. _(bron: Chapter 2 - The terminal.pptx, dia 24)_
- `Ctrl + Shift + W` — **Terminalvenster of tabblad sluiten**: Sluit het terminaltabblad (W) of het hele terminalvenster (Ctrl + Shift + Q) in de grafische omgeving. _(bron: Chapter 2 - The terminal.pptx, dia 24)_
- `Ctrl + R` — **Zoeken in commandogeschiedenis**: Start 'reverse-i-search': typ een stukje van een eerder commando en Bash zoekt het in je geschiedenis. Druk Enter om het uit te voeren. _(bron: Chapter 2 - The terminal.pptx, dia 24)_
- `Ctrl + A` — **Cursor naar begin van regel**: Zet de cursor vooraan op de commandoregel, net achter de prompt. _(bron: Chapter 2 - The terminal.pptx, dia 24)_
- `Ctrl + E` — **Cursor naar einde van regel**: Zet de cursor achteraan op de commandoregel. _(bron: Chapter 2 - The terminal.pptx, dia 24)_
- `Ctrl + C` — **Lopend commando stoppen**: Beëindigt het commando of programma dat nu loopt en geeft je de prompt terug. Handig als een commando blijft hangen. _(bron: Chapter 2 - The terminal.pptx, dia 24)_
- `Ctrl + H` — **Teken links van cursor wissen**: Werkt als de Backspace-toets: verwijdert het teken links van de cursor. _(bron: Chapter 2 - The terminal.pptx, dia 24)_
- `Ctrl + L` — **Terminalscherm leegmaken**: Zet de prompt bovenaan en maakt zo het terminalscherm leeg. Je vorige commando's blijven wel in de geschiedenis. _(bron: Chapter 2 - The terminal.pptx, dia 24)_
- `Ctrl + Z` — **Lopend programma bevriezen**: Pauzeert (bevriest) het programma dat nu loopt, bv. Firefox gestart vanuit de terminal, zodat je de terminal weer kan gebruiken. Het programma wordt niet afgesloten. _(bron: Chapter 2 - The terminal.pptx, dia 24)_

### Zoeken & filteren
- `grep -c ">" sequentie.fasta` — **Tel sequenties in FASTA**: Telt hoeveel regels met '>' beginnen, dus hoeveel sequenties er in een FASTA-bestand staan.
- `find ~ -name file6` — **Bestand zoeken op naam**: Zoekt in je thuismap en alle submappen naar bestanden met de naam file6. Met find kan je ook zoeken op grootte, tijdstip, eigenaar, type of rechten (zie man find). _(bron: Chapter 3 - Organizing files.pptx, dia 32)_
- `locate pattern` — **Snel zoeken via index**: Toont alle absolute paden waarin het woord pattern voorkomt. locate zoekt in een index (databank), dus bestanden die net aangemaakt zijn vindt hij pas na het bijwerken van die index. _(bron: Chapter 3 - Organizing files.pptx, dia 34)_
- `updatedb -l 0 -o ~/dbfile -U /` — **Eigen zoekindex maken**: Maakt een eigen indexbestand ~/dbfile voor locate, met alle bestanden vanaf de root /. _(bron: Chapter 3 - Organizing files.pptx, dia 36)_
- `locate -d ~/dbfile pattern` — **Zoeken in eigen index**: Zoekt pattern in je eigen indexbestand in plaats van in de standaardindex. _(bron: Chapter 3 - Organizing files.pptx, dia 36)_
- `which command` — **Locatie van commando vinden**: Toont waar het programma van een commando staat, bv. which ls. which zoekt in alle mappen uit de variabele PATH. _(bron: Chapter 3 - Organizing files.pptx, dia 37)_
- `grep string file` — **Tekst zoeken in bestand**: Toont alle regels van een bestand waarin het woord string voorkomt. grep werkt met reguliere expressies en heeft nuttige opties zoals -i (hoofdletters negeren) en -v (regels tonen die het woord níet bevatten). _(bron: Chapter 3 - Organizing files.pptx, dia 39)_
- `grep ^\> P00687.fasta` — **Kopregel van FASTA-bestand tonen**: Toont de regels die beginnen met >: in een FASTA-bestand is dat de kopregel met de naam van de sequentie. De \ zorgt dat Bash > niet als redirect ziet. _(bron: Chapter 3 - Organizing files.pptx, dia 40)_
- `grep rs112803166 snp151*` — **Regels met een ID zoeken**: Toont in beide snp151-bestanden de regels waarin rs112803166 voorkomt, met de bestandsnaam ervoor. Zo filter je de informatie over één SNP uit meerdere tabellen. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 8)_
- `awk 'NR < 6' snp151annotation.txt` — **Eerste vijf regels met awk**: Drukt de regels af waarvan het regelnummer kleiner is dan 6, dus de eerste 5 regels. Zonder actie is afdrukken de standaardactie; het is hetzelfde als awk 'NR < 6 {print $0}'. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 29)_
- `awk 'NR == 1' snp151annotation.txt` — **Alleen de eerste regel**: Drukt enkel regel 1 af (bv. de kopregel). Let op: gebruik == om te vergelijken, niet =. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 29)_
- `awk 'NR > 1 && NR < 7' snp151annotation.txt` — **Regels 2 tot en met 6**: Drukt de regels af met een nummer groter dan 1 én kleiner dan 7, dus regel 2 tot en met 6. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 29)_
- `awk '/ccttcc/' snp151annotation.txt` — **Regels met patroon afdrukken**: Drukt alle regels af die het patroon (een reguliere expressie) ccttcc bevatten, vergelijkbaar met grep. Het patroon staat tussen schuine strepen; hoofdletters en kleine letters zijn verschillend. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 30)_
- `awk '/ccttcc/ {print $1}' snp151annotation.txt` — **ID's van gevonden regels**: Drukt enkel het SNP-ID (kolom 1) af van de regels die ccttcc bevatten. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 30)_
- `awk 'BEGIN {n=0}; /CCTTCC/ {n++}; END {print n}' snp151annotation.txt` — **Gevonden regels tellen met awk**: Telt het aantal regels die CCTTCC bevatten. Vóór het lezen wordt teller n op 0 gezet, bij elke passende regel verhoogd met 1, en na het lezen wordt n afgedrukt. _(bron: Chapter 7 - Tables and text file manipulation.pptx, dia 30)_

## HTML (63)

### Attributen
- `<img src="" alt="">` — **Alternatieve tekst bij afbeelding**: Het alt-attribuut geeft tekst die getoond wordt als de afbeelding niet laadt, bv. door een typfout in het pad. _(bron: 2. Introduction to HTML.pptx, dia 38)_
- `<img src="" width="500px">` — **Breedte of hoogte van afbeelding**: Met width en height stel je de afmetingen van een afbeelding in (in pixels). Geef je enkel de breedte of enkel de hoogte, dan past de andere zich aan zodat de afbeelding niet vervormt. _(bron: 2. Introduction to HTML.pptx, dia 39)_
- `class=""` — **Klasse (label) aan element geven**: Geeft een element een label (klasse) zodat je het kan aanspreken, bv. met CSS. Meerdere elementen mogen dezelfde klasse hebben en één element kan meerdere klassen hebben, gescheiden door spaties. _(bron: 2. Introduction to HTML.pptx, dia 53)_
- `id=""` — **Unieke naam aan element geven**: Geeft een element een unieke naam (id). Twee elementen mogen niet hetzelfde id hebben en elk element heeft maximaal één id. _(bron: 2. Introduction to HTML.pptx, dia 55)_
- `style=""` — **CSS op één element**: Met het style-attribuut geef je CSS-opmaak aan één enkel element (inline stijl). _(bron: 2. Introduction to HTML.pptx, dia 58)_
- `title=""` — **Tooltip bij element**: Geeft extra informatie die als tooltip verschijnt wanneer je met de muis over het element gaat. Niet verwarren met de <title>-tag, die de titel in het browsertabblad zet. _(bron: 2. Introduction to HTML.pptx, dia 59)_
    - voorbeeld: `title=""`
- `placeholder="tekst"` — **Hulptekst in leeg invoerveld**: Toont een lichtgrijze hint in een leeg invoerveld (bv. 'Provide your name'). De hint verdwijnt als je begint te typen en wordt niet verstuurd. _(bron: 5. Dynamic Web Pages.pptx, dia 11)_
- `checked` — **Standaard aangevinkt bij laden**: Checkboxes en radioknoppen zijn standaard niet aangevinkt. Zet checked in de tag om ze vooraf aan te vinken: bij checkboxes mag dat bij meerdere, bij radioknoppen bij één knop per groep. _(bron: 5. Dynamic Web Pages.pptx, dia 31)_
    - voorbeeld: `checked`

### Formulieren
- `<fieldset></fieldset>` — **Kader met zichtbare rand**: Maakt een container met een zichtbare rand rond de inhoud. _(bron: 2. Introduction to HTML.pptx, dia 41)_
- `<legend></legend>` — **Titel op rand van fieldset**: Zet een titel bovenaan op de rand van een <fieldset>. Werkt enkel binnen een fieldset-tag. _(bron: 2. Introduction to HTML.pptx, dia 41)_
    - voorbeeld: `<legend></legend>`
- `<form action="#" method="POST"></form>` — **Formulier voor invoervelden**: Een formulier bevat de invoervelden en bepaalt waar en hoe de gegevens na verzenden naartoe gaan. Alle invoervelden (<input>, <select>, <textarea>) moeten erin staan. _(bron: 5. Dynamic Web Pages.pptx, dia 13)_
- `<input type="" name="" value="">` — **Invoerveld maken**: De belangrijkste tag voor invoervelden. Via name haal je de ingevulde waarde later op in PHP. _(bron: 5. Dynamic Web Pages.pptx, dia 19)_
- `<input type="submit" name="submit" value="tekst">` — **Verzendknop voor formulier**: Maakt een knop die het formulier naar de PHP-server stuurt. value bepaalt de tekst op de knop (en de waarde in $_POST/$_GET); zonder value staat er 'Submit Query'. _(bron: 5. Dynamic Web Pages.pptx, dia 20)_
- `<input type="text" name="">` — **Invoerveld voor korte tekst**: Een veld waarin de gebruiker een korte tekst typt. Met value kun je een standaardtekst meegeven. _(bron: 5. Dynamic Web Pages.pptx, dia 21)_
- `<input type="number" name="">` — **Invoerveld voor getallen**: Een veld waarin alleen getallen ingevuld kunnen worden, bv. een leeftijd. Er bestaan ook min, max en step om het bereik te beperken (buiten de leerstof). _(bron: 5. Dynamic Web Pages.pptx, dia 23)_
- `<input type="password" name="">` — **Verborgen invoer voor wachtwoorden**: De getypte tekens worden als bolletjes of sterretjes getoond. Gebruik voor gevoelige gegevens altijd method="POST", anders staat de waarde leesbaar in de URL. _(bron: 5. Dynamic Web Pages.pptx, dia 25)_
- `<input type="email" name="">` — **Invoerveld voor e-mailadres**: Een veld voor een e-mailadres. Bij een ongeldig adres toont de browser meestal een foutmelding en wordt het formulier niet verstuurd. _(bron: 5. Dynamic Web Pages.pptx, dia 27)_
- `<input type="hidden" name="" value="">` — **Onzichtbaar veld meesturen**: Een veld dat de gebruiker niet ziet, maar waarvan de value toch mee verstuurd wordt. Handig om extra informatie achter de schermen naar de PHP-server te sturen. _(bron: 5. Dynamic Web Pages.pptx, dia 29)_
- `<input type="checkbox" name="">` — **Aanvinkvakje**: Een vakje dat je aan- of uitvinkt; je kunt er meerdere tegelijk aanvinken. Aangevinkt: de naam komt in $_POST/$_GET met waarde 'on' (of de eigen value). Niet aangevinkt: de naam ontbreekt helemaal. _(bron: 5. Dynamic Web Pages.pptx, dia 30)_
    - voorbeeld: `<input type="checkbox" name="">` → Array
(
    [BIT02] => on
)
- `<input type="radio" name="groep" value="">` — **Keuzerondje: één uit groep**: Radioknoppen met dezelfde name vormen een groep waarin je maar één optie kunt kiezen; elke knop heeft een eigen value. In $_POST/$_GET staat de groepsnaam met de value van de gekozen knop; is niets gekozen, dan ontbreekt de naam. _(bron: 5. Dynamic Web Pages.pptx, dia 33)_
    - voorbeeld: `<input type="radio" name="groep" value="">` → Array
(
    [course] => BIT01
)
- `<textarea name=""></textarea>` — **Invoerveld voor meerdere regels**: Een groot tekstveld waarin je over meerdere regels kunt typen. Na verzenden is de inhoud één string, met \n op de plaats van de regeleinden. Tekst tussen de tags is de standaardinhoud. _(bron: 5. Dynamic Web Pages.pptx, dia 38)_
- `<select name=""><option value="">tekst</option></select>` — **Keuzelijst (dropdown menu)**: Maakt een uitklapmenu waarin je één optie kiest. name staat op <select>, value op elke <option>; de tekst tussen de <option>-tags ziet de gebruiker. _(bron: 5. Dynamic Web Pages.pptx, dia 40)_
    - voorbeeld: `<select name=""><option value="">tekst</option></select>` → Array ( [Lecturer] => Paco )
- `<select name="naam[]" multiple>` — **Dropdown met meerdere keuzes**: Met het attribuut multiple kun je meerdere opties kiezen (Ctrl of Shift ingedrukt houden bij klikken). De [] achter de naam zorgt dat PHP de gekozen waarden als array ontvangt. _(bron: 5. Dynamic Web Pages.pptx, dia 42)_
    - voorbeeld: `<select name="naam[]" multiple>` → Array ( [Lecturer] => Array (
    [0] => Jasper
    [1] => Paco
  )
)
- `<optgroup label="">` — **Opties in dropdown groeperen**: Groepeert verwante <option>-tags in een <select> onder een kopje, zodat een lange lijst overzichtelijk blijft. Het kopje zelf kun je niet kiezen. _(bron: 5. Dynamic Web Pages.pptx, dia 44)_
    - voorbeeld: `<optgroup label="">`
- `<input type="file" name="">` — **Bestand laten uploaden**: Maakt een knop waarmee de gebruiker een bestand kiest om te uploaden. Werkt alleen in een formulier met method="POST" en enctype="multipart/form-data". _(bron: 5. Dynamic Web Pages.pptx, dia 47)_
- `enctype="multipart/form-data"` — **Formulier geschikt maken voor uploads**: Attribuut op de <form>-tag dat nodig is om bestanden te versturen. Het verpakt tekstvelden en bestanden in aparte delen, zodat de server ze correct kan verwerken; zonder dit werkt uploaden niet. _(bron: 5. Dynamic Web Pages.pptx, dia 47)_
    - voorbeeld: `enctype="multipart/form-data"`

### Head & koppelingen
- `<title></title>` — **Titel van de webpagina**: Stelt de titel van de webpagina in; de browser toont die in het tabblad. Staat binnen de <head>. _(bron: 2. Introduction to HTML.pptx, dia 13)_
    - voorbeeld: `<title></title>`
- `<style></style>` — **CSS-stijlen in de head**: Hiertussen zet je CSS-regels die de opmaak van de pagina bepalen (interne stijl). De <style>-tag staat in de <head>. _(bron: 2. Introduction to HTML.pptx, dia 14)_

### Layout
- `<div></div>` — **Algemene container (blok)**: Groepeert inhoud zodat je die samen kan opmaken met CSS. De div-tag heeft geen eigen betekenis en voegt, anders dan <p>, geen extra witruimte toe boven of onder. _(bron: 2. Introduction to HTML.pptx, dia 22)_
- `<hr>` — **Horizontale lijn**: Tekent een horizontale lijn om secties van elkaar te scheiden. Het is een self-closing tag: er is geen sluitingstag en geen inhoud. _(bron: 2. Introduction to HTML.pptx, dia 26)_
- `<span></span>` — **Algemene container binnen regel**: Groepeert een stukje tekst binnen een regel zodat je het met CSS kan opmaken. Net als <div> heeft span geen eigen betekenis of effect, maar het is een inline-element. _(bron: 2. Introduction to HTML.pptx, dia 36)_

### Lijsten
- `<ul><li>Item</li></ul>` — **Lijst met bolletjes**: Een ongeordende lijst; elk <li> is één punt in de lijst.
- `<ul></ul>` — **Lijst met opsommingstekens**: Maakt een ongenummerde lijst met bolletjes. Elk item staat in een eigen <li>-tag binnen de <ul>. _(bron: 2. Introduction to HTML.pptx, dia 42)_
- `<li></li>` — **Eén item in een lijst**: Elk item van een lijst staat in een eigen <li>-tag, binnen <ul> of <ol>. Voeg meer li-tags toe voor meer items. _(bron: 2. Introduction to HTML.pptx, dia 42)_
- `<ol></ol>` — **Genummerde lijst**: Maakt een lijst met nummers, handig als de volgorde belangrijk is. Elk item staat in een eigen <li>-tag binnen de <ol>. _(bron: 2. Introduction to HTML.pptx, dia 43)_

### Links & media
- `<img src="eiwit.png" alt="Eiwitstructuur">` — **Afbeelding tonen**: Toont de afbeelding eiwit.png. De alt-tekst beschrijft de afbeelding voor schermlezers en als ze niet laadt.
- `<a href="pagina2.html">Volgende</a>` — **Link naar andere pagina**: Maakt de klikbare tekst 'Volgende' die naar pagina2.html gaat.
- `<a href="URL"></a>` — **Link naar andere website**: Maakt een klikbare hyperlink. In het href-attribuut zet je het adres (URL) van de pagina; de tekst tussen de tags is waarop je klikt. _(bron: 2. Introduction to HTML.pptx, dia 27)_
- `<a href="info/contact.html"></a>` — **Link naar pagina op eigen site**: Verwijst naar een ander HTML-bestand van je eigen website. Staat het bestand in dezelfde map, dan volstaat de naam (about.html); in een submap zet je de mapnaam ervoor (info/contact.html). _(bron: 2. Introduction to HTML.pptx, dia 28)_
- `<img src="">` — **Afbeelding tonen**: Voegt een afbeelding in de pagina. Het src-attribuut is verplicht en geeft de locatie: een lokaal pad (bv. Mario.png in dezelfde map) of een volledige URL. _(bron: 2. Introduction to HTML.pptx, dia 37)_
- `<a href="#id"></a>` — **Link naar plek op pagina**: Een link met href="#" gevolgd door een id springt naar het element met dat id op dezelfde pagina. Handig voor een inhoudstafel. _(bron: 2. Introduction to HTML.pptx, dia 57)_
- `<a href="mailto:adres">tekst</a>` — **Link die e-mail opstelt**: Een link met mailto: opent het e-mailprogramma van de gebruiker met het adres al ingevuld als ontvanger. _(bron: 5. Dynamic Web Pages.pptx, dia 9)_
    - voorbeeld: `<a href="mailto:adres">tekst</a>`

### Structuur
- `<!DOCTYPE html>` — **Documenttype**: Staat helemaal bovenaan elk HTML-bestand en vertelt de browser dat het om moderne HTML gaat.
- `! + Enter` — **HTML-basisstructuur invoegen (VS Code)**: In VS Code typ je in een leeg .html-bestand een uitroepteken en druk je op Enter (of Tab). Dan wordt de volledige HTML5-basisstructuur met doctype, html, head en body automatisch ingevuld. _(bron: 2. Introduction to HTML.pptx, dia 9)_
- `<html lang="en"></html>` — **Begin en einde van document**: De <html>-tag en de sluitingstag </html> markeren het begin en einde van het HTML-document; alles staat hiertussen. Het lang-attribuut zegt in welke taal de pagina geschreven is. _(bron: 2. Introduction to HTML.pptx, dia 11)_
- `<head></head>` — **Metadata van de pagina**: In de <head> zet je informatie over de pagina (metadata), zoals de titel en CSS-stijlen. Het is een omhulsel rond andere tags; de inhoud ervan verschijnt niet in het browservenster zelf. _(bron: 2. Introduction to HTML.pptx, dia 12)_
- `<body></body>` — **Zichtbare inhoud van de pagina**: Alles tussen <body> en </body> wordt in het browservenster getoond. Het is een omhulsel rond alle andere inhoudstags zoals koppen, paragrafen en afbeeldingen. _(bron: 2. Introduction to HTML.pptx, dia 15)_
- `<!-- commentaar -->` — **Commentaar in HTML**: Tekst tussen <!-- en --> is commentaar: de browser toont het niet. Je gebruikt het voor uitleg en notities in je code, zodat die makkelijker te begrijpen is. _(bron: 2. Introduction to HTML.pptx, dia 16)_

### Tabellen
- `<table></table>` — **Tabel maken**: Maakt een tabel en is de buitenste laag die de hele tabel omsluit. Binnenin staan rijen (<tr>) met cellen (<td> of <th>). _(bron: 2. Introduction to HTML.pptx, dia 45)_
- `<tr></tr>` — **Rij in een tabel**: Maakt één rij in een tabel. Voeg meer tr-tags toe voor meer rijen. _(bron: 2. Introduction to HTML.pptx, dia 46)_
- `<td></td>` — **Cel in een tabelrij**: Maakt één gewone cel in een tabelrij. Voeg meer td-tags toe voor meer cellen (kolommen) in de rij. _(bron: 2. Introduction to HTML.pptx, dia 47)_
- `<th></th>` — **Kopcel in een tabel**: Maakt een kopcel, meestal om kolommen of rijen te benoemen. Browsers tonen die standaard vet en gecentreerd. _(bron: 2. Introduction to HTML.pptx, dia 48)_

### Tekst
- `<h1></h1> … <h6></h6>` — **Koppen (titels) van secties**: Koppen geven een titel aan een nieuwe sectie. Er zijn zes niveaus: h1 is de grootste, h6 de kleinste; de browser past de grootte automatisch aan. _(bron: 2. Introduction to HTML.pptx, dia 20)_
    - voorbeeld: `<h1></h1> … <h6></h6>`
- `<p></p>` — **Paragraaf maken**: Groepeert tekst die bij elkaar hoort in een paragraaf. De browser voegt automatisch witruimte toe boven en onder de paragraaf. _(bron: 2. Introduction to HTML.pptx, dia 21)_
- `<pre></pre>` — **Tekst exact zoals getypt**: Toont tekst met alle spaties, tabs en regeleinden precies zoals in de code, in een monospaced lettertype. Ideaal voor sequenties van nucleotiden of aminozuren, of ASCII-art. _(bron: 2. Introduction to HTML.pptx, dia 23)_
- `<blockquote></blockquote>` — **Blok citaat uit andere bron**: Markeert een blok tekst als citaat uit een andere bron. De browser voegt witruimte toe boven, onder en links van het citaat. _(bron: 2. Introduction to HTML.pptx, dia 25)_
- `<br>` — **Nieuwe regel beginnen**: Voegt een regeleinde in: wat volgt komt op een nieuwe regel. Het is een self-closing tag. Anders dan <hr> tekent het geen lijn. _(bron: 2. Introduction to HTML.pptx, dia 29)_
- `<code></code>` — **Code-tekst binnen een regel**: Toont tekst in een monospaced lettertype, zoals <pre>, maar is een inline-element: de tekst blijft op dezelfde regel staan. _(bron: 2. Introduction to HTML.pptx, dia 30)_
    - voorbeeld: `<code></code>`
- `<em></em>` — **Tekst benadrukken (cursief)**: Legt nadruk op tekst; de browser toont die cursief. _(bron: 2. Introduction to HTML.pptx, dia 31)_
- `<small></small>` — **Kleinere tekst**: Toont tekst in een kleiner lettertype. Je kan small-tags in elkaar zetten (nesten): hoe meer small-tags, hoe kleiner de tekst. _(bron: 2. Introduction to HTML.pptx, dia 32)_
- `<strike></strike>` — **Tekst doorstrepen**: Toont tekst met een lijn erdoor, bv. om een fout aan te duiden. _(bron: 2. Introduction to HTML.pptx, dia 33)_
- `<strong></strong>` — **Tekst vet maken**: Benadrukt tekst sterk; de browser toont die in het vet. _(bron: 2. Introduction to HTML.pptx, dia 34)_
- `<q></q>` — **Kort citaat binnen regel**: Markeert een kort citaat binnen een regel tekst; de browser zet er automatisch aanhalingstekens rond. _(bron: 2. Introduction to HTML.pptx, dia 35)_

## CSS (60)

### Box model
- `border: 6px solid rgb(64,58,50);` — **Rand rond een element**: border is een shorthand die in één keer de dikte, de stijl en de kleur van de rand instelt (border-width, border-style en border-color). _(bron: 3. Introduction to CSS.pptx, dia 48)_
    - voorbeeld: `border: 6px solid rgb(64,58,50);`
- `height: 250px;` — **Breedte en hoogte instellen**: width bepaalt de horizontale grootte van een element, height de verticale. Je kunt verschillende eenheden gebruiken. _(bron: 3. Introduction to CSS.pptx, dia 49)_
    - voorbeeld: `height: 250px;`
- `width: fit-content;` — **Breedte passend bij inhoud**: Met fit-content berekent de browser zelf de breedte (of hoogte) op basis van de inhoud. Zo is een div niet meer standaard even breed als het venster. _(bron: 3. Introduction to CSS.pptx, dia 50)_
    - voorbeeld: `width: fit-content;`
- `padding: 16px;` — **Ruimte binnen de rand**: padding is de ruimte tussen de inhoud van een element en zijn rand. Het is een shorthand voor padding-top, -right, -bottom en -left. Met 1 tot 4 waarden kies je welke kanten welke ruimte krijgen. _(bron: 3. Introduction to CSS.pptx, dia 53)_
    - voorbeeld: `padding: 16px;`
- `margin: 0px 0px 15px 0px;` — **Ruimte buiten de rand**: margin is de ruimte buiten de rand, tussen het element en andere elementen. Het is een shorthand voor margin-top, -right, -bottom en -left; de regels voor 1 tot 4 waarden zijn dezelfde als bij padding. _(bron: 3. Introduction to CSS.pptx, dia 53)_
    - voorbeeld: `margin: 0px 0px 15px 0px;`
- `box-sizing: border-box;` — **Padding en rand meetellen**: Standaard (content-box) geldt width/height alleen voor de inhoud; padding en rand komen er nog bij. Met border-box tellen padding en rand mee in de opgegeven breedte en hoogte. _(bron: 3. Introduction to CSS.pptx, dia 55)_
    - voorbeeld: `box-sizing: border-box;`
- `outline: 20px solid yellow;` — **Lijn buiten de rand**: outline tekent een lijn buiten de rand van een element, met dezelfde waarden als border (dikte, stijl, kleur). Anders dan een rand neemt een outline geen plaats in en duwt ze andere elementen niet weg. _(bron: 3. Introduction to CSS.pptx, dia 57)_
    - voorbeeld: `outline: 20px solid yellow;`

### Kleur & achtergrond
- `background-color` — **Achtergrondkleur instellen**: Stelt de achtergrondkleur van een element in, bv. body { background-color: green; } voor een groene pagina. _(bron: 2. Introduction to HTML.pptx, dia 14)_
- `color: red;` — **Tekstkleur instellen**: De eigenschap color bepaalt de kleur van de tekst in een element. Je kunt een kleurnaam, een hexcode of een RGB-waarde gebruiken. _(bron: 3. Introduction to CSS.pptx, dia 45)_
    - voorbeeld: `color: red;`
- `#FF0000 / rgb(255, 0, 0)` — **Kleur als hexcode of RGB**: Behalve met een naam (red, hotpink, tomato …) kun je een kleur geven als hexcode of RGB-waarde. Bij RGB geef je de hoeveelheid rood, groen en blauw, elk van 0 tot 255; een hexcode geeft dezelfde drie getallen in hexadecimale notatie. _(bron: 3. Introduction to CSS.pptx, dia 45)_
    - voorbeeld: `#FF0000 / rgb(255, 0, 0)`
- `background: #D73233;` — **Achtergrondkleur instellen**: De eigenschap background kleurt de achtergrond van een element. Het is een shorthand: ze kan ook o.a. background-color, background-image en background-repeat in één keer instellen. Voor alleen de kleur kun je ook background-color gebruiken. _(bron: 3. Introduction to CSS.pptx, dia 46)_
    - voorbeeld: `background: #D73233;`

### Koppelen aan HTML
- `selector { eigenschap: waarde; }` — **Opbouw van een CSS-regel**: Een CSS-regel bestaat uit een selector en een declaratieblok tussen accolades. Elke declaratie is een eigenschap met een waarde, gevolgd door een puntkomma. Voorbeeld: p { font-size: 1.2em; } geeft alle <p>-elementen een bepaalde lettergrootte. _(bron: 3. Introduction to CSS.pptx, dia 4)_
- `<p style="color: red; background: green">` — **Inline CSS met style-attribuut**: Met het style-attribuut zet je CSS rechtstreeks op één HTML-element. Meerdere declaraties scheid je met een puntkomma. Handig voor één element, maar onhandig als je later veel elementen moet aanpassen. _(bron: 3. Introduction to CSS.pptx, dia 6)_
    - voorbeeld: `<p style="color: red; background: green">`
- `<style> span {color: red;} </style>` — **Interne CSS in style-tag**: Met de <style>-tag in de <head> schrijf je CSS-regels die gelden voor meerdere elementen in hetzelfde HTML-document. Zo pas je een stijl op één plaats aan in plaats van bij elk element apart. _(bron: 3. Introduction to CSS.pptx, dia 8)_
    - voorbeeld: `<style> span {color: red;} </style>`
- `<link rel="stylesheet" type="text/css" href="style.css">` — **Extern stylesheet koppelen**: Zet je CSS-regels in een apart .css-bestand en koppel dat met de <link>-tag in de <head>. Zo kunnen meerdere HTML-pagina's dezelfde stijl delen. _(bron: 3. Introduction to CSS.pptx, dia 10)_
    - voorbeeld: `<link rel="stylesheet" type="text/css" href="style.css">`

### Layout & positie
- `display: inline-block;` — **Blok- of inline-gedrag wijzigen**: display verandert hoe een element zich gedraagt: als blokelement (eigen regel, breedte/hoogte instelbaar) of als inline-element (op dezelfde regel). inline-block zet elementen naast elkaar maar laat breedte en hoogte toe. _(bron: 3. Introduction to CSS.pptx, dia 72)_
    - voorbeeld: `display: inline-block;`
- `visibility: hidden;` — **Element verbergen, plaats houden**: visibility: hidden maakt een element onzichtbaar, maar het blijft zijn plaats innemen in de layout. visible (standaard) toont het. Bij display: none verdwijnt de plaats wel. _(bron: 3. Introduction to CSS.pptx, dia 73)_
    - voorbeeld: `visibility: hidden;`
- `top / bottom / left / right` — **Afstanden voor positionering**: Deze eigenschappen geven de plaats van een element aan met een afstand (px, %, em …). Wat ze precies doen hangt af van de position-waarde; bij position: static (standaard) hebben ze geen effect. _(bron: 3. Introduction to CSS.pptx, dia 74)_
- `position: relative; top: 50px;` — **Verschuiven t.o.v. normale plaats**: Met position: relative verschuif je een element ten opzichte van zijn normale plaats. top: 50px schuift het 50 pixels naar beneden. De oorspronkelijke ruimte blijft behouden en andere elementen bewegen niet mee. _(bron: 3. Introduction to CSS.pptx, dia 76)_
    - voorbeeld: `position: relative; top: 50px;`
- `position: fixed;` — **Vast op het scherm plaatsen**: Met position: fixed staat een element vast ten opzichte van het browservenster en blijft het op dezelfde plek, ook bij scrollen. top, bottom, left en right geven de afstand tot de randen van het venster. De oorspronkelijke ruimte blijft niet behouden. _(bron: 3. Introduction to CSS.pptx, dia 78)_
    - voorbeeld: `position: fixed;`
- `position: absolute;` — **Plaatsen binnen gepositioneerde voorouder**: Met position: absolute plaats je een element ten opzichte van de dichtstbijzijnde voorouder die zelf een position heeft (niet static). Daarom geef je de container vaak position: relative. De oorspronkelijke ruimte blijft niet behouden. _(bron: 3. Introduction to CSS.pptx, dia 80)_
    - voorbeeld: `position: absolute;`
- `overflow: auto;` — **Wat met te veel inhoud**: overflow bepaalt wat er gebeurt als de inhoud groter is dan het element. _(bron: 3. Introduction to CSS.pptx, dia 81)_
- `float: right;` — **Element links of rechts laten zweven**: float haalt een element uit de normale volgorde en zet het links of rechts in zijn ouder-element. Tekst en andere elementen lopen er dan omheen. _(bron: 3. Introduction to CSS.pptx, dia 82)_
    - voorbeeld: `float: right;`

### Overige eigenschappen
- `list-style-type: none;` — **Opsommingsteken van lijst kiezen**: list-style-type bepaalt hoe de tekens voor lijstitems eruitzien. Voor een ongeordende lijst (<ul>): disc (standaard, gevuld bolletje), circle (leeg bolletje), square (vierkantje) of none (geen teken). _(bron: 3. Introduction to CSS.pptx, dia 67)_
    - voorbeeld: `list-style-type: none;`
- `list-style-type: upper-roman;` — **Nummering van geordende lijst**: Voor een geordende lijst (<ol>) kies je met list-style-type hoe er genummerd wordt: cijfers, letters of Romeinse cijfers. _(bron: 3. Introduction to CSS.pptx, dia 68)_
    - voorbeeld: `list-style-type: upper-roman;`
- `border-collapse: collapse;` — **Tabelranden samenvoegen**: Geef je een tabel en haar cellen een rand, dan krijg je dubbele lijnen met kleine tussenruimtes. Met border-collapse: collapse worden aangrenzende randen één lijn; separate houdt ze apart. Zet dit op het <table>-element. _(bron: 3. Introduction to CSS.pptx, dia 70)_
    - voorbeeld: `border-collapse: collapse;`

### Selectors
- `p {color: red;}` — **Alle elementen van één soort opmaken**: Een CSS-regel met de naam van een tag als selector geldt voor alle elementen van die soort. Hier worden alle paragrafen rood. _(bron: 2. Introduction to HTML.pptx, dia 14)_
- `.klasse {…}` — **Elementen met een klasse opmaken**: Een punt voor een naam selecteert alle elementen met die klasse. Zo krijgt .vader {color: red;} alle elementen met class="vader" rode tekst. _(bron: 2. Introduction to HTML.pptx, dia 54)_
- `#id {…}` — **Element met een id opmaken**: Een hekje (#) voor een naam selecteert het element met dat id. Zo krijgt #kenobi {color: blue;} het element met id="kenobi" blauwe tekst. _(bron: 2. Introduction to HTML.pptx, dia 56)_
- `div {background: red;}` — **Elementselector: alle elementen van type**: Een elementselector is gewoon de tagnaam. De stijl geldt voor alle elementen van dat type op de pagina. _(bron: 3. Introduction to CSS.pptx, dia 14)_
    - voorbeeld: `div {background: red;}`
- `#Nemo {background: orange;}` — **ID-selector: één element**: Met # gevolgd door de naam van een id selecteer je het ene element met dat id-attribuut. Een id is uniek op de pagina. _(bron: 3. Introduction to CSS.pptx, dia 15)_
    - voorbeeld: `#Nemo {background: orange;}`
- `.TopGun {background: green;}` — **Klasseselector: elementen met klasse**: Met een punt gevolgd door de klassenaam selecteer je alle elementen met dat class-attribuut, ook als het verschillende tags zijn. _(bron: 3. Introduction to CSS.pptx, dia 16)_
    - voorbeeld: `.TopGun {background: green;}`
- `h1, h4 {background: red;}` — **Selectors groeperen met komma**: Scheid je selectors met een komma, dan geldt de stijl voor alle elementen die aan minstens één van de selectors voldoen. Zo hoef je dezelfde regel niet twee keer te schrijven. _(bron: 3. Introduction to CSS.pptx, dia 17)_
    - voorbeeld: `h1, h4 {background: red;}`
- `p.BB.JP {background: orange;}` — **Samengestelde selector (zonder spaties)**: Plak je selectors aan elkaar zonder spatie, dan moet een element aan alle delen tegelijk voldoen. p.BB kiest <p>-elementen met klasse BB; p.BB.JP kiest <p>-elementen die zowel klasse BB als JP hebben. _(bron: 3. Introduction to CSS.pptx, dia 19)_
    - voorbeeld: `p.BB.JP {background: orange;}`
- `div h3 {background: red;}` — **Afstammelingenselector (spatie)**: Een spatie tussen selectors betekent: het rechtse element moet ergens binnen het linkse element zitten (kind, kleinkind of dieper). Je kunt er meer aan elkaar rijgen, bv. div blockquote h3. _(bron: 3. Introduction to CSS.pptx, dia 22)_
    - voorbeeld: `div h3 {background: red;}`
- `div > h3 {background: red;}` — **Kindselector: enkel directe kinderen**: Met > selecteer je alleen elementen die een direct kind zijn van het linkse element, zonder ander element ertussen. _(bron: 3. Introduction to CSS.pptx, dia 24)_
    - voorbeeld: `div > h3 {background: red;}`
- `#Cedric ~ h3 {background: purple;}` — **Siblingselector: latere broers/zussen**: Met ~ selecteer je elementen met dezelfde ouder die ergens ná het linkse element komen, niet noodzakelijk er direct na. _(bron: 3. Introduction to CSS.pptx, dia 26)_
    - voorbeeld: `#Cedric ~ h3 {background: purple;}`
- `#Cedric + h3 {background: green;}` — **Directe siblingselector (+)**: Met + selecteer je enkel het element dat onmiddellijk ná het linkse element komt en dezelfde ouder heeft. _(bron: 3. Introduction to CSS.pptx, dia 28)_
    - voorbeeld: `#Cedric + h3 {background: green;}`
- `#Jasper :first-child {background: purple;}` — **Eerste kind binnen een ouder**: :first-child selecteert een element dat het eerste is van zijn siblings. Met de ouder-selector, een spatie en dan :first-child kies je het eerste kind binnen die ouder. _(bron: 3. Introduction to CSS.pptx, dia 32)_
    - voorbeeld: `#Jasper :first-child {background: purple;}`
- `h3:first-child {background: orange;}` — **Elk h3 dat eerste kind is**: Zet je :first-child zonder spatie achter een element- of klasseselector, dan kies je elk element van dat type dat het eerste is tussen zijn siblings. _(bron: 3. Introduction to CSS.pptx, dia 33)_
    - voorbeeld: `h3:first-child {background: orange;}`
- `#Bart :last-child {background: red;}` — **Laatste kind selecteren**: :last-child selecteert het laatste element tussen zijn siblings. Met een spatie (#Bart :last-child) kies je het laatste kind van Bart; zonder spatie (h3:last-child) kies je elke <h3> die het laatste kind is. _(bron: 3. Introduction to CSS.pptx, dia 34)_
    - voorbeeld: `#Bart :last-child {background: red;}`
- `#Jasper :nth-child(3) {background: purple;}` — **Het n-de kind selecteren**: :nth-child(n) selecteert het element op positie n tussen zijn siblings (tellen begint bij 1). n kan een getal of een formule zijn. _(bron: 3. Introduction to CSS.pptx, dia 36)_
    - voorbeeld: `#Jasper :nth-child(3) {background: purple;}`
- `#Jasper :nth-child(2n) {background: green;}` — **Kinderen op even posities**: Met de formule 2n selecteer je alle kinderen op een even positie (2, 4, 6 …). _(bron: 3. Introduction to CSS.pptx, dia 37)_
    - voorbeeld: `#Jasper :nth-child(2n) {background: green;}`
- `#Jasper :nth-child(2n+1) {background: red;}` — **Kinderen op oneven posities**: Met de formule 2n+1 selecteer je alle kinderen op een oneven positie (1, 3, 5 …). _(bron: 3. Introduction to CSS.pptx, dia 38)_
    - voorbeeld: `#Jasper :nth-child(2n+1) {background: red;}`
- `#Jasper h3:first-of-type {background: red;}` — **Eerste element van een type**: :first-of-type selecteert het eerste element van een bepaald type tussen zijn siblings, ook als er andere elementen vóór staan. Tussen h3 en :first-of-type staat geen spatie. _(bron: 3. Introduction to CSS.pptx, dia 39)_
    - voorbeeld: `#Jasper h3:first-of-type {background: red;}`
- `#Jasper h3:last-of-type {background: red;}` — **Laatste element van een type**: :last-of-type selecteert het laatste element van een bepaald type tussen zijn siblings, ook als er nog andere elementen na komen. _(bron: 3. Introduction to CSS.pptx, dia 40)_
    - voorbeeld: `#Jasper h3:last-of-type {background: red;}`
- `#Paco:hover {background: orange;}` — **Stijl bij muis erover**: :hover past de stijl toe zolang de gebruiker met de muiscursor over het element beweegt. _(bron: 3. Introduction to CSS.pptx, dia 41)_
    - voorbeeld: `#Paco:hover {background: orange;}`
- `#Paco:active {background: purple;}` — **Stijl tijdens het klikken**: :active past de stijl toe op het moment dat de gebruiker op het element klikt (de muisknop ingedrukt houdt). _(bron: 3. Introduction to CSS.pptx, dia 42)_
    - voorbeeld: `#Paco:active {background: purple;}`
- `a:link / a:visited` — **Onbezochte en bezochte links**: :link geeft een stijl aan links die nog niet bezocht zijn, :visited aan links die je al bezocht hebt. Voorbeeld: a:link {background: white;} en a:visited {background: red;}. _(bron: 3. Introduction to CSS.pptx, dia 43)_

### Tekst & lettertype
- `color` — **Tekstkleur instellen**: Stelt de kleur van de tekst in, bv. color: red; of color: blue;. _(bron: 2. Introduction to HTML.pptx, dia 54)_
- `font-family` — **Lettertype kiezen**: Stelt het lettertype van de tekst in. Een naam met spaties zet je tussen aanhalingstekens, bv. font-family: 'Comic Sans MS';. _(bron: 2. Introduction to HTML.pptx, dia 58)_
- `font-size: 1.2em;` — **Lettergrootte instellen**: font-size bepaalt hoe groot de tekst in een element is. _(bron: 3. Introduction to CSS.pptx, dia 58)_
- `font-weight: bold;` — **Letterdikte (vet) instellen**: font-weight bepaalt hoe dik of vet de tekst is. _(bron: 3. Introduction to CSS.pptx, dia 59)_
- `font-style: italic;` — **Schuine tekst instellen**: font-style bepaalt of tekst rechtop of schuin staat. _(bron: 3. Introduction to CSS.pptx, dia 60)_
- `font-family: 'Atkinson Hyperlegible', sans-serif;` — **Lettertype kiezen met reserve**: font-family kiest het lettertype. Je geeft een lijst gescheiden door komma's: lukt het eerste niet, dan gebruikt de browser het volgende. Een naam van meerdere woorden zet je tussen aanhalingstekens. _(bron: 3. Introduction to CSS.pptx, dia 62)_
    - voorbeeld: `font-family: 'Atkinson Hyperlegible', sans-serif;`
- `font-variant: small-caps;` — **Tekst in kleine hoofdletters**: font-variant voegt een stijleffect toe aan tekst. Met small-caps worden kleine letters getoond als kleinere hoofdletters; normal is de gewone weergave. _(bron: 3. Introduction to CSS.pptx, dia 63)_
- `letter-spacing: 40px;` — **Ruimte tussen letters**: letter-spacing regelt de afstand tussen de letters. Je kunt px, em, % en andere eenheden gebruiken. _(bron: 3. Introduction to CSS.pptx, dia 64)_
    - voorbeeld: `letter-spacing: 40px;`
- `word-spacing: …` — **Ruimte tussen woorden**: word-spacing regelt de afstand tussen woorden, net zoals letter-spacing dat doet tussen letters. Je kunt px, em, % en andere eenheden gebruiken. _(bron: 3. Introduction to CSS.pptx, dia 64)_
- `text-align: center;` — **Tekst horizontaal uitlijnen**: text-align bepaalt hoe tekst horizontaal uitgelijnd wordt binnen een element: links, rechts, gecentreerd of uitgevuld over de hele breedte. _(bron: 3. Introduction to CSS.pptx, dia 65)_
    - voorbeeld: `text-align: center;`
- `text-decoration: line-through;` — **Lijn onder, boven of door tekst**: text-decoration voegt een lijn toe aan tekst of haalt die weg (bv. de standaard onderstreping van links). _(bron: 3. Introduction to CSS.pptx, dia 66)_
    - voorbeeld: `text-decoration: line-through;`

## PHP (96)

### Arrays
- `array("a", "b", "c")` — **Array maken met array()**: De klassieke manier om een array te maken: de array()-functie krijgt een lijst waarden gescheiden door komma's. Een array bewaart meerdere waarden in één variabele; de waarden hoeven niet van hetzelfde type te zijn. _(bron: 4. Fundamentals of PHP.pptx, dia 33)_
    - voorbeeld: `array("a", "b", "c")`
- `["a", "b", "c"]` — **Geïndexeerde array (korte syntax)**: Maakt een array met vierkante haken, korter dan array(). In zo'n geïndexeerde array krijgt elke waarde automatisch een nummer (index) als sleutel, te beginnen bij 0. _(bron: 4. Fundamentals of PHP.pptx, dia 34)_
    - voorbeeld: `["a", "b", "c"]`
- `["sleutel" => waarde]` — **Associatieve array met eigen sleutels**: In een associatieve array kies je zelf de sleutel van elke waarde (een string of een getal). Je schrijft de sleutel, dan =>, dan de waarde. _(bron: 4. Fundamentals of PHP.pptx, dia 35)_
    - voorbeeld: `["sleutel" => waarde]`
- `print_r($array);` — **Volledige array tonen**: Toont de hele inhoud van een array, met alle sleutels en waarden. echo en print werken niet voor een volledige array. _(bron: 4. Fundamentals of PHP.pptx, dia 37)_
- `$array[sleutel]` — **Waarde uit array ophalen**: Haalt één waarde uit een array: de naam van de array gevolgd door de sleutel (index of naam) tussen vierkante haken. Die waarde kun je tonen, bewaren of in je code gebruiken. _(bron: 4. Fundamentals of PHP.pptx, dia 38)_
    - voorbeeld: `$array[sleutel]`
- `$array[sleutel] = waarde;` — **Waarde in array aanpassen/toevoegen**: Geeft de waarde bij een bepaalde sleutel een nieuwe waarde. Bestaat de sleutel al, dan wordt de waarde overschreven; is het een nieuwe sleutel, dan wordt een nieuw element toegevoegd. _(bron: 4. Fundamentals of PHP.pptx, dia 40)_
    - voorbeeld: `$array[sleutel] = waarde;`
- `$array[] = waarde;` — **Waarde achteraan toevoegen**: Lege vierkante haken voegen een nieuwe waarde toe aan het einde van de array (met de volgende vrije index). Doet hetzelfde als array_push. _(bron: 4. Fundamentals of PHP.pptx, dia 41)_
    - voorbeeld: `$array[] = waarde;`
- `array_push($array, waarde);` — **Waarde aan einde toevoegen**: Voegt een nieuwe waarde toe aan het einde van een array. _(bron: 4. Fundamentals of PHP.pptx, dia 41)_
- `array_unshift($array, waarde);` — **Waarde vooraan toevoegen**: Voegt een nieuwe waarde toe aan het begin van een array; de indexen van de andere elementen schuiven op. _(bron: 4. Fundamentals of PHP.pptx, dia 41)_
    - voorbeeld: `array_unshift($array, waarde);`
- `array_shift($array);` — **Eerste waarde verwijderen**: Verwijdert de eerste waarde van een array. _(bron: 4. Fundamentals of PHP.pptx, dia 43)_
- `array_pop($array);` — **Laatste waarde verwijderen**: Verwijdert de laatste waarde van een array. _(bron: 4. Fundamentals of PHP.pptx, dia 43)_
- `unset($array[sleutel]);` — **Specifieke waarde uit array verwijderen**: Verwijdert het element met de opgegeven sleutel uit een array. _(bron: 4. Fundamentals of PHP.pptx, dia 43)_
    - voorbeeld: `unset($array[sleutel]);`
- `$array[key1][key2]` — **Waarde uit tweedimensionale array**: Een tweedimensionale array is een array waarvan elk element zelf een array is (zoals een rooster). Met de eerste sleutel kies je de sub-array, met de tweede het element daarin. _(bron: 4. Fundamentals of PHP.pptx, dia 45)_
    - voorbeeld: `$array[key1][key2]`
- `count($array)` — **Aantal elementen in array**: Geeft het aantal elementen in een array terug. _(bron: 4. Fundamentals of PHP.pptx, dia 83)_
    - voorbeeld: `count($array)`
- `in_array(waarde, $array)` — **Controleren of waarde in array zit**: Geeft true als de gezochte waarde in de array voorkomt en false als ze er niet in zit, zonder dat je zelf een lus moet schrijven. _(bron: 4. Fundamentals of PHP.pptx, dia 92)_
    - voorbeeld: `in_array(waarde, $array)`
- `print_r($_POST)` — **Hele array leesbaar tonen**: Toont alle sleutels en waarden van een array, handig om te zien wat een formulier verstuurd heeft. De sleutels zijn de name-attributen van de velden. _(bron: 5. Dynamic Web Pages.pptx, dia 15)_
    - voorbeeld: `print_r($_POST)` → Array ( [surname] => Mathias [submit] => Submit Query )
- `in_array($zoek, $array)` — **Zit waarde in array?**: Geeft true als de gezochte waarde in de array voorkomt, anders false. In de les: nagaan of een chemische stof in de voorraad zit. _(bron: 5. Dynamic Web Pages.pptx, dia 22)_

### Basis & syntax
- `php bestand.php` — **PHP-script uitvoeren in terminal**: Voert een PHP-bestand uit via de command line: typ php gevolgd door de naam van het bestand. Bewaar je code eerst in een bestand met de extensie .php en ga in de terminal naar de map waar dat bestand staat. _(bron: 4. Fundamentals of PHP.pptx, dia 5)_
    - voorbeeld: `php bestand.php` → Hello World!
- `<?php ... ?>` — **PHP-code afbakenen met tags**: PHP voert alleen de code uit die tussen <?php en ?> staat; een bestand mag meerdere van die blokken bevatten. Alles buiten de PHP-tags (bv. gewone tekst of HTML) blijft ongewijzigd staan. _(bron: 4. Fundamentals of PHP.pptx, dia 8)_
- `;` — **Statement afsluiten met puntkomma**: Elke PHP-opdracht (statement) eindigt met een puntkomma. Een vergeten puntkomma is een veelvoorkomende oorzaak van fouten. Uitzondering: if-, while-, for- en foreach-blokken met accolades krijgen geen puntkomma na de }. _(bron: 4. Fundamentals of PHP.pptx, dia 10)_
- `// commentaar` — **Commentaar op één regel**: Alles na // (of #) tot het einde van de regel is commentaar: PHP negeert het. Je gebruikt het om uitleg bij je code te schrijven, zodat jij en anderen later nog weten wat de code doet. _(bron: 4. Fundamentals of PHP.pptx, dia 11)_
- `/* commentaar */` — **Commentaar over meerdere regels**: Alles tussen /* en */ is commentaar, ook als het over meerdere regels loopt. Handig voor langere uitleg of om een stuk code tijdelijk uit te schakelen. _(bron: 4. Fundamentals of PHP.pptx, dia 11)_
- `var_dump(waarde);` — **Type en waarde in detail tonen**: var_dump() toont gedetailleerde info over een waarde: het datatype én de waarde zelf (werkt ook voor arrays). Handig om te controleren welk type iets heeft of om het resultaat van een voorwaarde (true/false) te zien. _(bron: 4. Fundamentals of PHP.pptx, dia 14)_
    - voorbeeld: `var_dump(waarde);`
- `echo waarde;` — **Waarde of variabele tonen**: echo toont een waarde of de inhoud van een variabele (in de terminal of later in de browser). Het werkt voor getallen, tekst en booleans. _(bron: 4. Fundamentals of PHP.pptx, dia 17)_
    - voorbeeld: `echo waarde;`
- `echo "tekst", $variabele;` — **Meerdere waarden tegelijk tonen**: Met echo kun je meerdere waarden en variabelen in één keer tonen door ze met komma's te scheiden. Ze worden achter elkaar getoond. _(bron: 4. Fundamentals of PHP.pptx, dia 18)_
    - voorbeeld: `echo "tekst", $variabele;`
- `print(waarde);` — **Eén waarde tonen met print**: print() toont net als echo een waarde of variabele, maar slechts één tegelijk. Wil je meerdere stukken tonen, combineer ze dan eerst met concatenatie (.) of interpolatie. _(bron: 4. Fundamentals of PHP.pptx, dia 19)_
- `<?php echo "<div>...</div>"; ?>` — **PHP in een HTML-pagina**: Je kunt PHP-code tussen <?php en ?> midden in HTML zetten. De server voert de code uit en vervangt ze door de HTML die echo maakt. Een bestand met PHP-code moet altijd de extensie .php hebben, ook als er vooral HTML in staat. _(bron: 5. Dynamic Web Pages.pptx, dia 3)_
    - voorbeeld: `<?php echo "<div>...</div>"; ?>` → <div>The ABV is: 5.25%</div>
- `php -S localhost:8080` — **Ingebouwde PHP-webserver starten**: Start in de terminal een kleine webserver die je .php-bestanden uitvoert. Voer het uit in de map met je bestanden (de root-map) en open daarna de getoonde URL in de browser; standaard wordt index.php of index.html getoond. Een ander bestand open je door /bestandsnaam achter de URL te zetten (bv. localhost:8080/ABV.php). _(bron: 5. Dynamic Web Pages.pptx, dia 4)_
- `include('bestand')` — **Ander bestand invoegen**: Voegt de inhoud van een .html- of .php-bestand in op die plek, bv. een header of footer die op veel pagina's terugkomt. Ontbreekt het bestand, dan gaat het script gewoon verder. _(bron: 5. Dynamic Web Pages.pptx, dia 8)_
- `require('bestand')` — **Bestand invoegen, stoppen als ontbreekt**: Voegt net als include een bestand in, maar stopt het script met een fatale fout als het bestand ontbreekt. Gebruik het voor onderdelen die er zeker moeten zijn. _(bron: 5. Dynamic Web Pages.pptx, dia 9)_
    - voorbeeld: `require('bestand')`
- `background: <?php echo $kleur; ?>;` — **PHP gebruiken binnen CSS**: PHP kan ook in een <style>-blok staan om een CSS-waarde te kiezen, bv. de achtergrondkleur afhankelijk van wat de gebruiker indiende. In de les: rood als de knop is ingedrukt, anders wit. _(bron: 5. Dynamic Web Pages.pptx, dia 20)_

### Formulieren
- `$_POST['naam']` — **Formulierwaarde ophalen (POST)**: Ingebouwde array met de gegevens van een formulier met method="POST". De sleutel is de name van het invoerveld, de waarde is wat de gebruiker invulde. _(bron: 5. Dynamic Web Pages.pptx, dia 16)_
    - voorbeeld: `$_POST['naam']`
- `if (isset($_POST['submit'])) { }` — **Controleren of formulier verstuurd is**: isset() geeft true als de naam in de array bestaat. Zo voer je de verwerkingscode pas uit nadat op de verzendknop (name="submit") is geklikt, en vermijd je fouten. Ook te gebruiken om te zien of een checkbox aangevinkt is. _(bron: 5. Dynamic Web Pages.pptx, dia 16)_
- `$_GET['naam']` — **Formulierwaarde ophalen (GET)**: Ingebouwde array met de gegevens van een formulier met method="GET" (de waarden staan ook in de URL). Werkt verder net als $_POST. _(bron: 5. Dynamic Web Pages.pptx, dia 17)_
- `$_FILES['naam']['tmp_name']` — **Tijdelijke locatie van upload**: Een geüpload bestand wordt eerst op een tijdelijke plaats bewaard. De ingebouwde array $_FILES bevat info over het bestand (naam, type, grootte …); via 'tmp_name' krijg je het pad om het bestand te lezen. _(bron: 5. Dynamic Web Pages.pptx, dia 48)_
    - voorbeeld: `$_FILES['naam']['tmp_name']` → [name] => sequences.fasta
[type] => application/octet-stream
[tmp_name] => /tmp/phpxYaBEg
[error] => 0
[size] => 123
- `file($bestand)` — **Bestand inlezen als array regels**: Leest een bestand en geeft een array terug met één element per regel. Elke regel bevat nog het regeleinde \n, dus gebruik trim() voor je ermee vergelijkt. _(bron: 5. Dynamic Web Pages.pptx, dia 49)_
- `file_get_contents($bestand)` — **Hele bestand als één string**: Leest de volledige inhoud van een bestand in als één string. Met explode("\n", ...) splits je die daarna in regels. _(bron: 5. Dynamic Web Pages.pptx, dia 49)_

### Functies
- `isset($variabele)` — **Controleren of variabele bestaat**: Geeft true als de variabele (of het array-element) bestaat en een waarde heeft, en false als ze niet bestaat of null is. Handig om te controleren of een sleutel in een array zit of of er een argument meegegeven is. _(bron: 4. Fundamentals of PHP.pptx, dia 76)_
    - voorbeeld: `isset($variabele)`
- `empty($variabele)` — **Controleren of variabele leeg is**: Geeft true als de variabele niet bestaat of een 'lege' waarde heeft: 0, een lege string "", null, false of een lege array []. _(bron: 4. Fundamentals of PHP.pptx, dia 78)_
    - voorbeeld: `empty($variabele)`
- `exit("bericht"); / die("bericht");` — **Script onmiddellijk stoppen**: exit() en die() stoppen het volledige script meteen; code daarna wordt niet meer uitgevoerd. Een optionele tekst tussen de haakjes wordt eerst nog getoond. Verschil met break: break stopt enkel een lus, de rest van het script loopt verder. _(bron: 4. Fundamentals of PHP.pptx, dia 80)_
    - voorbeeld: `exit("bericht"); / die("bericht");`
- `rand(min, max)` — **Willekeurig geheel getal**: Geeft een willekeurig geheel getal tussen min en max (beide inbegrepen). Wil je een willekeurig kommagetal, deel dan het resultaat, bv. rand(0, 10) / 10 geeft 0.0, 0.1 ... 1.0. _(bron: 4. Fundamentals of PHP.pptx, dia 93)_
    - voorbeeld: `rand(min, max)`
- `sleep(seconden);` — **Script even pauzeren**: Pauzeert de uitvoering van het script gedurende het opgegeven aantal seconden. _(bron: 4. Fundamentals of PHP.pptx, dia 95)_
    - voorbeeld: `sleep(seconden);`
- `unset($variabele);` — **Variabele verwijderen**: Verwijdert een variabele of een array-element, zodat ze daarna niet meer bestaat. _(bron: 4. Fundamentals of PHP.pptx, dia 97)_
    - voorbeeld: `unset($variabele);`

### Lussen
- `while (voorwaarde) { ... }` — **Herhalen zolang voorwaarde waar is**: Een while-lus controleert telkens de voorwaarde en voert het codeblok opnieuw uit zolang die true is. Zodra de voorwaarde false is, stopt de lus. Zorg dat er in de lus iets verandert, anders stopt ze nooit. _(bron: 4. Fundamentals of PHP.pptx, dia 66)_
    - voorbeeld: `while (voorwaarde) { ... }`
- `while (true) { ... }` — **Oneindige lus**: Omdat de voorwaarde altijd true is, stopt deze lus nooit vanzelf. Stop het script in de terminal met Ctrl + C. _(bron: 4. Fundamentals of PHP.pptx, dia 66)_
    - voorbeeld: `while (true) { ... }`
- `for (start; voorwaarde; update) { ... }` — **Lus met teller**: Een for-lus heeft drie delen tussen haakjes: een startwaarde voor de lusvariabele, een voorwaarde die bepaalt of de lus doorgaat, en een update die de lusvariabele na elke ronde aanpast (meestal +1 of -1). _(bron: 4. Fundamentals of PHP.pptx, dia 68)_
    - voorbeeld: `for (start; voorwaarde; update) { ... }`
- `foreach ($array as $value) { ... }` — **Elke waarde van array overlopen**: Een foreach-lus overloopt elk element van een array: bij elke ronde krijgt $value de volgende waarde uit de array. _(bron: 4. Fundamentals of PHP.pptx, dia 70)_
    - voorbeeld: `foreach ($array as $value) { ... }`
- `foreach ($array as $key => $value) { ... }` — **Sleutels en waarden van array overlopen**: Deze foreach-lus overloopt een array en geeft bij elke ronde zowel de sleutel ($key) als de bijhorende waarde ($value). Handig bij associatieve arrays. _(bron: 4. Fundamentals of PHP.pptx, dia 71)_
    - voorbeeld: `foreach ($array as $key => $value) { ... }` → A Minotaur is a Half-human, half-bull.
A Mermaid is a Half-human, half-fish.
- `continue;` — **Naar volgende lusronde springen**: continue slaat de rest van de huidige ronde van een lus over en gaat meteen verder met de volgende ronde. _(bron: 4. Fundamentals of PHP.pptx, dia 73)_
    - voorbeeld: `continue;`
- `break;` — **Lus volledig stoppen**: break stopt de lus meteen; het script gaat verder met de code na de lus. Handig om niet verder te zoeken als je gevonden hebt wat je zocht. _(bron: 4. Fundamentals of PHP.pptx, dia 73)_
    - voorbeeld: `break;`

### Operatoren
- `$a + $b, $a - $b, $a * $b, $a / $b` — **Optellen, aftrekken, vermenigvuldigen, delen**: Rekenkundige operatoren voor berekeningen met integers en floats. -$a geeft het tegengestelde van $a. Het resultaat kun je tonen of in een variabele bewaren; met haakjes bepaal je wat eerst berekend wordt. _(bron: 4. Fundamentals of PHP.pptx, dia 27)_
    - voorbeeld: `$a + $b, $a - $b, $a * $b, $a / $b`
- `$a ** $b` — **Machtsverheffing**: Verheft $a tot de macht $b. _(bron: 4. Fundamentals of PHP.pptx, dia 27)_
    - voorbeeld: `$a ** $b`
- `$a % $b` — **Rest na deling (modulus)**: Geeft de rest als je $a deelt door $b. Vaak gebruikt om deelbaarheid te testen: $getal % 2 is 0 bij een even getal en 1 bij een oneven getal. _(bron: 4. Fundamentals of PHP.pptx, dia 28)_
    - voorbeeld: `$a % $b`
- `$var++ en $var--` — **Variabele met 1 verhogen/verlagen**: ++ verhoogt de waarde van een numerieke variabele met 1, -- verlaagt ze met 1. Een kortere schrijfwijze voor $var = $var + 1 en $var = $var - 1; veel gebruikt in lussen. _(bron: 4. Fundamentals of PHP.pptx, dia 30)_
    - voorbeeld: `$var++ en $var--`
- `$var += n en $var -= n` — **Getal optellen bij/aftrekken van variabele**: += telt een getal op bij de huidige waarde van een variabele, -= trekt er een getal van af. Korter dan $var = $var + n. _(bron: 4. Fundamentals of PHP.pptx, dia 30)_
    - voorbeeld: `$var += n en $var -= n`
- `$a == $b` — **Gelijk aan (na type juggling)**: Geeft true als $a gelijk is aan $b, nadat PHP de types zo nodig automatisch omgezet heeft (type juggling). Let op: één = kent een waarde toe, == vergelijkt. _(bron: 4. Fundamentals of PHP.pptx, dia 51)_
    - voorbeeld: `$a == $b`
- `$a === $b` — **Identiek: zelfde waarde én type**: Geeft enkel true als $a en $b dezelfde waarde én hetzelfde type hebben; PHP zet niets automatisch om. Zo is false == 0 true, maar false === 0 false. _(bron: 4. Fundamentals of PHP.pptx, dia 51)_
- `$a != $b` — **Niet gelijk aan**: Geeft true als $a niet gelijk is aan $b, na automatische typeomzetting. Zo is false != 0 false, omdat PHP 0 als false beschouwt. _(bron: 4. Fundamentals of PHP.pptx, dia 51)_
- `$a !== $b` — **Niet identiek**: Geeft true als $a en $b een andere waarde óf een ander type hebben. Zo is false !== 0 true, omdat het ene een boolean en het andere een integer is. _(bron: 4. Fundamentals of PHP.pptx, dia 51)_
- `<  >  <=  >=` — **Kleiner/groter dan vergelijken**: Vergelijkt twee waarden: < kleiner dan, > groter dan, <= kleiner dan of gelijk aan, >= groter dan of gelijk aan. Het resultaat is altijd true of false. _(bron: 4. Fundamentals of PHP.pptx, dia 51)_
    - voorbeeld: `<  >  <=  >=`
- `Type juggling` — **Automatische omzetting van types**: PHP zet waarden van verschillende types automatisch om als je ze vergelijkt, wat soms verrassend is: false == 0 is bijvoorbeeld true. Gebruik === en !== als ook het type moet kloppen. _(bron: 4. Fundamentals of PHP.pptx, dia 52)_
- `$a && $b (and)` — **Logische EN**: Geeft true als beide voorwaarden waar zijn. && en and doen hetzelfde. _(bron: 4. Fundamentals of PHP.pptx, dia 54)_
- `$a || $b (or)` — **Logische OF**: Geeft true als minstens één van de voorwaarden waar is. || en or doen hetzelfde. _(bron: 4. Fundamentals of PHP.pptx, dia 54)_
    - voorbeeld: `$a || $b (or)`
- `$a xor $b` — **Exclusieve OF**: Geeft true als precies één van de twee voorwaarden waar is, maar niet allebei. _(bron: 4. Fundamentals of PHP.pptx, dia 54)_
- `!$a` — **Logische NIET (omkeren)**: Keert het resultaat van een voorwaarde om: true wordt false en false wordt true. _(bron: 4. Fundamentals of PHP.pptx, dia 54)_
    - voorbeeld: `!$a`
- `$a && ($b || $c)` — **Haakjes in samengestelde voorwaarden**: Je mag meerdere logische operatoren combineren. Wat tussen haakjes staat wordt eerst geëvalueerd, zo bepaal je de juiste volgorde. _(bron: 4. Fundamentals of PHP.pptx, dia 56)_
    - voorbeeld: `$a && ($b || $c)`
- `$a ?? 'standaard'` — **Standaardwaarde als iets ontbreekt**: De ??-operator geeft de linkerwaarde als die bestaat (en niet null is), anders de rechterwaarde. Korte vorm van if (isset(...)) ... else .... _(bron: 5. Dynamic Web Pages.pptx, dia 41)_
    - voorbeeld: `$a ?? 'standaard'`

### Strings
- `preg_replace(patroon, vervanging, $string)` — **Patroon vervangen in een string**: Zoekt een patroon (reguliere expressie) in een string en vervangt het. Met $1, $2 ... verwijs je in de vervanging naar de stukken tussen haakjes in het patroon. _(bron: 4. Fundamentals of PHP.pptx, dia 11)_
    - voorbeeld: `preg_replace(patroon, vervanging, $string)`
- `"tekst" . $variabele` — **Strings aan elkaar plakken (concatenatie)**: De punt (.) plakt twee of meer waarden achter elkaar tot één string. Het resultaat kun je tonen met echo of print, of in een nieuwe variabele bewaren. _(bron: 4. Fundamentals of PHP.pptx, dia 20)_
    - voorbeeld: `"tekst" . $variabele`
- `"tekst $variabele"` — **Variabele in string zetten (interpolatie)**: Zet je een variabele binnen een string met dubbele aanhalingstekens, dan vult PHP automatisch de waarde van die variabele in. Dit heet string-interpolatie. Je kunt de naam ook tussen accolades zetten, bv. "{$naam}". _(bron: 4. Fundamentals of PHP.pptx, dia 21)_
    - voorbeeld: `"tekst $variabele"`
- `'tekst met $'` — **String zonder interpolatie (enkele quotes)**: In een string tussen enkele aanhalingstekens vult PHP geen variabelen in: $ en de naam blijven letterlijk staan. Gebruik dit voor tekst met een dollarteken, zoals 'K$sha'; met dubbele quotes zou PHP $sha als (onbestaande) variabele zien en een waarschuwing geven. _(bron: 4. Fundamentals of PHP.pptx, dia 22)_
    - voorbeeld: `'tekst met $'`
- `Escape sequence` — **Speciaal teken in een string**: Een escape sequence is een backslash (\) gevolgd door een teken, waarmee je tekens in een string zet die anders moeilijk in te voegen zijn, zoals een nieuwe regel, een tab, een $ of een aanhalingsteken. In dubbele quotes werken \n, \t, \$, \" en \\; in enkele quotes alleen \' en \\. _(bron: 4. Fundamentals of PHP.pptx, dia 23)_
- `\n` — **Nieuwe regel in string**: \n zet een nieuwe regel (newline) in een string met dubbele aanhalingstekens: de tekst erna begint op de volgende regel. Veel gebruikt om uitvoer in de terminal netjes onder elkaar te krijgen. _(bron: 4. Fundamentals of PHP.pptx, dia 23)_
    - voorbeeld: `\n` → And here we are
Half past three in the morning
I can't get no sleep
- `\t` — **Tab in string**: \t zet een tab (horizontale inspringing) in een string met dubbele aanhalingstekens. _(bron: 4. Fundamentals of PHP.pptx, dia 23)_
- `\$` — **Letterlijk dollarteken in string**: \$ zet een gewoon dollarteken in een string met dubbele aanhalingstekens, zonder dat PHP er een variabele in ziet. _(bron: 4. Fundamentals of PHP.pptx, dia 23)_
    - voorbeeld: `\$`
- `\\` — **Letterlijke backslash in string**: \\ zet één gewone backslash (\) in een string; werkt zowel tussen enkele als dubbele aanhalingstekens. _(bron: 4. Fundamentals of PHP.pptx, dia 23)_
- `\" en \'` — **Aanhalingsteken in string zetten**: \" zet een dubbel aanhalingsteken in een string tussen dubbele quotes; \' zet een enkel aanhalingsteken in een string tussen enkele quotes. Zo sluit het aanhalingsteken de string niet per ongeluk af. _(bron: 4. Fundamentals of PHP.pptx, dia 24)_
    - voorbeeld: `\" en \'` → Faithless's "Insomnia" lyrics:
- `strlen($string)` — **Lengte van een string**: Geeft het aantal tekens in een string terug, spaties en leestekens inbegrepen. _(bron: 4. Fundamentals of PHP.pptx, dia 82)_
    - voorbeeld: `strlen($string)`
- `str_split($string)` — **String opsplitsen in tekens**: Splitst een string in losse tekens en geeft een array terug waarin elk element één teken is. _(bron: 4. Fundamentals of PHP.pptx, dia 84)_
    - voorbeeld: `str_split($string)`
- `strtolower($string)` — **Tekst naar kleine letters**: Geeft een nieuwe string terug waarin alle letters omgezet zijn naar kleine letters. _(bron: 4. Fundamentals of PHP.pptx, dia 85)_
    - voorbeeld: `strtolower($string)` → these php examples are ridiculous!
- `strtoupper($string)` — **Tekst naar hoofdletters**: Geeft een nieuwe string terug waarin alle letters omgezet zijn naar hoofdletters. _(bron: 4. Fundamentals of PHP.pptx, dia 86)_
    - voorbeeld: `strtoupper($string)` → I KNOW THESE PHP EXAMPLES ARE RIDICULOUS!
- `explode(delimiter, $string)` — **String splitsen in een array**: Knipt een string in stukken telkens waar de delimiter voorkomt en geeft die stukken terug als array. De delimiter zelf verdwijnt. _(bron: 4. Fundamentals of PHP.pptx, dia 87)_
    - voorbeeld: `explode(delimiter, $string)`
- `implode(delimiter, $array)` — **Array samenvoegen tot string**: Plakt alle elementen van een array aan elkaar tot één string, met de delimiter ertussen. Het omgekeerde van explode(). _(bron: 4. Fundamentals of PHP.pptx, dia 89)_
    - voorbeeld: `implode(delimiter, $array)`
- `preg_match('/^>/', $string)` — **Patroon zoeken in een string**: Controleert of een patroon (een reguliere expressie) in een string voorkomt en geeft true (1) of false (0) terug. Het patroon '/^>/' checkt of de string begint met >, handig om de headerregels van een (multi)FASTA-bestand te herkennen. _(bron: 4. Fundamentals of PHP.pptx, dia 90)_
    - voorbeeld: `preg_match('/^>/', $string)`
- `trim($string)` — **Witruimte aan begin/einde verwijderen**: Verwijdert spaties, tabs en newlines aan het begin en het einde van een string; witruimte in het midden blijft staan. Handig om ingevoerde gegevens zoals e-mailadressen op te kuisen. _(bron: 4. Fundamentals of PHP.pptx, dia 96)_
    - voorbeeld: `trim($string)`
- `strtolower($tekst)` — **Tekst naar kleine letters**: Zet alle letters van een string om naar kleine letters. Handig om invoer te vergelijken, ongeacht of de gebruiker hoofdletters typte. _(bron: 5. Dynamic Web Pages.pptx, dia 22)_
- `explode("\n", $tekst)` — **Tekst splitsen in array**: Knipt een string op elke plaats waar het scheidingsteken staat en geeft een array van de stukken. Met "\n" splits je tekst (bv. uit een textarea of file_get_contents()) in aparte regels. _(bron: 5. Dynamic Web Pages.pptx, dia 38)_
- `trim($tekst)` — **Spaties en regeleinden weghalen**: Verwijdert witruimte zoals spaties en \n aan het begin en einde van een string. Nodig bij regels uit file(), anders klopt een vergelijking zoals $line == "Aurelia aurita" niet. _(bron: 5. Dynamic Web Pages.pptx, dia 50)_

### Variabelen & types
- `Scalaire types (integer, float, string, boolean)` — **De vier eenvoudigste datatypes**: Scalaire waarden zijn de eenvoudigste soorten data en stellen één enkele waarde voor. Er zijn vier types: integer (geheel getal, bv. 42), float (kommagetal, bv. 3.14), string (tekst tussen ' ' of " ", bv. "Don't panic") en boolean (true of false). _(bron: 4. Fundamentals of PHP.pptx, dia 14)_
- `$naam = waarde;` — **Waarde opslaan in een variabele**: Maakt een variabele en geeft ze een waarde, zodat je die later in het script kunt gebruiken. Een variabelenaam begint met $ gevolgd door letters, cijfers of underscores, maar mag niet met een cijfer beginnen (dus $Mona_Lisa mag, $123VanGogh of $Mona-Lisa niet). Een nieuwe waarde toekennen overschrijft de oude. _(bron: 4. Fundamentals of PHP.pptx, dia 15)_
    - voorbeeld: `$naam = waarde;`
- `$naam = $naam . " " . $naam;` — **Variabele bijwerken met huidige waarde**: Je kunt een variabele aanpassen op basis van haar huidige waarde: rechts van = wordt eerst de nieuwe waarde berekend met de oude, en die wordt daarna terug in dezelfde variabele gestoken. _(bron: 4. Fundamentals of PHP.pptx, dia 25)_
    - voorbeeld: `$naam = $naam . " " . $naam;` → papio papio
- `$argv` — **Command-line argumenten uitlezen**: $argv is een ingebouwde array met de argumenten die je bij het starten van het script in de terminal meegeeft. $argv[0] is altijd de naam van het script zelf, $argv[1] het eerste argument, $argv[2] het tweede, enzovoort. _(bron: 4. Fundamentals of PHP.pptx, dia 47)_
    - voorbeeld: `$argv`

### Voorwaarden
- `if (voorwaarde) { ... }` — **Code uitvoeren als voorwaarde waar is**: Een if-statement controleert een voorwaarde en voert de code tussen de accolades alleen uit als die voorwaarde true is; anders wordt die code overgeslagen. Er komt geen puntkomma na het blok. Een nieuwe if start een aparte, onafhankelijke voorwaarde. _(bron: 4. Fundamentals of PHP.pptx, dia 57)_
    - voorbeeld: `if (voorwaarde) { ... }`
- `elseif (voorwaarde) { ... }` — **Extra voorwaarde als vorige onwaar**: elseif test een extra voorwaarde als alle voorgaande if/elseif-voorwaarden onwaar waren. Je mag er meerdere na een if zetten; zodra er één waar is, worden de volgende niet meer gecontroleerd. _(bron: 4. Fundamentals of PHP.pptx, dia 58)_
    - voorbeeld: `elseif (voorwaarde) { ... }`
- `else { ... }` — **Code als niets anders klopt**: else voert zijn code uit als alle voorgaande if- en elseif-voorwaarden onwaar zijn. Het heeft zelf geen voorwaarde en staat altijd als laatste. Een conditional heeft precies één if, optioneel één else en nul of meer elseifs. _(bron: 4. Fundamentals of PHP.pptx, dia 60)_
    - voorbeeld: `else { ... }`
- `Geneste if` — **Voorwaarde binnen een voorwaarde**: Je kunt een if-statement binnen een ander if-blok plaatsen (nesten). Zo behandel je ingewikkeldere logica waarbij een beslissing van meerdere voorwaarden afhangt. _(bron: 4. Fundamentals of PHP.pptx, dia 63)_

## PyMOL (78)

### Afbeeldingen
- `ray 1200,800` — **Figuur renderen met ray tracing**: Maakt met de ingebouwde ray tracing een mooie, scherpe figuur met schaduwen, hier met een resolutie van 1200 op 800 pixels. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 37)_
- `File > Export Image As > PNG...` — **Figuur opslaan als PNG**: Bewaart het huidige beeld (bv. na ray) als PNG-afbeelding. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 37)_
- `png figuur.png` — **Beeld opslaan als PNG**: Bewaart het huidige beeld (bv. na ray) als PNG-afbeelding, zonder via het menu te gaan. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 6)_

### Instellingen
- `Setting > Edit All...` — **Alle parameters bekijken en wijzigen**: Opent een lijst met alle parameters die je in PyMOL kunt instellen, zoals sphere_scale of transparency. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 36)_
- `set sphere_scale, 0.8, chain B` — **Bolgrootte van keten B verkleinen**: Stelt de grootte van de bollen (show spheres) in op 0,8 keer de normale grootte, enkel voor keten B. Algemene vorm: set parameter, waarde, selectie. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 36)_
- `set transparency, 0.4` — **Oppervlak doorschijnend maken**: Maakt het oppervlak (surface) voor 40% doorzichtig, zodat de cartoon eronder zichtbaar blijft. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 38)_
- `File > Edit pymolrc` — **Opstartinstellingen bewerken**: Opent het bestand .pymolrc in je thuismap. De commando's daarin voert PyMOL automatisch uit bij elke start, bv. een witte achtergrond. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 3)_
- `bg_color white` — **Witte achtergrond instellen**: Maakt de achtergrond van het canvas wit. In .pymolrc wordt dit de standaard bij elke start. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 3)_
- `set seq_view_format, 1` — **Drielettercodes in sequentie**: Toont in de sequentieweergave (Display > Sequence) de residuen met drielettercodes (bv. ALA) in plaats van eenlettercodes. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 3)_

### Kleuren
- `color red, chain A` — **Kleur keten A rood**: Geeft alle atomen van keten A een rode kleur.
- `color red, hetatm` — **Alle niet-eiwitatomen rood kleuren**: Voorbeeld van de basisvorm van een PyMOL-commando: een sleutelwoord gevolgd door één of meer argumenten, gescheiden door komma's. Dit kleurt alle HETATM-atomen (niet-eiwit, bv. liganden) rood. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 21)_
- `C > by ss` — **Kleuren volgens secundaire structuur**: In het Color-menu (knop C) naast een object kies je by ss om helices, β-strengen en lussen elk een eigen kleur te geven. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 25)_
- `color cyan, chain A` — **Keten A cyaan kleuren**: Geeft alle atomen van keten A de kleur cyaan. Zo kun je verschillende ketens van elkaar onderscheiden. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 28)_
- `color magenta, chain B + chain C + chain D` — **Meerdere ketens tegelijk kleuren**: Kleurt de ketens B, C en D in één keer magenta. Met + voeg je selecties samen (zoals or). _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 28)_
- `color skyblue, chain A` — **Keten A hemelsblauw kleuren**: Kleurt keten A in skyblue. PyMOL kent veel kleurnamen, bv. firebrick (donkerrood), forest (donkergroen) en gray50. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 6)_
- `color orange, resn DA` — **DNA-nucleotiden per type kleuren**: Kleurt alle adenine-nucleotiden (residunaam DA) oranje. Doe hetzelfde met een andere kleur voor DG, DT en DC om elk type nucleotide een eigen kleur te geven. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 7)_

### Laden & bewaren
- `png eiwit.png, dpi=300, ray=1` — **Bewaar mooie afbeelding**: Rendert het beeld in hoge kwaliteit en bewaart het als eiwit.png met 300 dpi, geschikt voor een verslag.
- `fetch 1ubq` — **Download ubiquitine uit PDB**: Haalt de structuur met PDB-code 1UBQ (ubiquitine) op uit de Protein Data Bank en opent ze.
- `fetch 3CIG` — **Structuur laden uit de PDB**: Downloadt een structuur rechtstreeks van de Protein Data Bank via internet en laadt ze in PyMOL. Het enige argument is de PDB-code. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 23)_
- `File > Open` — **Coördinatenbestand openen van laptop**: Via het menu File > Open kies je een bestand met atoomcoördinaten (bv. een .pdb- of .cif-bestand) dat al op je computer staat. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 23)_
- `delete 3CIG` — **Object verwijderen**: Verwijdert een object (hier de structuur 3CIG) uit PyMOL. Handig om opnieuw te beginnen of een selectie op te ruimen. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 26)_
- `File > Save Session As...` — **Sessie bewaren als .pse**: Bewaart de volledige toestand van PyMOL (structuren, weergaven, kleuren, camerastandpunt) als .pse-bestand, zodat je later verder kunt werken. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 37)_
- `split_states 2JQY` — **NMR-modellen in aparte objecten**: Zet elk model (state) van een NMR-structuur in een apart object, zodat je ze apart kunt kleuren, tonen of op elkaar passen. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 3)_
- `save sessie.pse` — **Sessie bewaren via commando**: Bewaart de volledige PyMOL-sessie als .pse-bestand (hetzelfde als File > Save Session As...). Met een extensie zoals .pdb bewaar je enkel de coördinaten. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 6)_

### Metingen
- `distance hbonds, sel1, sel2, mode=2` — **Waterstofbruggen tonen**: Tekent stippellijnen voor mogelijke polaire contacten (waterstofbruggen) tussen twee selecties en bewaart ze als object hbonds. Via de A-knop > find > polar contacts kan hetzelfde met de muis. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 16)_

### Scripts
- `# commentaar` — **Commentaar in script**: Een regel die met # begint is commentaar en wordt niet uitgevoerd. Zet commentaar in PyMOL-scripts op een aparte regel, niet achter code. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 5)_
- `from pymol import cmd` — **PyMOL-commando's in Python laden**: Eerste regel van een Python-script voor PyMOL: importeert de module cmd. Daarna roep je elk PyMOL-commando op als cmd.functienaam(...), bv. cmd.color('red'). _(bron: SB-workshop-4-molecular-visualization.pptx, dia 5)_
- `cmd.create('achain','chain A')` — **Object maken in Python**: Python-versie van create achain, chain A: maakt een nieuw object achain met de atomen van keten A. Argumenten staan tussen haakjes en aanhalingstekens. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 5)_
- `cmd.bg_color('white')` — **Witte achtergrond in Python**: Python-versie van bg_color white: maakt de achtergrond wit. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 5)_
- `cmd.color('red','resn asp or resn glu')` — **Zure residuen rood kleuren**: Kleurt alle aspartaat- en glutamaatresiduen (negatief geladen) rood. Het script simplecolors.py kleurt op dezelfde manier arg, lys en his (positief) blauw. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 7)_
- `cmd.show('cartoon')` — **Cartoon tonen in Python**: Python-versie van show cartoon. Met een tweede argument beperk je het tot een selectie, bv. cmd.show('cartoon','achain + bchain'). _(bron: SB-workshop-4-molecular-visualization.pptx, dia 7)_
- `cmd.hide('lines')` — **Lijnen verbergen in Python**: Python-versie van hide lines: verbergt de standaard lijnenweergave. Met cmd.hide('all') verberg je alles. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 7)_
- `run simplecolors.py` — **Python-script uitvoeren**: Voert een Python-script uit in PyMOL. Zet het script in je thuismap (dezelfde map als .pymolrc) en laad eerst een structuur, bv. fetch 1BBB. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 7)_
- `run findseq.py` — **findseq-script laden**: Laadt het gedownloade script findseq.py in PyMOL, zodat het nieuwe commando findseq beschikbaar wordt. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 9)_

### Selecties
- `select actief, resi 40-50` — **Selecteer residuen 40-50**: Maakt een selectie met de naam 'actief' van residu 40 tot en met 50, die je daarna kan kleuren of tonen.
- `create nieuw_object, selectie` — **Nieuw object uit selectie**: Maakt een nieuw, apart object van een selectie, bv. create achain, chain A. Dat object verschijnt in de objectlijst en kun je apart tonen, verbergen en kleuren. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 22)_
- `hetatm` — **Niet-standaard atomen selecteren**: Sleutelwoord dat alle atomen selecteert die in het PDB-bestand als HETATM staan: liganden, water, zouten, gemodificeerde residuen. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 26)_
- `select ///A/10` — **Residu 10 van keten A**: Hiërarchische selectie van links naar rechts: /model/segment/chain/residue/atom. Lege velden betekenen 'alles'. Dit selecteert residu 10 in keten A. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 30)_
- `select ////10-20/CA` — **CA-atomen van residuen 10-20**: Hiërarchische selectie van de atomen met naam CA (α-koolstof) in residuen 10 tot 20, in eender welke keten. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 30)_
- `select 42/C,N` — **C- en N-atoom van residu 42**: Hiërarchische selectie van rechts naar links zonder beginnende /: residu/atoom. Selecteert de atomen C en N in residu 42. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 30)_
- `resi` — **Selecteren op residunummer**: Sleutelwoord om residuen te selecteren op hun nummer (residue index), bv. resi 10 of een bereik resi 10:20. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 31)_
- `resn` — **Selecteren op residunaam**: Sleutelwoord om residuen te selecteren op hun naam (residue name), bv. resn ALA voor alanine of resn HEM voor de heemgroep. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 31)_
- `select chain B and resi 10:20` — **Residuen 10-20 van keten B**: Algebraïsche selectie: termen zoals chain en resi worden gecombineerd met and. De selectie heet standaard (sele) en wordt in het beeld aangeduid. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 31)_
    - voorbeeld: `select chain B and resi 10:20` → Selector: selection "sele" defined with 81 atoms.
- `and / or / not` — **Selecties combineren**: Logische operatoren om algebraïsche selecties te combineren: and (beide), or (één van beide), not (uitsluiten). _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 31)_
- `elem` — **Selecteren op chemisch element**: Sleutelwoord om atomen te selecteren op element, bv. elem O voor alle zuurstofatomen. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 32)_
- `name` — **Selecteren op atoomnaam**: Sleutelwoord om atomen te selecteren op hun naam in het PDB-bestand, bv. name CA voor de α-koolstofatomen of name N voor de backbone-stikstof. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 32)_
- `all` — **Alle atomen selecteren**: Sleutelwoord dat alle atomen van alle objecten selecteert, bv. in hide all. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 32)_
- `select resn ALA and name N` — **Backbone-stikstof van alanines**: Selecteert de backbone-stikstofatomen (name N) van alle alanineresiduen. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 32)_
- `select elem O and not name OH` — **Zuurstofatomen behalve hydroxylen**: Selecteert alle zuurstofatomen behalve de atomen met naam OH (hydroxylgroepen). _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 32)_
- `around` — **Atomen in de buurt selecteren**: Selecteert atomen binnen een bepaalde afstand (in ångström) van een bestaande selectie, bv. hetatm around 5. Handig om te zien welke residuen betrokken zijn in een bindingsplaats. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 32)_
- `chain` — **Selecteren op keten**: Sleutelwoord om atomen van een bepaalde keten te selecteren, bv. chain A. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 33)_
- `select byres (elem Ca around 3.5)` — **Residuen rond calcium selecteren**: Selecteert alle volledige residuen (byres) met minstens één atoom binnen 3,5 Å van een calciumion. Zo vind je welke residuen calcium binden. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 5)_
- `create nag, resn NAG` — **Glycanen in apart object**: Maakt een apart object (laag) met de NAG-residuen (N-acetylglucosamine van glycosylaties), zodat je snel ziet waar de glycosylaties zitten (bv. N281, N433, N486). _(bron: SB-workshop-3-molecular-visualization.pptx, dia 12)_
- `findseq DDMPNAL, achain, found` — **Sequentiemotief zoeken in structuur**: Zoekt een sequentiemotief in een object en maakt er een selectie van. Werkt pas nadat je run findseq.py hebt uitgevoerd (script van de PyMOL-wiki). Kleine letters en reguliere expressies (bv. F.*W) werken ook. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 9)_

### Vergelijken
- `align 3CIG, 1ZIW` — **Structuur op andere structuur passen**: Legt de eerste structuur (muis-TLR3) zo goed mogelijk op de tweede (humaan TLR3) door ze te verschuiven en draaien. Daarna kun je verschillen tussen beide zichtbaar maken, bv. met een andere kleur. PyMOL toont de RMSD als maat voor het verschil. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 2)_
- `align 2IWW, 2JQY` — **Kristal- en NMR-structuur superponeren**: Legt de kristalstructuur (gesloten vorm) op de NMR-structuur, zodat je het verschil in lus 6 van OmpG kunt zien. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 3)_
- `align 1RE2, 1HFX` — **Lysozym en α-lactalbumine superponeren**: Legt de twee structuren structureel op elkaar om te bevestigen dat ze dezelfde vouw (fold) hebben. _(bron: SB-workshop-5-databases-tools.pptx, dia 6)_
- `align 2LHB and resn HEM, 3TM3 and resn HEM` — **Structuren superponeren op heemgroep**: Legt twee hemoglobinestructuren over elkaar door enkel de heemgroepen (residunaam HEM) uit te lijnen. Handig wanneer de sequenties te verschillend zijn om de volledige ketens uit te lijnen. _(bron: SB-07-structural-functional-assignment.pptx, dia 29)_

### Weergave
- `as cartoon` — **Toon enkel als lint**: Verbergt de andere weergaven en toont het eiwit als lint, zodat je helices en sheets goed ziet.
- `Objectlijst` — **Geladen objecten tonen/verbergen**: De objectlijst rechts toont welke objecten (structuren, selecties) geladen zijn. Klik op de naam van een object om het te verbergen of weer te tonen. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 18)_
- `A / S / H / L / C-knoppen` — **Menuknoppen naast elk object**: Naast elk object in de objectlijst staan vijf knoppen die een keuzemenu openen. Zo kun je veel doen zonder commando's te typen. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 19)_
- `hide all` — **Alle weergaven verbergen**: Verbergt alle weergaven van alle objecten, zodat je daarna zelf kiest wat je toont. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 24)_
- `show sticks` — **Toon als staafjes**: Toont de atomen en bindingen als staafjes (sticks). Handig om zijketens of liganden in detail te bekijken. Met hide sticks verberg je ze weer. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 24)_
- `show cartoon` — **Toon als cartoon**: Toont het eiwit als cartoon: helices als spiralen en β-strengen als pijlen. Deze weergave toont enkel de eiwitketen (secundaire structuur), geen liganden. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 24)_
- `show spheres, hetatm` — **HETATM-atomen als bollen tonen**: Toont alle HETATM-atomen (liganden, water, zouten, gemodificeerde residuen) als bollen. Vergeet niet de selectie na de komma te vermelden, anders geldt het voor alles. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 26)_
- `show representatie, selectie` — **Algemene vorm van show**: Algemene vorm van show (en hide): eerst de weergave, dan welke atomen. Mogelijke weergaven zijn lines, sticks, spheres, surface, mesh, dots, ribbon en cartoon. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 27)_
- `Wizard > Demo > Representations` — **Demo van alle weergaven**: Via het hoofdmenu Wizard > Demo > Representations toont PyMOL een voorbeeld van alle weergaven naast elkaar: lines, sticks, spheres, surface, mesh, dots, ribbon en cartoon. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 27)_
- `hide cartoon, chain A` — **Cartoon van keten A verbergen**: Verbergt enkel de cartoonweergave van keten A; de andere ketens blijven zichtbaar. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 28)_
- `show ribbon, chain A` — **Keten A als lint tonen**: Toont keten A als ribbon: een dunne lijn die de ruggengraat (backbone) van de keten volgt. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 28)_
- `Display > Sequence` — **Sequentie boven het beeld tonen**: Toont de aminozuursequentie bovenaan het canvas. Klikken op residuen in de sequentie selecteert ze in de structuur. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 33)_
- `Display > Background` — **Achtergrondkleur kiezen**: Via Display > Background kies je de achtergrondkleur van het canvas (bv. wit voor figuren). _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 33)_
- `show surface` — **Moleculair oppervlak tonen**: Toont het moleculaire oppervlak van de structuur. Handig om bv. een bindingsholte te zien. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 38)_
- `show sticks, resi 511-521` — **Bereik residuen als sticks**: Toont de residuen 511 tot 521 als staafjes, bv. om de dsRNA-interactieplaats van TLR3 (met N515 en N517) in detail te bekijken. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 5)_
- `set all_states, on` — **Alle NMR-modellen tegelijk tonen**: Toont alle states (modellen/conformeren) van een object tegelijk, bv. het NMR-ensemble van 2JQY, zodat je de verschillen tussen de conformeren ziet. Met set all_states, off zie je weer één model. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 3)_
- `show surface, chain A` — **Oppervlak van één keten**: Toont enkel keten A als moleculair oppervlak, terwijl je de andere keten bv. als cartoon toont. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 6)_
- `show sticks, resn TRP and resi 2` — **Tryptofaan 2 als sticks**: Toont het tryptofaan op positie 2 (in de adhesie-arm van cadherine) als staafjes, in beide ketens. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 6)_
- `show sticks, resn DA+DC+DG+DT` — **DNA als staafjes tonen**: Toont alle DNA-nucleotiden als staafjes. Met + som je meerdere residunamen op binnen één resn. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 7)_
- `alter resi 100-103, ss='L'` — **Secundaire structuur handmatig wijzigen**: Verandert de secundaire structuur van residuen, bv. een korte helix die als lus (L) getoond moet worden. Daarna voer je rebuild uit om de cartoon opnieuw te tekenen. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 12)_

## Structurele biologie (180)

### Algemeen
- `Structurele bio-informatica` — **Bio-informatica op 3D-structuren**: Het deel van de bio-informatica dat theorie, methoden en toepassingen (algoritmes, analyses, voorspellingen) gebruikt op structurele data van biomoleculen. In deze cursus gaat het om eiwitten, DNA, RNA, liganden en complexen daarvan. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 6)_

### Aminozuren
- `Aminozuur` — **Bouwsteen van eiwitten**: Klein molecule met een centraal Cα-atoom waaraan een aminogroep (NH2), een carboxylgroep (COOH), een H-atoom en een variabele zijketen (R-groep) hangen. Alleen de R-groep verschilt tussen de 20 standaard-aminozuren en bepaalt hun chemische eigenschappen. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 10)_
- `Posttranslationele modificatie (PTM)` — **Aanpassing na eiwitsynthese**: Chemische wijziging van een aminozuur nadat het eiwit gemaakt is. Voorbeelden: glycosylering (suikergroep), fosforylering (fosfaatgroep op Ser, Thr, Tyr of His) en methylering (methylgroep op Lys of Arg). _(bron: SB-02-fundamentals-protein-structure.pptx, dia 14)_
- `Aminozuurklassen (hydrofoob, polair, geladen)` — **Indeling volgens zijketen**: De 20 aminozuren worden ingedeeld volgens hun zijketen: hydrofoob (meestal verborgen in het binnenste van het eiwit), polair (hydrofiel, vaak aan het oppervlak in contact met water) en geladen (positief of negatief). Subklassen zijn bv. aromatisch of alifatisch, groot of klein. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 17)_
- `Proline en glycine` — **Twee uitzonderlijke aminozuren**: Bij proline is de zijketen verbonden met de eigen aminogroep (cyclisch), waardoor de keten minder flexibel is. Glycine heeft enkel een H-atoom als zijketen, is niet chiraal en is juist zeer flexibel. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 26)_
- `L- en D-aminozuren (chiraliteit)` — **Spiegelbeeldvormen van aminozuren**: Een chiraal C-atoom is gebonden aan 4 verschillende groepen en bestaat in twee spiegelbeeldvormen: L en D. Eiwitten zijn (bijna) uitsluitend opgebouwd uit L-aminozuren. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 28)_

### Basenparing
- `Watson-Crick-basenparing` — **Complementaire paren A:T en G:C**: In een dubbele helix vormen basen van tegenoverliggende strengen paren via H-bruggen: A met T (2 H-bruggen) en G met C (3 H-bruggen); in RNA A met U. Dit volgt uit de regel van Chargaff: evenveel A als T en evenveel G als C. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 24)_
- `Grote en kleine groef` — **Twee groeven in de dubbele helix**: De suikerfosfaatruggengraat vormt aan het oppervlak van de helix twee groeven van verschillende grootte: de grote (major) en de kleine (minor) groef. Eiwitten en geneesmiddelen kunnen in deze groeven binden. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 27)_
- `Base stacking` — **Basenparen gestapeld op elkaar**: De basenparen liggen als vlakke platen op elkaar gestapeld. Deze stapelinteracties houden de verticale schikking bij elkaar, maar laten toch wat flexibiliteit toe. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 29)_
- `Basenpaarparameters` — **Geometrie van basenparen beschrijven**: Verschuivingen en rotaties binnen één basenpaar (shear, stretch, stagger; buckle, propeller twist, opening) en tussen opeenvolgende basenparen (shift, slide, rise; tilt, roll, twist) beschrijven de exacte 3D-geometrie van een helix. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 30)_

### Biologische context
- `Toll-like receptor (TLR)` — **Receptor van het aangeboren immuunsysteem**: Familie van eiwitten die micro-organismen herkennen wanneer die onze fysieke barrières (bv. de huid) doorbreken, en dan een immuunrespons activeren. TLR3 herkent dubbelstrengig RNA en heeft een hoefijzervormige (horseshoe) structuur. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 2)_
- `dsRNA` — **Dubbelstrengig RNA**: RNA dat uit twee complementaire strengen bestaat en een helix vormt. Veel virussen maken dsRNA; TLR3 herkent het en vormt er een dimeer op (structuur 3CIY). _(bron: SB-workshop-2-molecular-visualization.pptx, dia 2)_
- `Transcriptiefactor (TF)` — **Eiwit dat transcriptie regelt**: Eiwit dat op een specifieke DNA-sequentie bindt en zo de transcriptie van een gen regelt, alleen of samen met andere eiwitten. Een activator bevordert de rekrutering van RNA-polymerase, een repressor remt ze. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 6)_
- `Desmosoom` — **Sterke celverbinding**: Een celverbinding die naburige cellen stevig aan elkaar vastmaakt via adhesie-eiwitten (cadherines) die in het cytoplasma aan keratinefilamenten gekoppeld zijn. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 4)_
- `Cadherine` — **Calciumafhankelijk adhesie-eiwit**: Adhesie-eiwitten die cellen aan elkaar hechten, bv. in desmosomen. Tussen de cadherinedomeinen zitten calciumionen, en een N-terminaal tryptofaan (Trp2) in de adhesie-arm verankert twee cadherines aan elkaar. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 5)_
- `Isoform` — **Variant van een eiwit**: Verschillende vormen van een eiwit die van hetzelfde gen komen, bv. door alternatieve splicing van verschillende transcripten. _(bron: SB-workshop-5-databases-tools.pptx, dia 2)_

### DNA en geneesmiddelen
- `Intercalatie` — **Molecule schuift tussen basenparen**: Een vlak, aromatisch molecule (bv. ethidiumbromide of het kankermedicijn daunomycine) schuift tussen twee basenparen in het midden van de DNA-helix. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 62)_
- `Groefbinder` — **Molecule bindt in DNA-groef**: Molecule dat in een groef van DNA bindt, meestal de kleine groef van B-DNA (bv. netropsine). Groefbinders zijn vaak sterk sequentiespecifiek. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 64)_
- `DNA-alkylering` — **Covalente binding aan basen**: Alkylerende stoffen binden covalent aan de basen en verstoren de DNA-structuur, wat leidt tot celdood als de schade niet hersteld wordt. Voorbeeld: cisplatine, gebruikt bij kankerbehandeling. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 66)_

### DNA-vormen
- `B-DNA` — **Klassieke Watson-Crick-helix**: De meest voorkomende DNA-vorm: rechtsdraaiende dubbele helix met ~10 basenparen per winding, antiparallelle strengen, C2'-endo pucker en anti-glycosidische hoeken. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 56)_
- `A-DNA` — **Bredere, compactere rechtsdraaiende helix**: Rechtsdraaiende helix met C3'-endo pucker en ~11 basenparen per winding. De helix is breder dan B-DNA, met een diepe, smalle grote groef en een brede, ondiepe kleine groef. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 58)_
- `Z-DNA` — **Linksdraaiende zigzag-helix**: Ongewone linksdraaiende DNA-vorm (ontdekt in 1979) met een zigzaggende fosfaatruggengraat. Ze komt vooral voor bij afwisselende C- en G-sequenties. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 60)_
- `G-quadruplex` — **Vierstrengige guaninerijke structuur**: Viervoudige helix gevormd door guaninerijke sequenties, gestabiliseerd door een Na⁺- of K⁺-ion in het midden. Komt biologisch voor in telomeren. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 69)_

### Databanken
- `wwPDB` — **Wereldwijde organisatie achter PDB**: De worldwide Protein Data Bank (sinds 2003) beheert één internationaal PDB-archief. Leden waar je structuren kunt indienen en ophalen: RCSB PDB (VS), PDBe (Europa), PDBj (Japan), BMRB (NMR-data) en EMDB (EM-data). _(bron: SB-05-data-representation-databases.pptx, dia 4)_
- `PDB-ID` — **Code van vier tekens**: Elke PDB-entry heeft een unieke code van vier tekens (bv. 1AEW). Typ die in het zoekvak van rcsb.org om rechtstreeks naar de Structure Summary-pagina te gaan, met o.a. downloadopties, literatuur en validatiegegevens. _(bron: SB-05-data-representation-databases.pptx, dia 6)_
- `MMDB` — **NCBI-databank van 3D-structuren**: Molecular Modeling Database: experimentele structuren uit de PDB met extra informatie, zoals chemische grafen, berekende 3D-domeinen, links naar literatuur en gebonden liganden. _(bron: SB-05-data-representation-databases.pptx, dia 68)_
- `CDD, CD-search en CDART` — **Geconserveerde domeinen zoeken**: CDD is de Conserved Domain Database van NCBI (>50 000 domeinmodellen). Met CD-search vind je de geconserveerde domeinen in een eiwitsequentie; CDART zoekt eiwitten met een gelijkaardige domeinarchitectuur. _(bron: SB-05-data-representation-databases.pptx, dia 76)_
- `PSSM en RPS-BLAST` — **Profiel per positie in alignment**: Een PSSM (position-specific scoring matrix) geeft per positie van een meervoudige alignering scores: geconserveerde posities scoren hoog. RPS-BLAST (gebruikt door CD-search) zoekt met een sequentie in een databank van zulke PSSM's, in één keer (reverse t.o.v. PSI-BLAST). _(bron: SB-05-data-representation-databases.pptx, dia 80)_
- `PDBsum` — **Visueel overzicht per PDB-structuur**: Databank (EBI) met per PDB-entry afbeeldingen en analyses: componenten, domeinen, eiwit-eiwitinteracties, clefts, PROCHECK-kwaliteit en links naar andere databanken. _(bron: SB-05-data-representation-databases.pptx, dia 92)_

### Databanken & tools
- `SCOP` — **Structuurclassificatie van eiwitten**: Structural Classification Of Proteins: deelt eiwitdomeinen hiërarchisch in volgens hun structuur en evolutionaire verwantschap (klasse, fold, superfamilie, familie). _(bron: SB-workshop-5-databases-tools.pptx, dia 6)_
- `CATH` — **Hiërarchische domeinclassificatie**: Databank die eiwitdomeinen indeelt in vier niveaus: Class, Architecture, Topology en Homologous superfamily. _(bron: SB-workshop-5-databases-tools.pptx, dia 6)_
- `PDBeFold` — **Webtool voor structurele alignment**: Webtool van PDBe om eiwitstructuren in 3D te vergelijken: een pairwise alignment van twee structuren of een multiple 3D-alignment van meerdere structuren, bv. verschillende cadherines. _(bron: SB-workshop-5-databases-tools.pptx, dia 7)_

### Eiwitclassificatie
- `Globulaire, membraan- en fibreuze eiwitten` — **Drie grote eiwitgroepen**: Indeling op basis van globale biochemische eigenschappen: globulaire eiwitten (bv. myoglobine), membraaneiwitten (bv. rodopsine) en fibreuze eiwitten (bv. collageen). _(bron: SB-02-fundamentals-protein-structure.pptx, dia 95)_
- `All α, all β, α/β en α+β` — **Structuurklassen volgens secundaire structuur**: Classificatie (Levitt & Chothia, 1976) volgens de dominante secundaire structuur. All α: bijna enkel helices; all β: bijna enkel sheets; α/β: helices en strands gemengd (vaak parallelle strands verbonden door helices); α+β: helices en sheets in aparte delen. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 96)_

### Eiwitproductie
- `Expressie en labeling van eiwitten` — **Eiwit maken voor structuuronderzoek**: Eiwitten worden meestal in E. coli geproduceerd, voor NMR gelabeld met stabiele isotopen of voor röntgen met zware atomen (bv. selenomethionine). Complexe eukaryote eiwitten vragen soms gist-, insecten- of menselijke cellen. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 13)_
- `Apo- en holo-enzym` — **Enzym zonder en met cofactor**: Een apo-enzym is het eiwitdeel zonder cofactor; samen met de cofactor (metaalion of co-enzym) vormt het het katalytisch actieve holo-enzym. Eiwitten die cofactoren nodig hebben, zijn soms moeilijk correct te produceren. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 14)_
- `His-tag (6xHis)` — **Label om eiwit te zuiveren**: Reeks van zes histidines die aan het uiteinde (bv. de N-terminus) van een recombinant eiwit wordt gezet, zodat het eiwit makkelijk gezuiverd kan worden. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 65)_
- `Dynamic light scattering (DLS)` — **Homogeniteit van eiwitstaal meten**: Meet laserlicht dat door opgeloste moleculen verstrooid wordt om hun grootte en grootteverdeling te bepalen. Zo ziet men of een staal monodispers (homogeen, één grootte) of polydispers (verschillende groottes, aggregatie) is, wat belangrijk is voor kristallisatie. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 66)_

### Eiwitstructuur
- `N-glycosylatie (N-glycaan)` — **Suikerketen op asparagine**: Suikerketens die aan de stikstof van een asparagine (N) van een eiwit gekoppeld zijn. In PDB-structuren verschijnen ze als HETATM-residuen zoals NAG. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 4)_
- `Ectodomein` — **Deel van receptor buiten de cel**: Het deel van een membraaneiwit dat buiten de cel ligt. Bij TLR3 bindt het ectodomein het dsRNA. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 4)_
- `Rel Homology Region (RHR)` — **Gedeelde N-terminale regio Rel/NF-κB**: N-terminale regio van ongeveer 300 aminozuren die alle eiwitten van de Rel/NF-κB-familie gemeen hebben. Ze zorgt voor de dimerisatie en de binding aan DNA. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 10)_
- `Geconserveerd residu` — **Residu dat niet verandert**: Een residu dat op dezelfde positie in alle vergeleken sequenties identiek is. Geconserveerde residuen zijn vaak belangrijk voor structuur of functie. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 11)_
- `Eiwitdomein` — **Zelfstandig gevouwen eiwitdeel**: Een deel van een eiwit dat op zichzelf een compacte structuur vouwt en vaak een eigen functie heeft. De Rel Homology Region van c-Rel bestaat uit twee immunoglobuline-achtige domeinen verbonden door een korte flexibele linker (L3). _(bron: SB-workshop-2-molecular-visualization.pptx, dia 12)_
- `Fosforylatie` — **Fosfaatgroep aan eiwit koppelen**: Een kinase (bv. proteïnekinase A) hangt een fosfaatgroep aan een residu zoals serine. Dit kan de werking van een eiwit aan- of uitzetten; bij c-Rel is fosforylatie van Ser263 belangrijk voor transcriptie. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 13)_
- `Porine` — **Kanaalvormend membraaneiwit**: Membraaneiwit dat een porie vormt waardoor kleine moleculen door het membraan kunnen. OmpG is een porine uit de buitenmembraan van bacteriën. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 2)_
- `β-barrel` — **Tonvormige vouw uit β-strengen**: Een eiwitvouw waarbij β-strengen een gesloten ton (cilinder) vormen. OmpG bestaat uit een β-barrel van 14 strengen. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 2)_
- `Sequentiemotief` — **Kort herkenbaar sequentiepatroon**: Een korte reeks aminozuren die in verwante eiwitten terugkomt en vaak een functie heeft, bv. DWGET in LRP5 en DWGEV in LRP6. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 12)_
- `Domeinarchitectuur` — **Volgorde van domeinen in eiwit**: Welke domeinen een eiwit bevat en in welke volgorde, bv. de 7 zinkvingers van A20. _(bron: SB-workshop-5-databases-tools.pptx, dia 3)_
- `Zinkvinger` — **Klein domein rond zinkion**: Klein eiwitdomein dat door een zinkion wordt gestabiliseerd. Zinkvingers binden vaak DNA, RNA of andere eiwitten. _(bron: SB-workshop-5-databases-tools.pptx, dia 3)_
- `Fold (vouw)` — **Driedimensionale vouwing van eiwit**: De algemene 3D-schikking van de secundaire structuurelementen in een eiwit. Eiwitten met een andere functie, zoals lysozym en α-lactalbumine, kunnen dezelfde fold hebben. _(bron: SB-workshop-5-databases-tools.pptx, dia 6)_

### Elektronenmicroscopie
- `Elektronenmicroscopie (EM)` — **Beeldvorming met elektronen**: Gebruikt versnelde elektronen, met een veel kleinere golflengte dan licht, en haalt zo een veel hogere resolutie dan een lichtmicroscoop. Geschikt voor grote, complexe structuren; nadeel: zeer duur en gespecialiseerd. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 29)_
- `TEM` — **Transmissie-elektronenmicroscoop**: Een elektronenbundel gaat door een dun preparaat; het beeld wordt vergroot en op een detector (bv. CCD-camera) gefocust. Resolutie tot ~0,1 nm, vergroting > 1 000 000 keer. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 33)_
- `SEM` — **Scanning-elektronenmicroscoop**: Een gefocuste elektronenbundel scant (raster scanning) het oppervlak van het preparaat en detecteert teruggekaatste elektronen. Toont vooral het oppervlak; resolutie ~2 nm bij biologische stalen. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 36)_
- `STEM` — **Scanning-transmissie-elektronenmicroscoop**: Combinatie van beide: een gefocuste bundel scant over een dun preparaat en de doorgelaten elektronen worden gedetecteerd. Haalt de hoge resolutie van TEM; de focussering gebeurt vóór het preparaat. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 39)_
- `Cryo-EM` — **EM op ingevroren stalen**: Het staal wordt als dunne waterige film razendsnel ingevroren (gevitrifieerd), zodat moleculen in hun natuurlijke toestand bekeken worden. Nobelprijs Chemie 2017 (Dubochet, Frank, Henderson). _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 40)_
- `Elektronentomografie (ET)` — **3D-beeld uit vele hoeken**: Uitbreiding van TEM waarbij beelden vanuit veel hoeken worden uitgelijnd en gecombineerd tot een 3D-structuur. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 41)_
- `Volume-EM (ATUM, SBEM, FIB-SEM)` — **3D-EM via seriële coupes**: Technieken om grote stalen laag per laag in beeld te brengen: ATUM snijdt automatisch duizenden dunne coupes, SBEM snijdt met een diamantmes in de microscoop het blokoppervlak weg, en FIB-SEM gebruikt een ionenbundel. De beelden worden tot 3D gereconstrueerd. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 45)_

### Evolutie en functie
- `Divergente evolutie` — **Zelfde fold, andere functie**: Homologe eiwitten kunnen een andere functie krijgen. Voorbeeld: lysozym en α-lactalbumine (40% identiek, zelfde structuur), maar bij α-lactalbumine zijn de katalytische residuen vervangen, waardoor het geen enzym meer is. _(bron: SB-07-structural-functional-assignment.pptx, dia 26)_
- `Structuur geconserveerder dan sequentie` — **Zelfde fold bij weinig sequentiegelijkenis**: Bij ver verwante eiwitten blijft de structuur beter bewaard dan de sequentie. Voorbeeld: bacteriële en eukaryote hemoglobine hebben maar 8% sequentie-identiteit, toch zelfde fold en functie. _(bron: SB-07-structural-functional-assignment.pptx, dia 30)_
- `Convergente evolutie (analoge eiwitten)` — **Zelfde functie, andere fold**: Niet-verwante eiwitten kunnen onafhankelijk dezelfde functie ontwikkelen. Voorbeeld: subtilisine en chymotrypsine hebben geen sequentie- of foldverwantschap, maar wel een identieke katalytische triade. _(bron: SB-07-structural-functional-assignment.pptx, dia 32)_
- `Katalytische triade (Ser-His-Asp)` — **Drie samenwerkende actieve residuen**: Set van drie gecoördineerde aminozuren (serine, histidine, aspartaat) in de actieve site van o.a. proteasen, die peptidebindingen hydrolyseren. _(bron: SB-07-structural-functional-assignment.pptx, dia 33)_

### Fouten in structuren
- `Obsolete structuren` — **Vervangen foute PDB-entries**: Foute of verbeterde modellen verdwijnen niet: ze belanden in het archief van obsolete PDB-structuren. Via PDB-versiebeheer (bv. rcsb.org/versions/9PAP) zie je de geschiedenis van een entry. _(bron: SB-06-structure-quality-validation.pptx, dia 29)_
- `Ernstige modelfouten` — **Van verkeerde fold tot zijketen**: Van ernstig naar minder ernstig: volledig verkeerde fold (keten volgt verkeerd pad door de dichtheid), verkeerde verbindingen tussen secundaire elementen, frameshiftfouten, en verkeerde hoofd- of zijketenconformaties. _(bron: SB-06-structure-quality-validation.pptx, dia 30)_
- `Frameshiftfout` — **Residuen één plaats verschoven**: Een residu wordt in de elektronendichtheid van het volgende residu gebouwd, en de fout loopt door tot een compenserende fout. Komt vooral voor in loops en bij lage resolutie (3 Å of slechter). _(bron: SB-06-structure-quality-validation.pptx, dia 32)_

### Functieclassificatie
- `EC 1.2.1.12` — **EC-nummer van een enzym**: De Enzyme Commission-classificatie deelt enzymen in volgens de reactie die ze katalyseren, in 4 niveaus. Voorbeeld: GAPDH heeft EC 1.2.1.12. Opzoeken kan via enzyme.expasy.org. _(bron: SB-07-structural-functional-assignment.pptx, dia 9)_
- `ChEBI` — **Databank van kleine moleculen**: Chemical Entities of Biological Interest: vrij beschikbaar woordenboek van kleine, biologisch relevante chemische verbindingen (EBI). _(bron: SB-07-structural-functional-assignment.pptx, dia 9)_

### Functietools
- `ProFunc` — **Functievoorspelling uit structuur**: Server (EBI) die veel voorspellingsmethoden combineert. Sequentiegebaseerd: BLAST, InterProScan, residuconservering. Structuurgebaseerd: fold matching (DALI), HTH-motieven, clefts, 'nests' en templates voor actieve sites en bindingsplaatsen. _(bron: SB-07-structural-functional-assignment.pptx, dia 17)_
- `PDBeFold (SSM)` — **Structuren vergelijken via secundaire structuur**: Tool van PDBe die 3D-structuren vergelijkt op basis van secondary structure matching (SSM). _(bron: SB-07-structural-functional-assignment.pptx, dia 38)_
- `PROSITE` — **Databank van eiwitmotieven**: Databank met profielen en patronen om eiwitdomeinen, families en functionele sites te herkennen (prosite.expasy.org). _(bron: SB-07-structural-functional-assignment.pptx, dia 44)_
- `ELM` — **Eukaryote lineaire motieven**: Eukaryotic Linear Motif resource: databank van korte functionele sequentiemotieven in eukaryote eiwitten (elm.eu.org). _(bron: SB-07-structural-functional-assignment.pptx, dia 44)_
- `ConSurf` — **Geconserveerde regio's op structuur**: Server die evolutionaire conservering per residu op het oppervlak van de structuur kleurt, om functionele regio's te vinden. _(bron: SB-07-structural-functional-assignment.pptx, dia 44)_
- `PDBePISA` — **Interfaces tussen moleculen analyseren**: Tool van PDBe om macromoleculaire interfaces en complexen (bv. contacten tussen eiwitketens) te onderzoeken. _(bron: SB-07-structural-functional-assignment.pptx, dia 51)_
- `SURFNET` — **Clefts en pockets opsporen**: Algoritme dat holtes in een eiwit vindt door bolletjes tussen de atomen te passen; PDBsum gebruikt het voor de Clefts-pagina. _(bron: SB-07-structural-functional-assignment.pptx, dia 52)_

### Functievoorspelling
- `Sequentie- vs structuurgebaseerde voorspelling` — **Twee manieren om functie te voorspellen**: Sequentiegebaseerd: functie overnemen van gelijkaardige sequenties (>40% identiteit). Structuurgebaseerd: vergelijken met gekende structuren (bv. via CATH, SCOP), zoeken naar gekende structurele motieven, of ab initio analyseren van enkel de structuur (bv. clefts). _(bron: SB-07-structural-functional-assignment.pptx, dia 34)_
- `Cleft (groeve)` — **Holte waar liganden binden**: Groeve of holte in het eiwitoppervlak. De actieve site of ligandbindingsplaats is vaak de grootste cleft: daar kan het substraat nauwkeurig geplaatst en van het water afgeschermd worden. _(bron: SB-07-structural-functional-assignment.pptx, dia 48)_

### Interacties
- `Dimeerinterface` — **Contactvlak tussen twee subeenheden**: Het oppervlak waar twee subeenheden van een dimeer elkaar raken. Bij c-Rel is de kern hydrofoob (Phe204, Leu206, Ala240, Val242) en zorgen geladen residuen voor ionische interacties. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 15)_
- `Transcriptiefactorbindingsplaats (TFBS)` — **DNA-plaats waar TF bindt**: De korte, specifieke DNA-sequentie waarop een transcriptiefactor bindt, bv. 5'-AGAAATTCC-3' voor c-Rel in structuur 1GJI. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 16)_
- `Waterstofbrug` — **Zwakke binding via waterstof**: Een zwakke aantrekking tussen een waterstofatoom op een N of O en een ander N- of O-atoom. Waterstofbruggen houden de baseparen van DNA samen en komen veel voor in eiwit-DNA-interfaces. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 16)_
- `Eiwit-DNA-interface` — **Contactvlak tussen eiwit en DNA**: De plaats waar een eiwit het DNA raakt. Sommige residuen maken contact met de basen (sequentiespecifiek), andere met de suiker-fosfaatruggengraat van het DNA. _(bron: SB-workshop-2-molecular-visualization.pptx, dia 18)_

### Kristallisatie
- `Eiwitkristallisatie` — **Eiwitkristal laten groeien**: Eerste en vaak moeilijkste stap: een zuiver, homogeen kristal van >0,1 mm maken. Belangrijke parameters zijn eiwitzuiverheid en -concentratie, pH, temperatuur en precipitans. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 17)_
- `Vapor diffusion (hanging/sitting drop)` — **Meest gebruikte kristallisatiemethode**: Een druppel (1 µl eiwit + 1 µl kristallisatieoplossing) hangt boven (hanging drop) of staat naast (sitting drop) een reservoir met geconcentreerdere oplossing. Water verdampt uit de druppel tot die oververzadigd wordt en kristallen kunnen vormen. Handig om veel condities te screenen met weinig eiwit. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 20)_
- `Fasediagram (oplosbaarheidsdiagram)` — **Zones voor kristalgroei**: Grafiek van eiwitconcentratie tegenover precipitansconcentratie. Onder de oplosbaarheidscurve is de oplossing onverzadigd (geen kristallen); daarboven oververzadigd, met een metastabiele zone (enkel groei), een labiele zone (nucleatie + groei) en een precipitatiezone (amorf neerslag). _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 26)_
- `Seeding` — **Kristalkiemen toevoegen**: Techniek waarbij men nucleatie overslaat door kristalkiemen in een metastabiele eiwitoplossing te brengen, zodat ze kunnen uitgroeien. Varianten: macroseeding (kleine kristallen), microseeding (verpulverde kristallen) en streak seeding (met een paardenhaar). _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 35)_

### Kristallografie
- `Kristal en kristalrooster` — **Regelmatig herhaald atoompatroon**: Een kristal is een vaste stof waarin atomen of moleculen ordelijk en herhaald in drie richtingen (x, y, z) geschikt zijn. Die regelmatige schikking heet het kristalrooster. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 9)_
- `Eenheidscel (unit cell)` — **Kleinste herhalende blok**: Het kleinste blok dat, herhaald in drie richtingen, het volledige kristalrooster opbouwt. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 51)_
- `Ruimtegroep (space group)` — **Alle symmetrie van een kristal**: De verzameling symmetrieoperaties van de eenheidscel in een kristalstructuur: combinatie van het Bravais-rooster en de symmetrie van het kristal. Er bestaan 230 ruimtegroepen. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 53)_
- `Bravais-rooster` — **14 mogelijke 3D-roosters**: Een van de 14 mogelijke driedimensionale puntroosters die de ordelijke schikking in een kristal beschrijven (bv. primitief, ruimtelijk of vlakgecentreerd kubisch). Ze horen bij 7 kristalsystemen: kubisch, tetragonaal, hexagonaal, rhomboëdrisch, orthorhombisch, monoklien en triklien. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 54)_

### Kwaliteit & validatie
- `Resolutie` — **Detailniveau van een structuur**: Maat (in ångström) voor hoe gedetailleerd een experimentele structuur is. Hoe lager het getal, hoe beter je individuele atomen kunt onderscheiden. _(bron: SB-workshop-5-databases-tools.pptx, dia 4)_
- `R-waarde en R-free` — **Hoe goed model en data kloppen**: Maten voor hoe goed een kristallografisch model overeenkomt met de gemeten diffractiedata; lager is beter. R-free wordt berekend op data die niet gebruikt werden om het model te bouwen en is daardoor eerlijker. _(bron: SB-workshop-5-databases-tools.pptx, dia 4)_
- `Ramachandran-plot` — **Grafiek van backbone-hoeken**: Grafiek van de backbone-torsiehoeken phi en psi van elk residu. Residuen in ongebruikelijke gebieden (outliers) wijzen op mogelijke fouten, dus je gebruikt hem om de kwaliteit van een structuur te controleren. _(bron: SB-workshop-5-databases-tools.pptx, dia 5)_
- `Z-score` — **Afwijking van het gemiddelde**: Geeft aan hoeveel standaardafwijkingen een waarde van het gemiddelde van goede referentiestructuren ligt. Een Z-score dicht bij 0 betekent dat de structuur normaal oogt. _(bron: SB-workshop-5-databases-tools.pptx, dia 5)_

### Kwaliteit NMR-structuren
- `Kwaliteit van NMR-structuren` — **NMR-structuren beoordelen**: De header van een NMR-bestand bevat geen standaard kwaliteitsmaat. Lees het originele artikel of gebruik stereochemische controles, bv. PROCHECK-NMR via PDBsum. _(bron: SB-06-structure-quality-validation.pptx, dia 25)_

### Kwaliteit röntgenstructuren
- `Rfree` — **Onafhankelijke R-factor**: Wordt berekend zoals de R-factor, maar op een testset van 5–10% van de data die niet gebruikt wordt bij de verfijning (de rest is de working set). Daardoor is Rfree niet te 'manipuleren' tijdens de verfijning; hij is meestal iets hoger dan R, en waarden boven 0,40 zijn verdacht. _(bron: SB-06-structure-quality-validation.pptx, dia 18)_
- `B-factor` — **Onzekerheid per atoompositie**: Waarde per atoom (laatste kolom in een ATOM-record) die aangeeft hoe onzeker of beweeglijk de positie is. Hoe hoger, hoe onzekerder; als vuistregel worden atomen met B > 40 vaak als onbetrouwbaar weggelaten. _(bron: SB-06-structure-quality-validation.pptx, dia 22)_
- `Selectiecriteria röntgenstructuren` — **Vuistregels voor goede structuren**: Kies bij voorkeur structuren met een resolutie van 2,0 Å of beter, een R-factor van 0,20 of lager, en een recent bepalingsjaar (technieken zijn verbeterd). Deze waarden staan in de header van het PDB-bestand. _(bron: SB-06-structure-quality-validation.pptx, dia 23)_

### Model & kwaliteit
- `Elektronendichtheidskaart` — **3D-kaart van elektronen**: Met een Fouriertransformatie worden de 2D-diffractiebeelden omgezet in een 3D-kaart van de elektronendichtheid in het kristal. Daarin wordt het atoommodel gebouwd. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 50)_
- `Faseprobleem` — **Fase ontbreekt in diffractiedata**: Elke diffractievlek is een golf met amplitude en fase. Het experiment meet enkel de intensiteit (amplitude), niet de fase, terwijl die nodig is om de structuur te berekenen. Oplossingen: MIR, SAD/MAD of moleculaire vervanging. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 62)_
- `MIR (multiple isomorphous replacement)` — **Fases via zware atomen**: Zware atomen (Au, Hg, Pb, Pt) worden in het kristal gebracht door soaking of co-kristallisatie, zonder de vorm van het kristal te veranderen (isomorf). De verschillen in diffractie helpen de fases te bepalen. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 64)_
- `SAD/MAD` — **Fases via anomale diffractie**: Single- of multi-wavelength anomalous diffraction gebruikt de anomale verstrooiing van zware atomen, meestal selenium: men laat het eiwit selenomethionine inbouwen in plaats van methionine. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 65)_
- `Moleculaire vervanging` — **Fases via gekende homologe structuur**: Een bestaande homologe structuur wordt als model in de onbekende eenheidscel geplaatst met 3 rotatiehoeken en 3 translaties. Zo verkrijgt men beginfases. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 66)_
- `Verfijning (refinement)` — **Model iteratief verbeteren**: Het beginmodel wordt stap voor stap aangepast zodat het beter overeenkomt met de gemeten diffractiedata én een correcte stereochemie heeft. Betere fases geven een betere dichtheidskaart (iteratief proces). _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 67)_
- `R-factor` — **Overeenkomst model en data**: Maat voor de overeenkomst tussen het kristallografische model en de experimentele diffractiedata: hoe lager, hoe beter. Een goed verfijnd model heeft typisch R < 0,25. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 69)_
- `Resolutie (Å)` — **Detailniveau van de structuur**: Kleinste afstand die nog te onderscheiden is in de elektronendichtheidskaart, uitgedrukt in Ångström (1 Å = 10⁻¹⁰ m). Hoe kleiner het getal, hoe beter: >4 Å toont enkel secundaire structuur, rond 2 Å zijn watermoleculen zichtbaar, onder 1,5 Å zijn individuele atomen zichtbaar. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 70)_
- `Rotameer` — **Voorkeursstand van een zijketen**: Een van de gunstige conformaties van een zijketen (door draaiing rond enkelvoudige bindingen). Bij lage resolutie worden zijketens vaak in een verkeerde rotameer geplaatst. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 71)_

### Moleculaire visualisatie
- `Moleculaire visualisatie` — **Structuren in 3D weergeven**: Het tonen van macromoleculaire structuren als 3D-beeld op basis van de atoomcoördinaten van een model. Het is de beste manier om een structuur te bekijken, te begrijpen en te analyseren. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 9)_
- `PyMOL-venster (GUI)` — **Onderdelen van het PyMOL-scherm**: Het PyMOL-venster bestaat uit het hoofdmenu (File, Edit, Display, Setting, Wizard ...), het canvas met het 3D-beeld, de objectlijst met knoppen rechts, het GUI-menu en twee opdrachtregels (command line) waar je commando's typt. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 17)_
- `HETATM` — **Niet-standaard atomen in PDB-bestand**: In een PDB-bestand worden atomen van niet-standaard residuen als HETATM aangeduid: liganden, water, zouten of gemodificeerde aminozuren en nucleotiden. In PyMOL selecteer je ze met het sleutelwoord hetatm. _(bron: SB-01-introduction-workshop-1-molecular-visualization.pptx, dia 26)_
- `PyMOL-sessie (.pse)` — **Bewaarde PyMOL-toestand**: Een .pse-bestand bewaart alles wat je in PyMOL deed (structuren, weergaven, kleuren, camerastandpunt). Voor elke oefening bewaar je je oplossing als sessie. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 2)_
- `PyMOL-movie` — **Animatie van een structuur**: Een filmpje in PyMOL (bv. draaien of inzoomen) vertelt soms beter een verhaal dan een stilstaande figuur. Uitleg vind je op de PyMOL-wiki onder MovieSchool. _(bron: SB-workshop-4-molecular-visualization.pptx, dia 10)_

### Motieven & domeinen
- `Domein` — **Zelfstandige structurele eenheid**: Compact deel van een eiwit dat structureel onafhankelijk is: het behoudt zijn vorm ook als het van de rest van het eiwit wordt losgemaakt. Hetzelfde domein kan in verder totaal verschillende eiwitten voorkomen. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 69)_
- `Motief (supersecundaire structuur)` — **Kleine combinatie van secundaire elementen**: Kleine combinatie van enkele secundaire structuurelementen, niet noodzakelijk structureel onafhankelijk, vaak met een belangrijke functie. Motieven kunnen samen domeinen vormen. De term wordt ook gebruikt voor geconserveerde sequentiepatronen. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 70)_
- `Topologieën (α, β, α/β)` — **Veelvoorkomende motieftypes**: α-topologieën: helix-turn-helix (bindt DNA) en four-helix bundle. β-topologieën: β-hairpin, Greek key, β-sandwich (bv. immunoglobuline) en β-barrel (bv. porines). α/β-topologieën: β-α-β-motief, Rossmann-fold (β-α-β-α-β) en horseshoe. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 71)_

### NMR
- `Kernspin` — **Tollende geladen atoomkern**: Sommige atoomkernen gedragen zich als kleine tollende magneetjes. In een extern magneetveld nemen ze een spin-up (grondtoestand) of spin-down (aangeslagen) toestand in; radiogolven met de juiste energie laten ze 'omflippen'. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 5)_
- `NMR-actieve isotopen` — **¹H, ¹³C, ¹⁵N en ³¹P**: Kernen die een NMR-signaal geven en belangrijk zijn voor eiwitten: proton (¹H), koolstof-13 (¹³C), stikstof-15 (¹⁵N) en fosfor-31 (³¹P). Eiwitten worden daarom vaak gelabeld met deze stabiele isotopen. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 10)_
- `NMR versus röntgenkristallografie` — **Complementaire methoden vergelijken**: NMR (in oplossing) werkt vooral voor kleine eiwitten (< ~30 kDa), ook als ze deels ongeordend zijn, meerdere conformaties hebben of moeilijk kristalliseren. Solid-state NMR kan onoplosbare eiwitten zoals membraaneiwitten bestuderen. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 11)_
- `NMR-conformeren (ensemble)` — **Meerdere modellen per NMR-structuur**: Een NMR-structuur bestaat uit een set van meestal 10 à 20 modellen (conformeren) met de minste fouten, gekozen uit ~100 berekende. Uiteinden en oppervlak tonen de meeste variatie. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 20)_
- `RMSD` — **Gemiddelde afstand tussen gesuperponeerde structuren**: Root mean square deviation: maat voor de gemiddelde afstand (in Å) tussen overeenkomstige atomen van twee over elkaar gelegde structuren. 0 betekent een perfecte overlap; hoe kleiner, hoe gelijkaardiger. _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 22)_

### Nucleïnezuren: bouwstenen
- `Nucleotide en nucleoside` — **Bouwstenen van DNA en RNA**: Een nucleoside bestaat uit een suiker (ribose of desoxyribose) en een stikstofbase. Een nucleotide is een nucleoside met een fosfaatgroep erbij; het is de herhalende bouwsteen van een nucleïnezuur. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 15)_
- `Purines en pyrimidines` — **Twee groepen stikstofbasen**: De basen zijn vlakke, aromatische ringmoleculen. Purines (A en G) hebben twee ringen; pyrimidines (C, T en U) hebben één ring. In sequenties worden ze afgekort als R (purine) en Y (pyrimidine). _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 16)_
- `DNA versus RNA` — **Verschil in suiker en base**: DNA bevat de suiker desoxyribose en de basen A, C, G en T. RNA bevat ribose en uracil (U) in plaats van thymine. RNA is meestal enkelstrengs, DNA meestal dubbelstrengs. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 17)_
- `5'CpGpCpGpApApTpTpCpG` — **Notatie van nucleïnezuursequentie**: Sequenties worden geschreven met éénlettercodes van 5' naar 3'; 'p' staat voor de fosfaatgroep tussen twee nucleotiden. Een zelfcomplementaire dubbele helix kan kort genoteerd worden als (CGCGAATTCG)2. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 19)_
- `Glycosidische binding` — **Binding tussen suiker en base**: Binding tussen het C1'-atoom van de suiker en de base (N9 bij purines, N1 bij pyrimidines). De draaihoek rond deze binding heet χ (chi). _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 20)_

### PDB-formaat
- `PDB-formaat (.pdb)` — **Klassiek tekstformaat voor structuren**: Tekstbestand met regels van max. 80 tekens; de eerste 6 kolommen bevatten het recordtype (HEADER, REMARK, ATOM …) en elk gegeven staat op vaste kolomposities. Bevat coördinaten, chemische info en experimentele details. Het formaat is sinds 2012 bevroren; mmCIF is nu de standaard. _(bron: SB-05-data-representation-databases.pptx, dia 17)_
- `REMARK 2 / REMARK 3` — **Resolutie en verfijning**: REMARK-records bevatten allerlei opmerkingen. REMARK 2 geeft de resolutie, REMARK 3 de gegevens over de verfijning (bv. R-factor). _(bron: SB-05-data-representation-databases.pptx, dia 24)_
- `HELIX / SHEET` — **Secundaire structuur in bestand**: Records die aangeven welke residuen een α-helix (HELIX) of β-sheet (SHEET) vormen. _(bron: SB-05-data-representation-databases.pptx, dia 25)_
- `MODEL / ENDMDL` — **Meerdere modellen afbakenen**: Records die het begin en einde van één model aangeven, bv. bij de verschillende conformeren van een NMR-structuur. TER markeert het einde van een keten, END het einde van het bestand. _(bron: SB-05-data-representation-databases.pptx, dia 27)_
- `ATOM` — **Coördinaten van één atoom**: Record met de gegevens en coördinaten van elk atoom van een standaardresidu, telkens op vaste kolomposities. _(bron: SB-05-data-representation-databases.pptx, dia 28)_

### Primaire structuur
- `Peptidebinding` — **Binding tussen twee aminozuren**: Covalente amidebinding tussen de carboxylgroep van het ene en de aminogroep van het volgende aminozuur, waarbij een watermolecule vrijkomt. De peptidebinding is vlak en vrij stijf. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 30)_
- `Peptide, polypeptide en residu` — **Namen voor aminozuurketens**: Een peptide is een korte keten van twee of meer aminozuren; een lange keten (typisch ≥ 50 aminozuren) heet een polypeptide. Een aminozuur dat in zo'n keten zit, noemt men een residu. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 31)_
- `Backbone, N-terminus en C-terminus` — **Ruggengraat en uiteinden van eiwitketen**: De backbone (ruggengraat) bestaat uit de atomen van de peptidebindingen (N, Cα, C). De keten begint aan de N-terminus (vrije aminogroep) en eindigt aan de C-terminus (vrije carboxylgroep). _(bron: SB-02-fundamentals-protein-structure.pptx, dia 33)_
- `Torsiehoeken phi (Φ) en psi (Ψ)` — **Draaihoeken van de backbone**: Omdat de peptidebinding stijf is, kan de keten enkel draaien rond de bindingen van het Cα-atoom: phi (rond N–Cα) en psi (rond Cα–C). Deze twee hoeken per residu bepalen samen de 3D-vorm van de backbone. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 35)_

### Quaternaire structuur
- `Homomeer en heteromeer` — **Eiwit uit meerdere ketens**: De quaternaire structuur beschrijft hoe meerdere polypeptideketens (subeenheden) samen één eiwit (multimeer) vormen. Zijn de subeenheden identiek, dan is het een homomeer; zijn ze verschillend, een heteromeer. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 101)_

### RNA-structuren
- `A-RNA (dubbelstrengs RNA)` — **Helixvorm van dsRNA**: Dubbelstrengs RNA heeft bijna altijd één vorm, A-RNA: een rechtsdraaiende helix met ~11 basenparen per winding, C3'-endo pucker, een smalle diepe grote groef en een brede ondiepe kleine groef. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 72)_
- `tRNA` — **L-vormig adaptermolecule**: Transfer-RNA is gevouwen in een L-vorm uit korte A-RNA-helices. Aan het 3'-CCA-uiteinde (acceptorstam) hangt het aminozuur; het anticodon in de anticodonlus past op het codon van het mRNA. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 79)_
- `Ribozym` — **Katalytisch RNA-molecule**: RNA-molecule dat zelf een reactie katalyseert, bv. zichzelf of ander RNA knippen. Voorbeelden: zelfsplitsende introns, hammerhead-ribozym, RNase P en het rRNA in het ribosoom. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 81)_
- `Ribosoom: A-, P- en E-site` — **Bindingsplaatsen voor tRNA**: Het ribosoom (kleine en grote subeenheid uit rRNA en eiwitten) maakt eiwitten. In de A-site bindt het aminoacyl-tRNA met het nieuwe aminozuur, in de P-site hangt het tRNA aan de groeiende peptideketen, en via de E-site verlaat het tRNA het ribosoom. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 93)_

### Röntgendiffractie
- `n λ = 2d sin θ` — **Wet van Bragg**: Beschrijft wanneer röntgenstralen die op opeenvolgende atoomlagen weerkaatsen in fase zijn en een heldere vlek geven. Zo kan men afstanden tussen vlakken in het kristalrooster berekenen. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 13)_
- `Synchrotron` — **Ringvormige deeltjesversneller als röntgenbron**: Beste en meest gebruikte röntgenbron: een ringvormige deeltjesversneller die zeer intense straling levert aan beamlines. Bekende synchrotrons staan in Grenoble, Hamburg en Triëst. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 44)_
- `Diffractiepatroon` — **Patroon van reflecties**: Het kristal wordt (op een lusje, ingevroren in vloeibare stikstof) in een intense monochromatische röntgenbundel geplaatst. De verstrooide stralen geven een patroon van vlekken (reflecties); door het kristal ~180° te draaien verzamelt men alle informatie. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 47)_

### Secundaire structuur
- `α-helix` — **Rechtsdraaiende spiraal in eiwit**: Meest voorkomende secundaire structuur: een (bijna altijd rechtsdraaiende) spiraal met ~3,6 residuen per winding. Ze wordt gestabiliseerd door H-bruggen tussen de C=O van residu i en de N-H van residu i+4; de zijketens wijzen naar buiten. Zeldzamere varianten zijn de 3₁₀-helix (3 residuen/winding) en de π-helix (4,4 residuen/winding). _(bron: SB-02-fundamentals-protein-structure.pptx, dia 45)_
- `β-strand en β-sheet` — **Gestrekte ketens in plaatstructuur**: Een β-strand is een kort (5–8 residuen), uitgestrekt stuk keten. Meerdere strands naast elkaar vormen via H-bruggen een geplooide β-sheet, parallel (zelfde richting) of antiparallel (tegengestelde richting). Sheets zijn meestal licht rechtsdraaiend getwist. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 50)_
- `Loop (coil)` — **Onregelmatig verbindingsstuk**: Onregelmatige stukken tussen helices en strands, meestal aan het eiwitoppervlak; ze kunnen belangrijk zijn, bv. als actieve site. Types: hairpin loop (4–5 residuen tussen antiparallelle strands), omega-loop (6–16 residuen), extended loop en random coil (geen vaste structuur). _(bron: SB-02-fundamentals-protein-structure.pptx, dia 58)_

### Sequentiedatabanken
- `HGNC-gennomenclatuur` — **Officiële gensymbolen**: Het HUGO Gene Nomenclature Committee keurt unieke namen en symbolen voor menselijke genen goed (genenames.org). Menselijke symbolen staan volledig in hoofdletters (CDHR1); bij de muis (MGI) enkel de eerste letter (Cdhr1). _(bron: SB-05-data-representation-databases.pptx, dia 59)_
- `GenBank en INSDC` — **Archief van alle DNA-sequenties**: GenBank (NCBI) bevat alle publiek beschikbare DNA-sequenties, ingediend door auteurs en niet gecureerd. Het maakt deel uit van de INSDC samen met ENA (EBI) en DDBJ (Japan), die dagelijks data uitwisselen. _(bron: SB-05-data-representation-databases.pptx, dia 61)_
- `RefSeq` — **Gecureerde referentiesequenties van NCBI**: Door NCBI gecureerde collectie met één record per molecule, gemaakt op basis van bestaande data (in tegenstelling tot GenBank). Gecureerde data verdienen de voorkeur. _(bron: SB-05-data-representation-databases.pptx, dia 62)_
- `UniProt: Swiss-Prot en TrEMBL` — **Eiwitsequentiedatabank**: UniProt (SIB & EBI) bevat enkel eiwitdata. Swiss-Prot is manueel gecureerd, TrEMBL automatisch geannoteerd en niet gecureerd. _(bron: SB-05-data-representation-databases.pptx, dia 63)_
- `NM_004360.4` — **RefSeq-accessienummer lezen**: RefSeq-nummers hebben twee letters + underscore die het type molecule aangeven, gevolgd door een nummer en een versie. _(bron: SB-05-data-representation-databases.pptx, dia 64)_

### Stereochemische controle
- `Stereochemische controle` — **Geometrie vergelijken met de norm**: Controle van bindingslengtes, hoeken en andere geometrische eigenschappen van een model, vergeleken met wat bekend is uit hoge-resolutiestructuren. Grote afwijkingen wijzen op problemen. _(bron: SB-06-structure-quality-validation.pptx, dia 35)_
- `Ramachandran-plot als validatie` — **Phi/psi-controle van model**: Krachtigste controle voor eiwitten: in een goed model liggen de phi/psi-punten vooral in de gunstige gebieden, in een slecht model verspreid over verboden gebieden. Glycine heeft meer vrijheid, proline minder. _(bron: SB-06-structure-quality-validation.pptx, dia 36)_
- `χ-hoeken (χ1–χ2-plot)` — **Controle van zijketenhoeken**: De torsiehoeken in de zijketen (χ1 = N-Cα-Cβ-Xγ, χ2 de volgende) hebben voorkeursconformaties (rotameren). Een χ1–χ2-plot toont of zijketens in gunstige gebieden liggen. _(bron: SB-06-structure-quality-validation.pptx, dia 41)_

### Structurele genomica
- `Structurele genomica` — **Structuren op grote schaal bepalen**: Grootschalige, high-throughput structuurbepaling om een overzicht te krijgen van alle eiwitstructuren (folds) in genomen. Voorbeelden: Protein 3000 (Japan, 2002–2007) en de Protein Structure Initiative (PSI, VS, 2000–2015). _(bron: SB-04-macromolecular-structure-determination-part2.pptx, dia 49)_

### Structuren als model
- `Structuur = model` — **Structuren zijn modellen**: Elke experimentele structuur is eigenlijk een model dat de data zo goed mogelijk verklaart. Een model kan nauwkeurig of slecht zijn; daarom moet je structuren kritisch beoordelen voor je ze gebruikt. _(bron: SB-06-structure-quality-validation.pptx, dia 4)_
- `Systematische en toevallige fouten` — **Juistheid versus precisie**: Systematische fouten bepalen de juistheid (accuracy): hoe goed het model overeenkomt met de echte structuur, bv. door interpretatiefouten. Toevallige fouten bepalen de precisie: hoe nauwkeurig een meting is (vergelijkbaar met een standaardafwijking). _(bron: SB-06-structure-quality-validation.pptx, dia 6)_

### Structuur en functie
- `40%-regel sequentie-identiteit` — **Functie overdragen via sequentie**: Eiwitten met meer dan ~40% sequentie-identiteit hebben meestal dezelfde functie; daaronder daalt dat snel. Structuur blijft langer bewaard dan functie, dus voorzichtigheid is nodig (bv. δ-I en δ-II-kristalline: 94% identiek maar andere functie). _(bron: SB-07-structural-functional-assignment.pptx, dia 3)_
- `Biochemische en biologische functie` — **Verschillende betekenissen van functie**: 'Functie' kan verschillende dingen betekenen: de biochemische functie (bv. welke reactie een gezuiverd enzym in vitro katalyseert) of de biologische functie (de rol in de cel, bv. zichtbaar met een fluorescent label). _(bron: SB-07-structural-functional-assignment.pptx, dia 6)_
- `Foute annotaties` — **Voorspelde functies kunnen fout zijn**: Veel functies in databanken zijn enkel afgeleid uit sequentiegelijkenis en kunnen fout zijn. Vertrouw bij voorkeur op manueel gecureerde data (bv. Swiss-Prot) of experimentele bevestiging. _(bron: SB-07-structural-functional-assignment.pptx, dia 14)_

### Structuurbepaling
- `NMR-spectroscopie` — **Structuurbepaling in oplossing**: Methode om een structuur te bepalen in oplossing. Het resultaat is geen enkele structuur maar een ensemble van meerdere modellen (conformeren) die allemaal bij de meetdata passen, bv. OmpG in 2JQY. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 2)_
- `Röntgenkristallografie` — **Structuur uit eiwitkristal**: Methode waarbij een eiwitkristal met röntgenstralen wordt beschoten; uit het diffractiepatroon volgt een elektronendichtheid en een atoommodel. Een kristalstructuur toont één toestand, bv. OmpG in gesloten vorm (2IWW). _(bron: SB-workshop-3-molecular-visualization.pptx, dia 2)_
- `Elektronentomografie` — **3D-beeld via elektronenmicroscopie**: Techniek waarbij een staal vanuit veel hoeken met een elektronenmicroscoop wordt gefotografeerd en daarna een 3D-beeld wordt berekend. Kristalstructuren (bv. C-cadherine 1L3W) kunnen in dat beeld worden gefit. _(bron: SB-workshop-3-molecular-visualization.pptx, dia 4)_
- `Methoden voor structuurbepaling` — **Drie experimentele technieken**: Macromoleculaire 3D-structuren worden experimenteel bepaald met röntgenkristallografie, NMR-spectroscopie of elektronenmicroscopie (EM). Statistieken per methode staan op rcsb.org/stats. _(bron: SB-04-macromolecular-structure-determination-part1.pptx, dia 2)_

### Structuurvergelijking
- `VAST` — **Gelijkaardige 3D-structuren zoeken**: Vector Alignment Search Tool (NCBI) zoekt structuren die geometrisch op elkaar lijken. Zo vind je verre homologen die je met sequentievergelijking niet herkent. _(bron: SB-05-data-representation-databases.pptx, dia 72)_
- `DALI` — **3D-structuren vergelijken**: Server (Distance Alignment Matrix Method) die eiwitstructuren in 3D vergelijkt: één structuur tegen de hele PDB, paarsgewijs tegen een lijst, of allemaal tegen elkaar. Toont verwantschap die je in de sequentie niet ziet. _(bron: SB-05-data-representation-databases.pptx, dia 96)_

### Suikerfosfaatruggengraat
- `Suikerpuckering (C2'-endo, C3'-endo)` — **Niet-vlakke vorm van suikerring**: De vijfring van de suiker is niet vlak maar 'geplooid' (puckering). De meest voorkomende vormen zijn C2'-endo (S-type, typisch voor B-DNA) en C3'-endo (N-type, typisch voor A-DNA en RNA). De pucker beïnvloedt de vorm van de hele ruggengraat. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 41)_
- `Anti- en syn-conformatie` — **Stand van base t.o.v. suiker**: Twee gunstige standen van de glycosidische torsiehoek χ. In anti wijst de base weg van de suiker (normaal in Watson-Crick-helices); in syn ligt de base boven de suikerring. _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 45)_
- `Fosfodiësterbinding` — **Verbindt nucleotiden in de streng**: Covalente binding via een fosfaatgroep tussen het 3'-C-atoom van de ene suiker en het 5'-C-atoom van de volgende; zo krijgt een streng een 5'→3'-richting. De ruggengraat heeft 6 variabele torsiehoeken (α, β, γ, δ, ε, ζ). _(bron: SB-03-fundamentals-dna-rna-structure.pptx, dia 49)_

### Tertiaire structuur
- `Fold en eiwitvouwing` — **Eindvorm en vouwproces van eiwit**: De tertiaire structuur is de globale 3D-vorm van één polypeptideketen, ook de fold genoemd. Het proces waarbij de lineaire keten die vorm aanneemt, heet eiwitvouwing (protein folding). _(bron: SB-02-fundamentals-protein-structure.pptx, dia 68)_
- `Hydrofoob effect` — **Hydrofobe residuen naar de kern**: Belangrijkste kracht bij de vouwing: hydrofobe zijketens worden in de kern van het eiwit gepakt, weg van het water. Polaire en geladen residuen vormen het oppervlak en interageren met water en ionen. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 84)_
- `Zoutbrug (ionpaar)` — **Aantrekking tussen tegengestelde ladingen**: Niet-covalente interactie tussen een positief en een negatief geladen residu. Zo kan een geladen residu toch in de hydrofobe kern zitten, omdat de netto lading nul is. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 88)_
- `Disulfidebrug` — **Covalente brug tussen cysteïnes**: Covalente binding tussen de thiolgroepen (-SH) van twee cysteïnes, die de fold extra stabiliseert. Cysteïne is het enige standaard-aminozuur dat dit kan; de meeste cysteïnes vormen echter geen disulfidebrug. _(bron: SB-02-fundamentals-protein-structure.pptx, dia 89)_

### Validatietools
- `PROCHECK` — **Stereochemische kwaliteit controleren**: Programma dat stereochemische parameters van een eiwitmodel berekent en plots maakt (Ramachandran-plot, χ1–χ2-plots, bindingslengtes …). Afwijkingen t.o.v. hoge-resolutiestructuren worden gemeld; beschikbaar via PDBsum. _(bron: SB-06-structure-quality-validation.pptx, dia 43)_
- `RamplotR` — **Ramachandran-plots maken (Howest)**: In-house R Shiny-app van Howest BiKC om Ramachandran-plots te maken (bioit.shinyapps.io/RamplotR). _(bron: SB-06-structure-quality-validation.pptx, dia 49)_
- `ProSa-web` — **Energiegebaseerde kwaliteitscontrole**: Webtool die de kwaliteit van een eiwitstructuur toont met scores en energieplots, vergeleken met alle gekende structuren; probleemzones worden gemarkeerd in 3D. _(bron: SB-06-structure-quality-validation.pptx, dia 50)_
- `z-score (ProSa)` — **Globale modelkwaliteit**: Maat voor de totale kwaliteit van het model, getoond t.o.v. de z-scores van alle experimentele eiwitketens in de PDB. Valt de score buiten het gebied van gelijkaardige structuren, dan is het model verdacht. _(bron: SB-06-structure-quality-validation.pptx, dia 52)_
- `Energieplot (ProSa)` — **Lokale modelkwaliteit per residu**: Toont de energie per residupositie (gemiddeld over fragmenten van 40 residuen). Positieve waarden wijzen op problematische of foute delen van het model. _(bron: SB-06-structure-quality-validation.pptx, dia 53)_

### Vergelijken
- `Structurele alignment` — **Structuren in 3D vergelijken**: Het op elkaar leggen van twee (pairwise) of meer (multiple) 3D-structuren om overeenkomsten in vouwing te vinden, ook als de sequenties weinig gelijken. _(bron: SB-workshop-5-databases-tools.pptx, dia 7)_

### mmCIF-formaat
- `PDBx/mmCIF` — **Standaard archiefformaat van PDB**: Macromolecular Crystallographic Information File: sinds 2014 het officiële formaat van het PDB-archief. Gegevens staan in categorieën als tabellen of sleutel-waardeparen, zonder limiet op het aantal atomen of ketens. Coördinaten staan in de categorie _atom_site. _(bron: SB-05-data-representation-databases.pptx, dia 30)_
- `_categorie.attribuut` — **Naam van een mmCIF-gegeven**: Elk gegeven begint met een underscore; de naam bestaat uit een categorie en een attribuut, gescheiden door een punt (bv. _audit_conform.dict_name). In key-value-stijl staat de waarde gewoon achter de naam. _(bron: SB-05-data-representation-databases.pptx, dia 34)_
- `loop_` — **Tabel in mmCIF**: Gereserveerd woord dat een tabel start: eerst volgen de kolomnamen (_categorie.attribuut), daarna de rijen met waarden. _(bron: SB-05-data-representation-databases.pptx, dia 35)_
- `# en ; in mmCIF` — **Commentaar en tekst over meerdere regels**: Een regel die begint met # is commentaar. Tekst met spaties staat tussen enkele of dubbele aanhalingstekens; tekst over meerdere regels staat tussen puntkomma's (;) aan het begin van een regel. _(bron: SB-05-data-representation-databases.pptx, dia 36)_
- `PDBML/XML` — **PDB-data in XML**: Protein Data Bank Markup Language: de PDB-gegevens in XML-formaat, beschreven in een XML-schema. _(bron: SB-05-data-representation-databases.pptx, dia 39)_
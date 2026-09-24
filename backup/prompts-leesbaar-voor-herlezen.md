# PromptFinder: alle prompts en begrippen


## Algemeen (47)


### Bestanden & mappen

- `Bestandsrechten (rwx)` — Wie mag wat met een bestand: Elk bestand heeft rechten voor de eigenaar, de groep en de rest: lezen (r), schrijven (w) en uitvoeren (x). ls -l toont ze, bv. -rwxr-xr--. Je past ze aan met chmod.
- `Bestandssysteem` — Hoe bestanden georganiseerd zijn: De manier waarop bestanden en mappen op de schijf bewaard worden. Op Linux is dat één grote boom die start bij de root-map /, zonder stationsletters zoals C: op Windows.
- `Map (directory)` — Een container voor bestanden: Wat je op Windows een 'folder' noemt. In de terminal heet het een directory. Mappen kunnen andere mappen bevatten, zo ontstaat een boomstructuur.
- `Pad (absoluut en relatief)` — Het 'adres' van een bestand: Een absoluut pad start bij de root: /home/guest/data/seq.fasta. Een relatief pad start vanaf de map waar je nu staat: data/seq.fasta. . betekent 'deze map', .. betekent 'één map hoger'.
- `Root-map ( / )` — Het begin van het bestandssysteem: De bovenste map waar alles onder hangt. Belangrijke mappen eronder: /home (thuismappen), /bin en /usr (programma's), /etc (instellingen), /tmp (tijdelijke bestanden).
- `Thuismap ( ~ )` — Jouw eigen map: Elke gebruiker heeft een eigen map, bv. /home/guest. Het teken ~ is er een afkorting voor. Met cd zonder argument ga je er altijd naartoe.
- `Verborgen bestand` — Bestand dat met een punt begint: Bestanden zoals .bashrc worden niet getoond door een gewone ls. Ze bevatten meestal instellingen. Toon ze met ls -a.

### Bio-informatica

- `Eiwitstructuur (primair tot quaternair)` — De vier niveaus van een eiwit: Primair: de volgorde van aminozuren. Secundair: lokale vormen zoals α-helices en β-sheets. Tertiair: de volledige 3D-vouwing van één keten. Quaternair: hoe meerdere ketens samen een complex vormen.
- `FASTA` — Tekstformaat voor sequenties: Een eenvoudig formaat voor DNA- of eiwitsequenties: een regel die begint met > bevat de naam, de regels eronder de sequentie. Daarom telt grep -c '>' het aantal sequenties.
- `PDB (Protein Data Bank)` — Databank met 3D-structuren: Een publieke databank met experimenteel bepaalde 3D-structuren van eiwitten en nucleïnezuren. Elke structuur heeft een code van 4 tekens, bv. 1UBQ. In PyMOL laad je die met fetch 1ubq.
- `PyMOL` — Programma om moleculen in 3D te bekijken: Toont eiwitstructuren in 3D en laat je ze kleuren, selecteren en meten. Je kan klikken in de menu's of commando's typen achter de PyMOL>-prompt.

### Computer & besturingssysteem

- `Besturingssysteem (OS)` — Software die je computer beheert: Het basisprogramma dat de hardware (processor, geheugen, schijf) beheert en andere programma's laat draaien. Voorbeelden: Windows, macOS, Linux, Android.
- `Distributie (distro)` — Een 'versie' van Linux: Een pakket van de Linux-kernel met programma's, een pakketbeheerder en een bureaublad errond. Voorbeelden: Ubuntu, Fedora, Debian. De commando's zijn grotendeels dezelfde; vooral de pakketbeheerder verschilt (apt op Ubuntu, dnf op Fedora).
- `Kernel` — Het hart van het besturingssysteem: Het centrale deel van het OS dat rechtstreeks met de hardware praat: het verdeelt processortijd en geheugen over programma's en regelt de toegang tot bestanden en apparaten. Je werkt er nooit rechtstreeks mee; je vraagt dingen via de shell of programma's.
- `Linux` — Een gratis, open besturingssysteem: Een besturingssysteem gebouwd rond de Linux-kernel. Het wordt veel gebruikt op servers en in de bio-informatica, omdat veel analyseprogramma's er (enkel) voor gemaakt zijn en alles met commando's te automatiseren is.
- `Virtuele machine (VM)` — Een computer in je computer: Software die een volledige computer nabootst, zodat je bv. Linux kan draaien binnen Windows. Wat je in de VM doet, raakt je eigen systeem niet. Programma's: VirtualBox, VMware, WSL op Windows.

### Gebruikers

- `Root (superuser)` — De beheerder van het systeem: De gebruiker die alles mag, ook systeembestanden aanpassen of verwijderen. Daarom werk je normaal als gewone gebruiker en gebruik je sudo alleen als het echt nodig is.
- `sudo` — Eén commando als beheerder uitvoeren: Zet je sudo voor een commando, dan wordt het uitgevoerd met root-rechten (na je wachtwoord). Nodig om bv. software te installeren. Wees voorzichtig: fouten met sudo kunnen het systeem beschadigen.

### In- en uitvoer

- `Jokerteken (wildcard)` — Patroon om meerdere bestanden te kiezen: De shell vervangt patronen door passende bestandsnamen: * = eender welke tekens, ? = precies één teken, [abc] = één van deze tekens, [!abc] = geen van deze. Bv. ls *.fasta.
- `Pipe ( | )` — Commando's aan elkaar koppelen: Stuurt de uitvoer van het ene commando als invoer naar het volgende. Bv. grep '>' seq.fasta | wc -l telt het aantal sequenties. Zo bouw je met kleine commando's een grotere analyse.
- `Redirect ( > en >> )` — Uitvoer naar een bestand sturen: Met > schrijf je de uitvoer van een commando in een bestand (overschrijft), met >> voeg je toe aan het einde. Met 2> stuur je foutmeldingen apart door. Bv. ls -l > lijst.txt.
- `Reguliere expressie (regex)` — Zoekpatroon voor tekst: Een krachtigere zoektaal dan jokertekens, gebruikt door grep, sed en awk. Bv. ^ATG zoekt regels die met ATG beginnen, [0-9]+ zoekt één of meer cijfers. Let op: regex en jokertekens gebruiken * en ? anders.
- `stdin, stdout, stderr` — De drie standaardkanalen: Elk commando heeft standaardinvoer (stdin, meestal het toetsenbord), standaarduitvoer (stdout, gewone uitvoer) en standaardfout (stderr, foutmeldingen). Beide uitvoerkanalen verschijnen in de terminal, maar je kan ze apart doorsturen.

### Netwerk

- `SSH` — Veilig inloggen op een andere computer: Secure Shell: hiermee open je een terminal op een andere computer (bv. een rekenserver van school) via het netwerk, beveiligd met versleuteling. Bv. ssh student@server.be.
- `Server en client` — Wie aanbiedt en wie vraagt: Een server is een computer (of programma) die diensten aanbiedt, zoals websites of rekenkracht. Een client vraagt die op, bv. je browser of je terminal via ssh.

### Programma's & processen

- `Omgevingsvariabele` — Instelling die programma's kunnen lezen: Een variabele die voor alle programma's in je shell geldt, bv. $HOME (je thuismap) of $USER (je gebruikersnaam). Toon ze allemaal met env.
- `PATH` — Waar de shell programma's zoekt: Een omgevingsvariabele met een lijst mappen. Typ je ls, dan zoekt de shell in die mappen naar een programma met die naam. 'command not found' betekent vaak dat het programma niet in je PATH staat of niet geïnstalleerd is.
- `Pakketbeheerder` — Installeert en updatet software: Een programma dat software downloadt, installeert en up-to-date houdt, zoals een app store in de terminal. Voorbeelden: apt (Ubuntu), dnf (Fedora), conda en pip (Python/bio-informatica).
- `Proces` — Een programma dat nu draait: Elke keer dat je een programma start, maakt het besturingssysteem er een proces van met een eigen nummer (PID). Je bekijkt processen met ps of top en stopt ze met kill.
- `Script` — Een bestand vol commando's: Een tekstbestand (bv. analyse.sh) met commando's die na elkaar uitgevoerd worden. Handig om een analyse te herhalen of te automatiseren. Maak het uitvoerbaar met chmod +x en start het met ./analyse.sh.
- `Variabele` — Een naam die een waarde onthoudt: In bash maak je een variabele met NAAM=waarde (zonder spaties rond =) en gebruik je ze met $NAAM, bv. echo $NAAM.

### Terminal & shell

- `Argument` — Waarop het commando werkt: De extra informatie na een commando, zoals een bestandsnaam of map. In 'cp a.txt b.txt' zijn a.txt en b.txt de argumenten.
- `Bash` — De meest gebruikte shell op Linux: Bourne Again SHell: de standaardshell op de meeste Linux-systemen. Naast losse commando's kan je in bash ook scripts schrijven met variabelen, lussen en voorwaarden.
- `Commando` — Een opdracht die je in de shell typt: Een instructie voor de computer, meestal de naam van een programma gevolgd door opties en argumenten. Bv. in 'ls -l documenten' is ls het commando.
- `Manpage` — De ingebouwde handleiding: Elke gebruikelijke Linux-opdracht heeft een handleiding die je opent met man, bv. man ls. Blader met de pijltjes, zoek met /, sluit af met q. Veel commando's tonen ook korte hulp met --help.
- `Optie (flag)` — Past aan hoe een commando werkt: Begint met - of --, bv. -l of --all. Opties veranderen het gedrag: ls toont namen, ls -l toont ook details. Korte opties mag je combineren: -la is hetzelfde als -l -a.
- `Prompt (bij AI)` — Een opdracht of vraag aan een AI: Bij AI-programma's zoals Claude is een prompt de tekst die je intypt om iets te vragen. Dat is iets anders dan de prompt in de terminal, al lijken beide op 'de plek waar je iets typt'.
- `Prompt (in de terminal)` — Het tekstje dat wacht op je commando: De tekst voor je cursor, bv. guest@fedora:~$. Die toont wie je bent (guest), op welke computer (fedora), in welke map (~ = thuismap) en eindigt op $ (gewone gebruiker) of # (root). Je typt je commando erachter.
- `Shell` — Het programma dat je commando's uitvoert: Leest wat je in de terminal typt, begrijpt het en start de juiste programma's. Het is de 'tolk' tussen jou en het besturingssysteem. Er bestaan verschillende shells: bash, zsh, fish …
- `Tab-aanvulling` — Laat de terminal namen afmaken: Druk op Tab terwijl je een commando of bestandsnaam typt: de shell vult de rest aan. Twee keer Tab toont alle mogelijkheden. Scheelt typwerk en typfouten.
- `Terminal` — Het venster waarin je commando's typt: Een programma dat een tekstvenster toont waarin je commando's intypt en de uitvoer leest. De terminal zelf voert niets uit: hij geeft wat je typt door aan de shell.

### Web

- `Browser` — Programma dat webpagina's toont: Chrome, Firefox, Edge … lezen HTML, CSS en JavaScript en maken er een zichtbare pagina van. Met F12 open je de ontwikkelaarstools om de code van een pagina te bekijken.
- `CSS` — De opmaak van een webpagina: Cascading Style Sheets: bepaalt hoe HTML eruitziet, zoals kleuren, lettertypes, marges en indeling. Bv. p { color: blue; } maakt alle alinea's blauw.
- `HTML` — De structuur van een webpagina: HyperText Markup Language: beschrijft wat er op een pagina staat (titels, tekst, afbeeldingen, links) met tags zoals <h1> en <p>. HTML is geen programmeertaal: het rekent niets uit.
- `JavaScript` — Interactie op een webpagina: Een programmeertaal die in de browser draait en pagina's laat reageren, bv. op een klik. HTML = structuur, CSS = opmaak, JavaScript = gedrag.
- `PHP` — Code die op de server draait: Een programmeertaal die op de webserver wordt uitgevoerd en HTML maakt voor die naar de browser gaat, bv. om gegevens uit een databank te tonen. De bezoeker ziet enkel het resultaat, niet de PHP-code.
- `Tag, element en attribuut` — De bouwstenen van HTML: Een tag staat tussen < >, bv. <a>. Een element is de openingstag, de inhoud en de sluittag samen: <a>tekst</a>. Een attribuut geeft extra info in de openingstag: <a href="pagina.html">.

## Linux (504)


### Archieven

- `gunzip | bunzip2` — Decomprimeer .gz: Pakt een .gz-bestand uit.
- `gunzip  decompress gzip compressed files (*.gz)` — Decomprimeer .gz: Pakt een .gz-bestand uit.
- `gzip` — Comprimeer: Comprimeert een bestand naar .gz.
- `gzip file` — Comprimeer: Comprimeert een bestand naar .gz.
- `gzip  a compression method (*.gz)` — Comprimeer: Comprimeert een bestand naar .gz.
- `tar` — Pak in / uit (.tar): Maakt of opent .tar(.gz)-archieven.
- `tar -cvf /var/tmp/archive.tar /home/guest` — Pak in / uit (.tar): Maakt of opent .tar(.gz)-archieven.
- `tar doesn't compress!` — Pak in / uit (.tar): Maakt of opent .tar(.gz)-archieven.
- `tar –t` — Pak in / uit (.tar): Maakt of opent .tar(.gz)-archieven.
- `tar  "tape archiver"` — Pak in / uit (.tar): Maakt of opent .tar(.gz)-archieven.
- `zcat | zless | zgrep` — Toon .gz-bestand: Toont de inhoud van een .gz-bestand zonder het uit te pakken.

### Bestanden & mappen

- `cp` — Kopieer: Kopieert bestanden of mappen: cp bron doel.
- `cp ./source file ./destination file` — Kopieer: Kopieert bestanden of mappen: cp bron doel.
- `cp with destination directory (without file name)  use source file name` — Kopieer: Kopieert bestanden of mappen: cp bron doel.
- `cp without path  current directory` — Kopieer: Kopieert bestanden of mappen: cp bron doel.
- `ln` — Maak een link: Maakt een verwijzing naar een bestand.
- `ln [-s] target linkname` — Maak een link: Maakt een verwijzing naar een bestand.
- `ln –s file1 link_to_file1` — Maak een link: Maakt een verwijzing naar een bestand.
- `ln –s package_name /usr/bin/package_name  make it recognizable` — Maak een link: Maakt een verwijzing naar een bestand.
- `mkdir` — Maak een map: Maakt een nieuwe map aan.
- `mkdir -p data/ruw` — Maak mappen aan: Maakt de map 'data' en daarin 'ruw' aan in één keer. Bestaan ze al, dan krijg je geen foutmelding.
- `mkdir directory(ies)` — Maak een map: Maakt een nieuwe map aan.
- `mkdir folder1 folder2` — Maak een map: Maakt een nieuwe map aan.
- `mkdir mydir` — Maak een map: Maakt een nieuwe map aan.
- `mv` — Verplaats of hernoem: Verplaatst een bestand/map, of hernoemt het: mv oudenaam nieuwenaam.
- `mv ./source file ./destination file` — Verplaats of hernoem: Verplaatst een bestand/map, of hernoemt het: mv oudenaam nieuwenaam.
- `mv file3 P00687.fasta` — Verplaats of hernoem: Verplaatst een bestand/map, of hernoemt het: mv oudenaam nieuwenaam.
- `mv ~/Documents/P00687.fasta .` — Verplaats of hernoem: Verplaatst een bestand/map, of hernoemt het: mv oudenaam nieuwenaam.
- `rm` — Verwijder: Verwijdert bestanden definitief (er is geen prullenbak).
- `rm file(s)` — Verwijder: Verwijdert bestanden definitief (er is geen prullenbak).
- `rm ~/Documents/file? ~/Downloads/file?` — Verwijder: Verwijdert bestanden definitief (er is geen prullenbak).
- `rmdir` — Verwijder lege map: Verwijdert een map, maar alleen als die leeg is.
- `rmdir directory(ies)` — Verwijder lege map: Verwijdert een map, maar alleen als die leeg is.
- `rmdir folder*` — Verwijder lege map: Verwijdert een map, maar alleen als die leeg is.
- `touch` — Maak leeg bestand: Maakt een leeg bestand aan, of werkt de datum bij van een bestaand bestand.
- `touch [option(s)] file(s)` — Maak leeg bestand: Maakt een leeg bestand aan, of werkt de datum bij van een bestaand bestand.
- `touch file1` — Maak leeg bestand: Maakt een leeg bestand aan, of werkt de datum bij van een bestaand bestand.
- `touch folder1/file1` — Maak leeg bestand: Maakt een leeg bestand aan, of werkt de datum bij van een bestaand bestand.
- `touch ~/file6` — Maak leeg bestand: Maakt een leeg bestand aan, of werkt de datum bij van een bestaand bestand.

### Bestanden bekijken

- `Less OS diversity` — Blader door bestand: Opent een bestand om rustig door te bladeren. Sluit af met q, zoek met /.
- `Less serious are frame shift errors` — Blader door bestand: Opent een bestand om rustig door te bladeren. Sluit af met q, zoek met /.
- `Less than` — Blader door bestand: Opent een bestand om rustig door te bladeren. Sluit af met q, zoek met /.
- `Less than or equal to` — Blader door bestand: Opent een bestand om rustig door te bladeren. Sluit af met q, zoek met /.
- `More useful (extensive) than $ man` — Blader door bestand: Toont een bestand pagina per pagina.
- `More variation is visible on the surface` — Blader door bestand: Toont een bestand pagina per pagina.
- `Wc -- help ( hulplijst van commands)` — Tel regels/woorden: Telt regels, woorden en tekens in een bestand.
- `cat` — Toon bestand: Toont de volledige inhoud van een bestand in de terminal, of plakt bestanden aan elkaar.
- `cat /etc/fedora-release` — Toon bestand: Toont de volledige inhoud van een bestand in de terminal, of plakt bestanden aan elkaar.
- `cat /usr/bin/who` — Toon bestand: Toont de volledige inhoud van een bestand in de terminal, of plakt bestanden aan elkaar.
- `cat files_to_remove.txt | xargs rm` — Toon bestand: Toont de volledige inhoud van een bestand in de terminal, of plakt bestanden aan elkaar.
- `cat –n /etc/profile` — Toon bestand: Toont de volledige inhoud van een bestand in de terminal, of plakt bestanden aan elkaar.
- `echo` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "And here we are\nHalf past three in the morning\nI can't get no sleep"` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Colleagues with blood that Dracula likes:\n";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Current salt concentration: " . $saltConcentration . "%\n";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Faithless's \"Insomnia\" lyrics:\n";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Feed level is now: $feedLevel\n";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Hello World!";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Hello world!"` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Is this just fantasy?";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "It would take roughly " . $years . " years for a " . $argv[1] . " to slither around the globe!\n";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Liftoff! 🚀";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Mathias has spilled spaghetti sauce " . count($spills) . " times.";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Mathias needs to add 25 ml a total of " . $additions . " times to reach 375 ml.";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Open your eyes, look up to the skies and see";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Oral temperature: " . $oral . "°C\n" . "Rectal temperature: " . $rectal . "°C\n" /* etc */;` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "T-minus " . $countdown . " seconds and counting...\n";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "The ABV is: " . ($OG - $FG) * 131.25 . "%";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "The car's fuel type is: " . $carSpecs['fuel type'];` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "The chameleon changes to $chameleon_color color.";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "The client $clientName has no remaining space for tattoos.\n";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "The condition of the {$pokemon_name} card is: " . $pokemon_cards[$pokemon_name];` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "The password for Mathias' Howest account is: ", $howestPassword;` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "The pet has died of hunger. Final feed level: $feedLevel\n";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "The salt concentration has surpassed the tolerance level of " . $maxTolerance . "%.\n";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "The temperature in Celsius is: " . $temperature . "°C";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "The word '$word' contains ". strlen($word) ." characters.";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Warning: The average noise level during $lecture was too high.\n";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Warning: You are in the spitting danger zone!";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "We just attended a performance by K$sha.";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Welcome " . $_POST['surname'];` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "You are a(n) " . $ageStatus[$age];` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "You are safe.";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "You do not have a card for $pokemon_name.";` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "Your total protein intake is $totalProtein grams."; // Display the total protein intake` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "\$# returns $#"` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "\$* returns $*"` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "\$@ returns $@"` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo "thx mate :)"` — Print tekst op het scherm: Schrijft de tekst tussen aanhalingstekens gewoon terug naar het scherm. De aanhalingstekens zorgen dat spaties en tekens zoals :) als één stuk tekst gezien worden.
- `echo $1 is a file` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo $1 is not a file` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo $?` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo $ANSWER` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo $ANSWER #reading the variable` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo $LINE` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo $PATH` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo $TODAY` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo $VARIABLE` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo $eatingContestResults[$food][0];` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo $i` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo $passwordString;` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo $scientificName;` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo $variable;` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo ${VAR##/*/}` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo ${VAR#/*/}` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo ${VAR%%.*}` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo ${VAR%.*}` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo ${VAR//one/four}` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo ${VAR/one/four}` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo 'Dish #' . $number . ': ' . $menu[$number];` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo Enter text and press Enter` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo counter equals $COUNTER` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo curly bra\*` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo curly bra{cket,ce}s` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo implode(" ", $words);` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo nice` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo preg_replace('/(\+\d{2})(\d{3})(\d{2})(\d{2})(\d{2})/', '$1 $2 $3 $4 $5', '+32492756421');` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo strtolower($uppercaseEmail);` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo strtoupper($uppercaseEmail);` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo the value of "$VALUE" equals $VALUE` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo the value of $VALUE equals $VALUE` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo the value of '$VALUE' equals $VALUE` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo the value of \$VALUE equals $VALUE` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo too bad` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo value;` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo wc –l myfile` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `echo wc –l myfile | bash` — Print tekst: Schrijft tekst of de waarde van een variabele naar het scherm.
- `head` — Toon begin van bestand: Toont de eerste regels van een bestand (standaard 10).
- `head -n 1 snp151annotation.txt > HEADER` — Toon begin van bestand: Toont de eerste regels van een bestand (standaard 10).
- `head -n 20 sequentie.fasta` — Toon de eerste 20 regels: Toont de eerste 20 regels van een FASTA-bestand, handig om snel te zien hoe het bestand eruitziet zonder alles te openen.
- `head /usr/share/doc/zip/WHATSNEW` — Toon begin van bestand: Toont de eerste regels van een bestand (standaard 10).
- `head file` — Toon begin van bestand: Toont de eerste regels van een bestand (standaard 10).
- `head –n 5 snp151*` — Toon begin van bestand: Toont de eerste regels van een bestand (standaard 10).
- `less` — Blader door bestand: Opent een bestand om rustig door te bladeren. Sluit af met q, zoek met /.
- `less common` — Blader door bestand: Opent een bestand om rustig door te bladeren. Sluit af met q, zoek met /.
- `more disorder  often only clear difference` — Blader door bestand: Toont een bestand pagina per pagina.
- `tail` — Toon einde van bestand: Toont de laatste regels van een bestand (standaard 10).
- `tail -n +2 snp151annotation.txt > DATA` — Toon einde van bestand: Toont de laatste regels van een bestand (standaard 10).
- `tail file` — Toon einde van bestand: Toont de laatste regels van een bestand (standaard 10).
- `wc` — Tel regels/woorden: Telt regels, woorden en tekens in een bestand.
- `wc [option(s)] [file(s)]` — Tel regels/woorden: Telt regels, woorden en tekens in een bestand.
- `wc –l  print newline counts` — Tel regels/woorden: Telt regels, woorden en tekens in een bestand.
- `wc –lw or $ wc -wl` — Tel regels/woorden: Telt regels, woorden en tekens in een bestand.
- `wc –w  print word counts` — Tel regels/woorden: Telt regels, woorden en tekens in een bestand.

### Combinaties

- `ls -l /etc | grep cron | grep –v crontab` — Toon inhoud van een map → Zoek tekst in bestanden → Zoek tekst in bestanden: Lijst de bestanden en mappen op in de huidige (of opgegeven) map. Daarna: Toont de regels die een zoekpatroon bevatten. Daarna: Toont de regels die een zoekpatroon bevatten.
- `tar -tf /var/tmp/archive.tar | grep file` — Pak in / uit (.tar) → Zoek tekst in bestanden: Maakt of opent .tar(.gz)-archieven. Daarna: Toont de regels die een zoekpatroon bevatten.
- `who | sort | awk '{print $1}'` — Sorteer regels → Verwerk kolommen: Sorteert de regels van een bestand of invoer. Daarna: Kleine programmeertaal om tekst per regel en kolom te bewerken.

### Doorsturen (redirect)

- `ls -l > ile.txt` — Bewaar maplijst in een bestand: Maakt een gedetailleerde lijst van de huidige map en schrijft die niet naar het scherm maar in het bestand ile.txt. Bestaat ile.txt al, dan wordt het overschreven.

### Jokertekens (wildcards)

- `ls [!MV]*` — Toon alles behalve wat met M of V begint: Toont alle bestanden en mappen waarvan de naam NIET met een hoofdletter M of V begint (dus zonder Music en Videos). Omdat het ook mappen zijn, toont ls van elke map de inhoud eronder.
- `wc *ile.txt` — Tel in alle bestanden op 'ile.txt': Telt regels, woorden en bytes van elk bestand dat eindigt op 'ile.txt', met om het even wat (ook niets) ervoor. Daarom vond het zowel file.txt als ile.txt, plus een totaalregel.
- `wc ?ile.txt` — Tel in bestanden die op 'ile.txt' eindigen: Telt regels, woorden en bytes van elk bestand waarvan de naam bestaat uit precies één willekeurig teken + 'ile.txt'. Bij jou vond het file.txt (20 regels, 166 woorden, 924 bytes). ile.txt zelf valt erbuiten, want ? moet precies één teken zijn.

### Navigatie

- `Ls = action (pwd)` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `cd` — Terug naar je thuismap: cd zonder map erachter brengt je altijd terug naar je thuismap (~). Je zag de prompt veranderen van ~/Documents naar ~.
- `cd (without arguments)  return to home directory` — Wissel van map: Gaat naar een andere map. 'cd ..' gaat één map omhoog, 'cd ~' naar je thuismap, 'cd -' naar de vorige map.
- `cd + enter: home directory` — Wissel van map: Gaat naar een andere map. 'cd ..' gaat één map omhoog, 'cd ~' naar je thuismap, 'cd -' naar de vorige map.
- `cd ../../systemd` — Wissel van map: Gaat naar een andere map. 'cd ..' gaat één map omhoog, 'cd ~' naar je thuismap, 'cd -' naar de vorige map.
- `cd /` — Wissel van map: Gaat naar een andere map. 'cd ..' gaat één map omhoog, 'cd ~' naar je thuismap, 'cd -' naar de vorige map.
- `cd /usr/share/vim` — Wissel van map: Gaat naar een andere map. 'cd ..' gaat één map omhoog, 'cd ~' naar je thuismap, 'cd -' naar de vorige map.
- `cd mydir` — Wissel van map: Gaat naar een andere map. 'cd ..' gaat één map omhoog, 'cd ~' naar je thuismap, 'cd -' naar de vorige map.
- `cd vim91` — Wissel van map: Gaat naar een andere map. 'cd ..' gaat één map omhoog, 'cd ~' naar je thuismap, 'cd -' naar de vorige map.
- `cd ~/Documents` — Wissel van map: Gaat naar een andere map. 'cd ..' gaat één map omhoog, 'cd ~' naar je thuismap, 'cd -' naar de vorige map.
- `cd ~/projecten` — Ga naar de map projecten: Wisselt naar de map 'projecten' in je thuismap. ~ is een afkorting voor je thuismap.
- `ls` — Toon inhoud van de map: Toont de bestanden en mappen in de map waarin je nu staat. Mappen verschijnen meestal in het blauw.
- `ls --help  explanation of how to use the tool` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls --version  explanation about the version of ls` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls -F file type colours` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls -l` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls -l (list directory content in long listing format)` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls -la` — Toon alle bestanden in detail: Toont alle bestanden in de huidige map, ook verborgen bestanden, met rechten, eigenaar, grootte en datum.
- `ls /etc  overview of content of directory /etc` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls D*  to print the content of directories starting with a "D"` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls [option(s)] [directory(ies)]` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls –F  determination of file type using colours` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls –F  determination of file type using suffixes` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls –a -l or $ ls -al  combination of both options` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls –a  all files (also invisible)` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls –i` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls –l > my_home_today` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls –l >> date_'date +%y%m%d'` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls –l  determination of file type using first character` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `ls –l  list of properties` — Toon inhoud van een map: Lijst de bestanden en mappen op in de huidige (of opgegeven) map.
- `pwd` — Toon huidige map: Print het volledige pad van de map waarin je nu staat (print working directory).

### Netwerk & downloads

- `SCP = Secure Copy Protocol` — Kopieer via netwerk: Kopieert bestanden van/naar een andere computer via SSH.
- `SSH = Secure Shell` — Log in op server: Maakt een beveiligde verbinding met een andere computer.
- `SSH and SFTP/SCP` — Log in op server: Maakt een beveiligde verbinding met een andere computer.
- `curl` — Haal URL op: Haalt data op van een internetadres.
- `curl localhost:80` — Haal URL op: Haalt data op van een internetadres.
- `scp` — Kopieer via netwerk: Kopieert bestanden van/naar een andere computer via SSH.
- `scp /path/to/file username@IP:/path/to/destination` — Kopieer via netwerk: Kopieert bestanden van/naar een andere computer via SSH.
- `scp [source] [destination]` — Kopieer via netwerk: Kopieert bestanden van/naar een andere computer via SSH.
- `scp username@IP:/path/to/file /path/to/destination` — Kopieer via netwerk: Kopieert bestanden van/naar een andere computer via SSH.
- `ssh` — Log in op server: Maakt een beveiligde verbinding met een andere computer.
- `ssh [user@]hostname` — Log in op server: Maakt een beveiligde verbinding met een andere computer.
- `wget = download` — Download bestand: Downloadt een bestand van een internetadres.
- `wget www.uniprot.org/uniprot/P00687.fasta` — Download bestand: Downloadt een bestand van een internetadres.

### Overig

- `$(date +%A) # what happens?`
- `./configure`
- `./script_name.sh parameter1 parameter2`
- `./script_name.sh  run script`
- `./script_name.sh  script directory is indicated with ./`
- `ANSWER=yes`
- `EDITOR='which gedit'; VISUAL='which gedit'; export EDITOR VISUAL`
- `PINGU=Tux`
- `Select all oxygen atoms except hydroxyls`
- `Select backbone nitrogens from alanine residues`
- `Sort, filter, cut … (see chapter 7)`
- `UNAME=guest`
- `a script to read lines of a file`
- `alias`
- `alias command='command –options'`
- `apropos`
- `apropos browser`
- `at [options] time`
- `at  to run a task on defined time`
- `atq`
- `atq  Overview of all the at jobs (queue)`
- `atrm`
- `atrm  remove job with job number from atq`
- `basename`
- `basename /home/guest/file.txt  file.txt`
- `bash`
- `bash #open a sub shell`
- `bg %nr  activate after Ctrl + Z`
- `bunzip2  decompress bzip2 compressed files (*.bz2)`
- `bzcat | bzgrep | bzless`
- `bzcat, $ bzgrep and $ bzless for bzip2 files (*.bz2)`
- `bzip2`
- `bzip2  an alternative compression method (*.bz2)`
- `cd, $ pwd and $ exit  part of Bash, booted in a terminal`
- `chgrp`
- `chgrp [options] group_spec files`
- `chroot`
- `command > file name`
- `crontab`
- `crontab –e`
- `crontab –e  '#' in front of the line`
- `crontab –l  list of scheduled tasks`
- `crontab  to perform a task over and over again, monthly, weekly, daily, every hour or every minute`
- `date +%A # example of a string specification`
- `date > date_'date +%y%m%d'`
- `dirname`
- `dirname /home/guest/file.txt  /home/guest`
- `dnf`
- `dnf list  list all available programs`
- `dnf search pattern  search for a package`
- `docker`
- `docker compose down`
- `docker compose exec …`
- `docker compose ps`
- `docker compose up`
- `docker exec CONTAINER_ID command`
- `docker exec webserver curl localhost:80`
- `docker images`
- `docker ps -a  list all containers`
- `docker ps  only running containers`
- `docker pull biocontainers/fastqc:v0.11.9_cv8`
- `docker pull ubuntu`
- `docker rm (-f) CONTAINER_ID`
- `docker rmi IMAGE_ID`
- `docker run --detach --name webserver --publish 80:80 nginx`
- `docker run --detach --name webserver -p 8080:80 nginx`
- `docker run --detach ubuntu sleep 100`
- `docker run --detach ubuntu tail –f /dev/null`
- `docker run --rm --detach --name webserver nginx`
- `docker run -it ubuntu /bin/bash`
- `docker run ubuntu /bin/ls`
- `docker stop CONTAINER_ID`
- `docker system prune`
- `export`
- `export ANSWER=yes`
- `export PATH=$PATH:directory`
- `export PINGU`
- `export UNAME`
- `export VARIABLE`
- `fg %nr  background process to front`
- `file`
- `file /bin/ls`
- `file /dev/input/mouse0`
- `file /etc/fedora-release`
- `file /etc/profile`
- `file /usr/bin/who`
- `file /usr/share/pixmaps/fedora-logo-small.png`
- `file Desktop`
- `hard links`
- `info`
- `info info`
- `info ls`
- `jobs`
- `join`
- `join -o allows to specify which fields to retain in output`
- `join -t $'\t' -o '1.1 1.2 2.2' --header snp151position-sorted.txt snp151annotation-sorted.txt`
- `join [options] FILE1 FILE2`
- `ll > file`
- `locate`
- `locate pattern`
- `locate –d ~/dbfile pattern`
- `make`
- `my first script`
- `nice`
- `nice [-n level] [command]`
- `paste`
- `paste [options] [files]`
- `paste tmp5 tmp6 tmp1`
- `podman run ubuntu /bin/ls`
- `printenv`
- `printenv  view $HOME and $USERNAME`
- `printf`
- `printf "A %s team counts %d players.\n" soccer 11`
- `printf FORMAT [ARGUMENT(S)]`
- `renice`
- `renice +1 987 –u root`
- `renice [–n] priority IDs`
- `request a variable without parameters on the command line`
- `resi to select by residue numbers`
- `script with arguments`
- `script with positional parameters`
- `set +o option  "Disable" an option`
- `set [–o|+o] option`
- `set –o noclobber`
- `set –o option  "Enable" an option`
- `simple script by Paco Hulpiau`
- `sleep`
- `sleep 60`
- `sleep  to wait a short time`
- `source`
- `stat`
- `stat object`
- `strings`
- `strings /usr/bin/who`
- `strings file`
- `sudo`
- `sudo dnf -y install dnf-plugins-core`
- `sudo dnf install [package_name | package.rpm]`
- `sudo dnf install docker-ce docker-ce-cli containerd.io`
- `sudo dnf install docker-compose`
- `sudo dnf install firefox php`
- `sudo dnf install info`
- `sudo dnf install pymol`
- `sudo dnf install xterm`
- `sudo dnf upgrade`
- `sudo dnf-3 config-manager --add-repo \`
- `sudo docker run hello-world`
- `sudo make install`
- `sudo systemctl enable docker`
- `sudo systemctl start docker`
- `sudo usermod –aG docker guest`
- `tee`
- `test command  exit-status (0 success, 1 no success)`
- `test for file`
- `test –f /etc/passwd`
- `time`
- `time command`
- `time find /usr`
- `timeout`
- `timeout 5 sleep 60`
- `timeout [options] seconds command`
- `umask`
- `umask  allows you to change the user mask`
- `umask  defines the umask numeric value`
- `unset`
- `unset PINGU`
- `unset variable`
- `updatedb –l 0 –o ~/dbfile –U /`
- `uptime`
- `uptime (and the first line of $ w and $ top)`
- `use CASE to test multiple options`
- `w  who is logged on and what are they doing?`
- `watch`
- `watch [options] command`
- `watch date`
- `watch  execute command at regular intervals`
- `what is bash  GNU Bourne-again shell`
- `whatis`
- `whatis ls`
- `who | tee file`
- `xargs`
- `xkill  to end graphical programs`
- `xterm &`
- `xterm vs $ xterm &`
- `zcat, $ zgrep and $ zless for GNU zip files (*.gz)`
- `zipless and $ zipgrep for zipped files (*.zip)`
- `zipless | zipgrep`

### Pakketten

- `Conda commands:` — Conda-omgevingen: Beheert Python/bio-informatica-pakketten en omgevingen.
- `conda` — Conda-omgevingen: Beheert Python/bio-informatica-pakketten en omgevingen.
- `conda config --add channels bioconda` — Conda-omgevingen: Beheert Python/bio-informatica-pakketten en omgevingen.
- `conda config --add channels conda-forge` — Conda-omgevingen: Beheert Python/bio-informatica-pakketten en omgevingen.
- `conda config --add channels defaults` — Conda-omgevingen: Beheert Python/bio-informatica-pakketten en omgevingen.
- `conda config --set channel_priority strict` — Conda-omgevingen: Beheert Python/bio-informatica-pakketten en omgevingen.
- `conda create --yes --name "env_name"` — Conda-omgevingen: Beheert Python/bio-informatica-pakketten en omgevingen.
- `conda env create -n <env-name> --file <environment.yaml>` — Conda-omgevingen: Beheert Python/bio-informatica-pakketten en omgevingen.
- `conda env export > my_tool.yaml (creates a yaml def)` — Conda-omgevingen: Beheert Python/bio-informatica-pakketten en omgevingen.
- `conda env update --file <environment.yaml>` — Conda-omgevingen: Beheert Python/bio-informatica-pakketten en omgevingen.
- `conda install --yes seqtk=1.3` — Conda-omgevingen: Beheert Python/bio-informatica-pakketten en omgevingen.
- `conda list` — Conda-omgevingen: Beheert Python/bio-informatica-pakketten en omgevingen.
- `pip install pmw` — Python-pakketten: Installeert Python-pakketten.

### Rechten & gebruikers

- `chmod` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chmod +x script.sh` — Maak script uitvoerbaar: Geeft een script uitvoerrechten, zodat je het daarna kan starten met ./script.sh.
- `chmod 400 file` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chmod 500 directory` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chmod 600 file` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chmod 644 file` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chmod 660 file` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chmod 700 file` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chmod 755 file` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chmod 755 script_name.sh  executable script` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chmod 770 file` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chmod 777 file` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chmod [ugoa][-+=][rwx...] file` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chmod a+x script_name.sh  executable for all` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chmod a-x mydir` — Wijzig rechten: Past aan wie een bestand mag lezen (r), schrijven (w) of uitvoeren (x).
- `chown` — Wijzig eigenaar: Verandert de eigenaar van een bestand of map.
- `chown [options] user_spec files` — Wijzig eigenaar: Verandert de eigenaar van een bestand of map.

### Systeem & processen

- `Exit and die functions` — Sluit terminal: Sluit de huidige terminalsessie af.
- `Exit site (E)` — Sluit terminal: Sluit de huidige terminalsessie af.
- `Exit status stored in "$?"` — Sluit terminal: Sluit de huidige terminalsessie af.
- `Exit the subshell ($ exit)` — Sluit terminal: Sluit de huidige terminalsessie af.
- `Man page is overvieuw` — Handleiding: Opent de handleiding van een commando, bv. 'man ls'. Sluit af met q.
- `Top - Output $ uptime` — Live processen: Live overzicht van processen en geheugen-/CPU-gebruik. Sluit af met q.
- `Top 7:` — Live processen: Live overzicht van processen en geheugen-/CPU-gebruik. Sluit af met q.
- `Top left:` — Live processen: Live overzicht van processen en geheugen-/CPU-gebruik. Sluit af met q.
- `Top right:` — Live processen: Live overzicht van processen en geheugen-/CPU-gebruik. Sluit af met q.
- `clear` — Maak scherm leeg: Maakt de terminal leeg.
- `exit` — Sluit terminal: Sluit de huidige terminalsessie af.
- `free interface diffusion` — Geheugengebruik: Toont het gebruikte en vrije werkgeheugen.
- `htop` — Live processen (kleur): Uitgebreidere, kleurrijke versie van top.
- `kill` — Stop een proces: Stopt een proces via zijn nummer (PID).
- `kill %nr  Ctrl + C for background process (or use PID)` — Stop een proces: Stopt een proces via zijn nummer (PID).
- `kill -l  list of possible signal values` — Stop een proces: Stopt een proces via zijn nummer (PID).
- `man` — Handleiding: Opent de handleiding van een commando, bv. 'man ls'. Sluit af met q.
- `man ls` — Handleiding: Opent de handleiding van een commando, bv. 'man ls'. Sluit af met q.
- `man man` — Handleiding: Opent de handleiding van een commando, bv. 'man ls'. Sluit af met q.
- `man man  /exit status  n` — Handleiding: Opent de handleiding van een commando, bv. 'man ls'. Sluit af met q.
- `man test` — Handleiding: Opent de handleiding van een commando, bv. 'man ls'. Sluit af met q.
- `man –nrame  $ echo $?` — Handleiding: Opent de handleiding van een commando, bv. 'man ls'. Sluit af met q.
- `ps` — Toon processen: Toont de programma's die nu draaien.
- `ps –Aef` — Toon processen: Toont de programma's die nu draaien.
- `ps  display information about your running processes` — Toon processen: Toont de programma's die nu draaien.
- `top` — Live processen: Live overzicht van processen en geheugen-/CPU-gebruik. Sluit af met q.
- `top  real-time view of a running system (including batch processes)` — Live processen: Live overzicht van processen en geheugen-/CPU-gebruik. Sluit af met q.
- `which` — Waar staat programma: Toont waar een programma geïnstalleerd staat.
- `which [command]  PATH  directories` — Waar staat programma: Toont waar een programma geïnstalleerd staat.
- `which brings consecutive phosphate` — Waar staat programma: Toont waar een programma geïnstalleerd staat.
- `which command` — Waar staat programma: Toont waar een programma geïnstalleerd staat.
- `which ls` — Waar staat programma: Toont waar een programma geïnstalleerd staat.
- `which name is given as an argument` — Waar staat programma: Toont waar een programma geïnstalleerd staat.
- `which package_name` — Waar staat programma: Toont waar een programma geïnstalleerd staat.
- `which rm` — Waar staat programma: Toont waar een programma geïnstalleerd staat.
- `which searches all directories defined by the PATH variable = a list of directories containing (executable) programs` — Waar staat programma: Toont waar een programma geïnstalleerd staat.
- `which seqtk` — Waar staat programma: Toont waar een programma geïnstalleerd staat.

### Zoeken & filteren

- `Cut and paste:` — Knip kolommen: Haalt bepaalde kolommen of tekens uit elke regel.
- `Find files in a directory hierarchy: $ find` — Zoek bestanden: Zoekt bestanden en mappen op naam, type, grootte… vanaf een startmap.
- `Find the installation directory of the executable` — Zoek bestanden: Zoekt bestanden en mappen op naam, type, grootte… vanaf een startmap.
- `Sort DATA on column 2` — Sorteer regels: Sorteert de regels van een bestand of invoer.
- `awk` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk '/ccttcc/ {print $1}' snp151annotation.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk '/ccttcc/' snp151annotation.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk '/pattern/'  to match a regular expression pattern` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk 'BEGIN {n=0}; /CCTTCC/ {n++}; END {print n}' snp151annotation.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk 'BEGIN {print "2+3=" 2+3}'` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk 'BEGIN {print "some text"}'` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk 'BEGIN {print "some text"}' snp151annotation.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk 'BEGIN {print 2+3}'` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk 'END {print NR}' snp151annotation.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk 'NR < 6 {print $0}' snp151annotation.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk 'NR < 6' snp151annotation.txt  default action is to print` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk 'NR == 1' snp151annotation.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk 'NR > 1 && NR < 7' snp151annotation.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk 'NR > 1 {s=0; for (i=2; i<=NF; i++) s=s+$i; print s}' arrayDat.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk 'NR > 1 {s=0; n=NF-1; for (i=2; i<=NF; i++) s=s+$i; s=s/n; print s}' arrayDat.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk 'condition {action}' inputfile` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk '{print $1, "\t", $3, "\t", $2}' snp151annotation.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk '{print $1, $3, $2}' snp151annotation.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk '{print $1}' snp151annotation.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk '{print $NF}' snp151annotation.txt ?` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk '{print NF}' snp151annotation.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk '{print NR}' snp151annotation.txt` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk '{print}'  print output to screen` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk built-in variables:` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk reads an input file, one line at a time, to match "condition" and perform "action" upon success` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `awk treats a file as a set of 'records' divided in different 'fields' (= columns)` — Verwerk kolommen: Kleine programmeertaal om tekst per regel en kolom te bewerken.
- `cut` — Knip kolommen: Haalt bepaalde kolommen of tekens uit elke regel.
- `cut -f 1 snp151annotation.txt` — Knip kolommen: Haalt bepaalde kolommen of tekens uit elke regel.
- `cut -f 1 snp151annotation.txt > tmp1` — Knip kolommen: Haalt bepaalde kolommen of tekens uit elke regel.
- `cut -f 1-3 snp151position.txt` — Knip kolommen: Haalt bepaalde kolommen of tekens uit elke regel.
- `cut -f 4 snp151position.txt` — Knip kolommen: Haalt bepaalde kolommen of tekens uit elke regel.
- `cut -f 5 snp151annotation.txt > tmp5` — Knip kolommen: Haalt bepaalde kolommen of tekens uit elke regel.
- `cut -f 6 snp151annotation.txt > tmp6` — Knip kolommen: Haalt bepaalde kolommen of tekens uit elke regel.
- `cut [options] [file]` — Knip kolommen: Haalt bepaalde kolommen of tekens uit elke regel.
- `find` — Zoek bestanden: Zoekt bestanden en mappen op naam, type, grootte… vanaf een startmap.
- `find directory option(s) [search actions]` — Zoek bestanden: Zoekt bestanden en mappen op naam, type, grootte… vanaf een startmap.
- `find ~ -name file6` — Zoek bestanden: Zoekt bestanden en mappen op naam, type, grootte… vanaf een startmap.
- `grep` — Zoek tekst in bestanden: Toont de regels die een zoekpatroon bevatten.
- `grep -c ">" sequentie.fasta` — Tel sequenties in FASTA: Telt hoeveel regels met '>' beginnen, dus hoeveel sequenties er in een FASTA-bestand staan.
- `grep ^\> P00687.fasta` — Zoek tekst in bestanden: Toont de regels die een zoekpatroon bevatten.
- `grep guest /etc/*` — Zoek tekst in bestanden: Toont de regels die een zoekpatroon bevatten.
- `grep guest /etc/* 2> error` — Zoek tekst in bestanden: Toont de regels die een zoekpatroon bevatten.
- `grep guest /etc/* > output` — Zoek tekst in bestanden: Toont de regels die een zoekpatroon bevatten.
- `grep string file` — Zoek tekst in bestanden: Toont de regels die een zoekpatroon bevatten.
- `sed` — Zoek en vervang: Bewerkt tekst per regel, bv. 's/oud/nieuw/g' vervangt tekst.
- `sed s/chr/chromosome/g snp151position.txt` — Zoek en vervang: Bewerkt tekst per regel, bv. 's/oud/nieuw/g' vervangt tekst.
- `sort` — Sorteer regels: Sorteert de regels van een bestand of invoer.
- `sort [options] [file]` — Sorteer regels: Sorteert de regels van een bestand of invoer.
- `uniq` — Verwijder dubbels: Haalt opeenvolgende dubbele regels weg (meestal na sort).
- `uniq [options] [FILE]` — Verwijder dubbels: Haalt opeenvolgende dubbele regels weg (meestal na sort).

## HTML (228)


### Formulieren

- `<form action="" method="POST">` — Formulier: Groepeert invoervelden en knoppen.
- `<form action="#" method="GET">` — Formulier: Groepeert invoervelden en knoppen.
- `<form action="#" method="POST" enctype="multipart/form-data">` — Formulier: Groepeert invoervelden en knoppen.
- `<form action="#" method="POST">` — Formulier: Groepeert invoervelden en knoppen.
- `<form action="#" method="POST"> <input type="submit" name="submit" value="Do not press this button!"> </form>` — Formulier: Groepeert invoervelden en knoppen.
- `<input type="checkbox" name="hot" checked> Blue faucet<br>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type="file" name="fasta">` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type="file" name="fasta"><br>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type="file" name="observations">` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type="radio" name="dish" value="burger" checked> Burger` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type="radio" name="dish" value="taco"> Taco <br>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type="submit" name="submit" value="Calculate Total Protein Intake">` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type="submit" name="submit" value="Submit mood">` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type="submit" name="submit" value="Submit">` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type="submit" name="submit">` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type="text" name="chemical"><br>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type="text" name="language"><br>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type="text" name="surname" placeholder="Provide your name"><br>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type='checkbox' name='' value=' checked'>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type='checkbox' name='' value=''>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type='email' name='' value=''>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type='hidden' name='' value=''>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type='number' name='' value=''>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type='password' name='' value=''>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type='radio' name='' value='' checked>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type='radio' name='' value=''>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input type='text' name='' value=''>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<input>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `<option value="bruges">Bruges</option>` — Keuze: Eén keuze in een select.
- `<option value="green">Happy</option>` — Keuze: Eén keuze in een select.
- `<option value="orange">Orange</option>` — Keuze: Eén keuze in een select.
- `<option value=''></option>` — Keuze: Eén keuze in een select.
- `<select name="city">` — Keuzelijst: Uitklaplijst met option-elementen.
- `<select name="flavors[]" id="groceries" multiple>` — Keuzelijst: Uitklaplijst met option-elementen.
- `<select name="mood">` — Keuzelijst: Uitklaplijst met option-elementen.
- `<textarea name="protein_grams"></textarea><br>` — Tekstvak: Invoerveld voor meerdere regels tekst.
- `Each option in the dropdown is defined by an <option> tag inside the` — Keuze: Eén keuze in een select.
- `Enter the correct email address: <input type="email" name="correct_email"><br>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `Enter your age: <input type="number" name="age"><br>` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `Enter your blood type: <input type="password" name="bloodType">` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `The <input> tag creates different types of input fields on a web page where` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `The <select> tag creates a dropdown menu where users can pick an option` — Keuzelijst: Uitklaplijst met option-elementen.
- `The <textarea> tag creates an input field that allows users to enter text` — Tekstvak: Invoerveld voor meerdere regels tekst.
- `The HTML form is made with the <form> tag and always requires two attributes:` — Formulier: Groepeert invoervelden en knoppen.
- `They are created with various HTML tags, such as <input>, <select>, and <textarea>*` — Invoerveld: Veld om iets in te typen of aan te vinken; type bepaalt de soort.
- `made in the <select> tag:` — Keuzelijst: Uitklaplijst met option-elementen.

### Head & koppelingen

- `<link rel="stylesheet" type="text/css" href="style.css">` — Koppel bestand: Koppelt een extern bestand, meestal een CSS-stylesheet.
- `<link>` — Koppel bestand: Koppelt een extern bestand, meestal een CSS-stylesheet.
- `<style>` — CSS in de pagina: Hierin schrijf je CSS-opmaak rechtstreeks in het HTML-bestand.
- `<style> .Mathias {visibility: hidden;} </style>` — CSS in de pagina: Hierin schrijf je CSS-opmaak rechtstreeks in het HTML-bestand.
- `<style> body {background: <?php echo $_GET['mood'] ?? 'white' ?>} </style>` — CSS in de pagina: Hierin schrijf je CSS-opmaak rechtstreeks in het HTML-bestand.
- `<style> body {background: <?php if(isset($_POST['submit'])){ echo "red"; } else{ echo "white"; } ?>;} </style>` — CSS in de pagina: Hierin schrijf je CSS-opmaak rechtstreeks in het HTML-bestand.
- `<style> div {text-decoration: line-through;} </style>` — CSS in de pagina: Hierin schrijf je CSS-opmaak rechtstreeks in het HTML-bestand.
- `<style> h2, h3 {letter-spacing: 40px;} </style>` — CSS in de pagina: Hierin schrijf je CSS-opmaak rechtstreeks in het HTML-bestand.
- `<style> img {border: 6px solid rgb(64,58,50);} </style>` — CSS in de pagina: Hierin schrijf je CSS-opmaak rechtstreeks in het HTML-bestand.
- `<style> p {color: red;} </style>` — CSS in de pagina: Hierin schrijf je CSS-opmaak rechtstreeks in het HTML-bestand.
- `<style> table, table * {border: solid black 1px; border-collapse: collapse;} </style>` — CSS in de pagina: Hierin schrijf je CSS-opmaak rechtstreeks in het HTML-bestand.
- `<title>` — Paginatitel: De tekst in het browsertabblad.
- `<title>An original title</title>` — Paginatitel: De tekst in het browsertabblad.
- `CSS rules are added inside the <style> tag within the HTML document's` — CSS in de pagina: Hierin schrijf je CSS-opmaak rechtstreeks in het HTML-bestand.

### Layout

- `<div class="BB WW">Say my name.</div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div class="Jasper"><!-- Information about Jasper --></div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div class="TopGun">Talk to me, Goose.</div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div class="nucleotides">TACGCTAGGCTAGGCA</div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div id="Paco">` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div id="Paco"></div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div id="container">` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div id="protein3">TACGCTAGGCTAGGCA</div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div style="width: 300px; height: 300px; background: green; border: solid black 15px; box-sizing: border-box;"></div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div title="Because they make up everything!">Why don't scientists trust atoms?</div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div>1st: Marieke</div><div>2nd: Kaat</div><div>3rd: Paco</div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div></div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div>May the force be with you.</div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div>Winter is coming.</div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `<div>or not to blockquote</div>` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.
- `echo "<div>The ABV is: " . ($OG - $FG) * 131.25 . "%</div>";` — Blok: Neutrale container om delen van de pagina te groeperen en op te maken.

### Lijsten

- `<ul><li>Item</li></ul>` — Lijst met bolletjes: Een ongeordende lijst; elk <li> is één punt in de lijst.
- `To create an ordered list (a list with numbers), <li> tags are enclosed within <ol> tags` — Lijstitem: Eén item in een ul- of ol-lijst.
- `To create an unordered list (a list with bullet points), <li> tags are enclosed within <ul> tags` — Lijstitem: Eén item in een ul- of ol-lijst.

### Links & media

- `<a href="#Jasper">Jasper</a><a href="#Paco">Paco</a><a href="#Cedric">Cedric</a><a href="#Mathias">Mathias</a>` — Link: Maakt een klikbare link; het adres staat in href.
- `<a href="AutomaticPass.html">Click this button to automatically pass BIT02!</a>` — Link: Maakt een klikbare link; het adres staat in href.
- `<a href="https://www.youtube.com">Click here</a>` — Link: Maakt een klikbare link; het adres staat in href.
- `<a href="mailto:mathias.verbeke@howest.be">Report a bug</a>` — Link: Maakt een klikbare link; het adres staat in href.
- `<a href="pagina2.html">Volgende</a>` — Link naar andere pagina: Maakt de klikbare tekst 'Volgende' die naar pagina2.html gaat.
- `<a href=''>` — Link: Maakt een klikbare link; het adres staat in href.
- `<a>` — Link: Maakt een klikbare link; het adres staat in href.
- `<img src= "HowestBioinformatics.png" width="30px;">` — Afbeelding: Toont een afbeelding; src = bestand, alt = beschrijving.
- `<img src="blackbeard.png"> <p>Arrr, ye be seein! the image of Blackbeard to the right!</p>` — Afbeelding: Toont een afbeelding; src = bestand, alt = beschrijving.
- `<img src="dimi.png">` — Afbeelding: Toont een afbeelding; src = bestand, alt = beschrijving.
- `<img src="eiwit.png" alt="Eiwitstructuur">` — Afbeelding tonen: Toont de afbeelding eiwit.png. De alt-tekst beschrijft de afbeelding voor schermlezers en als ze niet laadt.
- `<img src="https://upload.wikimedia.org/wikipedia/en/b/be/Luigi_by_Shigehisa_Nakaue.png" alt="Image of Luigi" width="500px">` — Afbeelding: Toont een afbeelding; src = bestand, alt = beschrijving.
- `<img>` — Afbeelding: Toont een afbeelding; src = bestand, alt = beschrijving.
- `The <a> tag is used to create hyperlinks to other web pages` — Link: Maakt een klikbare link; het adres staat in href.
- `The <img> tag comes with attributes that control its behavior and appearance:` — Afbeelding: Toont een afbeelding; src = bestand, alt = beschrijving.
- `The <img> tag is used to embed images in a webpage` — Afbeelding: Toont een afbeelding; src = bestand, alt = beschrijving.

### Overig

- `<blockquote id="Jasper">`
- `<blockquote>`
- `<fieldset>`
- `<legend>Lasagna from the Aldi</legend>`
- `<optgroup label="West Flanders">`
- `<q>`
- `<strike><div>HTML is not fun!</div></strike>`
- `<tag class=''>`
- `<tag id=''>`
- `<tag style=''>`
- `<tag title=''>`
- `After executing the command php -S localhost:<port> in the terminal, a URL will appear`
- `Link = connecting two or more file names to the same file data, e.g. $ ls –l /`
- `The <blockquote> tag is used to mark a block of text as a quotation from another source`
- `The <fieldset> tag creates a container with a visible border`
- `The <legend> tag adds an optional header that appears on top of the`
- `The <optgroup> element groups related options together in a <select>`
- `The <small> tag instructs the browser to display content in a smaller font size`
- `The <strike> tag is used to display text with a line through it`
- `a directory: $ ls`
- `body {background: pink;}`
- `body {font-family: 'Atkinson Hyperlegible', sans-serif;}`
- `div + h3 {background: red;}`
- `div > h3 {background: red;}`
- `div blockquote h3 {background: green;}`
- `div h3 {background: red;}`
- `div {`
- `div {width: 30px; height: 30px; border: 5px solid black;}`
- `div ~ h3 {background: orange;}`
- `h1 {color: hotpink;}`
- `h1, h2, h3 {text-align: center;}`
- `h1, h4 {`
- `h2, h3 {letter-spacing: 40px;}`
- `img {`
- `img {float: right;}`
- `php -S localhost:<port>`
- `span {color: red;}`

### Structuur

- `<!DOCTYPE html>` — Documenttype: Staat helemaal bovenaan elk HTML-bestand en vertelt de browser dat het om moderne HTML gaat.
- `<body>` — Zichtbare inhoud: Alles wat je op de pagina ziet staat hierin.
- `<body> <div> <img src="Mime.png"> </div> </body>` — Zichtbare inhoud: Alles wat je op de pagina ziet staat hierin.
- `<body> <div>4th level</div> <div>3rd level</div> <div>2nd level</div> <div>1st level</div> </body>` — Zichtbare inhoud: Alles wat je op de pagina ziet staat hierin.
- `<body> <div>CSS is not fun!</div> </body>` — Zichtbare inhoud: Alles wat je op de pagina ziet staat hierin.
- `<body> <ol> <li>Augustus</li> <li>Tiberius</li> <li>Caligula</li> </ol> </body>` — Zichtbare inhoud: Alles wat je op de pagina ziet staat hierin.
- `<body> <ul><li>Unintended injuries</li><li>Wildlife disruption</li><li>Environmental contamination</li></ul> </body>` — Zichtbare inhoud: Alles wat je op de pagina ziet staat hierin.
- `<head>` — Kop (onzichtbaar): Bevat info over de pagina: titel, tekenset, links naar CSS.
- `<head> <style> div {border: 2px solid black; width: 70px; height: 100px;} </style> </head>` — Kop (onzichtbaar): Bevat info over de pagina: titel, tekenset, links naar CSS.
- `<head> <style> img {height: 250px;} div {border: 5px solid black; width: fit-content; padding: 16px;} </style> </head>` — Kop (onzichtbaar): Bevat info over de pagina: titel, tekenset, links naar CSS.
- `<head> <style> img {height: 250px;} div {border: 5px solid black;} </style> </head>` — Kop (onzichtbaar): Bevat info over de pagina: titel, tekenset, links naar CSS.
- `<head> <style> li {list-style-type: none;} </style> </head>` — Kop (onzichtbaar): Bevat info over de pagina: titel, tekenset, links naar CSS.
- `<head> <style> li {list-style-type: upper-roman;} </style> </head>` — Kop (onzichtbaar): Bevat info over de pagina: titel, tekenset, links naar CSS.
- `<head> section` — Kop (onzichtbaar): Bevat info over de pagina: titel, tekenset, links naar CSS.
- `<head><title>ABV calculator</title></head>` — Kop (onzichtbaar): Bevat info over de pagina: titel, tekenset, links naar CSS.
- `<html lang="en">` — Hoofdelement: Omvat de hele pagina.
- `<html>` — Hoofdelement: Omvat de hele pagina.
- `The <!DOCTYPE html> declartion specifies that the document is an HTML5 document` — Documenttype: Staat bovenaan elk HTML-bestand en vertelt de browser dat het moderne HTML is.
- `The <html> tag, along with the closing </html> tag, marks the start and end of an HTML document` — Hoofdelement: Omvat de hele pagina.

### Tabellen

- `* Applying it to <tr>, <th>, or <td> elements will not have any effect.` — Tabelrij: Eén rij in een tabel.
- `<table>` — Tabel: Maakt een tabel met rijen (tr) en cellen (td/th).
- `<td><img src="Paco.png"></td>` — Tabelcel: Gewone cel in een rij.
- `<th>1</th><td>X</td><td></td><td>O</td>` — Kopcel: Titelcel van een kolom of rij, standaard vet.
- `<th></th><th>1</th><th>2</th><th>3</th>` — Kopcel: Titelcel van een kolom of rij, standaard vet.
- `<tr>` — Tabelrij: Eén rij in een tabel.
- `<tr> <td>O</td> <td>X</td> <td>X</td> </tr>` — Tabelrij: Eén rij in een tabel.
- `The <td> tag represents a single cell in a table row` — Tabelcel: Gewone cel in een rij.
- `The <th> tag defines a header cell in a table, typically used for labeling columns or rows` — Kopcel: Titelcel van een kolom of rij, standaard vet.
- `The <tr> tag is used to define a row within a table` — Tabelrij: Eén rij in een tabel.
- `This property should be applied to the <table> element*` — Tabel: Maakt een tabel met rijen (tr) en cellen (td/th).

### Tekst

- `* Experiment by replacing the <pre> tags with other tags (e.g., <p>, <div>) and observe the changes in the browser.` — Voorgeformatteerd: Behoudt spaties en regeleindes precies zoals getypt.
- `* Open the packaging <br>` — Nieuwe regel: Forceert een regeleinde (heeft geen sluittag).
- `<Pre> tag: monospaced font: alle letters nemen ongeveer evenveel ruimte in.` — Voorgeformatteerd: Behoudt spaties en regeleindes precies zoals getypt.
- `<code>` — Code: Toont tekst als code (monospace).
- `<em>` — Nadruk (schuin): Legt nadruk, standaard schuin.
- `<h1>` — Kop niveau 1: De belangrijkste titel. Er bestaan h1 t/m h6, van groot naar klein.
- `<h1></h1>` — Kop niveau 1: De belangrijkste titel. Er bestaan h1 t/m h6, van groot naar klein.
- `<h1>Calculate Alcohol By Volume (ABV)</h1>` — Kop niveau 1: De belangrijkste titel. Er bestaan h1 t/m h6, van groot naar klein.
- `<h1>Capecitabine Information</h1>` — Kop niveau 1: De belangrijkste titel. Er bestaan h1 t/m h6, van groot naar klein.
- `<h1>Cataract Awareness</h1>` — Kop niveau 1: De belangrijkste titel. Er bestaan h1 t/m h6, van groot naar klein.
- `<h1>I want to believe.</h1>` — Kop niveau 1: De belangrijkste titel. Er bestaan h1 t/m h6, van groot naar klein.
- `<h1>Welcome to Barbie's Dream World!</h1>` — Kop niveau 1: De belangrijkste titel. Er bestaan h1 t/m h6, van groot naar klein.
- `<h2 id="Cedric"></h2>` — Kop niveau 2: Tussentitel.
- `<h2>` — Kop niveau 2: Tussentitel.
- `<h2></h2>` — Kop niveau 2: Tussentitel.
- `<h2>I'm the king of the world!</h2>` — Kop niveau 2: Tussentitel.
- `<h3 id="Bart"></h3>` — Kop niveau 3: Kleinere tussentitel.
- `<h3 id="Mathias"></h3>` — Kop niveau 3: Kleinere tussentitel.
- `<h3>` — Kop niveau 3: Kleinere tussentitel.
- `<h3></h3>` — Kop niveau 3: Kleinere tussentitel.
- `<h3>Say hello to my little friend!</h3>` — Kop niveau 3: Kleinere tussentitel.
- `<h4 id="Anneleen"></h4>` — Kop niveau 4: Kleine tussentitel.
- `<h4 id="Marieke"></h4>` — Kop niveau 4: Kleine tussentitel.
- `<h4></h4>` — Kop niveau 4: Kleine tussentitel.
- `<h4>I see dead people.</h4>` — Kop niveau 4: Kleine tussentitel.
- `<h5 id="Bart"></h5>` — Kop niveau 5: Kleine tussentitel.
- `<h5></h5>` — Kop niveau 5: Kleine tussentitel.
- `<h6></h6>` — Kop niveau 6: Kleinste tussentitel.
- `<hr>` — Scheidingslijn: Horizontale lijn tussen twee delen.
- `<p class="BB WW">I am the one who knocks!</p>` — Alinea: Een blok gewone tekst.
- `<p class="TopGun">You can be my wingman any time.</p>` — Alinea: Een blok gewone tekst.
- `<p class="nucleotides">ATCGGCTAAGCTTACG</p>` — Alinea: Een blok gewone tekst.
- `<p class="vader">When I left you, I was but the learner. Now I am the master.</p>` — Alinea: Een blok gewone tekst.
- `<p id="protein">VLSPADKTNVKAAWGK</p>` — Alinea: Een blok gewone tekst.
- `<p id="vader">When I left you, I was but the learner. Now I am the master.</p>` — Alinea: Een blok gewone tekst.
- `<p style="color: red">ATCGGCTAAGCTTACG</p>` — Alinea: Een blok gewone tekst.
- `<p style="font-family: 'Comic Sans MS';">Comic Sans is a font known for its whimsical` — Alinea: Een blok gewone tekst.
- `<p>` — Alinea: Een blok gewone tekst.
- `<p> This is a paragraph </p>` — Alinea: Een blok gewone tekst.
- `<p></p>` — Alinea: Een blok gewone tekst.
- `<p><em>Did</em> you buy a dog?</p>` — Alinea: Een blok gewone tekst.
- `<p>By clicking the button above, you acknowledge and agree to the terms set forth by` — Alinea: Een blok gewone tekst.
- `<p>Capecitabine is an oral chemotherapy drug used to treat certain types of cancer.</p>` — Alinea: Een blok gewone tekst.
- `<p>Cataracts are a condition that causes the lens of the eye to become cloudy, leading to vision impairment.</p>` — Alinea: Een blok gewone tekst.
- `<p>I am Groot.</p>` — Alinea: Een blok gewone tekst.
- `<p>You can't handle the truth.</p>` — Alinea: Een blok gewone tekst.
- `<pre>` — Voorgeformatteerd: Behoudt spaties en regeleindes precies zoals getypt.
- `<span style="background: #D73233;">Red is confident and sometimes cocky</span>,` — Stukje tekst: Neutrale container binnen een regel, vaak om een stukje op te maken.
- `<span style="color: red">` — Stukje tekst: Neutrale container binnen een regel, vaak om een stukje op te maken.
- `<span style="color: red;">Red is confident and sometimes cocky</span>,` — Stukje tekst: Neutrale container binnen een regel, vaak om een stukje op te maken.
- `<span>` — Stukje tekst: Neutrale container binnen een regel, vaak om een stukje op te maken.
- `<strong>` — Belangrijk (vet): Markeert belangrijke tekst, standaard vet.
- `EcoRI: <code>GAATTC</code><br>` — Code: Toont tekst als code (monospace).
- `In the example above, all <p> tags will have a specific font size` — Alinea: Een blok gewone tekst.
- `The <br> tag inserts a line break (i.e., a newline) into the document` — Nieuwe regel: Forceert een regeleinde (heeft geen sluittag).
- `The <em> tag is used to emphasize text by italicizing it` — Nadruk (schuin): Legt nadruk, standaard schuin.
- `The <hr> tag inserts a visible horizontal line into the document and is used` — Scheidingslijn: Horizontale lijn tussen twee delen.
- `The <pre> tag preserves all whitespace and displays text in a monospaced font, unlike other tags` — Voorgeformatteerd: Behoudt spaties en regeleindes precies zoals getypt.
- `The <span> tag, just like the <div> tag, is often used to group content together and apply styles*` — Stukje tekst: Neutrale container binnen een regel, vaak om een stukje op te maken.
- `The <strong> tag is used to emphasize text by making it appear in a bold font` — Belangrijk (vet): Markeert belangrijke tekst, standaard vet.
- `echo "<p>Dear student,</p>";` — Alinea: Een blok gewone tekst.
- `echo "<p>Number of occurrences of <strong>Aurelia aurita</strong>: $occurrences</p>";` — Alinea: Een blok gewone tekst.
- `echo "<p>Your email has reached the wrong address. The correct email is <strong>$email</strong>.</p>";` — Alinea: Een blok gewone tekst.
- `echo "You should restock the following flavors:<br>";` — Nieuwe regel: Forceert een regeleinde (heeft geen sluittag).
- `text into a <p> element, the image appears above the text instead of to the right. How can we` — Alinea: Een blok gewone tekst.

## PyMOL (60)


### Camera

- `Center for Eukaryotic Structural Genomics (specialized)` — Centreer: Zet een selectie in het midden van het beeld.

### Kleuren

- `Color an object or selection` — Kleur geven: Geeft een selectie een kleur: color kleur, selectie.
- `Color each of the chains differently` — Kleur geven: Geeft een selectie een kleur: color kleur, selectie.
- `Color each separate type of` — Kleur geven: Geeft een selectie een kleur: color kleur, selectie.
- `color` — Kleur geven: Geeft een selectie een kleur: color kleur, selectie.
- `color cyan, chain A` — Kleur geven: Geeft een selectie een kleur: color kleur, selectie.
- `color cyan, hetatm` — Kleur geven: Geeft een selectie een kleur: color kleur, selectie.
- `color green, chain B` — Kleur geven: Geeft een selectie een kleur: color kleur, selectie.
- `color red, chain A` — Kleur keten A rood: Geeft alle atomen van keten A een rode kleur.
- `color yellow, chain C` — Kleur geven: Geeft een selectie een kleur: color kleur, selectie.

### Laden & bewaren

- `Fetch a PDB structure` — Download structuur (PDB): Haalt een structuur op uit de Protein Data Bank via de 4-tekencode, bv. fetch 1ubq.
- `Fetch structures 1RE2 (lysozyme) and 1HFX (alpha-lactalbumine)` — Download structuur (PDB): Haalt een structuur op uit de Protein Data Bank via de 4-tekencode, bv. fetch 1ubq.
- `Load the molecule and show in cartoon` — Open bestand: Opent een structuurbestand (.pdb, .cif, …) van je computer.
- `Save error messages by appending 2>&1` — Bewaar bestand: Bewaart een structuur of sessie (.pse) naar een bestand.
- `Save the file as snp151annotation-short.txt` — Bewaar bestand: Bewaart een structuur of sessie (.pse) naar een bestand.
- `fetch` — Download structuur (PDB): Haalt een structuur op uit de Protein Data Bank via de 4-tekencode, bv. fetch 1ubq.
- `fetch 1GBV` — Download structuur (PDB): Haalt een structuur op uit de Protein Data Bank via de 4-tekencode, bv. fetch 1ubq.
- `fetch 1ubq` — Download ubiquitine uit PDB: Haalt de structuur met PDB-code 1UBQ (ubiquitine) op uit de Protein Data Bank en opent ze.
- `fetch | create | color | ray` — Download structuur (PDB): Haalt een structuur op uit de Protein Data Bank via de 4-tekencode, bv. fetch 1ubq.
- `png eiwit.png, dpi=300, ray=1` — Bewaar mooie afbeelding: Rendert het beeld in hoge kwaliteit en bewaart het als eiwit.png met 300 dpi, geschikt voor een verslag.
- `ray` — Render mooi beeld: Berekent een hoogwaardige weergave met schaduwen, voor publicatie-afbeeldingen.

### Selecties

- `Delete an object` — Verwijder object: Verwijdert een object of selectie uit de lijst.
- `Remove # (shortest match) and ## (longest match)` — Verwijder atomen: Verwijdert atomen uit de structuur, bv. remove solvent (water).
- `Remove the original file` — Verwijder atomen: Verwijdert atomen uit de structuur, bv. remove solvent (water).
- `delete` — Verwijder object: Verwijdert een object of selectie uit de lijst.
- `delete 3CIG` — Verwijder object: Verwijdert een object of selectie uit de lijst.
- `select ////10-20/CA # Select atoms called CA in residues 10-20 (any chain)` — Maak selectie: Maakt een benoemde selectie: select naam, voorwaarde.
- `select ///A/10 # Select residue 10 in chain A` — Maak selectie: Maakt een benoemde selectie: select naam, voorwaarde.
- `select 42/C,N # Select atoms C and N in residue 42` — Maak selectie: Maakt een benoemde selectie: select naam, voorwaarde.
- `select actief, resi 40-50` — Selecteer residuen 40-50: Maakt een selectie met de naam 'actief' van residu 40 tot en met 50, die je daarna kan kleuren of tonen.
- `select chain B and resi 10:20` — Maak selectie: Maakt een benoemde selectie: select naam, voorwaarde.
- `select elem O and not name OH` — Maak selectie: Maakt een benoemde selectie: select naam, voorwaarde.
- `select resn ALA and name N` — Maak selectie: Maakt een benoemde selectie: select naam, voorwaarde.

### Weergave

- `As PDBx/mmCIF format continues to evolve` — Enkel deze weergave: Toont alleen deze weergave en verbergt de andere, bv. as cartoon.
- `As a transparant molecular surface the underlying` — Enkel deze weergave: Toont alleen deze weergave en verbergt de andere, bv. as cartoon.
- `As an example download 1L3W.pdb` — Enkel deze weergave: Toont alleen deze weergave en verbergt de andere, bv. as cartoon.
- `Hide a specific representation` — Verberg weergave: Verbergt een weergave; 'hide everything' verbergt alles.
- `Hide the substrate in cleft` — Verberg weergave: Verbergt een weergave; 'hide everything' verbergt alles.
- `Set gedit as default :` — Instelling wijzigen: Wijzigt een instelling, bv. set cartoon_transparency, 0.5.
- `Show a specific representation e.g. cartoon` — Toon weergave: Toont een weergave (cartoon, sticks, surface…) voor een selectie.
- `Show the carbon monoxide (resn CMO)` — Toon weergave: Toont een weergave (cartoon, sticks, surface…) voor een selectie.
- `as cartoon` — Toon enkel als lint: Verbergt de andere weergaven en toont het eiwit als lint, zodat je helices en sheets goed ziet.
- `as correctly folded, soluble proteins in bacteria` — Enkel deze weergave: Toont alleen deze weergave en verbergt de andere, bv. as cartoon.
- `as measure of average distance` — Enkel deze weergave: Toont alleen deze weergave en verbergt de andere, bv. as cartoon.
- `as well` — Enkel deze weergave: Toont alleen deze weergave en verbergt de andere, bv. as cartoon.
- `hide` — Verberg weergave: Verbergt een weergave; 'hide everything' verbergt alles.
- `hide all` — Verberg weergave: Verbergt een weergave; 'hide everything' verbergt alles.
- `hide cartoon, chain A` — Verberg weergave: Verbergt een weergave; 'hide everything' verbergt alles.
- `hide cartoon, chain B` — Verberg weergave: Verbergt een weergave; 'hide everything' verbergt alles.
- `hide cartoon, chain C` — Verberg weergave: Verbergt een weergave; 'hide everything' verbergt alles.
- `set` — Instelling wijzigen: Wijzigt een instelling, bv. set cartoon_transparency, 0.5.
- `set sphere_scale, 0.8, chain B` — Instelling wijzigen: Wijzigt een instelling, bv. set cartoon_transparency, 0.5.
- `set transparency, 0.4` — Instelling wijzigen: Wijzigt een instelling, bv. set cartoon_transparency, 0.5.
- `show` — Toon weergave: Toont een weergave (cartoon, sticks, surface…) voor een selectie.
- `show cartoon` — Toon weergave: Toont een weergave (cartoon, sticks, surface…) voor een selectie.
- `show ribbon, chain A` — Toon weergave: Toont een weergave (cartoon, sticks, surface…) voor een selectie.
- `show spheres, chain B` — Toon weergave: Toont een weergave (cartoon, sticks, surface…) voor een selectie.
- `show spheres, hetatm` — Toon weergave: Toont een weergave (cartoon, sticks, surface…) voor een selectie.
- `show sticks, chain C` — Toon weergave: Toont een weergave (cartoon, sticks, surface…) voor een selectie.
- `show surface` — Toon weergave: Toont een weergave (cartoon, sticks, surface…) voor een selectie.

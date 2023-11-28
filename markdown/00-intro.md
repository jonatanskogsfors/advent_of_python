# Advent of Python
Lär dig något nytt genom att försätta dig i trams 

* * *

Jonatan Skogsfors
[@jonatanskogsfors@mastodon.social](https://mastodon.social/@jonatanskogsfors)

Python Linköping Meetup | 2023-11-29

<!-- Note -->
En introduktion till Advent of Code och hur du kommer igång med hjälp av Python.

Låt mig börja med ett citat.



> "Nobody actually creates perfect code the first time around, except me. <br/>
> But there's only one of me"

— Linus Torvalds

<!-- Note -->
Med andra ord kan vi andra andas ut, Vi har ingen press på oss att vara perfekta.
Vi har alla varit eller är nybörjare och oavsett hur länge man håller på finns det alltid något nytt att lära sig.

Eller för att citera en lite mer nyanserad poet än Linus, Tomas Tranströmmer.



> "Du blir aldrig färdig <br/>
> och det är som det skall"

— Tomas Tranströmmer

<!-- Note -->
Ja, alla produktägare håller kanske inte med om det.



## Hur blir man en bättre programmerare?

<!-- Note -->
Men blir man då en bättre programmerare?



## Kurser
## Böcker

<!-- Note -->
Man kan gå kurser, man läsa böcker.

Men det kan vara svårt att ta sig den tiden till efter ens utbildning.



## Arbete
## Hobbyprojekt

<!-- Note -->
Genom sitt arbete lär man sig såklart en massa 
och man kan ha egna hobbyprojetkt på sin fritid.

Men det är lätt hänt att man mest lär sig att lösa precis de uppgifter man får framför sig.
Hur lär man sig att bli en mer komplett programmerare?



![Advent of Code](images/advent_of_code.jpeg)

<!-- Note -->
Här kommer Advent of Code in.

Först lite historik.



![Eric Wastl](https://pbs.twimg.com/profile_images/1099812161700937729/Rgi3F1jI_400x400.png)
### Eric Wastl, 2015 

<!-- Note -->
Upphovsmannen till Advent of Code heter Eric Wastl från ???.

2015 kom han på idén att gör en adventskalender med programeringspussel. Han satte ihop en samling med uppgifter som skulle låsas upp varje dag i december fram till juldagen.

När planerade hur mycket infrastruktur han behövde för projektet så tänkte han inte att någon annan en hans egna vänner och kanske några av deras vänner skulle vara intreserade. Med lite extra marginal tog han höjd för 70 användare.



# 70? <!-- .element style="font-size: 100%" -->

<!-- Note -->
Dagarna innan den första luckan skulle öppnas hade 81 personer registrerat sig. 



# 81  <!-- .element style="font-size: 150%" -->

<!-- Note -->
Inte långt från hans beräkningar alltså.

Men så fort det första pusslet låstes upp hände det något oförutsett. Intresset spred sig och efter bara 12 timmar hade...



# 4 000  <!-- .element style="font-size: 200%" -->

<!-- Note -->
...4000 personer registrerat sig. Hoppsan!

Efter 24 timmar var det...



# 9 000  <!-- .element style="font-size: 250%" -->

<!-- Note -->
...9000. Eric fick bråttom att skala upp.

Ytterligare en dag senare var det...



# 15 000  <!-- .element style="font-size: 300%" -->

<!-- Note -->
...15000. Och i slutet av december fanns det inte mindre än...



# 52 000  <!-- .element style="font-size: 350%" -->

<!-- Note -->
...52000 användare.

Helt klart hade han hittat något som intresserade programerare så han upprepade Advent of Code varje december. Förra året hade sidan...



# > 1 000 000  <!-- .element style="font-size: 400%" -->

<!-- Note -->
...över en miljon registrerade användare.

Och kom ihåg att målgruppen inte är internetanvändare i allmänhet utan specifikt programmerare som vill ha lite julpyssel.

Uppgifterna man löser sitter ihop med en lättsam ramberättelse:



![Tomten](images/santa_hat.svg#svgView(viewBox(0,0,25,25))) <!-- .element width="40%" style="filter:invert(100%)"  -->

<!-- Note -->
Det är snart jul då tomten ska dela ut julklappar världen över.
Men varje dag uppstår det olika problem och vem kan lösa problem om inte en...



![Programmerare](images/programmer.svg#svgView(viewBox(0,0,180,180))) <!-- .element width="30%" style="filter:invert(100%)"  -->

<!-- Note -->
...programerare. Av en händelse är alla problem särskilt lämpade att lösa med hjälp av just programmering.
Här kommer du in.



![Kalender](images/kalender.png) <!-- .element height="50%" width="50%" -->

<!-- Note -->
Varje dag från 1 till 25 december släpps en tvådelad uppgift.



![Dag 1](images/day_1.png) <!-- .element width="50%" -->




![Kalender](images/day_1_description.png) <!-- .element width="50%" -->

<!-- Note -->
Det finns en beskrivning av problemet.



![Kalender](images/day_1_example.png) <!-- .element width="50%" --> 
 
<!-- Note -->
Några enkla exempel.



![Kalender](images/day_1_question.png) <!-- .element width="50%" -->

<!-- Note -->
En konkret fråga.



![Kalender](images/day_1_input.png) <!-- .element width="50%" -->

<!-- Note -->
En länk till en textfil med indata.



![Kalender](images/day_1_answer.png) <!-- .element width="50%" -->

<!-- Note -->
Och till sist en rutan där man ska ange svaret. Svaret är alltid ett nummer eller en textstäng.

Löser man den första uppgiften får man en stjärna och en följduppgift.



![Stjärna](images/star.svg#svgView(viewBox(0,0,130,120))) <!-- .element width="20%" style="filter: invert(94%) sepia(47%) saturate(838%) hue-rotate(340deg) brightness(108%) contrast(103%);"  -->

<!-- Note -->

Löser man den får man...



![Stjärna](images/star.svg#svgView(viewBox(0,0,130,120))) <!-- .element width="20%" style="filter: invert(94%) sepia(47%) saturate(838%) hue-rotate(340deg) brightness(108%) contrast(103%);"  -->
![Stjärna](images/star.svg#svgView(viewBox(0,0,130,120))) <!-- .element width="20%" style="filter: invert(94%) sepia(47%) saturate(838%) hue-rotate(340deg) brightness(108%) contrast(103%);"  -->

<!-- Note -->
...en andra stjärna och sedan är dagen slut. Allt som allt blir det 50 stjärnor per år.



![Avancera](images/advance.svg#svgView(viewBox(0,0,100,100))) <!-- .element width="40%" style="filter:invert(100%)"  -->

<!-- Note -->
Den första uppgiften är mer grundläggande och den andra bygger vidare på samma koncept. Beroende på hur man har valt att lösa den första uppgiften kan det hända att den andra blir trivial att lösa med samma kod eller att man måste börja om från början. Oftast är det någonstans där emellan.

På samma sätt tenderar uppgifterna att bli svårare för varje dag. De senare uppgifterna är ofta rejäla utmaningar som bara ett fåtal av alla användare lyckas lösa.

Handlingsmässigt har varje år ett sammanhängande tema.



![](images/saturn.svg#svgView(viewBox(0,0,150,100))) <!-- .element width="25%" style="filter:invert(100%)"  -->
![](images/submarine.svg#svgView(viewBox(0,0,150,100))) <!-- .element width="25%" style="filter:invert(100%)" -->
![](images/djungle.svg#svgView(viewBox(0,0,150,100))) <!-- .element width="25%" style="filter:invert(100%)" -->

<!-- Note -->
Tomten har varit strandsatt ute i rymden
Nyckeln till tomtens släde har tappats ner i havet och behövt räddas med ubåt.
Renarna har behövt vara på bete i djungeln för att få i sig magisk stjärnfrukt.



![Förstoringsglass](images/looking_glass.svg#svgView(viewBox(0,0,250,250))) <!-- .element width="25%" style="filter:invert(100%)" -->

<!-- Note -->
Men det är också så att det finns återkommande teman på själva uppgifterna.

Tidiga uppgifter blir ofta en introduktion till mer avancerade uppgifter senare i månaden. Man belönas därför på sätt och vis om man tar sig tid att tänka igenom även de lättare uppgifterna mer analystiskt.



![Varninsskylt](images/warning.svg#svgView(viewBox(0,0,100,100))) <!-- .element width="25%" style="filter:invert(100%)" -->

<!-- Note -->
Problemen har ofta en finurlig twist. Det är inte ovanligt att de till en början verkar lätta att lösa. Man knåpar ihop en lösning som funkar jättebra med exempeldatat. Men när man sedan kör koden på den riktiga indatan....



![Aktivitet](images/waiting.svg#svgView(viewBox(0,0,100,100))) <!-- .element width="25%" style="filter:invert(100%)" -->

<!-- Note -->
Då står datorn bara och snurrar. När man undersösker saken lite närmre visar det sig att det kommer ta flera år för datorn att räkna klart.

Eller annars kanske det är allt minne som snabbt tar slut.

Kruxet är att komma på smartare algoritmer och mer effektiva datastrukturer.



# Är det en tävling?

<!-- Note -->
Är det en tävling?



# Kanske?

<!-- Note -->
Visst, om man verkligen vill kan man försöka bli klar snabbast. De 100 första som löser uppgiften i världen får poäng.

Man kan okcså skapa egna grupper och där får man poäng inom sin grupp på samma sätt.
Men...



![Sova](images/sleeping.svg#svgView(viewBox(0,0,450,400))) <!-- .element width="40%" style="filter:invert(100%)" -->

<!-- Note -->
Uppgifterna släpps vid midnatt amerikansk östkusttid. Det är kl 06:00 svensk tid.

Personligen är jag inte intresserad av tävlingen: Vem kan gå upp först. 

Dessutom handlar det mer om uthållighet. Att lösa en uppgift är inte det svåra. All lösa 50 uppgifter är svårt. Förra året var det 288538 som löste den allra första uppgiften men bara 12893, drygt 4%, som löste den sista.



![Vågskål](images/justice.svg#svgView(viewBox(0,0,100,100))) <!-- .element width="40%" style="filter:invert(100%)" -->

<!-- Note -->
Det finns heller inga strikta regler.

Alla får unik input och därmed unika svar så kan man inte skriva in någon annans lösning.

Men, det finns inget som hindrar att man laddar ner någon annans kod och kör med sin egen input.



![Robot](images/c3p0.svg#svgView(viewBox(0,0,100,100))) <!-- .element width="40%" style="filter:invert(100%)" -->

<!-- Note -->
Eric Wastl vädjar att man ska undvika att lösa problemen med AI innan de första hundra har löst uppgiften. Men efter det är det fritt fram.

Låt mig erbjuda ett annat perspektiv:



# Är det en tävling?

<!-- Note -->
Är det en tävling?



# JA!

<!-- Note -->
JA



# Vem tävlar du mot?

<!-- Note -->
Vem tävlar du mot?



![Pekfinger](images/you.svg#svgView(viewBox(0,0,100,100))) <!-- .element width="50%" style="filter:invert(100%)" -->

<!-- Note -->
Dig själv



# Vad är reglerna?

<!-- Note -->
Vad är reglerna?



# Det är upp till dig

<!-- Note -->
Det är upp till dig.



![Python](images/python.svg#svgView(viewBox(0,0,125,115))) <!-- .element width="20%" -->
![C](images/c.svg#svgView(viewBox(0,0,40,40))) <!-- .element width="20%" -->
![Rust](images/rust.svg#svgView(viewBox(0,0,110,110))) <!-- .element width="20%" style="filter:invert(100%)" -->

<!-- Note -->
En del väljer att lösa problemen med ett specifikt programmeringsspråk. Det är ett utmärkt sätt att lära sig ett nytt språk eller att slipa på språk man redan kan.

En del utmanar sig genom att använda ett oväntat språk.



![Excel](images/excel.svg#svgView(viewBox(0,0,2700,2700))) <!-- .element width="30%" -->

<!-- Note -->
T.ex. finns det de som använder Excel.



![Mind blown](images/exploding_head.svg#svgView(viewBox(0,0,110,110))) <!-- .element width="40%" style="filter:invert(100%)" -->

<!-- Note -->
Några byter språk varje dag.



![Santa-lang](images/santa_lang.png) <!-- .element width="50%" -->

<!-- Note -->
Det finns det som skapar ett eget språk specifikt för Advent of Code.



![Willy Wonka](images/wonka.jpg) <!-- .element width="50%" -->

<!-- Note -->
En del kommer säga till dig att ett visst språk är bättre för att lösa Advent of Code.

Då är det bara att nicka och le tills den där rust programmeraren lämnat rummet.



![Tidtagarur](images/stopwatch.svg#svgView(viewBox(0,0,13,13))) <!-- .element width="40%" style="filter:invert(100%)" -->

<!-- Note -->
Om man av  jagar millisekunder så kommer vissa språk så klart att vara snabbare än andra. Men det som avgör mest är vilka algoritmer man väljer.

"Rätt" lösning i ett långsamt språk vinner med hästlängder över "Fel" lösning i ett väldigt snabbt språk.



![Python](images/python.svg#svgView(viewBox(0,0,125,115))) <!-- .element width="40%" -->

<!-- Note -->
Själv brukar jag skriva i Python och ofta har jag begränsat mig själv till att bara använda standardbiblioteket.

Jag är inte unik på något sätt.

Det finns ingen officiell statistik, men genom att analysera publika github-repon taggade med AdventOfCode verkar det som att det allra populäraste språket är Python.



![Språkstatistik](images/popular_languages.png) <!-- .element width="50%" -->

https://masalmon.eu/2018/12/15/adventofcode/

<!-- Note -->
Här är ett godtyckligt diagram. Källa internet.



# Verktyg och strategier

<!-- Note -->
Några tips om verktyg och strategier



![Octocat](images/github-mark-white.svg) <!-- .element width="25%" --> <br/>
![GitHUb](images/GitHub_Logo_White.png) <!-- .element width="25%" -->

<!-- Note -->
Hur du än än jobbar: Spara din kod. Och gör den gärna publik på GitHub.

Det behöver verkligen inte vara polerat. Du behöver inte skämmas över koden eller för hur många uppgifter du löst.



r/adventofcode

<!-- Note -->
Jag rekommenderar starkt att man går med i r/adventofcode på Reddit.

Där diskuteras problemen. Folk hjälper varandra.

För den som vill kan man läsa sida efter sida med konkreta lösningar i alla tänkbara språk.



<iframe width="560" height="315" src="https://www.youtube.com/embed/QIhoGfhb6CY?si=CwDTlbBNqUmZ0_uz" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<!-- Note -->
Många lägger upp visualiseringar av problemen.



![Trender](images/trends.webp) <!-- .element width="75%" -->

<!-- Note -->
Lite aktuella söktrender på google



![Meme](images/meme_1.jpg) <!-- .element width="75%" -->

<!-- Note -->
Och framför allt. Skoj och memes.

Hundratusentals programmerare över hela världen får plötsligt en massa internskämt.



![Jupyter]()

<!-- Note -->
Om du inte specifikt vill träna på att kodarkitektur så är det väldigt smidigt att använda Jupyter lab.


<!-- Note -->
För den som inte vet:
- Man insallerar jupyter lab.
- Starta
- Öppna din browser.
- Största nackdelen är att man inte får all den hjälp man får av en mer avancerad editor men å andra sidan kan vscode öppna dem.

Kata?


<!-- Note -->
TDD
Varje dag får man exempelinput med tillhörande exempelsvar.
Det lämpar sig perfekt för en testdriven approach.


<!-- Note -->
Här t.ex.är en uppgift som säger att...
Jag skriver ett test
Jag implementerar kod som löser får testet att funka
Om jag inte har missat något kan jag byta input
Om det visar sig att jag måste ändra något i min kod så har jag kvar testet så att jag vet att det fortfarande funkar med exempelinputen.



<!-- Note -->
Om det känns oöverstigligt.
- Man behöver inte lösa ett år i taget. Det finns x år av tidiga uppgifter.
- Lös det tillsammans med någon annan
- Det här är inte högskoleprovet. Man kan inte fuska. Om du kör fast och ger upp lär du dig inget. Ibland kan det räcka att med att man får reda på rätt nyckelord. Aha, jag ska använda något som heter Dijkstras algoritm. Då kan jag själv google på hur det funkar. Du kan fortfarande lära dig något om du inspireras av andras lösnigar. Ja, t.o.m. om du kopierar någon annans lösning helt så länge du faktiskt går igneom koden.



<!-- Note -->
Så nu ska vi tillsammans lösa en uppgift
- Tänk på att vi har olika nivåer
- Om du ser lösningen snabbt, låt processen ha sin gång

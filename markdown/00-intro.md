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
Advent of Code kom till 2015 av en man som heter Eric Wastl.
Han kom på idén att gör en adventskalender med programeringspussel men att det antagligen mest var hans vänner och kanske deras vänner som skulle vara intreserade.



### 70?

<!-- Note -->
Han tog höjd för att servern han deployade på skulle klara av runt 70 deltagare.



### 81

<!-- Note -->
Dagarna innan kalendern startade hade 81 personer registrerat sig men så fort första pusslet låstes upp hände det något oförutsätt.



## 4 000

<!-- Note -->
Efter 12 timmar hade 4000 personer registrerat sig.



## 9 000

<!-- Note -->
Efter 24 timmar var det 9000.



# 52 000

<!-- Note -->
Dagen efter 15000 och i slutet av december 52000.



# > 1 000 000
<!-- Note -->
Förra året fanns det över en miljon registrerade användare.

Formen för Advent of Code är som följer



![Tomten](images/santa.jpg)

<!-- Note -->
Det är snart jul då tomten ska dela ut julklappar världen över.
Men varje dag uppstår det problem och vem kan lösa problem om inte en programmerare. Av en händelse är alla problem särskilt lämpade att lösa med hjälp av just programmering.



![Kalender](images/kalender.png) <!-- .element height="50%" width="50%" -->

<!-- Note -->
Här kommer du in. Varje dag från 1 till 25 december släpps en tvådelad uppgift. Förutom beskrivning av problemet får man en fil med indata. Svaret ges genom att man fyller i något, ett nummer eller en textstäng.  Den första uppgiften är i regel mer grundläggande och när du har löst den får du en fortsättningsuppgift som bygger vidare på samma koncept. De första dagarna är enklare men för varje dag ökar svårighetsdagen och i slutet är det riktigt avancerat.



# APA

<!-- Note -->
Varje år har ett sammanhängande tema.
Tomten har varit strandsatt ute i rymden
Nyckeln till tomtens släde har tappats ner i havet och behövt räddas med ubåt.
Renarna har behövt vara på bete i djungeln för att få i sig magisk stjärnfrukt.




<!-- Note -->
Men det är också så att det finns teman på själva uppgifterna. Tidiga uppgifter blir ofta en introduktion till mer avancerade uppgifter senare i månaden.


<!-- Note -->
Ofta händer det att problemen till en början verkar lätta att lösa. Man knäpar ihop en lösning som funkar jättebra med exempeldata som uppgiften har. Men när man sedan kör koden på den riktiga indatan visar det sig att det kommer ta flea år för datorn att räkna klart eller att allt minne snabbt tar slut. Kruxet är att komma på smartare algoritmer och mer effektiva datastrukturer.


<!-- Note -->
Är det en tävling?


<!-- Note -->
Visst, om man verkligen vill kan man försöka bli klar snabbast. De 100 första som löser uppgiften i världen får poäng. Man kan skapa egna grupper och där får man poäng inom sin grupp på samma sätt.
Men


<!-- Note -->
Uppgifterna släpps vid midnatt amerikansk östkusttid. Det är 06:00 svensk tid. Personligen är jag inte intresserad av tävlingen: Vem kan gå upp först. 
Dessutom handlar det mer om uthållighet. Att lösa en uppgift är inte det svåra. All lösa 50 uppgifter är svårt. Förra året var det 288538 som löste den allra första uppgiften men bara 12893, drygt 4 %, som löste den sista.


<!-- Note -->
Det finns heller inga strikta regler. Visst, eftersom alla får unik input och därmed unika svar så kan man inte skriva in någon annans lösning. Men, det finns inget som hindrar att man lassar ner någon annans kod och kör sin egen input på.


<!-- Note -->
Eric Wastl vädjar att man ska undvika att lösa problemen med AI innan de första hundra har löst uppgiften. Men efter det är det fritt fram.


<!-- Note -->
Låt mig erbjuda ett annat perspektiv.
Är det en tävling?


<!-- Note -->
JA


<!-- Note -->
Vem tävlar du mot?


<!-- Note -->
Dig själv


<!-- Note -->
Vad är reglerna?


<!-- Note -->
De du själv vill ha.


<!-- Note -->
En del väljer att lösa problemen med ett specifikt programmeringsspråk. Det är ett utmärkt sätt att lära sig ett nytt språk eller att slipa på språk man redan kan.


<!-- Note -->
En del utmanar sig genom att använda ett väldigt oväntat språk. T.ex. finns det de som använder Excel.



<!-- Note -->
Några byter språk varje dag.



<!-- Note -->
En del skriver ett eget språk.



<!-- Note -->
En del kommer säga till er att ett visst språk är bättre för att lösa Advent of Code. Då är det bara att nicka och le tills den där rust programmeraren lämnat rummet.



<!-- Note -->
Om man av någon anledning jagar millisekunder så kommer vissa språk så klart att vara snabbare än andra. Men det som avgör mest är vilka algoritmer man väljer. "Rätt" lösning i ett långsamt språk vinnar med astronomiska hästlängder över "Fel" lösning i ett väldigt snabbt språk.


<!-- Note -->
Själv brukar jag skriva i Python och ofta har jag begränsat mig själv till att bara använda standardbiblioteket.


<!-- Note -->
Jag är inte unik på något sätt.
Det finns ingen officiell statistik men genom att analysera publika githubrepon verkar det som att det allra populäraste språket är Python.


<!-- Note -->
Några tips om verktyg och strategier


<!-- Note -->
GitHub
Vad du än gör, spara undan din kod. Och gör den gärna publik. Det behöver verkligen inte vara polerat. Du behöver inte skämmas över koden, du behöver inte skämmas om ligger efter eller inte blir klar.


<!-- Note -->
Jag rekommenderar att man går med i r/adventofcode
Där diskuteras problemen. Folk hjälper varandra. För den som vill kan man läsa sida efter sida med konkreta lösningar i alla tänkbara språk.



<!-- Note -->
Många lägger upp snygga visualiseringar av problemen.


<!-- Note -->
Och framför allt. Skoj och memes.


<!-- Note -->
Om du inte specifikt vill träna på att kodarkitektur så är det väldigt smidigt att använda Jupyter Notebook.


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

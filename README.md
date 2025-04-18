# BijbelvertalingmetAI
Dit project is opgezet om een experiment met betrekking tot Bijbelvertaling met Claude te demonstreren. Met behulp van meerdere prompts zijn Bijbelteksten vertaald in de stijl van de BGT.
We hebben meerdere projecten gebruikt die te vinden zijn in de bestanden. Project 1: Vertaling, Project 2: Titelkopjes/perikopen en project 3: controle boek BGT. 

In het eerste project wordt de tekst vertaald op basis van onze prompt die eerst letterlijk vertaald. Over het algemeen werkt dit project best aardig en komen er serieuze BGT-stijl vertalingen uit. In dit project hebben we ook een BGT-woordenlijst opgenomen in de project knowledge en een link naar (https://woordenboekgrieks.nl/). De BGT-woordenlijst stuurt Claude de juiste richting op qua taalgebruik (dit blijkt te werken), van de site is het lastig om het effect in te schatten. Zie de prompt voor kleinere issues die we verder hebben opgelost.
In project 2 wordt de tekst vervolgens ingedeeld in perikopen met titelkopjes. Daar hebben we de dezelfde BGT-woordenlijst toegevoegd, wat de kwaliteit heeft verbeterd. In dit project is de kwaliteit wel instabiel, soms komen er nog slechte kopjes tussendoor. Het lukt Claude ook niet om qua opmaak de vers nummers in superscript te zetten. 
In project 3 hebben we drie hoofdstukken uit het boek van Matthijs over de BGT gekoppeld, waarmee Claude de inputtekst moet beoordelen. Soms komt Claude met behoorlijk goede wijzigingen, maar de kwaliteit blijft inconsistent. De grote uitdaging in dit project was – en is nog steeds – om Claude niet te dwingen tot wijzigingen. In eerste instantie herschreef Claude de volledige tekst, maar na aanpassing van de prompt werd hij juist erg snel tevreden met de input en bracht hij geen wijzigingen meer aan. We zoeken nog steeds naar de juiste balans.
We hebben geëxperimenteerd met een project 4: culturele verschuivingen. Daarbij was dit het doel: “Ons doel is een vertaling die qua taalgebruik heel duidelijk en begrijpelijk is, maar die qua culturele waarden, ethiek, religieuze voorstellingen nog steeds de sfeer van de Bijbelse cultuur ademt.” Dit bleek echter te hoog gegrepen, Claude herhaalde slechts onze voorbeelden of maakte eenvoudige zinnen onnodig complex.

Wij hebben tot nu toe geëxperimenteerd met passages uit de Deuterocanonieke boeken.

**Prompts 28-3-2025**

**Project 1**
Jij bent een expert in het vertalen van KOINE Grieks naar hedendaags Nederlands. Voor elke inputtekst in het KOINE Grieks lever je de volgende outputs:
OUTPUT 1 [LETTERLIJK]: Een vertaling die zo letterlijk mogelijk aansluit bij de grondtaal en structuur. Gebruik hiervoor het recente online woordenboek https://woordenboekgrieks.nl/ en daarnaast andere hulpmiddelen. 
OUTPUT 2 [BGT]: Maak de meest accurate vertaling in de stijl van de BGT, binnen de kaders van de betekenisnuances van de oorspronkelijke tekst. Doe dat volgens deze regels: 1. Gebruik de train_random_subset en volg de daarin gemaakte vertaalkeuzes. Zorg dat jouw output 2 de woordkeuze en stijl van deze voorbeelden volgt.  
2. Gebruik in je output 2 uitsluitend woorden die op de woordenlijst in je project knowledge staan. Gebruik, behalve eigennamen, geen woorden die niet in deze woordenlijst staan. Als je echt per se een woord wilt gebruiken dat niet op deze lijst staat, dan mag dat, maar dan moet je dat wel apart vermelden in een opmerking onder de vertaling. (Bijvoorbeeld zo: In vers x heb ik het woord y gebruikt ook al staat het niet op de lijst, omdat ...).  
3. Zorg dat het in output 2 altijd duidelijk is wie er spreekt of handelt. Maak dus aan het begin van een nieuwe stukje altijd duidelijk over wie het gaat. Niet 'ze' of 'zij' maar 'de leiders' of 'Susanna', etc. 
4. Als er relevante informatie verdwijnt door het gebruik van eenvoudige taal, los dat dan op met extra verduidelijking. Bijv. het woord 'dienstmeisjes' staat niet in de woordenlijst, dus dat wordt 'meisjes' in output 2; verduidelijk dit dan de eerste keer dat ze genoemd worden, met 'de meisjes die voor Susanna werkten' of 'de meisjes die bij haar in dienst waren'; in de verzen die volgen is dan 'de meisjes' voldoende.
4. Hanteer de versnummers zoals ingegeven in de input, geef alleen het nummer weer, geen andere symbolen. 
Voordat je output 2 levert, controleer je eerst of die voldoet aan de regels hierboven.  
Voorbeeld input:
KOINE: 1 ἐν παντὶ θλιβόμενοι ἀλλ’ οὐ στενοχωρούμενοι, ἀπορούμενοι ἀλλ’ οὐκ ἐξαπο
Voorbeeld output:
## OUTPUT 1 [LETTERLIJK]: 
1 In alles verdrukt worden, maar niet benauwd zijn; in problemen zijn, maar niet wanhopig.
## OUTPUT 2 [BGT]: 
1. Ik moet lijden, maar ik verlies de moed niet. Ik leef in onzekerheid, maar ik blijf op God vertrouwen.
Het is niet nodig de letterlijke input-zin in de output te herhalen.

**Project 2**
Je gaat de ingegeven teksten indelen in perikopen. Houd je daarbij aan de volgende regels: 
1.  Gebruik de voorbeeldteksten uit de BGT in het bijgevoegde document als voorbeeld. Maak op basis daarvan een indeling van de ingegeven tekst in perikopen van ongeveer 80-150 woorden.  
2. Let er heel goed op dat de perikopen de opbouw van de tekst goed weerspiegelen. Een perikoop valt vaak samen met een scene in het verhaal. De perikopen laten het verhaalverloop zien. Een perikoop heeft doorgaans tussen de 80 en 150 woorden en vormt in literair opzicht een eenheid. Als het nodig is mag een perikoop korter of langer zijn om het gestelde doel te bereiken.   
3. Zet boven elke perikoop een titelkopje in bold lettertype. Het titelkopje moet inhoudelijk goed bij de perikoop passen. De titelkopjes moeten duidelijk zijn en kort. De titelkopjes mogen geen moeilijke woorden bevatten. Gebruik voor de titelkopjes dezelfde gewone taal als voor de vertaling. Gebruik in de titelkopjes alleen woorden die voorkomen in de woordenlijst in de project knowledge.
4. De titelkopjes geven heel kort de essentie weer van de perikoop waar ze boven staan. Als je alleen de titelkopjes leest, moet je daaruit kunnen volgen waar de tekst over gaat. 
5. Behoud de versnummering uit de input volledig, zonder enige vorm van visuele opmaak of markering. Laat de versnummers er exact hetzelfde uitzien als in de originele tekst. Gebruik géén doorhalingstekens (~), géén vet, cursief of andere opmaak. De versnummers zijn onderdeel van de tekst.
6. Na elke perikoop volgt een witregel
Voordat je output levert, controleer je eerst of die voldoet aan de regels hierboven.
Gebruik de voorbeeldteksten in je project knowledge als voorbeeld.
Voorbeeld 1: Filippus vertelt over Jezus
Voorbeeld 2: Veel mensen komen naar Jezus toe

**Project 3**
Je moet de ingegeven tekst controleren op duidelijkheid en begrijpelijkheid en indien nodig moet je die verbeteren. Houd je daarbij aan de volgende regels: 
1. Analyseer de twee teksten uit het boek ´Hoe vertaal je de Bijbel in gewone taal´ en gebruik deze informatie om de ingegeven tekst te beoordelen op duidelijkheid en begrijpelijkheid en waar nodig te verbeteren. 
2. De ingegeven tekst is het uitgangspunt, breng alleen wijzigingen aan als dat nodig is voor de duidelijkheid en begrijpelijkheid van de tekst. Het is niet de bedoeling om de tekst te herschrijven! Als je een aanpassing doet, benoem dan expliciet welke keuzes je maakt op basis van welk deel van het boek. Bijvoorbeeld: Ik kies ervoor om X expliciet te maken, omdat hoofdstuk 4 van het boek beschrijft: Als de tekst iets impliceert, mag dat – omwille van de duidelijkheid – expliciet gemaakt worden.
3. Elke wijziging die je aanbrengt in de tekst, moet voldoen aan de eisen van gewone taal. Gebruik daarom alleen woorden die in de woordenlijst staan. 
4. Let vooral op de richtlijnen en adviezen in de project knowlegde die ervoor zorgen dat het resultaat een begrijpelijke en duidelijke tekst wordt. Geef aandacht aan de samenhang van het verhaal: volgt alles logisch en begrijpelijk op elkaar? 
5. Hanteer de versnummering van de input. 
6. Verander de titelkopjes qua inhoud en opmaak niet.
Voordat je output levert, controleer je eerst of die voldoet aan de regels hierboven.
Lever als output de ingegeven tekst opnieuw aan met je wijzigingen daarin verwerkt. Geef eerst de hele tekst en geef daarna de toelichting op de gemaakte wijzigingen.  
Noem daarnaast ook vijf dingen in de tekst die al goed waren en door het boek bevestigd worden.
